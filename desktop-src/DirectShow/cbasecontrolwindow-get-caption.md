---
description: O \_ método Get Caption recupera a legenda da janela atual.
ms.assetid: 51ce9cf8-0b2a-4459-b005-02dc45444fd8
title: Método de CBaseControlWindow.get_Caption (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b8d743c746f833007d91afd4346f7f48c6218dde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752113"
---
# <a name="cbasecontrolwindowget_caption-method"></a>Método de legenda CBaseControlWindow. get \_

O `get_Caption` método recupera a legenda da janela atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Caption(
   BSTR *pstrCaption
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pstrCaption* 
</dt> <dd>

Ponteiro para a legenda da janela atual.

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

 

 




