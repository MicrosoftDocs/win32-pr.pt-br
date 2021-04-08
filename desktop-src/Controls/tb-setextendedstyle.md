---
title: Mensagem de TB_SETEXTENDEDSTYLE (commctrl. h)
description: Define os estilos estendidos para um controle ToolBar.
ms.assetid: aec64bc7-74b4-4efc-9864-2c8a9fbd35c2
keywords:
- Controles de TB_SETEXTENDEDSTYLE de mensagens do Windows
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
ms.openlocfilehash: b9a540aaeff61bd81b649f0509e064a29282f598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086009"
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

## <a name="return-value"></a>Retornar valor

Retorna um **DWORD** que representa os estilos estendidos anteriores. Esse valor pode ser uma combinação de [estilos estendidos](toolbar-extended-styles.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TB \_ Extended**](tb-getextendedstyle.md)
</dt> </dl>

 

 





