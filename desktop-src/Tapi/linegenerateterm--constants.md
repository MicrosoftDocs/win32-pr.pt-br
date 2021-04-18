---
description: As \_ constantes de sinalizador de bit LINEGENERATETERM descrevem as condições sob as quais a geração de dígito ou Tom é encerrada.
ms.assetid: 5cdc43c0-2349-4ffc-9bf7-3b498b35db95
title: Constantes de LINEGENERATETERM_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6804b09879471a77780a95ca4ed35b7aaa5b6e1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800021"
---
# <a name="linegenerateterm_-constants"></a>\_Constantes LINEGENERATETERM

As constantes de sinalizador de bit **LINEGENERATETERM \_** descrevem as condições sob as quais a geração de dígito ou Tom é encerrada.

<dl> <dt>

<span id="LINEGENERATETERM_CANCEL"></span><span id="linegenerateterm_cancel"></span>**LINEGENERATETERM \_ cancelar**
</dt> <dd> <dl> <dt>



A solicitação de geração de dígitos ou tons foi cancelada por este aplicativo, por outro aplicativo ou porque a chamada foi encerrada. Esse valor também pode ser retornado quando a geração de dígitos ou tons não pode ser concluída devido a uma falha interna do provedor de serviços.


</dt> </dl> </dd> <dt>

<span id="LINEGENERATETERM_DONE"></span><span id="linegenerateterm_done"></span>**LINEGENERATETERM \_ concluído**
</dt> <dd> <dl> <dt>



O número solicitado de dígitos ou os tons solicitados foram gerados para a duração solicitada.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




