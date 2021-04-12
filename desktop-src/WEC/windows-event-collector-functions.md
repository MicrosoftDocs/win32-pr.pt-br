---
title: Funções do coletor de eventos do Windows
description: A lista a seguir descreve brevemente as funções que são usadas no coletor de eventos do Windows.
ms.assetid: 48155df6-ba9c-4abe-ba84-6190cee95878
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c20e3bbee6226d385681c7471bb7fd3f337dfa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291764"
---
# <a name="windows-event-collector-functions"></a>Funções do coletor de eventos do Windows

A lista a seguir descreve brevemente as funções que são usadas no coletor de eventos do Windows.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose)
</dt> <dd>

Fecha um identificador recebido de outras funções do coletor de eventos.

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

Recupera valores de propriedade para as origens de evento de uma assinatura.

</dd> <dt>

[**EcGetObjectArraySize**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarraysize)
</dt> <dd>

Recupera o número de índices da matriz de valores de propriedade para as origens de evento de uma assinatura.

</dd> <dt>

[**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty)
</dt> <dd>

Recupera um valor de propriedade de um objeto de assinatura.

</dd> <dt>

[**EcGetSubscriptionRunTimeStatus**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionruntimestatus)
</dt> <dd>

Recupera as informações de status de tempo de execução para uma origem de evento de uma assinatura ou a própria assinatura.

</dd> <dt>

[**EcInsertObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecinsertobjectarrayelement)
</dt> <dd>

Insere um objeto vazio em uma matriz de valores de propriedade para as origens de evento de uma assinatura.

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

Salva as informações de configuração da assinatura.

</dd> <dt>

[**EcSetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetobjectarrayproperty)
</dt> <dd>

Define um valor de propriedade em uma matriz de valores de propriedade para as origens de evento de uma assinatura.

</dd> <dt>

[**EcSetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetsubscriptionproperty)
</dt> <dd>

Define novos valores ou atualiza os valores existentes de uma assinatura.

</dd> <dt>

[**EcRemoveObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecremoveobjectarrayelement)
</dt> <dd>

Remove um elemento de uma matriz de objetos que contêm valores de propriedade para as origens de evento de uma assinatura.

</dd> <dt>

[**EcRetrySubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecretrysubscription)
</dt> <dd>

Tenta se conectar novamente à origem do evento de uma assinatura que não está conectada.

</dd> </dl>

 

 




