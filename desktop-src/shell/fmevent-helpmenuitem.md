---
description: Enviado a um procedimento de DLL de extensão do Gerenciador de arquivos quando o usuário pressiona F1 em um menu ou item de comando de barra de ferramentas. A extensão deve chamar WinHelp, com o parâmetro hWnd da função definido como o valor do parâmetro hWnd da extensão.
title: Mensagem de FMEVENT_HELPMENUITEM (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPMENUITEM
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 6298061d-7e24-45ab-8bc4-96b28e071080
ms.openlocfilehash: 46cb246e91f9901204432527ba36fd8ac72beba4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842307"
---
# <a name="fmevent_helpmenuitem-message"></a>\_Mensagem FMEVENT HELPMENUITEM

Enviado a um procedimento de DLL de extensão do Gerenciador de arquivos quando o usuário pressiona F1 em um menu ou item de comando de barra de ferramentas. A extensão deve chamar [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa), com o parâmetro *HWND* da função definido como o valor do parâmetro *hWnd* da extensão.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*uItem* 
</dt> <dd>

Um valor que identifica o menu ou o item de comando da barra de ferramentas para o qual a ajuda é desejada. O procedimento de extensão usa esse valor para determinar a melhor maneira de chamar o [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um procedimento de DLL de extensão deve retornar zero se ele processar essa mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FMEVENT \_ HelpString**](fmevent-helpstring.md)
</dt> </dl>

 

 




