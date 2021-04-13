---
title: IDXCoreAdapterFactory::UnregisterEventNotification
description: Cancela o registro de uma notificação que você registrou anteriormente para o.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6bb12126769a914680ea17ac9e6060346001c795
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366505"
---
# <a name="idxcoreadapterfactoryunregistereventnotification-method"></a>Método IDXCoreAdapterFactory:: UnregisterEventNotification

Cancela o registro de uma notificação que você registrou anteriormente para o. Para obter diretrizes de programação e exemplos de código, consulte [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Sintaxe

```cpp
virtual HRESULT STDMETHODCALLTYPE UnregisterEventNotification(
  uint32_t eventCookie) = 0;
```

## <a name="parameters"></a>Parâmetros

### <a name="eventcookie"></a>eventCookie

Tipo: **uint32_t**

O valor do cookie (retornado quando você chamou [IDXCoreAdapterFactory:: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)) que representa um registro anterior para o qual você deseja cancelar o registro.

## <a name="returns"></a>Retornos

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se a função for realizada com sucesso, ela retornará **S_OK**. Caso contrário, ele retorna um [código de erro](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valor retornado|Descrição|
|-|-|
|E_INVALIDARG|O valor de *eventCookie* não é um cookie válido que representa um registro anterior.|

## <a name="remarks"></a>Comentários

**UnregisterEventNotification** retorna somente após a conclusão de todos os retornos de chamada pendentes/em andamento para este registro. DXCore garante que nenhum novo retorno de chamada ocorrerá para esse registro depois que **UnregisterEventNotification** for retornado. No entanto, para evitar um deadlock, se você chamar **UnregisterEventNotification** de dentro de seu retorno de chamada, o **UnregisterEventNotification** não aguardará a conclusão do retorno de chamada ativo.

> [!IMPORTANT]
> Antes de destruir o objeto DXCore representado pelo argumento *dxCoreObject* passado para [IDXCoreAdapterFactory:: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), você deve usar o valor de cookie para cancelar o registro desse objeto de notificações chamando **UnregisterEventNotification**. Se você não fizer isso, uma exceção fatal será gerada quando a situação for detectada.

Depois que você cancela o registro de um valor de cookie, esse valor é qualificado para ser retornado por um registro subsequente

## <a name="see-also"></a>Confira também

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [IDXCoreAdapterFactory:: UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)