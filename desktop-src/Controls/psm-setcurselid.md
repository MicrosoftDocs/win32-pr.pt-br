---
title: Mensagem de PSM_SETCURSELID (Prsht. h)
description: Ativa a página determinada em uma folha de propriedades com base no identificador de recurso da página. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet \_ SetCurSelByID.
ms.assetid: 6db5f6ab-77ce-4a80-a84d-cb66eb1cdeaa
keywords:
- Controles de PSM_SETCURSELID de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_SETCURSELID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da6ec827bbf3b9bade0af649f124d25c420d299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086024"
---
# <a name="psm_setcurselid-message"></a>Mensagem de PSM \_ SETCURSELID

Ativa a página determinada em uma folha de propriedades com base no identificador de recurso da página. Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ SetCurSelByID**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de recurso da página a ser ativada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

A janela que está perdendo a ativação recebe o código de notificação [PSN \_ KILLACTIVE](psn-killactive.md) e a janela que está recebendo a ativação recebe o código de notificação [ \_ SetActive PSN](psn-setactive.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





