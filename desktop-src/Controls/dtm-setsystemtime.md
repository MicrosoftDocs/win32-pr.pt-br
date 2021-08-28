---
title: DTM_SETSYSTEMTIME mensagem (Commctrl.h)
description: Define a hora em um controle DTP (selador de data e hora). Você pode enviar essa mensagem explicitamente ou usar a macro DateTime \_ SetSystemtime.
ms.assetid: aab023ac-22ef-485b-be2f-2aa76dfcf57f
keywords:
- DTM_SETSYSTEMTIME controles de Windows mensagem
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
ms.openlocfilehash: 5acd0c6a09e3fc7bd9d068e27049329f3289a8ba1968ffae4592c7e07db9f2eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088966"
---
# <a name="dtm_setsystemtime-message"></a>Mensagem DTM \_ SETSYSTEMTIME

Define a hora em um controle DTP (selador de data e hora). Você pode enviar essa mensagem explicitamente ou usar a [**macro DateTime \_ SetSystemtime.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um valor que especifica a ação que deve ser executada. Esse valor deve ser definido como um dos seguintes:



| Valor                                                                                                                                             | Significado                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDT_VALID"></span><span id="gdt_valid"></span><dl> <dt>**GDT \_ VALID**</dt> </dl> | Definir o controle DTP de acordo com os dados dentro da estrutura para a que *lParam* aponta. <br/>                                                                                                                                                                 |
| <span id="GDT_NONE"></span><span id="gdt_none"></span><dl> <dt>**GDT \_ NONE**</dt> </dl>    | Des marque o controle DTP como "sem data" e des marque a caixa de seleção. Quando esse sinalizador é especificado, *lParam* é ignorado. Esse sinalizador se aplica somente a controles DTP definidos com o [**estilo DTS \_ SHOWNONE.**](date-and-time-picker-control-styles.md) <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que contém o tempo do sistema usado para definir o controle DTP.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará diferente de zero se for bem-sucedido ou zero caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

