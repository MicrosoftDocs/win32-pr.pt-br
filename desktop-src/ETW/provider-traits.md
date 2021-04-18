---
description: As características do provedor são um método para anexar mais dados a um registro de provedor individual.
ms.assetid: 97755D64-BF57-4C0D-8ED4-040FC375C4AF
title: Características do provedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c67b25857070edb6419be9a2898d2667f3a179d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968111"
---
# <a name="provider-traits"></a>Características do provedor

As características do provedor são um método para anexar mais dados a um registro de provedor individual. Eles podem ser usados para provedores baseados em manifesto ou TraceLogging. Atualmente, isso inclui suporte para adicionar um nome de provedor e/ou grupo de provedores a um registro de provedor individual. É provável que mais tipos de características sejam adicionados no futuro. Essas informações são armazenadas no kernel como um blob binário de um formato definido.

As características só podem ser definidas uma vez para um registro. Qualquer tentativa adicional de definir as características desse registro falhará.

Para definir as características do provedor em um provedor baseado em manifesto, chame a função [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) com a classe de informações EventProviderSetTraits. O buffer EventInformation deve conter um blob binário do seguinte formato:

``` syntax
{
   UINT16 TraitsSize   // Total size of the traits including this field
   CHAR[] ProviderName // Null terminated utf-8 provider name
   TRAIT[] Traits      // Zero or more individual traits
}
```

As características individuais devem estar no seguinte formato:

``` syntax
TRAIT {
      UINT16 TraitSize // Size of this individual trait including this field
      UINT8 Type       // ETW_PROVIDER_TRAIT_TYPE
      BYTE[] Data
      }
```

Da característica individual, o tipo de característica do provedor de ETW \_ \_ \_ é definido como:

``` syntax
typedef enum {
    EtwProviderTraitTypeGroup = 1,
    EtwProviderTraitTypeMax
} ETW_PROVIDER_TRAIT_TYPE;
```

Os provedores de TraceLogging definem automaticamente as características do provedor quando a função [**TraceLoggingRegister**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) é chamada. O nome do provedor TraceLogging sempre será incluído em suas características. Um grupo pode ser definido em um provedor TraceLogging usando a macro [**TraceLoggingOptionGroup**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup) na definição do provedor.

## <a name="custom-traits"></a>Características personalizadas

Embora a maioria dos 255 tipos de característica possíveis ainda não esteja definida, os tipos de característica 1-127 são reservados para definição pela Microsoft. Os valores de tipo mais indexados restantes podem ser usados por desenvolvedores externos como se comportarem. Qualquer pessoa que considere adicionar suas próprias características personalizadas ao provedor deve tentar manter seu tamanho total de características abaixo de 256 bytes pelos seguintes motivos:

-   As características são incluídas em todos os eventos escritos para o provedor. As características grandes podem levar a arquivos de log muito grandes.
-   As características são armazenadas no pool de kernel não paginável durante o tempo de vida do provedor.

## <a name="provider-groups"></a>Grupos de provedores

Um grupo de provedores é uma entidade controlável definida pelo GUID muito parecida com um provedor em si. A principal diferença é que, embora um GUID de provedor seja usado para controlar os registros de apenas seu provedor, um grupo controlará todos os seus registros de membros. Por exemplo, habilitar um grupo de provedores com uma determinada palavra-chave e nível habilitará todos os registros de membro de grupos com essa palavra-chave e nível.

A associação de grupo pode ser restrita por permissões. Se o chamador de [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) não tiver permissões para ingressar no grupo especificado, a associação será negada.

Em alguns casos, o controlador de sessão de rastreamento pode querer excluir alguns provedores da sua habilitação de um grupo. Isso pode ser feito definindo uma lista de não permitir. Uma lista de não permitir é uma lista de GUIDs de provedor que não será habilitada com base nas configurações de grupo para uma única sessão de log. Não permitir que as listas possam ser alteradas dinamicamente com [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) e a classe de informações TraceSetDisallowList.

Embora a maioria das ações de habilitação possa ser feita para grupos de provedores de maneira semelhante a provedores individuais, há algumas exceções. As exceções incluem:

-   Os grupos de provedores não podem ser controlados por sessões de rastreamento particulares.
-   O nome do evento, a ID do evento e os filtros de carga não são aplicáveis aos grupos de provedor, pois eles assumem informações específicas de um provedor individual.

 

 
