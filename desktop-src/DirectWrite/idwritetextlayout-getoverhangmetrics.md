---
title: Método IDWriteTextLayout GetOvermetrics
description: Retorna os excessos (em DIPs) do layout e todos os objetos contidos nele, incluindo glifos de texto e objetos em linha.
ms.assetid: 4b23f6c5-cacc-41e2-8934-6f95208b999a
keywords:
- Gravação direta do método GetOvermetrics
- Método GetOvermetrics Direct Write , interface IDWriteTextLayout
- IDWriteTextLayout interface Direct Write , GetOvermetrics method
topic_type:
- apiref
api_name:
- IDWriteTextLayout.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb3591df5dc02fdc63215ff2276202df62347ed21aef23991b4ddcadef094281
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649741"
---
# <a name="idwritetextlayoutgetoverhangmetrics-method"></a>Método IDWriteTextLayout::GetOvermetrics

Retorna os excessos (em DIPs) do layout e todos os objetos contidos nele, incluindo glifos de texto e objetos em linha.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*over over* \[ out\]
</dt> <dd>

Tipo: **[ **DWRITE \_ OVER DIGIT \_ METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***

Sobrefiliações de extensão visíveis (em DIPs) fora do layout.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Sublinhados e tachados não contribuem para a determinação da caixa preta, pois eles são realmente desenhados pelo renderador, que tem permissão para desenhá-los em qualquer variedade de estilos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

