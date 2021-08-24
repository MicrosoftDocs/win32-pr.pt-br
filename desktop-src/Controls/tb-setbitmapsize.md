---
title: Mensagem de TB_SETBITMAPSIZE (commctrl. h)
description: Define o tamanho das imagens de bitmap a serem adicionadas a uma barra de ferramentas.
ms.assetid: 20b99cd8-6ef1-4037-92d2-c64a1003b5fe
keywords:
- controles de Windows de mensagem de TB_SETBITMAPSIZE
topic_type:
- apiref
api_name:
- TB_SETBITMAPSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db2a26dacd63c00d1dd793163facce0ab4a45302e85dde11522f8844977eb0ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167969"
---
# <a name="tb_setbitmapsize-message"></a>TB de \_ mensagem SETBITMAPSIZE

Define o tamanho das imagens de bitmap a serem adicionadas a uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica a largura, em pixels, das imagens de bitmap. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a altura, em pixels, das imagens de bitmap.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

O tamanho pode ser definido somente antes de adicionar qualquer bitmap à barra de ferramentas. Se um aplicativo não definir explicitamente o tamanho do bitmap, o tamanho padrão será 16 por 15 pixels.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

