---
description: Enviado para a função CPlApplet de um aplicativo de painel de controle quando o controle de aplicativo do painel de controle é fechado. O aplicativo de controle envia a mensagem uma vez para cada caixa de diálogo à qual o aplicativo dá suporte.
title: Mensagem de CPL_STOP (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4f632b91-8200-42a3-90cc-a98889704ca4
api_name:
- CPL_STOP
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 78f8926d85b35b8cf5e55188c6cd76b014b3c4c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967347"
---
# <a name="cpl_stop-message"></a>CPL \_ mensagem de parada

Enviado para a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de um aplicativo de painel de controle quando o controle de aplicativo do painel de controle é fechado. O aplicativo de controle envia a mensagem uma vez para cada caixa de diálogo à qual o aplicativo dá suporte.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*uAppNum* 
</dt> <dd>

O número da caixa de diálogo.

</dd> <dt>

*lData* 
</dt> <dd>

O valor que o aplicativo do painel de controle carregou no membro **lpData** da estrutura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) ou [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) da caixa de diálogo. O aplicativo carrega o membro **lpData** em resposta à mensagem [**CPL de \_ consulta**](cpl-inquire.md) ou [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) processar essa mensagem com êxito, ela deverá retornar zero.

## <a name="remarks"></a>Comentários

Em resposta a essa mensagem, um aplicativo do painel de controle deve executar a limpeza para a caixa de diálogo especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>CPL. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CPL de \_ saída**](cpl-exit.md)
</dt> <dt>

[**CPL \_ GETcount**](cpl-getcount.md)
</dt> </dl>

 

 
