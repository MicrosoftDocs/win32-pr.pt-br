---
title: Mensagem de TBM_GETTHUMBRECT (commctrl. h)
description: Recupera o tamanho e a posição do retângulo delimitador para o controle deslizante em um TrackBar.
ms.assetid: f53fd7af-36f8-4490-aa95-f1fa20f34efb
keywords:
- Controles de TBM_GETTHUMBRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_GETTHUMBRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dce1bba8af9a65f297aa0515c1103c50daa1626d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009391"
---
# <a name="tbm_getthumbrect-message"></a>\_Mensagem tbm GETTHUMBRECT

Recupera o tamanho e a posição do retângulo delimitador para o controle deslizante em um TrackBar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) . A mensagem preenche essa estrutura com o retângulo delimitador do controle deslizante do TrackBar nas coordenadas do cliente da janela do TrackBar.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

