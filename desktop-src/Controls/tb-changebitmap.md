---
title: Mensagem de TB_CHANGEBITMAP (commctrl. h)
description: Altera o bitmap de um botão em uma barra de ferramentas.
ms.assetid: 112b6f4e-6034-4e13-8b2f-b8411a351fbd
keywords:
- controles de Windows de mensagem de TB_CHANGEBITMAP
topic_type:
- apiref
api_name:
- TB_CHANGEBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb75e4586960a68e68c52d01d19ad78a3b3c848dcfb7acbd495dffbe530770c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957935"
---
# <a name="tb_changebitmap-message"></a>TB de \_ mensagem CHANGEBITMAP

Altera o bitmap de um botão em uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando do botão que deve receber um novo bitmap.

</dd> <dt>

*lParam* 
</dt> <dd>

Índice de base zero de uma imagem na lista de imagens da barra de ferramentas. O sistema exibe a imagem especificada no botão. Defina esse parâmetro como I \_ IMAGECALLBACK e a barra de ferramentas enviará a notificação [**tbn \_ GETDISPINFO**](tbn-getdispinfo.md) para recuperar o índice de imagem quando necessário.

[Versão 5,81](common-control-versions.md). Defina esse parâmetro como I \_ IMAGENONE para indicar que o botão não tem uma imagem. O layout do botão não incluirá nenhum espaço para um bitmap, somente texto.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





