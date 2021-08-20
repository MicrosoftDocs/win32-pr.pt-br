---
title: Mensagem de TB_SETMAXTEXTROWS (commctrl. h)
description: Define o número máximo de linhas de texto exibidas em um botão da barra de ferramentas.
ms.assetid: a14d74e8-cc21-482d-9bca-38dc7c0528ec
keywords:
- controles de Windows de mensagem de TB_SETMAXTEXTROWS
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
ms.openlocfilehash: 1d6a1e1a2cda7b3dced4cf538623578d48b41d38925629f2985a35974baed229
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167476"
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

## <a name="return-value"></a>Valor retornado

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="remarks"></a>Comentários

Para fazer com que o texto seja quebrado, você deve definir a largura máxima do botão enviando uma mensagem [**\_ SETBUTTONWIDTH TB**](tb-setbuttonwidth.md) . O texto é quebrado em uma quebra de palavra; quebras de linha (" \\ n") no texto são ignoradas. O texto nas \_ barras de ferramentas da lista de TBSTYLE sempre é mostrado em uma única linha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





