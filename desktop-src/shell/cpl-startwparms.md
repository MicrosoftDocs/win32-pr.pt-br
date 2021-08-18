---
description: Enviado para notificar CPlApplet que o usuário escolheu o ícone associado a uma determinada caixa de diálogo. CPlApplet deve exibir a caixa de diálogo correspondente e executar qualquer tarefa especificada pelo usuário.
title: Mensagem de CPL_STARTWPARMS (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 04ac5117-39c9-4d3f-b32d-8f8d2b515be1
api_name:
- CPL_STARTWPARMS
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f836f868b81daa49e87eb4efc804442bed25690ce126852891327d0eb042aaec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460605"
---
# <a name="cpl_startwparms-message"></a>CPL \_ mensagem STARTWPARMS

Enviado para notificar [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) que o usuário escolheu o ícone associado a uma determinada caixa de diálogo. **CPlApplet** deve exibir a caixa de diálogo correspondente e executar qualquer tarefa especificada pelo usuário.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*uAppNum* 
</dt> <dd>

O número da caixa de diálogo. Esse número deve estar no intervalo de zero a um menor que o valor retornado em resposta à mensagem [**CPL \_ GetCount**](cpl-getcount.md) (CPL \_ GetCount – 1).

</dd> <dt>

*lpszExtra* 
</dt> <dd>

Uma cadeia de caracteres com direções adicionais para execução.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **true** se a mensagem tiver sido tratada ou **false** caso contrário.

## <a name="remarks"></a>Comentários

**CPL \_ STARTWPARMS** é semelhante a [**CPL \_ DBLCLK**](cpl-dblclk.md) , mas permite que você passe uma cadeia de caracteres para [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) em vez de um **int**. Você pode usar essa cadeia de caracteres como uma maneira flexível de fornecer instruções detalhadas para execução.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos de área de trabalho do Windows XP\]<br/>           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>CPL. h</dt> </dl> |



 

 
