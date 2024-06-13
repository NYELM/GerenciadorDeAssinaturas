# GerenciadorDeAssinaturas

## Descrição

O **GerenciadorDeAssinaturas** é uma ferramenta para monitorar a expiração de assinaturas e oferecer notificações com descontos exclusivos para renovação. Mantenha suas assinaturas em dia e aproveite ofertas especiais antes da expiração.

## Funcionalidades

- **Monitoramento de Expiração:** Verifica quantos dias faltam para a expiração da assinatura.
- **Notificações Automatizadas:** Envia alertas personalizados com base na proximidade da data de expiração.
- **Descontos Exclusivos:** Oferece descontos especiais para renovação quando a assinatura está prestes a expirar.
- **Mensagens Personalizadas:** Exibe mensagens claras e diretas sobre o status da assinatura e possíveis economias.

## Como Funciona

1. O sistema gera um número aleatório de dias até a expiração da assinatura.
2. Dependendo do número de dias restantes, uma mensagem personalizada é exibida para o usuário.
3. Se a assinatura está prestes a expirar (1 dia ou menos de 5 dias), o sistema oferece um desconto especial para a renovação.

## Exemplo de Uso

Random random = new Random();
int daysUntilExpiration = random.Next(12);
int discountPercentage = 0;

if (daysUntilExpiration == 0)
{
    Console.WriteLine("Sua assinatura expirou.");
}
else if (daysUntilExpiration == 1)
{
    Console.WriteLine("Sua assinatura expira dentro de um dia!");
    discountPercentage = 20;
}
else if (daysUntilExpiration <= 5)
{
    Console.WriteLine($"Sua assinatura expira em {daysUntilExpiration} dias.");
    discountPercentage = 10;
}
else if (daysUntilExpiration <= 10)
{
    Console.WriteLine("Sua assinatura vai expirar em breve. Renove agora!");
}

if (discountPercentage > 0)
{
    Console.WriteLine($"Renove agora e economize {discountPercentage}%.");
}

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).
