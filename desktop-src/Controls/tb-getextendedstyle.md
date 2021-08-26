---
title: TB_GETEXTENDEDSTYLE mensagem (Commctrl.h)
description: Recupera os estilos estendidos para um controle de barra de ferramentas.
ms.assetid: d9e31a8e-5e5a-4d2d-bc3b-65ac40e8592f
keywords:
- TB_GETEXTENDEDSTYLE controles de Windows mensagem
topic_type:
- apiref
api_name:
- TB_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab059933c2019009ebc746cc59df6affb840f09c40a201a4ee4048dc2498a17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918856"
---
# <a name="tb_getextendedstyle-message"></a>Mensagem \_ GETEXTENDEDSTYLE de TB

Recupera os estilos estendidos para um controle de barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **DWORD** que representa os estilos atualmente em uso para o controle de barra de ferramentas. Esse valor pode ser uma combinação de [estilos estendidos.](toolbar-extended-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TB \_ SETEXTENDEDSTYLE**](tb-setextendedstyle.md)
</dt> </dl>

 

 





