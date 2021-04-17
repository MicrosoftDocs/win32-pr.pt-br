---
description: Essas constantes são usadas por um TSP para identificar o resultado de uma solicitação de QoS (qualidade de serviço).
ms.assetid: 617ddbf4-212f-4990-93c2-f38f04b035ab
title: Constantes de LINEEQOSINFO_ (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 423cc6172a1c6c87c1f3bb38929f727a15dad5c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769404"
---
# <a name="lineeqosinfo_-constants"></a>\_Constantes LINEEQOSINFO

Essas constantes são usadas por um TSP para identificar o resultado de uma solicitação de QoS (qualidade de serviço).

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



Não foi possível atender à solicitação de QoS.


</dt> </dl> </dd> <dt>

<span id="LINEEQOSINFO_POLICYFAILURE"></span><span id="lineeqosinfo_policyfailure"></span>**LINEEQOSINFO \_ POLICYFAILURE**
</dt> <dd> <dl> <dt>

 0x00000003
</dt> <dt>



Não há suporte para o tipo de QoS solicitado.


</dt> </dl> </dd> <dt>

<span id="LINEEQOSINFO_GENERICERROR"></span><span id="lineeqosinfo_genericerror"></span>**LINEEQOSINFO \_ erro genérico**
</dt> <dd> <dl> <dt>

 0x00000004
</dt> <dt>



Erro de QoS não especificado.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,2<br/>                                                      |
| parâmetro<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



 

 




