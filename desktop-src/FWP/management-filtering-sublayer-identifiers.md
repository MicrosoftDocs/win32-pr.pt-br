---
title: Filtrando identificadores de subcamadas (Fwpmu. h)
description: As constantes de identificador de subcamadas para filtragem de gerenciamento de API WFP.
ms.assetid: 4c8dbe35-e84b-4490-bf7a-7ff8b94e2022
topic_type:
- apiref
api_name:
- FWPM_SUBLAYER_EDGE_TRAVERSAL / FWPM_SUBLAYER_TEREDO
- FWPM_SUBLAYER_INSPECTION
- FWPM_SUBLAYER_IPSEC_DOSP
- FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL
- FWPM_SUBLAYER_IPSEC_TUNNEL
- FWPM_SUBLAYER_LIPS
- FWPM_SUBLAYER_RPC_AUDIT
- FWPM_SUBLAYER_SECURE_SOCKET
- FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD
- FWPM_SUBLAYER_TCP_TEMPLATES
- FWPM_SUBLAYER_UNIVERSAL
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d597fa1b75f6c965da9cf8d71bcc3e729d0b0b2f4f4220c984a1be8c94c09d39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068876"
---
# <a name="filtering-sublayer-identifiers"></a>Filtrando identificadores de subcamadas

os identificadores de subcamadas da WFP (plataforma de filtragem de Windows) são representados por um GUID.

Esses identificadores são definidos da seguinte maneira.

<dl> <dt>

<span id="FWPM_SUBLAYER_EDGE_TRAVERSAL________________________FWPM_SUBLAYER_TEREDO"></span><span id="fwpm_sublayer_edge_traversal________________________fwpm_sublayer_teredo"></span>**FWPM de \_ borda de SUBcamadas \_ \_ /FWPM \_ \_ TEREDO**
</dt> <dd> <dl> <dt>



Os filtros de percurso de borda são adicionados a essa subcamada.

> [!Note]  
> para o Windows 7 e posterior, use a **\_ travessia de \_ borda \_ da subcamada FWPM**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_INSPECTION"></span><span id="fwpm_sublayer_inspection"></span>**\_inspeção de SUBcamada FWPM \_**
</dt> <dd> <dl> <dt>



Esta é a subcamada com o menor peso. Ele é usado somente para filtros de inspeção.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_DOSP"></span><span id="fwpm_sublayer_ipsec_dosp"></span>**FWPM \_ DOSP IPSec SUBcamada \_ \_**
</dt> <dd> <dl> <dt>



Os filtros de proteção de DoS IPsec são adicionados a essa subcamada.

> [!Note]  
> disponível somente no Windows Vista com SP1, Windows Server 2008 e posterior.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL"></span><span id="fwpm_sublayer_ipsec_forward_outbound_tunnel"></span>**\_túnel de saída de \_ \_ encaminhamento IPsec do FWPM \_ subcamada \_**
</dt> <dd> <dl> <dt>



Os filtros de túnel de saída de encaminhamento IPsec são adicionados a essa subcamada.

> [!Note]  
> disponível somente no Windows 7, Windows Server 2008 R2 e posterior.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_TUNNEL"></span><span id="fwpm_sublayer_ipsec_tunnel"></span>**\_túnel IPSec de SUBcamada FWPM \_ \_**
</dt> <dd> <dl> <dt>



Os filtros de túnel IPsec são adicionados a essa subcamada.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_LIPS"></span><span id="fwpm_sublayer_lips"></span>**\_Lips de SUBcamadas FWPM \_**
</dt> <dd> <dl> <dt>



Os filtros IPsec herdados são adicionados a essa subcamada.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_RPC_AUDIT"></span><span id="fwpm_sublayer_rpc_audit"></span>**\_auditoria de RPC da SUBcamada FWPM \_ \_**
</dt> <dd> <dl> <dt>



Os filtros de auditoria RPC são adicionados a essa subcamada. Esses filtros auditam chamadas de entrada RPC como parte do C2 e da conformidade dos critérios comuns.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_SECURE_SOCKET"></span><span id="fwpm_sublayer_secure_socket"></span>**\_soquete seguro de SUBcamada FWPM \_ \_**
</dt> <dd> <dl> <dt>



Os filtros de soquete seguro são adicionados a essa subcamada.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_sublayer_tcp_chimney_offload"></span>**descarregamento de CHIMNEY TCP de FWPM de \_ SUBcamadas \_ \_ \_**
</dt> <dd> <dl> <dt>



Os filtros de descarregamento TCP Chimney são adicionados a essa subcamada.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_TCP_TEMPLATES______________________"></span><span id="fwpm_sublayer_tcp_templates______________________"></span>**\_modelos TCP de SUBcamadas FWPM \_ \_** 
</dt> <dd> <dl> <dt>



Os filtros de modelo TCP são adicionados a essa subcamada.

> [!Note]  
> disponível somente em Windows 8, Windows Server 2012 e posterior.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_UNIVERSAL"></span><span id="fwpm_sublayer_universal"></span>**FWPM de \_ SUBcamamento \_ Universal**
</dt> <dd> <dl> <dt>



Essa subcamada hospeda todos os filtros que não estão atribuídos a nenhuma das outras subcamadas.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



 

 





