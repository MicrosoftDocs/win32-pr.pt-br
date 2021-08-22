---
title: WM_HOTKEY mensagem (Winuser.h)
description: Postado quando o usuário pressiona uma tecla de acesso registrada pela função RegisterHotKey. A mensagem é colocada na parte superior da fila de mensagens associada ao thread que registrou a tecla de hot.
ms.assetid: 28d87c2f-b2bb-4176-910b-0addea6beb93
keywords:
- WM_HOTKEY entrada do mouse e teclado da mensagem
topic_type:
- apiref
api_name:
- WM_HOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51dbd37b61fea12e559323a73cbf6b4a5cb54704a74663f865d9aa89636d3c46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119557136"
---
# <a name="wm_hotkey-message"></a>Mensagem WM \_ HOTKEY

Postado quando o usuário pressiona uma tecla de acesso registrada pela [**função RegisterHotKey.**](/windows/win32/api/winuser/nf-winuser-registerhotkey) A mensagem é colocada na parte superior da fila de mensagens associada ao thread que registrou a tecla de hot.


```C++
#define WM_HOTKEY                       0x0312
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O identificador da tecla quente que gerou a mensagem. Se a mensagem tiver sido gerada por uma chave quente definida pelo sistema, esse parâmetro será um dos valores a seguir.



| Valor                                                                                                                                                                                                                             | Significado                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="IDHOT_SNAPDESKTOP"></span><span id="idhot_snapdesktop"></span><dl> <dt>**IDHOT \_ SNAPDESKTOP**</dt> <dt>-2</dt> </dl> | A tecla de hot key "snap desktop" foi pressionada.<br/> |
| <span id="IDHOT_SNAPWINDOW"></span><span id="idhot_snapwindow"></span><dl> <dt>**IDHOT \_ SNAPWINDOW**</dt> <dt>-1</dt> </dl>    | A tecla de tecla quente "snap window" foi pressionada.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem baixa especifica as chaves que devem ser pressionadas em combinação com a chave especificada pela palavra de ordem alta para gerar a mensagem **WM \_ HOTKEY.** Essa palavra pode ser um ou mais dos valores a seguir. A palavra de ordem alta especifica o código de chave virtual da chave quente.



| Valor                                                                                                                                                                                                               | Significado                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MOD_ALT"></span><span id="mod_alt"></span><dl> <dt>**MOD \_ Alt**</dt> <dt>0x0001</dt> </dl>             | Qualquer tecla ALT foi mantida para baixo.<br/>                                                                                                                                      |
| <span id="MOD_CONTROL"></span><span id="mod_control"></span><dl> <dt>**MOD \_ CONTROLE**</dt> <dt>0x0002</dt> </dl> | Qualquer tecla CTRL foi mantida para baixo.<br/>                                                                                                                                     |
| <span id="MOD_SHIFT"></span><span id="mod_shift"></span><dl> <dt>**MOD \_ SHIFT**</dt> <dt>0x0004</dt> </dl>       | Qualquer tecla SHIFT foi mantida para baixo.<br/>                                                                                                                                    |
| <span id="MOD_WIN"></span><span id="mod_win"></span><dl> <dt>**MOD \_ WIN**</dt> <dt>0x0008</dt> </dl>             | Uma das teclas WINDOWS foi mantida para baixo. Essas chaves são rotuladas com o logotipo Windows dados. Teclas de atalho que envolvem Windows chave de segurança são reservadas para uso pelo sistema operacional.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

**WM \_ HOTKEY** não está relacionado às teclas de acesso [**WM \_ GETHOTKEY**](wm-gethotkey.md) [**e WM \_ SETHOTKEY.**](wm-sethotkey.md) A **mensagem WM \_ HOTKEY** é enviada para chaves quentes genéricas, enquanto as mensagens **WM \_ SETHOTKEY** e **WM \_ GETHOTKEY** estão relacionadas às teclas de acesso de ativação da janela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Registerhotkey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[**WM \_ GETHOTKEY**](wm-gethotkey.md)
</dt> <dt>

[**WM \_ SETHOTKEY**](wm-sethotkey.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Entrada do teclado](keyboard-input.md)
</dt> </dl>

 

