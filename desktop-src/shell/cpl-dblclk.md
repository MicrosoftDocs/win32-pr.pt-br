---
description: Enviado para a função CPlApplet de um aplicativo do painel de controle quando o usuário clica duas vezes no ícone de uma caixa de diálogo com suporte no aplicativo.
title: Mensagem de CPL_DBLCLK (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 68d74372-2fc2-45ed-8f77-574b943d28fa
api_name:
- CPL_DBLCLK
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d6c67204c7b4fae5275e50d428a0371af4cf2e2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988744"
---
# <a name="cpl_dblclk-message"></a>CPL \_ mensagem DBLCLK

Enviado para a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de um aplicativo do painel de controle quando o usuário clica duas vezes no ícone de uma caixa de diálogo com suporte no aplicativo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*uAppNum* 
</dt> <dd>

O número da caixa de diálogo. Esse número deve estar no intervalo de zero a um menor que o valor retornado em resposta à mensagem [**CPL \_ GetCount**](cpl-getcount.md) (CPL \_ GetCount – 1).

</dd> <dt>

*lData* 
</dt> <dd>

O valor que o aplicativo do painel de controle carregou no membro **lpData** da estrutura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) ou [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) da caixa de diálogo. O aplicativo carrega o membro **lpData** em resposta à mensagem [**CPL de \_ consulta**](cpl-inquire.md) ou [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) processar essa mensagem com êxito, o valor de retorno será zero; caso contrário, ele será diferente de zero.

## <a name="remarks"></a>Comentários

Em resposta a essa mensagem, um aplicativo do painel de controle deve exibir a caixa de diálogo correspondente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>CPL. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CPL de \_ seleção**](cpl-select.md)
</dt> </dl>

 

 
