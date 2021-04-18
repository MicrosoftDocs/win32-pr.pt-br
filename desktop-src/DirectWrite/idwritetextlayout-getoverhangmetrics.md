---
title: Método IDWriteTextLayout GetOverhangMetrics
description: Retorna os sobretravamentos (em DIPs) do layout e todos os objetos contidos nele, incluindo os glifos de texto e objetos embutidos.
ms.assetid: 4b23f6c5-cacc-41e2-8934-6f95208b999a
keywords:
- Gravação direta do método GetOverhangMetrics
- Método GetOverhangMetrics Direct Write, interface IDWriteTextLayout
- IDWriteTextLayout interface de gravação direta, método GetOverhangMetrics
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
ms.openlocfilehash: 8d8a015998f0a673a310319f93d8f4892dd4b1c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766922"
---
# <a name="idwritetextlayoutgetoverhangmetrics-method"></a>Método IDWriteTextLayout:: GetOverhangMetrics

Retorna os sobretravamentos (em DIPs) do layout e todos os objetos contidos nele, incluindo os glifos de texto e objetos embutidos.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sobretravamentos* \[ fora\]
</dt> <dd>

Tipo: **[ **DWRITE \_ de \_ métricas de folga**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***

Sobrelançações de extensões visíveis (em DIPs) fora do layout.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Sublinhados e tachados não contribuem para a determinação da caixa preta, pois eles são, na verdade, desenhados pelo renderizador, que tem permissão para desenhá-los em qualquer variedade de estilos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

