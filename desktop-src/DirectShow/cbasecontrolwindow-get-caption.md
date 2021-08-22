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
ms.openlocfilehash: 0f05501adbd486eaa60e939aacfdd5896c0fbcae059673029f04fcca8aeb742a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640881"
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

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

a maioria das janelas de nível superior em uma área de trabalho baseada em Windows tem um título (legenda) associado a elas. Essa propriedade pode ser consultada e definida por meio da interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) . Qualquer conjunto de legendas será visível somente se a janela tiver o \_ estilo de legenda WS aplicado. Se não tiver, a legenda ainda poderá ser definida (e recuperada), embora não seja visível para o usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




