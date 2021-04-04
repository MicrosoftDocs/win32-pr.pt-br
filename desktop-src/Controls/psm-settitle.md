---
title: Mensagem de PSM_SETTITLE (Prsht. h)
description: Define o título de uma folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetTitle PropSheet.
ms.assetid: 53ce8e20-4554-41f4-bad9-fb24c2c93c34
keywords:
- Controles de PSM_SETTITLE de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_SETTITLE
- PSM_SETTITLEA
- PSM_SETTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a848a5bdaeaae64b6f1825740d1e8ade07a5a22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918028"
---
# <a name="psm_settitle-message"></a>Mensagem de PSM \_ USERtitle

Define o título de uma folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetTitle PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sinalizador que indica se deve incluir o prefixo "Propriedades para" ou o sufixo "Properties" (dependendo da versão) pela cadeia de título especificada. Se esse valor for PSH \_ PROPTITLE, o prefixo ou sufixo será incluído.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para um buffer que contém a cadeia de título. Se o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) desse parâmetro for **nulo**, a folha de propriedades carregará o recurso de cadeia de caracteres especificado em [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Em um assistente Aero, essa mensagem pode ser usada para alterar o título de uma página interior dinamicamente; por exemplo, ao lidar com a notificação [ \_ SetActive PSN](psn-setactive.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **PSM \_ SETTITLEW** (Unicode) e **PSM \_ settítuloa** (ANSI)<br/>              |



 

