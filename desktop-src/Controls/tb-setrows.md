---
title: Mensagem de TB_SETROWS (commctrl. h)
description: Define o número de linhas de botões em uma barra de ferramentas.
ms.assetid: d8ea7b80-d23e-4593-8eb1-d23808173fc9
keywords:
- controles de Windows de mensagem de TB_SETROWS
topic_type:
- apiref
api_name:
- TB_SETROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2c0e95d6f0f19c2b1c9b76cf22a37da0086987b22fe144603cdb2afa8a1ad83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119293636"
---
# <a name="tb_setrows-message"></a>Mensagem de TB \_ SETrows

Define o número de linhas de botões em uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o número de linhas solicitadas. O número mínimo de linhas é um, e o número máximo de linhas é igual ao número de botões na barra de ferramentas.

O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) é um **bool** que indica se é necessário criar mais linhas do que o solicitado quando o sistema não pode criar o número de linhas especificado por *wParam*. Se **for true**, o sistema criará mais linhas. Se **for false**, o sistema criará menos linhas.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recebe o retângulo delimitador da barra de ferramentas depois que as linhas são definidas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Como o sistema não divide os grupos de botões ao definir o número de linhas, o número resultante de linhas pode ser diferente do número solicitado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

