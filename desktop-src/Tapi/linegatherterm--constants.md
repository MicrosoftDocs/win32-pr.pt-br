---
description: As \_ constantes de sinalizador de bit LINEGATHERTERM descrevem as condições sob as quais a coleta de dígitos em buffer é encerrada.
ms.assetid: 409e1984-e5a4-4636-ab53-5973fe7b78ea
title: Constantes de LINEGATHERTERM_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968492a584024c7750b417a9fd03b68ac1df42ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783359"
---
# <a name="linegatherterm_-constants"></a>\_Constantes LINEGATHERTERM

As constantes de sinalizador de bit **LINEGATHERTERM \_** descrevem as condições sob as quais a coleta de dígitos em buffer é encerrada.

<dl> <dt>

<span id="LINEGATHERTERM_BUFFERFULL"></span><span id="linegatherterm_bufferfull"></span>**LINEGATHERTERM \_ BUFFERFULL**
</dt> <dd> <dl> <dt>



O número de dígitos solicitado foi coletado. O buffer está cheio.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_CANCEL"></span><span id="linegatherterm_cancel"></span>**LINEGATHERTERM \_ cancelar**
</dt> <dd> <dl> <dt>



A solicitação foi cancelada por este aplicativo, por outro aplicativo ou porque a chamada foi encerrada.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_FIRSTTIMEOUT"></span><span id="linegatherterm_firsttimeout"></span>**LINEGATHERTERM \_ FIRSTTIMEOUT**
</dt> <dd> <dl> <dt>



O tempo limite do primeiro dígito expirou. O buffer não contém dígitos.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_INTERTIMEOUT"></span><span id="linegatherterm_intertimeout"></span>**intertempo de LINEGATHERTERM \_**
</dt> <dd> <dl> <dt>



O tempo limite entre dígitos expirou. O buffer contém pelo menos um dígito.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_TERMDIGIT"></span><span id="linegatherterm_termdigit"></span>**LINEGATHERTERM \_ TERMDIGIT**
</dt> <dd> <dl> <dt>



Um dos dígitos de encerramento correspondeu a um dígito recebido. O dígito de terminação correspondente é o último dígito no buffer.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




