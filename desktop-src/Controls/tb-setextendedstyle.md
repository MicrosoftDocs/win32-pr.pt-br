---
title: Mensagem de TB_SETEXTENDEDSTYLE (commctrl. h)
description: Define os estilos estendidos para um controle ToolBar.
ms.assetid: aec64bc7-74b4-4efc-9864-2c8a9fbd35c2
keywords:
- controles de Windows de mensagem de TB_SETEXTENDEDSTYLE
topic_type:
- apiref
api_name:
- TB_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 600e5904637215eeb052c85ec0203c9b86c75ed6b179be643dc9a213156b3afd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318876"
---
# <a name="tb_setextendedstyle-message"></a>Mensagem de TB \_ SETextendedattribute

Define os estilos estendidos para um controle ToolBar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor que especifica os novos estilos estendidos. Esse parâmetro pode ser uma combinação de [estilos estendidos](toolbar-extended-styles.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **DWORD** que representa os estilos estendidos anteriores. Esse valor pode ser uma combinação de [estilos estendidos](toolbar-extended-styles.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TB \_ Extended**](tb-getextendedstyle.md)
</dt> </dl>

 

 





