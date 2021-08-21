---
title: TTM_DELTOOL mensagem (Commctrl.h)
description: Remove uma ferramenta de um controle de dica de ferramenta.
ms.assetid: 433b6f1c-3e9f-4e3a-9834-d447a3f9e6a5
keywords:
- TTM_DELTOOL controles de Windows mensagem
topic_type:
- apiref
api_name:
- TTM_DELTOOL
- TTM_DELTOOLA
- TTM_DELTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea54eefd2b9cc84b3aabe5dd600c5fcc32c7468cae01d1819b5fda7b631aeabd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166379"
---
# <a name="ttm_deltool-message"></a>Mensagem TTM \_ DELTOOL

Remove uma ferramenta de um controle de dica de ferramenta.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura TOOLINFO.**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) Os **membros hwnd** e **uId** identificam a ferramenta a ser removido e o membro **cbSize** deve especificar o tamanho da estrutura. Todos os outros membros são ignorados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TTM \_ DELTOOLW** (Unicode) e **TTM \_ DELTOOLA** (ANSI)<br/>                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**TTM \_ ADDTOOL**](ttm-addtool.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Sobre controles de dica de ferramenta](tooltip-controls.md)
</dt> </dl>

 

 





