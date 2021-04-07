---
title: Mensagem de SB_GETICON (commctrl. h)
description: Recupera o ícone de uma parte em uma barra de status.
ms.assetid: f99508e3-afa8-48fd-b87a-fce41c4410ff
keywords:
- Controles de SB_GETICON de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_GETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab86809df54d796b8e83f05f2a2b9041450ce2fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824623"
---
# <a name="sb_geticon-message"></a>\_Mensagem de GETICON SB

Recupera o ícone de uma parte em uma barra de status.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base zero da parte que contém o ícone a ser recuperado. Se esse parâmetro for-1, a barra de status será considerada uma barra de status de [modo simples](status-bars.md) .

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador para o ícone, se for bem-sucedido, ou **NULL** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





