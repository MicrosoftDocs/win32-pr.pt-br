---
description: O método put \_ Caption define o título ou a legenda da janela.
ms.assetid: 6671805a-e1ef-40f1-bc3f-bf7954ff9851
title: CBaseControlWindow.put_Caption método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c7f0c9da5ad2c3ae409e14a1ca9918a0c1aa7ef04615ab4d647ce1a3467c7311
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983696"
---
# <a name="cbasecontrolwindowput_caption-method"></a>Método CBaseControlWindow.put \_ Caption

O `put_Caption` método define o título ou legenda da janela.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_Caption(
   BSTR strCaption
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strCaption* 
</dt> <dd>

Legenda da nova janela.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="remarks"></a>Comentários

A maioria das janelas de nível superior Windows área de trabalho baseada em Windows tem um título (legenda) associado a elas. Essa propriedade pode ser consultada e definida por meio da interface [**IVideoWindow.**](/windows/desktop/api/Control/nn-control-ivideowindow) Qualquer conjunto de legendas ficará visível somente se a janela tiver o estilo CAPTION do WS \_ aplicado. Se não, a legenda ainda poderá ser definida (e recuperada), embora não seja visível para o usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




