---
description: Localidades personalizadas
ms.assetid: 110efeab-c02f-4244-8950-a975cfc91e8a
title: Localidades personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acda75d0d097bf6860e1385bb2557d56c2b2d2a1df530404781817590e381b3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754916"
---
# <a name="custom-locales"></a>Localidades personalizadas

**Windows Vista e posterior:** As localidades personalizadas suportam propriedades internacionais que proporcionam uma experiência de usuário mais culturalmente apropriada do que aquelas fornecidas com as localidades padrão enviadas pela Microsoft com o sistema operacional. O uso de localidades personalizadas permite que os administradores estendam o conjunto de localidades fornecido pela Microsoft ou substituam os dados em uma localidade fornecida por Windows, por exemplo, símbolos de moeda ou nomes dos meses do ano.

Os dois tipos de localidades personalizadas são localidades complementares e localidades de substituição. Localidades complementares são localidades personalizadas que permitem que empresas, universidades, governos e outros terceiros criem dados de localidade não disponíveis no sistema operacional de envio. As localidades de substituição são localidades personalizadas que são navegáveis com o sistema operacional sem alterar os [identificadores de](locale-identifiers.md) localidade ou [os nomes de localidade.](locale-names.md)

Você pode usar o utilitário Construtor de Localidade fornecido pelo NLS para criar localidades personalizadas. Para obter mais informações, consulte [Microsoft Locale Builder](https://www.microsoft.com/download/details.aspx?id=41158). Instruções para usar localidades personalizadas em seus aplicativos são fornecidas em [Trabalhando com localidades personalizadas.](working-with-custom-locales.md)

## <a name="comparison-of-custom-locale-types"></a>Comparação de tipos de localidade personalizados

A tabela a seguir descreve as diferenças entre localidades complementares e de substituição.



| Item                                                                                                                           | Localidade suplementar                                                                                                                                                                                                                   | Localidade de substituição                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Calendários                                                                                                                      | Pode incluir qualquer um dos calendários fornecidos pela Microsoft. Pelo menos um dos calendários fornecidos deve ser o calendário gregoriano localizado.                                                                                              | Pode incluir qualquer um dos calendários fornecidos pela Microsoft. Pelo menos um dos calendários fornecidos deve ser o calendário gregoriano localizado e a coleção deve incluir o calendário padrão da localidade substituída. |
| Classificação                                                                                                                        | Pode usar qualquer uma das classificações fornecidas pela Microsoft.                                                                                                                                                                                          | Retém o comportamento de classificação da localidade que está sendo substituída.                                                                                                                                                            |
| Nomes de dia e mês                                                                                                            | Pode ser personalizado somente para o calendário gregoriano padrão, não para calendários não gregorianos e não para calendários gregorianos especializados, como o calendário gregoriano do Oriente Médio francês.                                           | O mesmo que para a localidade complementar.                                                                                                                                                                                      |
| Nome do idioma ([LOCALE \_ SLANGUAGE ou](locale-slanguage.md) [LOCALE \_ SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md)) | Retorna [LOCALE \_ SNATIVELANGNAME](locale-snative-constants.md) [ou LOCALE \_ SNATIVELANGUAGENAME](locale-snative-constants.md).                                                                                                       | Mantém o nome do idioma da localidade que está sendo substituída.                                                                                                                                                                 |
| Identificador de localidade                                                                                                              | Definido como [LOCALE \_ CUSTOM \_ UNSPECIFIED,](locale-custom-constants.md) a menos que a localidade seja a localidade Padrão e Formatos selecionada no momento pelo usuário, nesse caso, ela é definida como [LOCALE \_ CUSTOM \_ DEFAULT.](locale-custom-constants.md) | Mantém o identificador de localidade da localidade que está sendo substituída.                                                                                                                                                             |
| Nome da localidade                                                                                                                    | Arbitrário; deve se ajustar ao padrão discutido em [Nomes de Localidade.](locale-names.md)                                                                                                                                                      | Mantém o nome da localidade que está sendo substituída.                                                                                                                                                                   |



 

## <a name="supplemental-locale-examples"></a>Exemplos de localidade suplementar



| Nome da localidade    | Descrição                                                                                                                                                                                                                                                                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en-CA-fabricam | Fabricam é um fabricante de PC canadá com escritórios em todo o mundo. Para fornecer um comportamento consistente da interface do usuário para todos os seus computadores, a empresa desenvolve uma localidade para usar em toda a empresa.                                                                                                                                                          |
| fr-US          | O Woodlawn Bank usa Windows XP Embedded para seus caixas eletrônicos automatizados, que o banco envia por todo o América do Norte com interfaces do usuário em francês, inglês e espanhol. Para fornecer uma experiência consistente, o banco cria uma localidade para francês no Estados Unidos que tem Estados Unidos, mas nomes de dia e mês em francês. |



 

## <a name="replacement-locale-example"></a>Exemplo de localidade de substituição



| Nome da localidade | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| pt-BR       | Fabricam é um fabricante de PC canadá com escritórios em todo o mundo. Para fornecer um comportamento consistente da interface do usuário para todos os seus computadores, a empresa desenvolve uma localidade para usar em toda a empresa. Ele usa um relógio de 24 horas, mas, caso contrário, se comporta como a localidade de inglês (Estados Unidos) com suporte. Como a localidade personalizada é tão semelhante à localidade com suporte, o Fabricam decide implementá-la como uma localidade de substituição em vez de uma localidade complementar. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Localidades e idiomas](locales-and-languages.md)
</dt> <dt>

[Trabalhando com localidades personalizadas](working-with-custom-locales.md)
</dt> </dl>

 

 



