---
description: As \_ constantes de sinalizador de bit LINECALLPARTYID descrevem a natureza das informações disponíveis sobre as partes envolvidas em uma chamada.
ms.assetid: e2a89f25-15f0-4f3c-9ac8-1e6b72c0d8db
title: Constantes de LINECALLPARTYID_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5dd8cca75fe6e91b97fac63dca6c0fdda554394
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813056"
---
# <a name="linecallpartyid_-constants"></a>\_Constantes LINECALLPARTYID

As constantes de sinalizador de bit **LINECALLPARTYID \_** descrevem a natureza das informações disponíveis sobre as partes envolvidas em uma chamada.

<dl> <dt>

<span id="LINECALLPARTYID_ADDRESS"></span><span id="linecallpartyid_address"></span>**\_endereço LINECALLPARTYID**
</dt> <dd> <dl> <dt>



As informações de identificador de terceiros consistem no endereço da parte em formato de endereço canônico ou formato de endereço de discagem.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_BLOCKED"></span><span id="linecallpartyid_blocked"></span>**LINECALLPARTYID \_ bloqueado**
</dt> <dd> <dl> <dt>



As informações de identificador de terceiros não estão disponíveis porque foram bloqueadas pela parte remota.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_NAME"></span><span id="linecallpartyid_name"></span>**nome do LINECALLPARTYID \_**
</dt> <dd> <dl> <dt>



As informações de identificador de terceiros consistem no nome da parte (como, por exemplo, de um diretório mantido dentro do comutador).


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_OUTOFAREA"></span><span id="linecallpartyid_outofarea"></span>**LINECALLPARTYID \_ OUTOFAREA**
</dt> <dd> <dl> <dt>



As informações de ID do chamador para a chamada não estão disponíveis porque não são propagadas por meio da rede.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_PARTIAL"></span><span id="linecallpartyid_partial"></span>**LINECALLPARTYID \_ parcial**
</dt> <dd> <dl> <dt>



As informações de identificador de terceiros são válidas, mas são limitadas apenas a informações parciais.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_UNAVAIL"></span><span id="linecallpartyid_unavail"></span>**LINECALLPARTYID não \_ disp.**
</dt> <dd> <dl> <dt>



As informações do identificador da parte não estão disponíveis e não serão disponibilizadas mais tarde. As informações podem estar indisponíveis por motivos não especificados. Por exemplo, as informações não foram entregues pela rede, elas foram ignoradas pelo provedor de serviços e assim por diante.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_UNKNOWN"></span><span id="linecallpartyid_unknown"></span>**LINECALLPARTYID \_ desconhecido**
</dt> <dd> <dl> <dt>



As informações de identificador de terceiros atualmente são desconhecidas, mas podem se tornar conhecidas mais tarde.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

Para cada uma das partes possíveis envolvidas em uma chamada, as **constantes \_ LINECALLPARTYID** descrevem como as informações do identificador da parte são formatadas. Essas informações são fornecidas na estrutura de dados [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




