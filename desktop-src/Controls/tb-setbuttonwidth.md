---
title: Mensagem de TB_SETBUTTONWIDTH (commctrl. h)
description: Define as larguras mínima e máxima do botão no controle da barra de ferramentas.
ms.assetid: 3311216a-e0b2-48bb-bad7-0a04185573cf
keywords:
- Controles de TB_SETBUTTONWIDTH de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETBUTTONWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e105770d72e90108b9c31311f77599520cecea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085582"
---
# <a name="tb_setbuttonwidth-message"></a>TB de \_ mensagem SETBUTTONWIDTH

Define as larguras mínima e máxima do botão no controle da barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica a largura mínima do botão, em pixels. Os botões da barra de ferramentas nunca serão mais estreitos que esse valor.

O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a largura máxima do botão, em pixels. Se o texto do botão for muito grande, o controle o exibirá com pontos de reticências.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="remarks"></a>Comentários

Use **TB \_ SETBUTTONWIDTH** para definir as larguras máximas e mínimas permitidas para botões antes de serem adicionadas. Use [**TB \_ SetButtons**](tb-setbuttonsize.md) para definir o tamanho real dos botões.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

