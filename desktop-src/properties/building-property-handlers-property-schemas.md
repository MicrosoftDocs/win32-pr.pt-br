---
description: As propriedades usadas no sistema de propriedades do Windows Vista e posterior são declaradas em esquemas de propriedade.
ms.assetid: 4e301210-df3a-41db-a58e-015ee8d41714
title: Criando propriedades personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90849383e25889edf7f3abd4704c36354eff153c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296978"
---
# <a name="creating-custom-properties"></a>Criando propriedades personalizadas

As propriedades usadas no sistema de propriedades do Windows Vista e posterior são declaradas em esquemas de propriedade. Esses esquemas de propriedade são definidos em arquivos XML e descrevem vários aspectos de uma propriedade, incluindo seu tipo (incluindo informações sobre seu tipo primitivo e se ele tem vários valores), como ele pode ser exibido na interface do usuário do Windows, que tipo de rótulos (cadeias de caracteres de edição amigáveis) devem ser usados com ele e como ele é armazenado em cache no repositório de pesquisa para acesso mais As propriedades são identificadas por seu nome canônico ou sua chave de propriedade (PKEY).

Um nome canônico é o nome amigável para o leitor da propriedade e usa uma Convenção de namespace semelhante àquela usada em Microsoft .NET. Para propriedades definidas pelo sistema (aquelas incluídas no Windows), a Convenção é `System.GroupName.PropertyName` . Observe que o esquema de maiúsculas e minúsculas do Pascal, que usa letras maiúsculas no início de cada palavra, é usado nesses nomes. Os nomes canônicos são usados em vários locais, incluindo listas de propriedades e nomes de colunas no cache de propriedades. Portanto, eles são usados em consultas de linguagem SQL (SQL) para recuperar um valor de propriedade.

Um PKEY é um par de valores que consiste em um GUID e um **DWORD**, chamados de *FormatID* e *propID* , respectivamente. Ele é representado por uma estrutura [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) . A maioria das APIs do sistema de propriedades aceita essas chaves de propriedade. O SDK (Software Development Kit) do Windows inclui o arquivo de cabeçalho Propkey. h que inclui uma definição de macro de cada uma das `System` chaves de propriedade com a Convenção de `PKEY_GroupName_PropertyName` . Por exemplo, `PKEY_Photo_DateTaken` é a chave de propriedade para a propriedade com nome canônico `System.Photo.DateTaken` . Os valores de propriedade são armazenados na forma de uma estrutura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) , que é uma extensão dos tipos de variante OLE.

Esta seção contém o tópico a seguir, que é integral para a criação de propriedades personalizadas:

-   [Compreendendo o esquema de descrição da propriedade](./propdesc-schema-entry.md)

> [!Note]  
> Devido a possíveis dificuldades que o indexador pode ter ao consumir o esquema do sistema de propriedades, é fundamental que você defina atributos com cuidado e estrategicamente para a primeira versão do esquema. Qualquer alteração nos atributos (tipo, largura da coluna, se indexible) não será refletida no banco de dados depois que um esquema tiver sido registrado. As únicas maneiras de ter essas alterações reconhecidas depois que o esquema foi registrado uma vez em um sistema seriam recriar o índice e, em seguida, registrar o novo esquema, ou registrar o esquema e, em seguida, criar uma nova propriedade para cada versão subsequente; por exemplo `PKEY_GroupName_PropertyNameV2` , `PKEY_GroupName_PropertyNameV3` , e assim por diante). Não recomendamos a criação de novas propriedades dessa maneira, pois várias colunas estranhas podem afetar o desempenho do sistema.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Implementando manipuladores de propriedade](./building-property-handlers.md)
</dt> <dt>

[Esquema de descrição da propriedade](./propdesc-schema-entry.md)
</dt> </dl>

 

 
