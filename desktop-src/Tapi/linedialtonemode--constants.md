---
description: As constantes de sinalizador de bits LINEDIALTONEMODE \_ descrevem diferentes tipos de tom de discagem. Um tom de discagem especial normalmente tem um significado especial (como com a espera de mensagens).
ms.assetid: 0b040482-35cf-42e8-84bc-33002635b591
title: LINEDIALTONEMODE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6b51ac15da6c1cba2b1b4e5b51710f04ba54549d2e08f4e9b50a20c543c305d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119309956"
---
# <a name="linedialtonemode_-constants"></a>Constantes LINEDIALTONEMODE \_

As constantes de sinalizador de bits **LINEDIALTONEMODE \_** descrevem diferentes tipos de tom de discagem. Um tom de discagem especial normalmente tem um significado especial (como com a espera de mensagens).

<dl> <dt>

<span id="LINEDIALTONEMODE_EXTERNAL"></span><span id="linedialtonemode_external"></span>**LINEDIALTONEMODE \_ EXTERNAL**
</dt> <dd> <dl> <dt>



Esse é um tom de discagem externo (rede pública).


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_INTERNAL"></span><span id="linedialtonemode_internal"></span>**LINEDIALTONEMODE \_ INTERNO**
</dt> <dd> <dl> <dt>



Esse é um tom de discagem interno, como dentro de um PBX.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_NORMAL"></span><span id="linedialtonemode_normal"></span>**LINEDIALTONEMODE \_ NORMAL**
</dt> <dd> <dl> <dt>



Esse é um tom de discagem normal, que normalmente é um tom contínuo.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_SPECIAL"></span><span id="linedialtonemode_special"></span>**LINEDIALTONEMODE \_ SPECIAL**
</dt> <dd> <dl> <dt>



Esse é um tom de discagem especial que indica que uma determinada condição (conhecida pelo comutador ou rede) está em vigor no momento. Os tons de discagem especiais normalmente usam um tom interrompido. Assim como com um tom de discagem normal, isso indica que a opção está pronta para receber o número a ser discado.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_UNAVAIL"></span><span id="linedialtonemode_unavail"></span>**LINEDIALTONEMODE \_ UNAVAIL**
</dt> <dd> <dl> <dt>



O modo de tom de discagem não está disponível e não se tornará conhecido.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_UNKNOWN"></span><span id="linedialtonemode_unknown"></span>**LINEDIALTONEMODE \_ DESCONHECIDO**
</dt> <dd> <dl> <dt>



O modo de tom de discagem não é conhecido no momento, mas pode se tornar conhecido posteriormente.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Os 16 bits de ordem alta podem ser atribuídos a extensões específicas do dispositivo. Os 16 bits de ordem baixa são reservados.

As **\_ constantes LINEDIALTONEMODE** são usadas dentro da estrutura de dados [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) para uma chamada no estado dialtone.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




