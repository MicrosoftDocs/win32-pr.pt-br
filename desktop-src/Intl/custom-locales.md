---
description: Localidades personalizadas
ms.assetid: 110efeab-c02f-4244-8950-a975cfc91e8a
title: Localidades personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50108750fb1209aa210b04d8be9adcd48e5fd308
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922551"
---
# <a name="custom-locales"></a>Localidades personalizadas

**Windows Vista e posterior:** As localidades personalizadas dão suporte a propriedades internacionais, fornecendo uma experiência de usuário de cultura mais adequada do que aquelas fornecidas com as localidades padrão fornecidas pela Microsoft com o sistema operacional. O uso de localidades personalizadas permite que os administradores estendam o conjunto de localidades fornecido pela Microsoft ou substituam os dados em uma localidade fornecida com o Windows, por exemplo, símbolos de moeda ou nomes dos meses do ano.

Os dois tipos de localidades personalizadas são localidades complementares e localidades de substituição. As localidades complementares são localidades personalizadas que permitem que as corporações, universidades, governos e outros terceiros criem dados de localidade não disponíveis no sistema operacional de remessa. As localidades de substituição são localidades personalizadas que acompanham o sistema operacional sem alterar os [identificadores de localidade](locale-identifiers.md) ou os [nomes de localidade](locale-names.md).

Você pode usar o utilitário do Locale Builder fornecido pelo NLS para criar localidades personalizadas. Para obter mais informações, consulte [Microsoft Locale Builder](https://www.microsoft.com/download/details.aspx?id=41158). As instruções para usar localidades personalizadas em seus aplicativos são fornecidas em [trabalhando com localidades personalizadas](working-with-custom-locales.md).

## <a name="comparison-of-custom-locale-types"></a>Comparação de tipos de localidade personalizados

A tabela a seguir descreve as diferenças entre as localidades complementares e substitutas.



| Item                                                                                                                           | Localidade suplementar                                                                                                                                                                                                                   | Localidade de substituição                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Calendários                                                                                                                      | Pode incluir qualquer um dos calendários fornecidos pela Microsoft. Pelo menos um dos calendários fornecidos deve ser o calendário localizado gregoriano.                                                                                              | Pode incluir qualquer um dos calendários fornecidos pela Microsoft. Pelo menos um dos calendários fornecidos deve ser o calendário localizado em gregoriano e a coleção deve incluir o calendário padrão da localidade substituída. |
| Classificação                                                                                                                        | Pode usar qualquer uma das classificações fornecidas pela Microsoft.                                                                                                                                                                                          | Retém o comportamento de classificação da localidade que está sendo substituída.                                                                                                                                                            |
| Nomes de dia e mês                                                                                                            | Pode ser personalizado apenas para o calendário gregoriano padrão, não para calendários não gregorianos e não para calendários gregorianos especializados, como o calendário gregoriano francês do Oriente Médio.                                           | O mesmo que para a localidade suplementar.                                                                                                                                                                                      |
| Nome do idioma ([localidade \_ SLANGUAGE](locale-slanguage.md) ou [localidade \_ SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md)) | Retorna a [localidade \_ SNATIVELANGNAME](locale-snative-constants.md) ou [localidade \_ SNATIVELANGUAGENAME](locale-snative-constants.md).                                                                                                       | Mantém o nome do idioma da localidade que está sendo substituída.                                                                                                                                                                 |
| Identificador de localidade                                                                                                              | Definido como [localidade \_ personalizado não \_ especificado](locale-custom-constants.md) , a menos que a localidade seja a localidade de padrões e formatos padrão selecionada no momento, nesse caso, ela é definida como [ \_ \_ Default personalizado de localidade](locale-custom-constants.md). | Mantém o identificador de localidade da localidade que está sendo substituída.                                                                                                                                                             |
| Nome da localidade                                                                                                                    | Execução deve se ajustar ao padrão discutido nos [nomes de localidade](locale-names.md).                                                                                                                                                      | Mantém o nome da localidade da localidade que está sendo substituída.                                                                                                                                                                   |



 

## <a name="supplemental-locale-examples"></a>Exemplos de localidade complementares



| Nome da localidade    | Descrição                                                                                                                                                                                                                                                                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en-CA-fabricam | Fabricam é um fabricante de PC canadense com escritórios em todo o mundo. Para fornecer um comportamento consistente de interface do usuário para todos os seus computadores, a empresa desenvolve uma localidade para usar toda a empresa.                                                                                                                                                          |
| fr-US          | O Woodlawn Bank usa o Windows XP Embedded para seus caixas eletrônicos, que acompanham todos os América do Norte com interfaces de usuário em francês, inglês e espanhol. Para fornecer uma experiência consistente, o banco cria uma localidade para o francês no Estados Unidos que tem formatos de Estados Unidos, mas os nomes de dia e mês em francês. |



 

## <a name="replacement-locale-example"></a>Exemplo de localidade de substituição



| Nome da localidade | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en-US       | Fabricam é um fabricante de PC canadense com escritórios em todo o mundo. Para fornecer um comportamento consistente de interface do usuário para todos os seus computadores, a empresa desenvolve uma localidade para usar toda a empresa. Ele usa um relógio de 24 horas, mas, caso contrário, se comporta como a localidade com suporte em inglês (Estados Unidos). Como a localidade personalizada é tão semelhante à localidade com suporte, o fabricam decide implementá-la como uma localidade de substituição em vez de uma localidade complementar. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Localidades e idiomas](locales-and-languages.md)
</dt> <dt>

[Trabalhando com localidades personalizadas](working-with-custom-locales.md)
</dt> </dl>

 

 



