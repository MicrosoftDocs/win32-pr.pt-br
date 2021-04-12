---
title: IDXCoreAdapterFactory::RegisterEventNotification
description: Registra para receber notificações de condições específicas de uma lista de adaptador ou adaptador DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 3643fbb01fc955049c297a577f18d4d276e73f46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454246"
---
# <a name="idxcoreadapterfactoryregistereventnotification-method"></a>Método IDXCoreAdapterFactory:: RegisterEventNotification

Registra para receber notificações de condições específicas de uma lista de adaptador ou adaptador DXCore. Para obter diretrizes de programação e exemplos de código, consulte [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Sintaxe

```cpp
virtual HRESULT STDMETHODCALLTYPE RegisterEventNotification(
  _In_ IUnknown *dxCoreObject,
  DXCoreNotificationType notificationType,
  _In_ PFN_DXCORE_NOTIFICATION_CALLBACK callbackFunction,
  _In_opt_ void *callbackContext,
  _Out_ uint32_t *eventCookie) = 0;
```

## <a name="parameters"></a>Parâmetros

### <a name="dxcoreobject-in"></a>dxCoreObject [in]

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

O objeto DXCore ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) ou [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)) cujas notificações você está assinando.

### <a name="notificationtype"></a>notificationType

Tipo: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**

O tipo de notificação para o qual você está se registrando. Consulte a tabela em [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) para obter informações sobre quais tipos são válidos com quais tipos de objetos.

### <a name="callbackfunction-in"></a>callbackFunction [in]

Tipo: **[PFN_DXCORE_NOTIFICATION_CALLBACK](./nc-dxcore_interface-pfn_dxcore_notification_callback.md)**

Um ponteiro para uma função de retorno de chamada (implementado pelo seu aplicativo), que é chamado pelo objeto DXCore para eventos de notificação. Para a assinatura da função, consulte [PFN_DXCORE_NOTIFICATION_CALLBACK](./nc-dxcore_interface-pfn_dxcore_notification_callback.md).

### <a name="callbackcontext-in"></a>callbackContext [in]

Tipo: **void \***

Um ponteiro opcional para um objeto que contém informações de contexto. Esse objeto é passado para sua função de retorno de chamada quando a notificação é gerada.

### <a name="eventcookie-out"></a>eventCookie [saída]

Tipo: **uint32_t \***

Um ponteiro para um valor **uint32_t** . Se for bem-sucedida, a função desreferenciará o ponteiro e definirá o valor para um valor de cookie diferente de zero que representa esse registro. Use esse valor de cookie para cancelar o registro da notificação chamando [IDXCoreAdapterFactory:: UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md). Consulte **comentários**.

Se não for bem-sucedida, a função desreferenciará o ponteiro e definirá o valor como zero, que representa um valor de cookie inválido.

## <a name="returns"></a>Retornos

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se a função for realizada com sucesso, ela retornará **S_OK**. Caso contrário, ele retorna um [código de erro](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valor retornado|Descrição|
|-|-|
|DXGI_ERROR_INVALID_CALL|Não há suporte para *notificationType* pelo sistema operacional (SO).|
|E_INVALIDARG|`nullptr` foi fornecido para *dxCoreObject*, ou se uma combinação *notificationType* e *dxCoreObject* inválida foi fornecida.|
|E_POINTER|`nullptr` foi fornecido para *callbackFunction* ou *eventCookie*.|

## <a name="remarks"></a>Comentários

Você usa **RegisterEventNotification** para se registrar em eventos gerados pelas interfaces [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) e [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) . Há suporte para esses tipos de notificação.

|[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)|*DxCoreObject* com suporte|Observações|
|-|-|-|
|AdapterListStale|**IDXCoreAdapterList**|Indica que a lista de adaptadores que atendem aos critérios de filtro foi alterada. Se a lista de adaptadores estiver obsoleta no momento do registro, o retorno de chamada será chamado imediatamente. Esse retorno de chamada ocorre no máximo uma vez por registro.|
|AdapterNoLongerValid|**IDXCoreAdapter**|Indica que o adaptador não é mais válido. Se o adaptador for inválido no momento do registro, o retorno de chamada será chamado imediatamente.|
|AdapterBudgetChange|**IDXCoreAdapter**|Indica que ocorreu um evento de orçamento de memória e que você deve chamar [IDXCoreAdapter:: QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) (com [DXCoreAdapterState:: AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md)) para avaliar o estado de orçamento da memória atual. Após o registro, um retorno de chamada inicial sempre ocorrerá para permitir que você consulte o estado inicial.|
|AdapterHardwareContentProtectionTeardown|**IDXCoreAdapter**|Indica que você deve reavaliar o status da sessão de criptografia atual; por exemplo, chamando [ID3D11VideoContext1:: CheckCryptoSessionStatus](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) para determinar o impacto da desmontagem de hardware para uma interface [ID3D11CryptoSession](/windows/win32/api/d3d11/nn-d3d11-id3d11cryptosession) específica. Após o registro, um retorno de chamada inicial sempre ocorrerá para permitir que você consulte o estado inicial.|

Uma chamada para a função que você fornece no *callbackFunction* é feita de forma assíncrona em um thread em segundo plano por DXCore quando o evento detectado ocorre. Nenhuma garantia é feita como a ordenação ou o tempo de retornos de chamada que &mdash; vários retornos de chamada podem ocorrer em qualquer ordem, ou até mesmo simultaneamente. É possível até que o retorno de chamada seja invocado antes que **RegisterEventNotification** seja concluído. Nesse caso, o DXCore garante que seu *eventCookie* seja definido antes de o retorno de chamada ser chamado. Vários retornos de chamada para um registro específico serão serializados na ordem.

Os retornos de chamada podem ocorrer a qualquer momento até que você chame [UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)e seja concluído. Os retornos de chamada ocorrem em seus próprios threads e você pode fazer chamadas para a API DXCore nesses threads, incluindo **UnregisterEventNotification**. No entanto, você não deve liberar a última referência para o *dxCoreObject* neste thread.

> [!IMPORTANT]
> Antes de destruir o objeto DXCore representado pelo argumento *dxCoreObject* passado para **RegisterEventNotification**, você deve usar o valor de cookie para cancelar o registro desse objeto de notificações chamando [IDXCoreAdapterFactory:: UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md). Se você não fizer isso, uma exceção fatal será gerada quando a situação for detectada.

## <a name="see-also"></a>Confira também

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [IDXCoreAdapterFactory:: UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)