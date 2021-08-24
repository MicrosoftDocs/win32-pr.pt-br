---
description: Preterido. O PenInputPanel foi substituído pelo painel de entrada de texto (TIP). Ocorre quando o objeto PenInputPanel está sendo movido.
ms.assetid: 0c51d875-cef9-4087-b17d-5c5af04f81a5
title: Evento PenInputPanel. PanelMoving (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4a152afdef9fcd10fb92fdec55d9a460faf58ca91536e96c9876203fbad44c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596593"
---
# <a name="peninputpanelpanelmoving-event"></a>Evento PenInputPanel. PanelMoving

Preterido. O [**PenInputPanel**](peninputpanel-class.md) foi substituído pelo painel de [entrada de texto (TIP)](text-input-panel-reference.md).

Ocorre quando o objeto [**PenInputPanel**](peninputpanel-class.md) está sendo movido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PanelMoving(
  [in, out] long *Left,
  [in, out] long *Top
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*À esquerda* \[ entrada, saída\]
</dt> <dd>

A nova posição horizontal, ou eixo x, da borda esquerda do objeto [**PenInputPanel**](peninputpanel-class.md) , em coordenadas da tela.

</dd> <dt>

*Superior* \[ entrada, saída\]
</dt> <dd>

A nova posição vertical, ou eixo y, da borda esquerda do objeto [**PenInputPanel**](peninputpanel-class.md) , em coordenadas da tela.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse evento for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

O evento **PanelMoving** foi projetado para ser usado para alterar a posição do painel de entrada da caneta, alterando os parâmetros *esquerdo* e *superior* .

Os métodos [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) e [**Refresh**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh) fazem com que o objeto [**PenInputPanel**](peninputpanel-class.md) chame seu código de posicionamento automático, que dispara um evento **PanelMoving** . Consequentemente, chamar esses métodos dentro de um manipulador **PanelMoving** pode resultar em um loop infinito recursivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PenInputPanel**](peninputpanel-class.md)
</dt> </dl>

 

 




