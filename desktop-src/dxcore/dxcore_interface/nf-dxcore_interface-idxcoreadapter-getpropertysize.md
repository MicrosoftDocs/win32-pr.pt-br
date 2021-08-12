---
title: IDXCoreAdapter::GetPropertySize
description: Para uma propriedade de adaptador especificada, recupera o tamanho do buffer, em bytes, necessário para uma chamada para [GetProperty.](./nf-dxcore_interface-idxcoreadapter-getproperty.md)
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 525e2657ab7af5fa6f7cee4f527b74604d2674dbc67da232dd6501ddc45b0291
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279248"
---
# <a name="idxcoreadaptergetpropertysize-method"></a>Método IDXCoreAdapter::GetPropertySize

Para uma propriedade de adaptador especificada, recupera o tamanho do buffer, em bytes, necessário para uma chamada para [GetProperty.](./nf-dxcore_interface-idxcoreadapter-getproperty.md) Antes de **chamar GetPropertySize** para um tipo de propriedade, chame [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar se o tipo de propriedade está disponível para esse adaptador e sistema operacional (SO).

## <a name="syntax"></a>Sintaxe

```cpp
virtual HRESULT STDMETHODCALLTYPE GetPropertySize(
  DXCoreAdapterProperty property,
  _Out_ size_t *bufferSize) = 0;
```

## <a name="parameters"></a>Parâmetros

### <a name="property"></a>propriedade

Tipo: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**

O tipo da propriedade cujo tamanho, em bytes, você deseja recuperar.

### <a name="buffersize-out"></a>bufferSize [out]

Tipo: **size_t \***

Um ponteiro para um **size_t** valor. A função desreferencia o ponteiro e define o valor para o tamanho, em bytes, do buffer de saída que você deve alocar e passar como o argumento *propertyData* em sua chamada para [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).

## <a name="returns"></a>Retornos

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se a função for bem-sucedida, ela **retornará S_OK**. Caso contrário, retornará um [**código de erro HRESULT**](../../com/structure-of-com-error-codes.md) [.](../../com/com-error-codes-10.md)

|Valor retornado|Descrição|
|-|-|
|DXGI_ERROR_INVALID_CALL|O tipo de propriedade especificado na *propriedade não* é reconhecido por esse sistema operacional (SO). Chame [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar se o tipo de propriedade está disponível para esse adaptador e sistema operacional (SO).|
|DXGI_ERROR_UNSUPPORTED|O tipo de propriedade especificado *na propriedade* não é suportado pelo adaptador. Chame [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar se o tipo de propriedade está disponível para esse adaptador e sistema operacional (SO).|
|E_POINTER|`nullptr` foi fornecido para *bufferSize*.|

## <a name="remarks"></a>Comentários

Você pode chamar **GetPropertySize** em um adaptador que não seja mais válido, &mdash; a função não falhará.

## <a name="see-also"></a>Confira também

[IDXCoreAdapter,](./nn-dxcore_interface-idxcoreadapter.md) [Referência de DXCore,](../dxcore-reference.md) [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)