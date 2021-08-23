---
title: Método getmetrics IDWriteTextLayout2
description: Recupera as métricas gerais para a cadeia de caracteres formatada.
ms.assetid: EADCD83A-9FF5-44AB-8AB5-35FCB3A84889
keywords:
- Gravação direta do método getmetrics
- Método getmetrics Direct Write, interface IDWriteTextLayout2
- IDWriteTextLayout2 interface Direct Write, método getmetrics
topic_type:
- apiref
api_name:
- IDWriteTextLayout2.GetMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7f08a0b1e47003bb818f0b80ebc3b13f639f8ded8334137d8b8812e7f0154a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070736"
---
# <a name="idwritetextlayout2getmetrics-method"></a>Método IDWriteTextLayout2:: getmetrics

Recupera as métricas gerais para a cadeia de caracteres formatada.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT GetMetrics(
  [out] DWRITE_TEXT_METRICS1 * textMetrics
) = 0;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

 *textMetrics* \[ fora\]
</dt> <dd>

Tipo: **[ **DWRITE \_ Text \_ METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1)\***

Quando esse método retorna, contém as distâncias medidas do texto e do conteúdo associado depois de serem formatados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Aplicativos de aplicativos UWP da área de trabalho R2 \|\]<br/>                          |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteTextLayout2**](idwritetextlayout2.md)
</dt> </dl>

 

 





