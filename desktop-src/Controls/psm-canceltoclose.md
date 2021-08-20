---
title: Mensagem de PSM_CANCELTOCLOSE (Prsht. h)
description: Enviado por um aplicativo quando ele realizou alterações desde a notificação de aplicação de PSN mais recente \_ que não pode ser cancelada. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet \_ CancelToClose.
ms.assetid: 0a4b6176-7ddb-469f-8ebf-a31e533a8690
keywords:
- controles de Windows de mensagem de PSM_CANCELTOCLOSE
topic_type:
- apiref
api_name:
- PSM_CANCELTOCLOSE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65c37c46e1232d8f99b8666e86058a13b840fbc975d94355d75ef40a810ee23c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169812"
---
# <a name="psm_canceltoclose-message"></a>Mensagem de PSM \_ CANCELTOCLOSE

Enviado por um aplicativo quando ele realizou alterações desde a notificação de [ \_ aplicação de PSN](psn-apply.md) mais recente que não pode ser cancelada. Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ CancelToClose**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) .

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

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

**PSM \_ CANCELTOCLOSE** desabilita o botão **Cancelar** e altera o texto do botão **OK** para "fechar".

A maioria das folhas de propriedades aguarda a execução de alterações irreversíveis até que uma notificação de aplicação de PSN \_ seja recebida. No entanto, em algumas circunstâncias, uma folha de propriedades pode fazer alterações irreversíveis fora da \_ sequência de redefinição de aplicação/PSN padrão PSN \_ . Um exemplo é uma folha de propriedades que contém um botão de **edição** que é usado para exibir uma caixa de diálogo para editar uma propriedade. Quando o usuário clica em **OK** para enviar a alteração, a página da folha de propriedades tem várias opções.

-   Ele pode registrar as alterações, mas aguarde até receber uma notificação de \_ aplicação de PSN para aplicá-las. Essa é a abordagem preferida.
-   Ele pode aplicar as alterações imediatamente após sair da caixa de diálogo, mas lembre-se das configurações originais. Essas configurações podem ser usadas para restaurar o estado original se uma \_ notificação de redefinição de PSN for recebida.
-   Ele pode aplicar as alterações imediatamente e não tentar restaurar as configurações originais quando receber uma notificação de [ \_ redefinição de PSN](psn-reset.md) . Essa abordagem não é recomendada, mas pode ser necessária se as alterações estiverem muito longe para que as outras duas opções sejam práticas.

Para a terceira opção, os aplicativos devem enviar uma mensagem de **PSM \_ CANCELTOCLOSE** para a folha de propriedades. Ele indica ao usuário que as alterações feitas com a caixa de diálogo não podem ser revertidas clicando no botão **Cancelar** .

> [!Note]  
> Não há suporte para esta mensagem ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





