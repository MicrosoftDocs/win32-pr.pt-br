---
description: Enviado a uma DLL de extensão quando o usuário seleciona o menu para a extensão na barra de menus do Gerenciador de arquivos. A extensão pode usar essa notificação para inicializar itens de menu.
title: Mensagem de FMEVENT_INITMENU (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_INITMENU
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8074a09f-ad94-4a7a-8c0b-965b0f8f6334
ms.openlocfilehash: 4bbb959feeb2c1bf99eaa999b4c51b69b0d0cf63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164181"
---
# <a name="fmevent_initmenu-message"></a>\_Mensagem FMEVENT INITMENU

Enviado a uma DLL de extensão quando o usuário seleciona o menu para a extensão na barra de menus do Gerenciador de arquivos. A extensão pode usar essa notificação para inicializar itens de menu.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*hmenu* 
</dt> <dd>

Um identificador para a barra de menus do Gerenciador de arquivos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Uma DLL de extensão deve retornar zero se ela processar essa mensagem.

## <a name="remarks"></a>Comentários

Uma extensão DLL recebe essa mensagem somente quando o usuário seleciona o menu de nível superior. Se a extensão contiver submenus, ela deverá inicializá-las ao mesmo tempo que inicializar o menu de nível superior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




