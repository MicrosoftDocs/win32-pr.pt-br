---
title: Mensagem de SB_SETICON (commctrl. h)
description: Define o ícone de uma parte em uma barra de status.
ms.assetid: d8528cd1-54d2-44ba-b0d6-29111f75616a
keywords:
- Controles de SB_SETICON de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_SETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f720c414238eb89cf98bf0556ebabffefceae4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824620"
---
# <a name="sb_seticon-message"></a>\_Mensagem de SETICON SB

Define o ícone de uma parte em uma barra de status.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice de base zero da parte que receberá o ícone. Se esse parâmetro for-1, a barra de status será considerada uma barra de status simples.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador para o ícone a ser definido. Se esse valor for **nulo**, o ícone será removido da parte.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="remarks"></a>Comentários

A barra de status não destruirá o ícone. É responsabilidade do aplicativo de chamada manter o controle e destruir os ícones.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





