---
title: Mensagem de TBM_GETNUMTICS (commctrl. h)
description: Recupera o número de marcas de escala em um TrackBar.
ms.assetid: 3c3f7ebb-a544-474c-ba14-68eae543ee38
keywords:
- Controles de TBM_GETNUMTICS de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_GETNUMTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 712e1a0190334ec279f28a68959f3e3d5d5ffd1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918162"
---
# <a name="tbm_getnumtics-message"></a>\_Mensagem tbm GETNUMTICS

Recupera o número de marcas de escala em um TrackBar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se nenhum [sinalizador de tique](trackbar-control-styles.md) for definido, ele retornará 2 para os tiques inicial e final. Se o [**TBS \_ notiques**](trackbar-control-styles.md) for definido, ele retornará zero. Caso contrário, ele usa a diferença entre o intervalo mínimo e o máximo, divide pela frequência de tique e adiciona 2.

## <a name="remarks"></a>Comentários

A mensagem **tbm \_ GETNUMTICS** conta todas as marcas de escala, incluindo as primeiras e as últimas marcas de escala criadas pelo TrackBar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





