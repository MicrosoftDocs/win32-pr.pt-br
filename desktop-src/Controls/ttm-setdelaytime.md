---
title: Mensagem de TTM_SETDELAYTIME (commctrl. h)
description: Define as durações inicial, pop-up e Reexibir para um controle ToolTip.
ms.assetid: 0a73def0-550c-4d01-9cb1-1eb1f4356fa3
keywords:
- Controles de TTM_SETDELAYTIME de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_SETDELAYTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b633dc75baa0a8f385cf8cdb9bf7e9fa254809
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918464"
---
# <a name="ttm_setdelaytime-message"></a>TTM de \_ mensagens

Define as durações inicial, pop-up e Reexibir para um controle ToolTip.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sinalizador que especifica qual valor de tempo definir. Esse parâmetro pode ser um dos valores a seguir



| Valor                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <dt>**TTDT \_ AUTOPOP**</dt> </dl>       | Defina a quantidade de tempo que uma janela de dica de ferramenta permanecerá visível se o ponteiro for estático dentro do retângulo delimitador de uma ferramenta. Para retornar o tempo de atraso Autopop ao valor padrão, defina *lParam* como-1.<br/>                                                                                                                                                         |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <dt>**TTDT \_ inicial**</dt> </dl>       | Defina a quantidade de tempo que um ponteiro deve permanecer fixo dentro do retângulo delimitador de uma ferramenta antes que a janela de dica de ferramentas seja exibida. Para retornar o tempo de atraso inicial para seu valor padrão, defina *lParam* como-1.<br/>                                                                                                                                                    |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <dt>**remostrar TTDT \_**</dt> </dl>          | Defina a quantidade de tempo que leva para que janelas de dica de ferramenta subsequentes apareçam à medida que o ponteiro se move de uma das ferramentas para outra. Para retornar o tempo de atraso de reexibição para seu valor padrão, defina *lParam* como-1.<br/>                                                                                                                                                           |
| <span id="TTDT_AUTOMATIC"></span><span id="ttdt_automatic"></span><dl> <dt>**TTDT \_ automático**</dt> </dl> | Defina todos os três tempos de atraso para as proporções padrão. A hora de Autopop será dez vezes a hora inicial e o tempo de reapresentação será de uma quinta a hora inicial. Se esse sinalizador estiver definido, use um valor positivo de *lParam* para especificar a hora inicial, em milissegundos. Defina *lParam* como um valor negativo para retornar todos os três tempos de atraso para seus valores padrão.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o tempo de atraso, em milissegundos. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor retornado para esta mensagem não é usado.

## <a name="remarks"></a>Comentários

Os tempos de atraso padrão se baseiam no tempo de clique duplo. Para o tempo de clique duplo padrão de 500 MS, os tempos de atraso inicial, Autopop e reshow são 500 milhões, 5000ms e 100 ms, respectivamente. O fragmento de código a seguir usa a função [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime) para determinar os três tempos de atraso para qualquer sistema.


```
initial = GetDoubleClickTime();

autopop = GetDoubleClickTime() * 10;

reshow = GetDoubleClickTime() / 5;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TTM \_ GETdelaytime**](ttm-getdelaytime.md)
</dt> </dl>

 

