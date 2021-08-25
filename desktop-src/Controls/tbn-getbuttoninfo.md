---
title: TBN_GETBUTTONINFO de notificação (Commctrl.h)
description: Recupera informações de personalização da barra de ferramentas e notifica a janela pai da barra de ferramentas de quaisquer alterações feitas na barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 088527fe-5a38-4c35-ba68-d0cbfdee410c
keywords:
- TBN_GETBUTTONINFO código de notificação Windows Controles
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
ms.openlocfilehash: 32a73b7da3efee0b1bb1ba829cf40356e6060a5f7e7fdfcc2467e2cca32226a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876856"
---
# <a name="tbn_getbuttoninfo-notification-code"></a>Código de \_ notificação TBN GETBUTTONINFO

Recupera informações de personalização da barra de ferramentas e notifica a janela pai da barra de ferramentas de quaisquer alterações feitas na barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_GETBUTTONINFO 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMTOOLBAR.**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) O **membro iItem** especifica um índice baseado em zero que fornece uma contagem dos botões que a caixa de diálogo Personalizar Barra de Ferramentas exibe como disponíveis e presentes na barra de ferramentas. O **membro pszText** especifica o endereço do texto do botão atual e **cchText** especifica seu comprimento em caracteres. O aplicativo deve preencher a estrutura com informações sobre o botão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se as informações do botão foram copiadas para a estrutura especificada, caso **contrário, FALSE.**

## <a name="remarks"></a>Comentários

O controle da barra de ferramentas aloca um buffer e o receptor (janela pai) deve copiar o texto para esse buffer. O **membro cchText** contém o comprimento do buffer alocado pela barra de ferramentas quando TBN \_ GETBUTTONINFO é enviado para a janela pai.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TBN \_ GETBUTTONINFOW** (Unicode) e **TBN \_ GETBUTTONINFOA** (ANSI)<br/>       |



 

 





