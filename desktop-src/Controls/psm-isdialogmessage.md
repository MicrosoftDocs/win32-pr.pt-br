---
title: Mensagem de PSM_ISDIALOGMESSAGE (Prsht. h)
description: Passa uma mensagem para uma caixa de diálogo de folha de propriedades e indica se a caixa de diálogo processou a mensagem. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet \_ IsDialogMessage.
ms.assetid: 7629c3f8-0b10-4585-8a95-9309c75b3ebb
keywords:
- controles de Windows de mensagem de PSM_ISDIALOGMESSAGE
topic_type:
- apiref
api_name:
- PSM_ISDIALOGMESSAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12f28d63e5586d3b083282db4e029551ce4e61d0ef997e36e3e874e9f032095b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088676"
---
# <a name="psm_isdialogmessage-message"></a>Mensagem de PSM \_ ISDIALOGMESSAGE

Passa uma mensagem para uma caixa de diálogo de folha de propriedades e indica se a caixa de diálogo processou a mensagem. Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ IsDialogMessage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura de [**msg**](/windows/win32/api/winuser/ns-winuser-msg) que contém a mensagem a ser verificada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **true** se a mensagem tiver sido processada ou **false** se a mensagem não tiver sido processada.

## <a name="remarks"></a>Comentários

Seu loop de mensagem deve usar a mensagem de **PSM \_ ISDIALOGMESSAGE** com folhas de propriedades sem janela restrita para passar mensagens para a caixa de diálogo folha de propriedades. Em sistemas que dão suporte a Unicode, use as versões Unicode das funções [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) e [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) (**GetMessageW** e **PeekMessageW**) para recuperar mensagens.

Se o valor de retorno indicar que a mensagem foi processada, ela não deverá ser passada para a função [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) ou [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) .

> [!Note]  
> Não há suporte para esta mensagem ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Folha**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

