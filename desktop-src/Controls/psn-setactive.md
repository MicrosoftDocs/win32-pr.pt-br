---
title: PSN_SETACTIVE código de notificação (Prsht. h)
description: Notifica uma página que está prestes a ser ativada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 0cf918b7-9f0d-4dec-8df1-a1d2d8ac6463
keywords:
- PSN_SETACTIVE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- PSN_SETACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f38db77c1c60ef60ce713d41a6112b42235b79a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918697"
---
# <a name="psn_setactive-notification-code"></a>\_Código de notificação PSN SETactive

Notifica uma página que está prestes a ser ativada. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
PSN_SETACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contém informações sobre o código de notificação. Essa estrutura contém uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como seu primeiro membro, **HDR**. O membro **hwndFrom** dessa estrutura **NMHDR** contém o identificador para a folha de propriedades. O membro **lParam** da estrutura **PSHNOTIFY** não contém nenhuma informação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna zero para aceitar a ativação ou-1 para ativar a próxima ou a página anterior (dependendo se o usuário clicou no botão **próximo** ou **voltar** ). Para definir a ativação para uma página específica, retorne o identificador de recurso da página.

## <a name="remarks"></a>Comentários

O \_ código de notificação PSN SetActive é enviado antes que a página fique visível. Um aplicativo pode usar esse código de notificação para inicializar dados na página.

> [!Note]  
> A folha de propriedades está no processo de manipulação da lista de páginas quando o código de \_ notificação SETactive da PSN é enviado. Não tente adicionar, remover ou inserir páginas enquanto manipula este código de notificação. Isso terá resultados imprevisíveis.

 

Para definir o valor de retorno, o procedimento da caixa de diálogo para a página deve usar a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com o \_ valor MSGRESULT DWL e o procedimento da caixa de diálogo deve retornar **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

