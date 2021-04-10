---
title: TBN_GETBUTTONINFO código de notificação (commctrl. h)
description: Recupera informações de personalização da barra de ferramentas e notifica a janela pai da barra de ferramentas sobre quaisquer alterações feitas na barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 088527fe-5a38-4c35-ba68-d0cbfdee410c
keywords:
- TBN_GETBUTTONINFO de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_GETBUTTONINFO
- TBN_GETBUTTONINFOA
- TBN_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 409297306901980fa8b831e5c1129a13c596ef0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918854"
---
# <a name="tbn_getbuttoninfo-notification-code"></a>Código de notificação do TBN \_ GETBUTTONINFO

Recupera informações de personalização da barra de ferramentas e notifica a janela pai da barra de ferramentas sobre quaisquer alterações feitas na barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TBN_GETBUTTONINFO 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) . O membro **iItem** especifica um índice de base zero que fornece uma contagem dos botões que a caixa de diálogo Personalizar barra de ferramentas exibe como ambos disponíveis e presentes na barra de ferramentas. O membro **pszText** especifica o endereço do texto do botão atual e **cchText** especifica seu comprimento em caracteres. O aplicativo deve preencher a estrutura com informações sobre o botão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **true** se as informações do botão foram copiadas para a estrutura especificada; caso contrário, **false** .

## <a name="remarks"></a>Comentários

O controle Toolbar aloca um buffer e o receptor (janela pai) deve copiar o texto para esse buffer. O membro **cchText** contém o comprimento do buffer alocado pela barra de ferramentas quando tbn \_ GETBUTTONINFO é enviado para a janela pai.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **Tbn \_ GETBUTTONINFOW** (Unicode) e **tbn \_ GETBUTTONINFOA** (ANSI)<br/>       |



 

 





