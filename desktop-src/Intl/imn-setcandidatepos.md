---
description: Notifica um aplicativo quando o processamento do candidato é concluído e o IME está prestes a mover a janela candidata. O aplicativo recebe esse comando por meio da mensagem WM \_ IME \_ NOTIFY com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: 64252d88-130b-44c3-854a-78b01def7a13
title: IMN_SETCANDIDATEPOS de notificação (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 689dfe0c38f5508c853af94e271bb1f333bfbad0df18b3fab09450d73497e7fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107056"
---
# <a name="imn_setcandidatepos-notification-code"></a>Código de notificação \_ IMN SETCANDIDATEPOS

Notifica um aplicativo quando o processamento do candidato é concluído e o IME está prestes a mover a janela candidata. O aplicativo recebe esse comando por meio da mensagem [**WM \_ IME \_ NOTIFY**](wm-ime-notify.md) com configurações de parâmetro, conforme mostrado abaixo.


```C++
IMN_SETCANDIDATEPOS
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Definido como IMN \_ SETCANDIDATEPOS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Sinalizador de lista de candidatos. Cada bit corresponde a uma lista de candidatos: bit 0 para a primeira lista, bit 1 para o segundo e assim por diante. Se um bit especificado for 1, a janela candidata correspondente estará prestes a ser movida.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse comando não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

Um aplicativo deverá processar esse comando se ele exibir a janela candidata em si.

A janela do IME move a janela candidata quando processa esse comando.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>Imm.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de Métodos de Entrada](input-method-manager.md)
</dt> <dt>

[Comandos do Gerenciador de Métodos de Entrada](input-method-manager-commands.md)
</dt> <dt>

[**NOTIFICAÇÃO \_ DO WM IME \_**](wm-ime-notify.md)
</dt> </dl>

 

 




