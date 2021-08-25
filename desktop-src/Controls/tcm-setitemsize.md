---
title: Mensagem de TCM_SETITEMSIZE (commctrl. h)
description: Define a largura e a altura das guias em um controle de tabulação de largura fixa ou de desenho proprietário. Você pode enviar essa mensagem explicitamente ou usando a \_ macro Setitems TabCtrl.
ms.assetid: 3935d686-f8bc-41fb-b025-04120cf03f02
keywords:
- controles de Windows de mensagem de TCM_SETITEMSIZE
topic_type:
- apiref
api_name:
- TCM_SETITEMSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8845aa54cd3cca413f31ee01f4a9583e24dc875a876d1aff691f574214f6f793
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876226"
---
# <a name="tcm_setitemsize-message"></a>\_Mensagem de SETitems TCM

Define a largura e a altura das guias em um controle de tabulação de largura fixa ou de desenho proprietário. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ setitems TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemsize) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é um valor **int** que especifica a nova largura, em pixels. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) é um valor **int** que especifica a nova altura, em pixels.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a largura e a altura antigas. A largura está em [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) do valor de retorno e a altura está no [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).

## <a name="remarks"></a>Comentários

Se a largura for definida como um valor menor que a largura da imagem definida por [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create), a largura da guia será definida com o menor valor que for maior que a largura da imagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

