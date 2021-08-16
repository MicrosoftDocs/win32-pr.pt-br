---
description: Essas constantes são usadas por um TSP para identificar o resultado de uma solicitação de QoS (Qualidade de Serviço).
ms.assetid: 617ddbf4-212f-4990-93c2-f38f04b035ab
title: LINEEQOSINFO_ constantes (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c07a2d532e578b1f7df752cfd4930660d1d22dd4dd8406f0f8cc8bd61924bf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761389"
---
# <a name="lineeqosinfo_-constants"></a>Constantes LINEEQOSINFO \_

Essas constantes são usadas por um TSP para identificar o resultado de uma solicitação de QoS (Qualidade de Serviço).

<dl> <dt>

<span id="LINEEQOSINFO_NOQOS"></span><span id="lineeqosinfo_noqos"></span>**LINEEQOSINFO \_ NOQOS**
</dt> <dd> <dl> <dt>

 0x00000001
</dt> <dt>



A QoS não está disponível.


</dt> </dl> </dd> <dt>

<span id="LINEEQOSINFO_ADMISSIONFAILURE"></span><span id="lineeqosinfo_admissionfailure"></span>**LINEEQOSINFO \_ ADMISSIONFAILURE**
</dt> <dd> <dl> <dt>

 0x00000002
</dt> <dt>



A solicitação de QoS não pôde ser atendida.


</dt> </dl> </dd> <dt>

<span id="LINEEQOSINFO_POLICYFAILURE"></span><span id="lineeqosinfo_policyfailure"></span>**LINEEQOSINFO \_ POLICYFAILURE**
</dt> <dd> <dl> <dt>

 0x00000003
</dt> <dt>



Não há suporte para o tipo de QoS solicitado.


</dt> </dl> </dd> <dt>

<span id="LINEEQOSINFO_GENERICERROR"></span><span id="lineeqosinfo_genericerror"></span>**LINEEQOSINFO \_ GENERICERROR**
</dt> <dd> <dl> <dt>

 0x00000004
</dt> <dt>



Erro de QoS não especificado.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.2<br/>                                                      |
| Cabeçalho<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



 

 




