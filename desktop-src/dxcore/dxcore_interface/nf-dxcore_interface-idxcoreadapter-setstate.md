---
title: IDXCoreAdapter::SetState
description: Define o estado do item especificado no adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c80ca670be26ffdcefa5e89cee079d2225d204ee97e99e41f69686300a46230b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042904"
---
# <a name="idxcoreadaptersetstate-method"></a>Método IDXCoreAdapter:: SetState

Define o estado do item especificado no adaptador. Antes de chamar **SetState** para um tipo de propriedade, chame [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) para confirmar que a configuração do tipo de estado está disponível para esse adaptador e sistema operacional (SO).

## <a name="syntax"></a>Sintaxe

```cpp
virtual HRESULT STDMETHODCALLTYPE SetState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t inputDataSize,
  _In_reads_bytes_(inputDataSize) const void *inputData) = 0;

template <class T1, class T2>
HRESULT SetState( 
  DXCoreAdapterState state,
  const T1 *inputStateDetails,
  const T2 *inputData);
```

## <a name="parameters"></a>Parâmetros

### <a name="state"></a>state

Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**

O tipo de item de estado no adaptador cujo estado você deseja definir. Consulte a tabela em [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obter mais informações sobre cada tipo de estado de adaptador.

### <a name="inputstatedetailssize"></a>inputStateDetailsSize

Tipo: **size_t**

O tamanho, em bytes, do buffer de detalhes de estado de entrada que você (opcionalmente) aloca e fornece em *inputStateDetails*.

### <a name="inputstatedetails-in"></a>inputStateDetails [in]

Tipo: **void const \***

Um ponteiro opcional para um buffer de detalhes de estado de entrada constante que você aloca em seu aplicativo, contendo qualquer informação sobre a solicitação necessária para o tipo de estado que você especificar no *estado*. Consulte a tabela em [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obter mais informações sobre qualquer requisito de buffer de entrada para um determinado tipo de estado.

### <a name="inputdatasize"></a>inputDataSize

Tipo: **size_t**

O tamanho, em bytes, do buffer de entrada que você aloca e fornece em *inputData*.

### <a name="inputdata-in"></a>inputData [in]

Tipo: **void \***

Um ponteiro para um buffer de entrada que você aloca em seu aplicativo, contendo as informações de estado a serem definidas para o item de Estado cujo tipo você especificar no *estado*. Consulte a tabela em [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obter mais informações sobre o requisito de buffer de entrada para um determinado tipo de estado.

## <a name="returns"></a>Retornos

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se a função for realizada com sucesso, ela retornará **S_OK**. Caso contrário, ele retorna um [código de erro](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valor retornado|Descrição|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|O adaptador não está mais em um estado válido.|
|DXGI_ERROR_INVALID_CALL|O tipo de estado especificado no *estado* não é reconhecido por este sistema operacional (SO). Chame [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) para confirmar que a configuração do tipo de estado está disponível para esse adaptador e sistema operacional (SO).|
|DXGI_ERROR_UNSUPPORTED|O adaptador não dá suporte ao tipo de estado especificado no *estado* . Chame [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) para confirmar que a configuração do tipo de estado está disponível para esse adaptador e sistema operacional (SO).|
|E_INVALIDARG|Um tamanho de buffer insuficiente é fornecido para *inputData* (ou para *inputStateDetails* onde um buffer de detalhes de estado de entrada é necessário).|
|E_POINTER|`nullptr` foi fornecido para *inputData* (ou para *inputStateDetails* onde um buffer de detalhes de estado de entrada é necessário).|

## <a name="see-also"></a>Confira também

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)