---
description: Essas constantes são usadas por um TSP para identificar o tipo de nível de QoS (Qualidade de Serviço) necessário.
ms.assetid: 9fc3f6eb-7103-43c5-84f8-3842757e5be7
title: LINEQOSSERVICELEVEL_ constantes (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a74a4508b54a8b56e8e9cb359f966122c5c009f0e5ede0f1b8544cd1e46330c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003004"
---
# <a name="lineqosservicelevel_-constants"></a>Constantes LINEQOSSERVICELEVEL \_

Essas constantes são usadas por um TSP para identificar o tipo de nível de QoS (Qualidade de Serviço) necessário.

<dl> <dt>

<span id="LINEQOSSERVICELEVEL_NEEDED"></span><span id="lineqosservicelevel_needed"></span>**LINEQOSSERVICELEVEL \_ NECESSÁRIO**
</dt> <dd> <dl> <dt>

 0x00000001
</dt> <dt>



A qualidade do nível de serviço solicitada é um requisito.


</dt> </dl> </dd> <dt>

<span id="LINEQOSSERVICELEVEL_IFAVAILABLE"></span><span id="lineqosservicelevel_ifavailable"></span>**LINEQOSSERVICELEVEL \_ IFAVAILABLE**
</dt> <dd> <dl> <dt>

 0x00000002
</dt> <dt>



A qualidade do nível de serviço necessária, se disponível.


</dt> </dl> </dd> <dt>

<span id="LINEQOSSERVICELEVEL_BESTEFFORT"></span><span id="lineqosservicelevel_besteffort"></span>**LINEQOSSERVICELEVEL \_ BESTEFIÇO**
</dt> <dd> <dl> <dt>

 0x00000003
</dt> <dt>



A qualidade do nível de serviço necessária é o "melhor esforço".


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.2<br/>                                                      |
| Cabeçalho<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



 

 




