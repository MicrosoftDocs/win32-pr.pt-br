---
title: Mensagem de LVM_SETTILEVIEWINFO (commctrl. h)
description: Define informações que um controle de exibição de lista usa no modo de exibição de bloco.
ms.assetid: 1c4f2aff-1ce1-484a-9360-3efbe870b39b
keywords:
- controles de Windows de mensagem de LVM_SETTILEVIEWINFO
topic_type:
- apiref
api_name:
- LVM_SETTILEVIEWINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf22f94ec3db661823bfb1582dd97975e41bc11d2803e4380d8f0f45afae02f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119217376"
---
# <a name="lvm_settileviewinfo-message"></a>\_Mensagem SETTILEVIEWINFO LVM

Define informações que um controle de exibição de lista usa no modo de exibição de bloco.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Ponteiro para uma estrutura <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a> que contém as informações a serem definidas.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





