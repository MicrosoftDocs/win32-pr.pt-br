---
title: Mensagem de PSM_REBOOTSYSTEM (Prsht. h)
description: Indica que o sistema precisa ser reiniciado para que as alterações entrem em vigor. Você pode enviar a mensagem de PSM \_ REBOOTSYSTEM explicitamente ou usando a \_ macro PropSheet REBOOTSYSTEM.
ms.assetid: 461fce3c-183a-4b9b-8eab-ed2838d9f866
keywords:
- Controles de PSM_REBOOTSYSTEM de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_REBOOTSYSTEM
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14f5018dc3845d699561740ccd9cbb0a9c793f15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454927"
---
# <a name="psm_rebootsystem-message"></a>Mensagem de PSM \_ REBOOTSYSTEM

Indica que o sistema precisa ser reiniciado para que as alterações entrem em vigor. Você pode enviar a mensagem de **PSM \_ REBOOTSYSTEM** explicitamente ou usando a macro [**PropSheet \_ REBOOTSYSTEM**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) .

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

Um aplicativo deve enviar essa mensagem somente em resposta à mensagem de notificação [PSN \_ Apply](psn-apply.md) ou [PSN \_ KILLACTIVE](psn-killactive.md) .

Essa mensagem faz com que a função [**folha**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) retorne o \_ valor PSREBOOTSYSTEM da ID, mas somente se o usuário clicar no botão **OK** para fechar a folha de propriedades. É responsabilidade do aplicativo reinicializar o sistema, o que pode ser feito usando a função [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) .

Essa mensagem substitui todas as mensagens de [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) que precedem ou seguem.

> [!Note]  
> Não há suporte para esta mensagem ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

