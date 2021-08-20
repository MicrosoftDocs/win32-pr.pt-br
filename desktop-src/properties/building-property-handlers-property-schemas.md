---
description: As propriedades usadas no sistema de propriedades do Windows Vista e posterior são declaradas em esquemas de propriedade.
ms.assetid: 4e301210-df3a-41db-a58e-015ee8d41714
title: Criando propriedades personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d33ebd18c799dca757c1cf7e5b2f16fd35edb6072a52f7d1f5d41749ec0b8341
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117685552"
---
# <a name="creating-custom-properties"></a>Criando propriedades personalizadas

As propriedades usadas no sistema de propriedades do Windows Vista e posterior são declaradas em esquemas de propriedade. Esses esquemas de propriedade são definidos em arquivos XML e descrevem vários aspectos de uma propriedade, incluindo seu tipo (incluindo informações sobre seu tipo primitivo e se ele tem valores múltiplos), como ele pode ser exibido na interface do usuário do Windows, que tipo de rótulos (cadeias de caracteres de edição amigáveis) devem ser usados com ele e como ele é armazenado em cache no armazenamento de pesquisa para acesso mais rápido. As propriedades são identificadas pelo nome canônico ou pela PKEY (chave de propriedade).

Um nome canônico é o nome amigável ao leitor da propriedade e usa uma convenção de namespace semelhante à usada no Microsoft .NET. Para propriedades definidas pelo sistema (aquelas incluídas com Windows), a convenção é `System.GroupName.PropertyName` . Observe que o esquema de maiúsculas e maiúsculas pascal, que capitaliza letras no início de cada palavra, é usado nesses nomes. Nomes canônicos são usados em vários locais, incluindo listas de propriedades e nomes de coluna no cache de propriedades. Portanto, eles são usados em linguagem SQL (SQL) para recuperar um valor da propriedade.

Uma PKEY é um par de valores que consistem em um GUID e um **DWORD**, chamados de *formatID* e *propID,* respectivamente. Ele é representado por uma estrutura [**PROPERTYKEY.**](/windows/win32/api/wtypes/ns-wtypes-propertykey) A maioria das APIs do sistema de propriedades aceita essas chaves de propriedade. O Windows SDK (Software Development Kit) inclui o arquivo de header Propkey.h que inclui uma definição de macro de cada uma das chaves de propriedade com a convenção `System` de `PKEY_GroupName_PropertyName` . Por exemplo, `PKEY_Photo_DateTaken` é a chave de propriedade para a propriedade com o nome canônico `System.Photo.DateTaken` . Os valores de propriedade são armazenados na forma de [**uma estrutura PROPVARIANT,**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) que é uma extensão dos tipos OLE VARIANT.

Esta seção contém o tópico a seguir, que é integral para a criação de propriedades personalizadas:

-   [Noções básicas sobre o esquema de descrição da propriedade](./propdesc-schema-entry.md)

> [!Note]  
> Devido a possíveis dificuldades que o indexador pode ter ao consumir o esquema do sistema de propriedades, é essencial que você defina atributos cuidadosamente e estrategicamente para a primeira versão do esquema. Quaisquer alterações nos atributos (tipo, largura da coluna, se indexável) não serão refletidas no banco de dados depois que um esquema tiver sido registrado. As únicas maneiras de fazer com que essas alterações sejam reconhecidas depois que o esquema tiver sido registrado uma vez em um sistema seria recriar o índice e registrar o novo esquema ou registrar o esquema e, em seguida, criar uma nova propriedade para cada versão subsequente; por `PKEY_GroupName_PropertyNameV2` exemplo, `PKEY_GroupName_PropertyNameV3` , e assim por diante). Não é recomendável criar novas propriedades dessa maneira, pois várias colunas diferentes podem afetar o desempenho do sistema.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Implementando manipuladores de propriedade](./building-property-handlers.md)
</dt> <dt>

[Esquema de descrição da propriedade](./propdesc-schema-entry.md)
</dt> </dl>

 

 
