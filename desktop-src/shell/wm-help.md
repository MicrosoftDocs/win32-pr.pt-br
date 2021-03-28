---
description: Indica que o usuário pressionou a tecla F1.
ms.assetid: 6a090125-67dd-4267-9973-10e32c6e4f1f
title: Mensagem de WM_HELP (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dd1b042a2e57fb64eb3aa81f38cec336e33efab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967878"
---
# <a name="wm_help-message"></a>Mensagem de ajuda do WM \_

Indica que o usuário pressionou a tecla F1. Se um menu estiver ativo quando F1 for pressionado, **a \_ ajuda do WM** será enviada para a janela associada ao menu; caso contrário, a **\_ ajuda do WM** será enviada para a janela que tem o foco do teclado. Se nenhuma janela tiver o foco do teclado, a **\_ ajuda do WM** será enviada para a janela ativa no momento.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lphi* 
</dt> <dd>

O endereço de uma estrutura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) que contém informações sobre o item de menu, controle, caixa de diálogo ou janela para a qual a ajuda é solicitada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **true**.

## <a name="remarks"></a>Comentários

A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) passa **a \_ ajuda do WM** para a janela pai de uma janela filho ou para o proprietário de uma janela de nível superior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h</dt> </dl> |



 

 
