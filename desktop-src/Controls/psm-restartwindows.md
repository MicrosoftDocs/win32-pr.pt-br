---
title: Mensagem de PSM_RESTARTWINDOWS (Prsht. h)
description: Indica que o Windows precisa ser reiniciado para que as alterações entrem em vigor.
ms.assetid: 5bf634ee-7408-45df-adb6-c5b947f6c47b
keywords:
- Controles de PSM_RESTARTWINDOWS de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_RESTARTWINDOWS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb12126ae0a2b9187a941ccc1aff53186a0cda7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824334"
---
# <a name="psm_restartwindows-message"></a>Mensagem de PSM \_ RESTARTWINDOWS

Indica que o Windows precisa ser reiniciado para que as alterações entrem em vigor.

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

Um aplicativo deve enviar essa mensagem somente em resposta ao código de notificação [PSN \_ Apply](psn-apply.md) ou [PSN \_ KILLACTIVE](psn-killactive.md) . Você pode enviar a mensagem de **PSM \_ RESTARTWINDOWS** explicitamente ou usando a macro [**PropSheet \_ RESTARTWINDOWS**](/windows/desktop/api/Prsht/nf-prsht-propsheet_restartwindows) .

Essa mensagem faz com que a função [**folha**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) retorne o \_ valor PSRESTARTWINDOWS da ID, mas somente se o usuário clicar no botão **OK** para fechar a folha de propriedades. É responsabilidade do aplicativo reiniciar o Windows, o que pode ser feito usando a função [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) .

> [!Note]  
> Não há suporte para esta mensagem ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

