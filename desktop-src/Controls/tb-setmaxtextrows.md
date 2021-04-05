---
title: Mensagem de TB_SETMAXTEXTROWS (commctrl. h)
description: Define o número máximo de linhas de texto exibidas em um botão da barra de ferramentas.
ms.assetid: a14d74e8-cc21-482d-9bca-38dc7c0528ec
keywords:
- Controles de TB_SETMAXTEXTROWS de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETMAXTEXTROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0984c0b73280ec90c4e659d3bb3b4cc89cdcf4c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918167"
---
# <a name="tb_setmaxtextrows-message"></a>TB de \_ mensagem SETMAXTEXTROWS

Define o número máximo de linhas de texto exibidas em um botão da barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número máximo de linhas de texto que podem ser exibidas.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="remarks"></a>Comentários

Para fazer com que o texto seja quebrado, você deve definir a largura máxima do botão enviando uma mensagem [**\_ SETBUTTONWIDTH TB**](tb-setbuttonwidth.md) . O texto é quebrado em uma quebra de palavra; quebras de linha (" \\ n") no texto são ignoradas. O texto nas \_ barras de ferramentas da lista de TBSTYLE sempre é mostrado em uma única linha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





