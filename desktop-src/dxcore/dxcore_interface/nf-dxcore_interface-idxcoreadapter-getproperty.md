---
title: IDXCoreAdapter::GetProperty
description: Recupera o valor da propriedade de adaptador especificada.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 8adb48994580125d153c36394c4db65cb38f4a08306814d1638e5c27eb3d4868
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279396"
---
# <a name="idxcoreadaptergetproperty-method"></a>Método IDXCoreAdapter:: GetProperty

Recupera o valor da propriedade de adaptador especificada. Antes de chamar **GetProperty** para um tipo de propriedade, chame [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que o tipo de propriedade está disponível para esse adaptador e sistema operacional (SO). Além disso, antes de chamar **GetProperty**, chame [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) para determinar o tamanho necessário do buffer no qual receber o valor da propriedade.

## <a name="syntax"></a>Sintaxe

```cpp
virtual HRESULT STDMETHODCALLTYPE GetProperty(
  DXCoreAdapterProperty property,
  size_t bufferSize,
  _Out_writes_bytes_(bufferSize) void *propertyData) = 0;

template <class T>
HRESULT GetProperty( 
  DXCoreAdapterProperty property,
  _Out_writes_bytes_(sizeof(T)) T *propertyData);
```

## <a name="parameters"></a>Parâmetros

### <a name="property"></a>propriedade

Tipo: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**

O tipo da propriedade cujo valor você deseja recuperar. Consulte a tabela em [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) para obter mais informações sobre cada propriedade de adaptador.

### <a name="buffersize"></a>bufferSize

Tipo: **size_t**

O tamanho, em bytes, do buffer de saída que você aloca e fornece em *PropertyData*.

### <a name="propertydata-out"></a>propertyData [saída]

Tipo: **void \***

Um ponteiro para um buffer de saída que você aloca em seu aplicativo e que a função preenche. Chame [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) para determinar o tamanho que o buffer *PropertyData* deve ter para uma determinada propriedade de adaptador.

## <a name="returns"></a>Retornos

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se a função for realizada com sucesso, ela retornará **S_OK**. Caso contrário, ele retorna um [código de erro](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valor retornado|Descrição|
|-|-|
|DXGI_ERROR_INVALID_CALL|O tipo de propriedade especificado na *Propriedade* não é reconhecido por este sistema operacional (SO). Chame [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que o tipo de propriedade está disponível para este adaptador e sistema operacional (SO).|
|DXGI_ERROR_UNSUPPORTED|O adaptador não dá suporte ao tipo de propriedade especificado na *Propriedade* . Chame [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que o tipo de propriedade está disponível para este adaptador e sistema operacional (SO).|
|E_INVALIDARG|Um tamanho de buffer insuficiente é fornecido em *PropertyData*. Chame [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) para determinar o tamanho que o buffer *PropertyData* deve ter para uma determinada propriedade de adaptador.|
|E_POINTER|`nullptr` foi fornecido para *PropertyData*.|

## <a name="remarks"></a>Comentários

Você pode chamar **GetProperty** em um adaptador que não é mais válido &mdash; . a função não falhará como resultado disso. Essa função zera o buffer *PropertyData* antes de preenchê-lo.

## <a name="see-also"></a>Confira também

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)