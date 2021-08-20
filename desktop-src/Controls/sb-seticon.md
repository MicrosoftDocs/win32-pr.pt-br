---
title: SB_SETICON mensagem (Commctrl.h)
description: Define o ícone de uma parte em uma barra de status.
ms.assetid: d8528cd1-54d2-44ba-b0d6-29111f75616a
keywords:
- SB_SETICON controles de Windows mensagem
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
ms.openlocfilehash: d0e08b1c3b0ce1a453ca9050c20552a14169a594c8091708339b4a436f1fb1a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540066"
---
# <a name="sb_seticon-message"></a>Mensagem \_ SB SETICON

Define o ícone de uma parte em uma barra de status.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice baseado em zero da parte que receberá o ícone. Se esse parâmetro for -1, a barra de status será assumida como uma barra de status simples.

</dd> <dt>

*lParam* 
</dt> <dd>

Lidar com o ícone a ser definido. Se esse valor for **NULL,** o ícone será removido da parte.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará diferente de zero se for bem-sucedido ou zero caso contrário.

## <a name="remarks"></a>Comentários

A barra de status não destruirá o ícone. É responsabilidade do aplicativo de chamada manter o controle e destruir todos os ícones.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





