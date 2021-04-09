---
title: Mensagem de PSM_SETCURSEL (Prsht. h)
description: Ativa a página especificada em uma folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a \_ macro Setcurseal PropSheet.
ms.assetid: 800aadde-cabc-424e-8e63-60fc7ce952d7
keywords:
- Controles de PSM_SETCURSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_SETCURSEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12f41f0ba2ec8d13a7bfc932b553b355399f76b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085458"
---
# <a name="psm_setcursel-message"></a>Mensagem de PSM \_ SETcurse

Ativa a página especificada em uma folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ setcurseal PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice de base zero da página. Um aplicativo pode especificar o índice ou o identificador ou ambos. Se ambos forem especificados, *lParam* terá precedência.

</dd> <dt>

*lParam* 
</dt> <dd>

O identificador da página a ser ativada. Um aplicativo pode especificar o índice ou o identificador ou ambos. Se ambos forem especificados, *lParam* terá precedência.

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



 

 





