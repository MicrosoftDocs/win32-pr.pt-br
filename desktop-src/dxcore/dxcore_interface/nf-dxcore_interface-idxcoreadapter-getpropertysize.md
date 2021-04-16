---
title: IDXCoreAdapter::GetPropertySize
description: Para uma propriedade de adaptador especificada, recupera o tamanho do buffer, em bytes, que é necessário para uma chamada para [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ff077d3c4c827a55f7fd9b10dfe93f1271649f72
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105808382"
---
# <a name="idxcoreadaptergetpropertysize-method"></a>Método IDXCoreAdapter:: GetPropertySize

Para uma propriedade de adaptador especificada, recupera o tamanho do buffer, em bytes, que é necessário para uma chamada para [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md). Antes de chamar **GetPropertySize** para um tipo de propriedade, chame [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que o tipo de propriedade está disponível para esse adaptador e sistema operacional (SO).

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

### <a name="buffersize-out"></a>bufferSize [saída]

Tipo: **size_t \***

Um ponteiro para um valor **size_t** . A função desreferencia o ponteiro e define o valor para o tamanho, em bytes, do buffer de saída que você deve alocar e passar como o argumento *PropertyData* em sua chamada para [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).

## <a name="returns"></a>Retornos

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se a função for realizada com sucesso, ela retornará **S_OK**. Caso contrário, ele retorna um [código de erro](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valor retornado|Descrição|
|-|-|
|DXGI_ERROR_INVALID_CALL|O tipo de propriedade especificado na *Propriedade* não é reconhecido por este sistema operacional (SO). Chame [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que o tipo de propriedade está disponível para este adaptador e sistema operacional (SO).|
|DXGI_ERROR_UNSUPPORTED|O adaptador não dá suporte ao tipo de propriedade especificado na *Propriedade* . Chame [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que o tipo de propriedade está disponível para este adaptador e sistema operacional (SO).|
|E_POINTER|`nullptr` foi fornecido para *BufferSize*.|

## <a name="remarks"></a>Comentários

Você pode chamar **GetPropertySize** em um adaptador que não é mais válido &mdash; . a função não falhará.

## <a name="see-also"></a>Confira também

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)