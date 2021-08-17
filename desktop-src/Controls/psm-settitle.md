---
title: PSM_SETTITLE mensagem (Prsht.h)
description: Define o título de uma folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a \_ macro PropSheet SetTitle.
ms.assetid: 53ce8e20-4554-41f4-bad9-fb24c2c93c34
keywords:
- PSM_SETTITLE controles Windows mensagem
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
ms.openlocfilehash: 782d5ebf3e7fe0850b89d9f52f0dc5c406dbd41c9bdad694b41b8ae9ea4c8b0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985446"
---
# <a name="psm_settitle-message"></a>Mensagem \_ PSM SETTITLE

Define o título de uma folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a [**macro \_ PropSheet SetTitle.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sinalizador que indica se o prefixo "Propriedades para" ou o sufixo "Propriedades" (dependendo da versão) com a cadeia de caracteres de título especificada. Se esse valor for PSH \_ PROPTITLE, o prefixo ou sufixo será incluído.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para um buffer que contém a cadeia de caracteres de título. Se a [**HIWORD desse**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) parâmetro for **NULL,** a folha de propriedades carregará o recurso de cadeia de caracteres especificado no [**LOWORD.**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Em um Assistente do Aero, essa mensagem pode ser usada para alterar o título de uma página interior dinamicamente; por exemplo, ao manipular a [notificação \_ SETACTIVE PSN.](psn-setactive.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **PSM \_ SETTITLEW** (Unicode) e **PSM \_ SETTITLEA** (ANSI)<br/>              |



 

