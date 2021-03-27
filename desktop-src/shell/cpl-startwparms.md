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
ms.openlocfilehash: 790779c1c45acbc211fe36e28b2e55d5ae2e60da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920752"
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

## <a name="return-value"></a>Retornar valor

Retornará **true** se a mensagem tiver sido tratada ou **false** caso contrário.

## <a name="remarks"></a>Comentários

**CPL \_ STARTWPARMS** é semelhante a [**CPL \_ DBLCLK**](cpl-dblclk.md) , mas permite que você passe uma cadeia de caracteres para [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) em vez de um **int**. Você pode usar essa cadeia de caracteres como uma maneira flexível de fornecer instruções detalhadas para execução.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                             |
| parâmetro<br/>                   | <dl> <dt>CPL. h</dt> </dl> |



 

 
