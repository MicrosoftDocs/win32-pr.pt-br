---
title: IDXCoreAdapter::QueryState
description: Recupera o estado atual do item especificado no adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 2e5c585c249141c1491ddf36ee798d8b11148425026e9011bd0653169f998fb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117716"
---
# <a name="idxcoreadapterquerystate-method"></a>Método IDXCoreAdapter:: QueryState

Recupera o estado atual do item especificado no adaptador. Antes de chamar **QueryState** para um tipo de propriedade, chame [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) para confirmar que a consulta do tipo de estado está disponível para esse adaptador e so (sistema operacional).

## <a name="syntax"></a>Sintaxe

```cpp
virtual HRESULT STDMETHODCALLTYPE QueryState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t outputBufferSize,
  _Out_writes_bytes_(outputBufferSize) void *outputBuffer) = 0;

template <class T1, class T2>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _In_reads_bytes_opt_(sizeof(T1)) const T1 *inputStateDetails,
  _Out_writes_bytes_(sizeof(T2)) T2 *outputBuffer);

template <class T>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _Out_writes_bytes_(sizeof(T)) T *outputBuffer);
```

## <a name="parameters"></a>Parâmetros

### <a name="state"></a>state

Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**

O tipo de item de estado no adaptador cujo estado você deseja recuperar. Consulte a tabela em [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obter mais informações sobre cada tipo de estado de adaptador.

### <a name="inputstatedetailssize"></a>inputStateDetailsSize

Tipo: **size_t**

O tamanho, em bytes, do buffer de detalhes de estado de entrada que você (opcionalmente) aloca e fornece em *inputStateDetails*.

### <a name="inputstatedetails-in"></a>inputStateDetails [in]

Tipo: **void const \***

Um ponteiro opcional para um buffer de detalhes de estado de entrada constante que você aloca em seu aplicativo, contendo qualquer informação sobre a solicitação necessária para o tipo de estado que você especificar no *estado*. Consulte a tabela em [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obter mais informações sobre qualquer requisito de buffer de entrada para um determinado tipo de estado.

### <a name="outputbuffersize"></a>outputBufferSize

Tipo: **size_t**

O tamanho, em bytes, do buffer de saída que você aloca e fornece em *OUTPUTBUFFER*.

### <a name="outputbuffer-out"></a>outputBuffer [saída]

Tipo: **void \***

Um ponteiro para um buffer de saída que você aloca em seu aplicativo e que a função preenche. Consulte a tabela em [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obter mais informações sobre o requisito de buffer de saída para um determinado tipo de estado.

## <a name="returns"></a>Retornos

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se a função for realizada com sucesso, ela retornará **S_OK**. Caso contrário, ele retorna um [código de erro](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valor retornado|Descrição|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|O adaptador não está mais em um estado válido.|
|DXGI_ERROR_INVALID_CALL|O tipo de estado especificado no *estado* não é reconhecido por este sistema operacional (SO). Chame [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) para confirmar que a consulta do tipo de estado está disponível para esse adaptador e sistema operacional (SO).|
|DXGI_ERROR_UNSUPPORTED|O adaptador não dá suporte ao tipo de estado especificado no *estado* . Chame [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) para confirmar que a consulta do tipo de estado está disponível para esse adaptador e sistema operacional (SO).|
|E_INVALIDARG|Um tamanho de buffer insuficiente é fornecido para *OUTPUTBUFFER* (ou para *inputStateDetails* onde um buffer de detalhes de estado de entrada é necessário).|
|E_POINTER|`nullptr` foi fornecido para *OUTPUTBUFFER* (ou para *inputStateDetails* onde um buffer de detalhes de estado de entrada é necessário).|

## <a name="remarks"></a>Comentários

Consulte [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obter mais informações sobre cada tipo de estado de adaptador e quais entradas e saídas são usadas. Essa função zera o buffer *OUTPUTBUFFER* antes de preenchê-lo.

## <a name="see-also"></a>Confira também

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)