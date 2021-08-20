---
title: Identificadores de provedor integrados (Fwpmu.h)
description: Os identificadores para os provedores que são integrados à plataforma de filtragem Windows (WFP) são representados por um GUID.
ms.assetid: 61bc1e2d-f6ee-45db-892f-c49680d27072
topic_type:
- apiref
api_name:
- FWPM_PROVIDER_IKEEXT
- FWPM_PROVIDER_IPSEC_DOS_CONFIG
- FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD
- FWPM_PROVIDER_TCP_TEMPLATES
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8982fe6ebbe3f4cf5135f2b67f07826ddf9d3f970ca0568c7095931c617cdce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951305"
---
# <a name="built-in-provider-identifiers"></a>Identificadores de provedor integrados

Os identificadores para os provedores que são integrados à plataforma de filtragem Windows (WFP) são representados por um GUID.

Esses identificadores são definidos da seguinte forma.

<dl> <dt>

<span id="FWPM_PROVIDER_IKEEXT"></span><span id="fwpm_provider_ikeext"></span>**\_IKEEXT DO \_ PROVEDOR FWPM**
</dt> <dd> <dl> <dt>

{10ad9216-ccde-456c-8b16-e9f04e60a90b}
</dt> <dt>



Usado para identificar todos os filtros adicionados por IKE/AuthIP.


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_IPSEC_DOS_CONFIG"></span><span id="fwpm_provider_ipsec_dos_config"></span>**CONFIGURAÇÃO DE \_ \_ IPSEC DOS DO PROVEDOR \_ \_ FWPM**
</dt> <dd> <dl> <dt>

{3c6c0519-c05c-4bb9-8338-2327814ce8bf}
</dt> <dt>



Usado para identificar todos os filtros adicionados pela Proteção contra DoS IPsec.

> [!Note]  
> Disponível somente no Windows 7 e Windows Server 2008 R2.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_provider_tcp_chimney_offload"></span>**DESCARREGADO \_ \_ TCP \_ DE TCP DO PROVEDOR FWPM \_**
</dt> <dd> <dl> <dt>

{896aa19e-9a34-4bcb-ae79-beb9127c84b9}
</dt> <dt>



Usado para identificar todos os filtros adicionados pelo Descarregado de Torção de TCP.


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_TCP_TEMPLATES"></span><span id="fwpm_provider_tcp_templates"></span>**MODELOS TCP DO \_ \_ PROVEDOR FWPM \_**
</dt> <dd> <dl> <dt>

{76cfcd30-3394-432d-bed3-441ae50e63c3}
</dt> <dt>



Usado para identificar todos os filtros adicionados por modelos TCP.

> [!Note]  
> Disponível somente em Windows 8 e Windows Server 2012.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Fwpmu.h</dt> </dl> |



 

 





