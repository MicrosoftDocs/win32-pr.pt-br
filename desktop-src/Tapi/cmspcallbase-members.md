---
description: A lista a seguir contém os membros do CMSPCAllBase.
ms.assetid: a3193639-e0c4-4851-a879-551eca8023f9
title: Membros do CMSPCallBase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ddae67d85a64a5a443727b3950054957c7f24f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169672"
---
# <a name="cmspcallbase-members"></a>Membros do CMSPCallBase



| Tipo de membro                   | Nome             | Descrição                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IUnknown                      | \*\_pFTM m        | Ponteiro para o Marshaller com thread livre.                                                                                                                                                                                                                                                                                                          |
| CMSPAddress\*                 | \*\_pMSPAddress m | O ponteiro para o objeto de endereço MSP. Ele será usado para obter os terminais padrão se o aplicativo não selecionar nenhum. Ele também transporta um Refcount (via [**MSPAddressAddRef**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref), não AddRef) para que o endereço agregado não seja descontinuado enquanto a chamada ainda estiver ativa, mas o endereço da TAPI 3 não é AddRef'ed. |
| \_identificador MSP                   | \*\_htCall m      | O identificador para chamar TAPI3's. Usado para acionar eventos de chamada.                                                                                                                                                                                                                                                                                             |
| DWORD                         | \_dwMediaType m   | Bitmask dos tipos de mídia nesta chamada.                                                                                                                                                                                                                                                                                                          |
| CMSPArray <ITStream \*> | \_fluxos m       | A lista de objetos de fluxo na chamada.                                                                                                                                                                                                                                                                                                           |
| CMSPCritSection               | bloqueio de m \_          | O bloqueio que protege as listas de fluxos.                                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CMSPCallBase**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 



