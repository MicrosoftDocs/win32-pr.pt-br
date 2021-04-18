---
description: Essas constantes são usadas por um TSP para identificar o tipo de nível de QoS (qualidade de serviço) necessário.
ms.assetid: 9fc3f6eb-7103-43c5-84f8-3842757e5be7
title: Constantes de LINEQOSSERVICELEVEL_ (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c0629715e461a15e21e1730f86edb61d83d60db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760152"
---
# <a name="lineqosservicelevel_-constants"></a>\_Constantes LINEQOSSERVICELEVEL

Essas constantes são usadas por um TSP para identificar o tipo de nível de QoS (qualidade de serviço) necessário.

<dl> <dt>

<span id="LINEQOSSERVICELEVEL_NEEDED"></span><span id="lineqosservicelevel_needed"></span>**LINEQOSSERVICELEVEL \_ necessário**
</dt> <dd> <dl> <dt>

 0x00000001
</dt> <dt>



A qualidade do nível de serviço solicitada é um requisito.


</dt> </dl> </dd> <dt>

<span id="LINEQOSSERVICELEVEL_IFAVAILABLE"></span><span id="lineqosservicelevel_ifavailable"></span>**LINEQOSSERVICELEVEL \_ IFAVAILABLE**
</dt> <dd> <dl> <dt>

 0x00000002
</dt> <dt>



A qualidade de nível de serviço necessária, se disponível.


</dt> </dl> </dd> <dt>

<span id="LINEQOSSERVICELEVEL_BESTEFFORT"></span><span id="lineqosservicelevel_besteffort"></span>**LINEQOSSERVICELEVEL \_ BESTEFFORT**
</dt> <dd> <dl> <dt>

 0x00000003
</dt> <dt>



A qualidade do nível de serviço necessária é o "melhor esforço".


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,2<br/>                                                      |
| parâmetro<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



 

 




