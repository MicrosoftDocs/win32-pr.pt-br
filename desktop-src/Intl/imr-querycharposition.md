---
description: Notifica um aplicativo quando o IME selecionado precisa de informações sobre as coordenadas de um caractere na cadeia de caracteres de composição. O aplicativo recebe esse comando por meio da \_ mensagem de solicitação IME do WM \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: cae7e5b3-8aaf-452d-80df-fb0ae04a342c
title: IMR_QUERYCHARPOSITION código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6a37679dce6a17d5687aeed1c8fbd1d5c8bf6651b3cfc597cfdfc2e419ecba3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948763"
---
# <a name="imr_querycharposition-notification-code"></a>Código de notificação do IMR \_ QUERYCHARPOSITION

Notifica um aplicativo quando o IME selecionado precisa de informações sobre as coordenadas de um caractere na cadeia de caracteres de composição. O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ solicitação IME do WM**](wm-ime-request.md) com configurações de parâmetro, conforme mostrado abaixo.


```C++
LRESULT IMR_QUERYCHARPOSITION
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Defina como IMR \_ QUERYCHARPOSITION.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Ponteiro para uma estrutura [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) que contém a posição do caractere na janela de composição.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um valor diferente de zero se o aplicativo preenche a estrutura [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) . Caso contrário, o comando retornará 0.

## <a name="remarks"></a>Comentários

Um aplicativo que desenha a própria cadeia de caracteres de composição, em vez de depender do IME, é responsável por preencher todos os membros da estrutura [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) . Caso contrário, o aplicativo deve passar o comando para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ou [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea) se ele tiver sua própria janela de interface do usuário do IME.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>Imm. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Comandos do Gerenciador de métodos de entrada](input-method-manager-commands.md)
</dt> <dt>

[**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition)
</dt> <dt>

[**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> <dt>

[**\_solicitação do IME do WM \_**](wm-ime-request.md)
</dt> </dl>

 

 
