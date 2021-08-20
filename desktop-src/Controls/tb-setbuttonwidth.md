---
title: TB_SETBUTTONWIDTH mensagem (Commctrl.h)
description: Define as larguras mínima e máxima do botão no controle da barra de ferramentas.
ms.assetid: 3311216a-e0b2-48bb-bad7-0a04185573cf
keywords:
- TB_SETBUTTONWIDTH controles de Windows mensagem
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
ms.openlocfilehash: 145ae1459b76fba60dd76b34e36d222cf62b93af071f2b430321d86956a3a871
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167591"
---
# <a name="tb_setbuttonwidth-message"></a>Mensagem TB \_ SETBUTTONWIDTH

Define as larguras mínima e máxima do botão no controle da barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

A [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica a largura mínima do botão, em pixels. Os botões da barra de ferramentas nunca serão mais estreitos do que esse valor.

O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a largura máxima do botão, em pixels. Se o texto do botão for muito largo, o controle o exibirá com pontos de reellipse.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará diferente de zero se for bem-sucedido ou zero caso contrário.

## <a name="remarks"></a>Comentários

Use **TB \_ SETBUTTONWIDTH** para definir as larguras máximas e mínimas permitidas para os botões antes que eles sejam adicionados. Use [**TB \_ SETBUTTONSIZE**](tb-setbuttonsize.md) para definir o tamanho real dos botões.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

