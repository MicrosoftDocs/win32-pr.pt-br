---
description: O \_ método Put Caption define o título ou a legenda da janela.
ms.assetid: 6671805a-e1ef-40f1-bc3f-bf7954ff9851
title: Método de CBaseControlWindow.put_Caption (Ctlutil. h)
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
ms.openlocfilehash: aca8e5e7ad04acae9fab1cfe2d44f982266805e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749855"
---
# <a name="cbasecontrolwindowput_caption-method"></a>Método de legenda CBaseControlWindow. put \_

O `put_Caption` método define o título ou a legenda da janela.

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

Nova legenda da janela.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

A maioria das janelas de nível superior em uma área de trabalho baseada no Windows tem um título (legenda) associado a elas. Essa propriedade pode ser consultada e definida por meio da interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) . Qualquer conjunto de legendas será visível somente se a janela tiver o \_ estilo de legenda WS aplicado. Se não tiver, a legenda ainda poderá ser definida (e recuperada), embora não seja visível para o usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




