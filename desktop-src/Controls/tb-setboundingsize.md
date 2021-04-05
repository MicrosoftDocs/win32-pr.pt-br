---
title: Mensagem de TB_SETBOUNDINGSIZE (commctrl. h)
description: Define o tamanho delimitador para um controle de barra de ferramentas de várias colunas.
ms.assetid: f406d9e3-1c40-4317-8cf1-51706f4c6adf
keywords:
- Controles de TB_SETBOUNDINGSIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETBOUNDINGSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 419595da16148f7382da5053d3187e9cce9e00a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824150"
---
# <a name="tb_setboundingsize-message"></a>TB de \_ mensagem SETBOUNDINGSIZE

\[Destinado ao uso interno; Não recomendado para uso em aplicativos. Essa mensagem pode não ter suporte em versões futuras do Windows.\]

Define o tamanho delimitador para um controle de barra de ferramentas de várias colunas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura de [**tamanho**](/previous-versions//dd145106(v=vs.85)) cujo membro **CY** contém a altura delimitadora. O membro **CX** (a largura) é ignorado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno não é usado.

## <a name="security-considerations"></a>Considerações de segurança

O uso dessa mensagem pode comprometer a segurança do seu programa.

## <a name="remarks"></a>Comentários

O tamanho de limite controla como os botões são organizados em colunas. Se o controle Toolbar não tiver o estilo [**de \_ \_ várias colunas TBSTYLE ex**](toolbar-extended-styles.md) , essa mensagem não terá nenhum efeito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

