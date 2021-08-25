---
title: Mensagem de PSM_SETCURSELID (Prsht. h)
description: Ativa a página determinada em uma folha de propriedades com base no identificador de recurso da página. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet \_ SetCurSelByID.
ms.assetid: 6db5f6ab-77ce-4a80-a84d-cb66eb1cdeaa
keywords:
- controles de Windows de mensagem de PSM_SETCURSELID
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
ms.openlocfilehash: 7be1d21b5153d480e409c6e9e7f4204746b5509b058bc292509e24ad9e03b538
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877016"
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

## <a name="return-value"></a>Valor retornado

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

A janela que está perdendo a ativação recebe o código de notificação [PSN \_ KILLACTIVE](psn-killactive.md) e a janela que está recebendo a ativação recebe o código de notificação [ \_ SetActive PSN](psn-setactive.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





