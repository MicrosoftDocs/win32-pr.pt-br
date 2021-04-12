---
title: Mensagem de WM_HOTKEY (WinUser. h)
description: Postado quando o usuário pressiona uma tecla de atalho registrada pela função RegisterHotKey. A mensagem é colocada na parte superior da fila de mensagens associada ao thread que registrou a tecla de acesso.
ms.assetid: 28d87c2f-b2bb-4176-910b-0addea6beb93
keywords:
- Entrada de mouse e teclado de mensagem WM_HOTKEY
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
ms.openlocfilehash: 3f09e81a964542a6a8166ae54a0df4d7127466c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369498"
---
# <a name="wm_hotkey-message"></a>Mensagem de tecla de atalho do WM \_

Postado quando o usuário pressiona uma tecla de atalho registrada pela função [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) . A mensagem é colocada na parte superior da fila de mensagens associada ao thread que registrou a tecla de acesso.


```C++
#define WM_HOTKEY                       0x0312
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O identificador da tecla de acesso que gerou a mensagem. Se a mensagem tiver sido gerada por uma tecla de acesso definida pelo sistema, esse parâmetro será um dos valores a seguir.



| Valor                                                                                                                                                                                                                             | Significado                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="IDHOT_SNAPDESKTOP"></span><span id="idhot_snapdesktop"></span><dl> <dt>**IDHOT \_ SNAPDESKTOP**</dt> <dt>-2</dt> </dl> | A tecla de atalho "ajustar área de trabalho" foi pressionada.<br/> |
| <span id="IDHOT_SNAPWINDOW"></span><span id="idhot_snapwindow"></span><dl> <dt>**IDHOT \_ SNAPWINDOW**</dt> <dt>-1</dt> </dl>    | A tecla de atalho "ajustar janela" foi pressionada.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem inferior Especifica as chaves que foram pressionadas em combinação com a chave especificada pela palavra de ordem superior para gerar a mensagem de **\_ tecla de atalho do WM** . Esta palavra pode ser um ou mais dos valores a seguir. A palavra de ordem superior especifica o código de chave virtual da tecla de atalho.



| Valor                                                                                                                                                                                                               | Significado                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MOD_ALT"></span><span id="mod_alt"></span><dl> <dt>**Mod \_ ALT**</dt> <dt>0x0001</dt> </dl>             | A tecla ALT foi mantida inativa.<br/>                                                                                                                                      |
| <span id="MOD_CONTROL"></span><span id="mod_control"></span><dl> <dt>**Mod \_**</dt> <dt>0X0002</dt> de controle </dl> | A tecla CTRL foi mantida inativa.<br/>                                                                                                                                     |
| <span id="MOD_SHIFT"></span><span id="mod_shift"></span><dl> <dt>**Mod \_ SHIFT**</dt> <dt>0x0004</dt> </dl>       | A tecla SHIFT foi mantida inativa.<br/>                                                                                                                                    |
| <span id="MOD_WIN"></span><span id="mod_win"></span><dl> <dt>**Mod \_ WIN**</dt> <dt>0x0008</dt> </dl>             | A chave do WINDOWS foi mantida. Essas chaves são rotuladas com o logotipo do Windows. As teclas de tecla que envolvem a chave do Windows são reservadas para uso pelo sistema operacional.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

**WM \_ A tecla de atalho** não está relacionada às teclas de acesso do WM prekeys e do [**WM \_ settecla**](wm-sethotkey.md) . [**\_**](wm-gethotkey.md) A mensagem de **\_ tecla** de acesso do WM é enviada para chaves ativas genéricas enquanto as mensagens do WM AutoKeys e do **WM \_** estão relacionadas às teclas de **acesso de ativação \_** do Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[**WM \_**](wm-gethotkey.md)
</dt> <dt>

[**WM \_ SETtecla de atalho**](wm-sethotkey.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

