---
description: Enviado por uma extensão do Gerenciador de arquivos para fazer com que o Gerenciador de arquivos repinte sua janela ativa ou todas as suas janelas.
title: Mensagem de FM_REFRESH_WINDOWS (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_REFRESH_WINDOWS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 210168c6-d83b-4ffd-93d4-d22fa748cef2
ms.openlocfilehash: 386fdee5c7a8b56899fa7e13282445c57eccff08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164183"
---
# <a name="fm_refresh_windows-message"></a>Mensagem de atualização de FM do \_ \_ Windows

Enviado por uma extensão do Gerenciador de arquivos para fazer com que o Gerenciador de arquivos repinte sua janela ativa ou todas as suas janelas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fRepaint* 
</dt> <dd>

Um valor que indica se o Gerenciador de arquivos redesenha sua janela ativa ou todas as suas janelas. Se esse parâmetro for **true**, o Gerenciador de arquivos repintará todas as suas janelas. Caso contrário, o Gerenciador de arquivos repintará apenas sua janela ativa.

</dd> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

As alterações do sistema de arquivos causadas por uma extensão são detectadas automaticamente pelo Gerenciador de arquivos. Uma extensão deve usar essa mensagem somente em situações em que as conexões de unidade são feitas ou canceladas.

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

 

 




