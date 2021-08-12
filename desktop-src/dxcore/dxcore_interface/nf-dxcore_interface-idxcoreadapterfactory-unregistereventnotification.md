---
title: IDXCoreAdapterFactory::UnregisterEventNotification
description: Não registra em uma notificação que você registrou anteriormente.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 64fb54226f1fad0d1d36f8f4260c9c9172b105dc6239ea5cb805c32b57a938ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118278877"
---
# <a name="idxcoreadapterfactoryunregistereventnotification-method"></a>Método IDXCoreAdapterFactory::UnregisterEventNotification

Não registra em uma notificação que você registrou anteriormente. Para obter diretrizes de programação e exemplos de código, consulte [Usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Sintaxe

```cpp
virtual HRESULT STDMETHODCALLTYPE UnregisterEventNotification(
  uint32_t eventCookie) = 0;
```

## <a name="parameters"></a>Parâmetros

### <a name="eventcookie"></a>eventCookie

Tipo: **uint32_t**

O valor do cookie (retornado quando você chamou [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)) que representa um registro anterior para o que agora você deseja não registrar.

## <a name="returns"></a>Retornos

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se a função for bem-sucedida, ela **retornará S_OK**. Caso contrário, retornará um [**código de erro HRESULT**](../../com/structure-of-com-error-codes.md) [.](../../com/com-error-codes-10.md)

|Valor retornado|Descrição|
|-|-|
|E_INVALIDARG|O valor de *eventCookie* não é um cookie válido que representa um registro anterior.|

## <a name="remarks"></a>Comentários

**UnregisterEventNotification** retorna somente após a conclusão de todos os retornos de chamada pendentes/em andamento para esse registro. O DXCore garante que nenhum novo retorno de chamada ocorrerá para esse registro depois **que UnregisterEventNotification** for retornado. No entanto, para evitar um deadlock, se você chamar **UnregisterEventNotification** de dentro do retorno de chamada, **UnregisterEventNotification** não aguardará a conclusão do retorno de chamada ativo.

> [!IMPORTANT]
> Antes de destruir o objeto DXCore representado pelo argumento *dxCoreObject* passado para [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), você deve usar o valor do cookie para não registrar esse objeto de notificações chamando **UnregisterEventNotification**. Se você não fizer isso, uma exceção fatal será criada quando a situação for detectada.

Depois que você encerra o registro de um valor de cookie, esse valor é qualificado para ser retornado por um registro subsequente

## <a name="see-also"></a>Confira também

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [IDXCoreAdapterFactory::UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [Referência de DXCore](../dxcore-reference.md), Usando [DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)