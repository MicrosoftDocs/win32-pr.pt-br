---
title: Windows Funções do Coletor de Eventos
description: A lista a seguir descreve brevemente as funções que são usadas no Windows de Eventos.
ms.assetid: 48155df6-ba9c-4abe-ba84-6190cee95878
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17dd89cb98e3803f171633df0f902250f1147a25bce9d43c83947c2d1e83b6ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937218"
---
# <a name="windows-event-collector-functions"></a>Windows Funções do Coletor de Eventos

A lista a seguir descreve brevemente as funções que são usadas no Windows de Eventos.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose)
</dt> <dd>

Fecha um handle recebido de outras funções do Coletor de Eventos.

</dd> <dt>

[**EcDeleteSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription)
</dt> <dd>

Exclui uma assinatura existente.

</dd> <dt>

[**EcEnumNextSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecenumnextsubscription)
</dt> <dd>

Continua a enumeração das assinaturas registradas no computador local.

</dd> <dt>

[**EcGetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarrayproperty)
</dt> <dd>

Recupera valores de propriedade para as fontes de evento de uma assinatura.

</dd> <dt>

[**EcGetObjectArraySize**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarraysize)
</dt> <dd>

Recupera o número de índices da matriz de valores de propriedade para as fontes de evento de uma assinatura.

</dd> <dt>

[**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty)
</dt> <dd>

Recupera um valor da propriedade de um objeto de assinatura.

</dd> <dt>

[**EcGetSubscriptionRunTimeStatus**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionruntimestatus)
</dt> <dd>

Recupera as informações de status de tempo de run time para uma origem de evento de uma assinatura ou da própria assinatura.

</dd> <dt>

[**EcInsertObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecinsertobjectarrayelement)
</dt> <dd>

Insere um objeto vazio em uma matriz de valores de propriedade para as fontes de evento de uma assinatura.

</dd> <dt>

[**EcOpenSubscriptionEnum**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscriptionenum)
</dt> <dd>

Cria um enumerador de assinatura para enumerar todas as assinaturas registradas no computador local.

</dd> <dt>

[**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription)
</dt> <dd>

Abre uma assinatura existente ou cria uma nova assinatura.

</dd> <dt>

[**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription)
</dt> <dd>

Salva informações de configuração de assinatura.

</dd> <dt>

[**EcSetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetobjectarrayproperty)
</dt> <dd>

Define um valor da propriedade em uma matriz de valores de propriedade para as fontes de evento de uma assinatura.

</dd> <dt>

[**EcSetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetsubscriptionproperty)
</dt> <dd>

Define novos valores ou atualiza os valores existentes de uma assinatura.

</dd> <dt>

[**EcRemoveObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecremoveobjectarrayelement)
</dt> <dd>

Remove um elemento de uma matriz de objetos que contêm valores de propriedade para as fontes de evento de uma assinatura.

</dd> <dt>

[**EcRetrySubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecretrysubscription)
</dt> <dd>

Tentar se conectar à origem do evento de uma assinatura que não está conectada.

</dd> </dl>

 

 




