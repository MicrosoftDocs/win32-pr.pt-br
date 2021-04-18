---
description: As \_ constantes de sinalizador de bit LINEDIALTONEMODE descrevem tipos diferentes de tons de discagem. Um tom de discagem especial normalmente apresenta um significado especial (assim como acontece com a mensagem em espera).
ms.assetid: 0b040482-35cf-42e8-84bc-33002635b591
title: Constantes de LINEDIALTONEMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5128f2a176f3aeaf92bc3487b131b7720568085e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792615"
---
# <a name="linedialtonemode_-constants"></a>\_Constantes LINEDIALTONEMODE

As constantes de sinalizador de bit **LINEDIALTONEMODE \_** descrevem tipos diferentes de tons de discagem. Um tom de discagem especial normalmente apresenta um significado especial (assim como acontece com a mensagem em espera).

<dl> <dt>

<span id="LINEDIALTONEMODE_EXTERNAL"></span><span id="linedialtonemode_external"></span>**LINEDIALTONEMODE \_ externo**
</dt> <dd> <dl> <dt>



Este é um tom de discagem externo (rede pública).


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_INTERNAL"></span><span id="linedialtonemode_internal"></span>**LINEDIALTONEMODE \_ interno**
</dt> <dd> <dl> <dt>



Esse é um tom de discagem interna, como em um PBX.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_NORMAL"></span><span id="linedialtonemode_normal"></span>**LINEDIALTONEMODE \_ normal**
</dt> <dd> <dl> <dt>



Esse é um tom de discagem normal, que normalmente é um tom contínuo.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_SPECIAL"></span><span id="linedialtonemode_special"></span>**LINEDIALTONEMODE \_ especial**
</dt> <dd> <dl> <dt>



Esse é um tom de discagem especial que indica que uma determinada condição (conhecida pelo comutador ou pela rede) está em vigor no momento. Os tons de discagem especiais normalmente usam um tom interrompido. Assim como com um tom de discagem normal, isso indica que a opção está pronta para receber o número a ser discado.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_UNAVAIL"></span><span id="linedialtonemode_unavail"></span>**LINEDIALTONEMODE não \_ disp.**
</dt> <dd> <dl> <dt>



O modo de Tom de discagem não está disponível e não se tornará conhecido.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_UNKNOWN"></span><span id="linedialtonemode_unknown"></span>**LINEDIALTONEMODE \_ desconhecido**
</dt> <dd> <dl> <dt>



O modo de Tom de discagem não é conhecido no momento, mas pode ser conhecido mais tarde.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Os 16 bits de ordem superior podem ser atribuídos para extensões específicas do dispositivo. Os 16 bits de ordem inferior são reservados.

As **\_ constantes LINEDIALTONEMODE** são usadas na estrutura de dados [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) para uma chamada no estado de disinalização.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




