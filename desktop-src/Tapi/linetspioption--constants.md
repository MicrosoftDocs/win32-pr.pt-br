---
description: As \_ constantes LINETSPIOPTION descrevem os provedores de serviço de pedidos que devem ser chamados.
ms.assetid: af91f466-d87e-4767-a2c6-d882b9108f21
title: Constantes de LINETSPIOPTION_ (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e8fa13047dcbad60472fac371b255f7533809c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780118"
---
# <a name="linetspioption_-constants"></a>\_Constantes LINETSPIOPTION

As **\_ constantes LINETSPIOPTION** descrevem os provedores de serviço de pedidos que devem ser chamados.

<dl> <dt>

<span id="LINETSPIOPTION_NONREENTRANT"></span><span id="linetspioption_nonreentrant"></span>**LINETSPIOPTION \_ NONREENTRANT**
</dt> <dd> <dl> <dt>



A TAPI deve chamar funções neste provedor de serviços, uma de cada vez; Ele deve aguardar a conclusão de cada função (mas não para que as funções assíncronas sejam concluídas) antes de chamar a mesma ou outra função, seja na mesma ou em um thread diferente, no mesmo ou em um processador diferente.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



 

 




