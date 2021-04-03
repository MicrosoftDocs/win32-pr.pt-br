---
title: Mensagem de TB_CHANGEBITMAP (commctrl. h)
description: Altera o bitmap de um botão em uma barra de ferramentas.
ms.assetid: 112b6f4e-6034-4e13-8b2f-b8411a351fbd
keywords:
- Controles de TB_CHANGEBITMAP de mensagens do Windows
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
ms.openlocfilehash: 1367a2a1b4e35d6f52bf1e7a0be42f1e75daa7ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824849"
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

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





