---
description: Enviado por uma extensão do Gerenciador de arquivos (ou outro aplicativo) para fazer com que o Gerenciador de arquivos recarregue todas as DLLs de extensão listadas na \[ \] seção Complementos do arquivo de Winfile.ini.
ms.assetid: 5103a986-5f45-4deb-aaae-c6e87cb60051
title: Mensagem de FM_RELOAD_EXTENSIONS (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_RELOAD_EXTENSIONS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: 9e82ec9ec638cb70cc7b571ed9e5e76d604cd4da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967941"
---
# <a name="fm_reload_extensions-message"></a>\_Mensagem de extensões de REcarregamento de FM \_

Enviado por uma extensão do Gerenciador de arquivos (ou outro aplicativo) para fazer com que o Gerenciador de arquivos recarregue todas as DLLs de extensão listadas na \[ \] seção Complementos do arquivo de Winfile.ini.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Outros aplicativos podem usar a função [**CreateMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) para enviar essa mensagem ao Gerenciador de arquivos. Para obter o identificador apropriado da janela do Gerenciador de arquivos, um aplicativo pode especificar "WFS \_ frame" como o parâmetro *lpszClassName* em uma chamada para a função [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) .

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

 

 
