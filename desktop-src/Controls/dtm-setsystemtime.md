---
title: Mensagem de DTM_SETSYSTEMTIME (commctrl. h)
description: Define a hora em um controle DTP (data and time Picker). Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetSystemTime DateTime.
ms.assetid: aab023ac-22ef-485b-be2f-2aa76dfcf57f
keywords:
- Controles de DTM_SETSYSTEMTIME de mensagens do Windows
topic_type:
- apiref
api_name:
- DTM_SETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b2a3c625ad4ff02bed138a8086ca0da984de35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918921"
---
# <a name="dtm_setsystemtime-message"></a>DTM de \_ mensagens

Define a hora em um controle DTP (data and time Picker). Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetSystemTime DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um valor que especifica a ação que deve ser executada. Esse valor deve ser definido como um dos seguintes:



| Valor                                                                                                                                             | Significado                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDT_VALID"></span><span id="gdt_valid"></span><dl> <dt>**GDT \_ válida**</dt> </dl> | Defina o controle DTP de acordo com os dados dentro da estrutura que os *lParam* apontam. <br/>                                                                                                                                                                 |
| <span id="GDT_NONE"></span><span id="gdt_none"></span><dl> <dt>**GDT \_ None**</dt> </dl>    | Defina o controle DTP como "sem data" e desmarque sua caixa de seleção. Quando esse sinalizador é especificado, *lParam* é ignorado. Esse sinalizador se aplica somente a controles DTP que são definidos para o estilo [**DTS \_ All None**](date-and-time-picker-control-styles.md) . <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que contém a hora do sistema usada para definir o controle DTP.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

