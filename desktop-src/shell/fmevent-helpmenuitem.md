---
description: Enviado para um procedimento de DLL de extensão do Gerenciador de Arquivos quando o usuário pressiona F1 em um menu ou item de comando da barra de ferramentas. A extensão deve chamar WinHelp, com o parâmetro hwnd dessa função definido como o valor do parâmetro hwnd da extensão.
title: FMEVENT_HELPMENUITEM mensagem (Wfext.h)
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
ms.openlocfilehash: 69078274ccd8a7a7b91bbd7bd8e8d84b3b033cec6dbcf4ce495ac2ebfd0e8381
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224160"
---
# <a name="fmevent_helpmenuitem-message"></a>Mensagem FMEVENT \_ HELPMENUITEM

Enviado para um procedimento de DLL de extensão do Gerenciador de Arquivos quando o usuário pressiona F1 em um menu ou item de comando da barra de ferramentas. A extensão deve chamar [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa), com o parâmetro *hwnd* dessa função definido como o valor do parâmetro *hwnd da* extensão.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*Uitem* 
</dt> <dd>

Um valor que identifica o menu ou o item de comando da barra de ferramentas para o qual a Ajuda é desejada. O procedimento de extensão usa esse valor para determinar a melhor maneira de chamar [**WinHelp.**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um procedimento de DLL de extensão deverá retornar zero se ele processa essa mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FMEVENT \_ HELPSTRING**](fmevent-helpstring.md)
</dt> </dl>

 

 




