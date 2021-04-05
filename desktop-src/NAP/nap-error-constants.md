---
title: Constantes de erro NAP (WinError. h)
description: As constantes de erro NAP a seguir são definidas no WinError. h.
ms.assetid: b2fba990-75d9-4153-8058-c01e97700d00
topic_type:
- apiref
api_name:
- NAP_E_INVALID_PACKET
- NAP_E_MISSING_SOH
- NAP_E_CONFLICTING_ID
- NAP_E_NO_CACHED_SOH
- NAP_E_STILL_BOUND
- NAP_E_NOT_REGISTERED
- NAP_E_NOT_INITIALIZED
- NAP_E_MISMATCHED_ID
- NAP_E_NOT_PENDING
- NAP_E_ID_NOT_FOUND
- NAP_E_MAXSIZE_TOO_SMALL
- NAP_E_SERVICE_NOT_RUNNING
- NAP_S_CERT_ALREADY_PRESENT
- NAP_E_ENTITY_DISABLED
- NAP_E_NETSH_GROUPPOLICY_ERROR
- NAP_E_TOO_MANY_CALLS
- NAP_E_SHV_CONFIG_EXISTED
- NAP_E_SHV_CONFIG_NOT_FOUND
- NAP_E_SHV_TIMEOUT
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b871d6f00174f05ab580aad54395851fa70af877
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918945"
---
# <a name="nap-error-constants"></a>Constantes de erro NAP

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

As constantes de erro NAP a seguir são definidas no WinError. h.

<dl> <dt>

<span id="NAP_E_INVALID_PACKET"></span><span id="nap_e_invalid_packet"></span>**\_pacote NAP E \_ inválido \_**
</dt> <dd> <dl> <dt>

\_\_TYPEDEF \_ de HRESULT (0x80270001L)
</dt> <dt>



O pacote NAP [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) é inválido.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MISSING_SOH"></span><span id="nap_e_missing_soh"></span>**NAP \_ E \_ faltando \_ soh**
</dt> <dd> <dl> <dt>

\_\_TYPEDEF \_ de HRESULT (0x80270002L)
</dt> <dt>



Uma [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) estava ausente no pacote NAP.


</dt> </dl> </dd> <dt>

<span id="NAP_E_CONFLICTING_ID"></span><span id="nap_e_conflicting_id"></span>**NAP \_ E \_ ID conflitante \_**
</dt> <dd> <dl> <dt>

\_\_TYPEDEF \_ de HRESULT (0x80270003L)
</dt> <dt>



A ID da entidade está em conflito com uma ID de entidade já registrada.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NO_CACHED_SOH"></span><span id="nap_e_no_cached_soh"></span>**NAP \_ E \_ nenhum \_ soh armazenado em cache \_**
</dt> <dd> <dl> <dt>

\_\_TYPEDEF \_ de HRESULT (0x80270004L)
</dt> <dt>



Nenhum [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) armazenado em cache está presente.


</dt> </dl> </dd> <dt>

<span id="NAP_E_STILL_BOUND"></span><span id="nap_e_still_bound"></span>**NAP \_ E \_ ainda \_ associado**
</dt> <dd> <dl> <dt>

\_\_TYPEDEF \_ de HRESULT (0x80270005L)
</dt> <dt>



A entidade ainda está associada ao sistema NAP.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_REGISTERED"></span><span id="nap_e_not_registered"></span>**\_E/s NAP \_ não \_ registradas**
</dt> <dd> <dl> <dt>

\_\_TYPEDEF \_ de HRESULT (0x80270006L)
</dt> <dt>



A entidade não está registrada com o sistema NAP.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_INITIALIZED"></span><span id="nap_e_not_initialized"></span>**NAP \_ E \_ não \_ inicializado**
</dt> <dd> <dl> <dt>

\_\_TYPEDEF \_ de HRESULT (0x80270007L)
</dt> <dt>



A entidade não foi inicializada com o sistema NAP.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MISMATCHED_ID"></span><span id="nap_e_mismatched_id"></span>**ID de NAP \_ E não \_ correspondente \_**
</dt> <dd> <dl> <dt>

\_\_TYPEDEF \_ de HRESULT (0x80270008L)
</dt> <dt>



As IDs de correlação na solicitação [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) e na resposta **soh** não correspondem.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_PENDING"></span><span id="nap_e_not_pending"></span>**NAP \_ E \_ não \_ pendente**
</dt> <dd> <dl> <dt>

\_\_TYPEDEF \_ de HRESULT (0x80270009L)
</dt> <dt>



A conclusão foi indicada em uma solicitação que não está pendente no momento.


</dt> </dl> </dd> <dt>

<span id="NAP_E_ID_NOT_FOUND"></span><span id="nap_e_id_not_found"></span>**\_ID NAP \_ E \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

\_\_TYPEDEF \_ de HRESULT (0x8027000AL)
</dt> <dt>



A ID do componente NAP não foi encontrada.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MAXSIZE_TOO_SMALL"></span><span id="nap_e_maxsize_too_small"></span>**NAP \_ E \_ MaxSize \_ muito \_ pequeno**
</dt> <dd> <dl> <dt>

\_\_TYPEDEF \_ de HRESULT (0x8027000BL)
</dt> <dt>



O tamanho máximo da conexão é muito pequeno para um pacote SoH.


</dt> </dl> </dd> <dt>

<span id="NAP_E_SERVICE_NOT_RUNNING"></span><span id="nap_e_service_not_running"></span>**o \_ serviço NAP E \_ \_ não \_ está em execução**
</dt> <dd> <dl> <dt>

\_\_TYPEDEF \_ de HRESULT (0x8027000CL)
</dt> <dt>



O serviço NapAgent não está em execução.


</dt> </dl> </dd> <dt>

<span id="NAP_S_CERT_ALREADY_PRESENT"></span><span id="nap_s_cert_already_present"></span>**o \_ certificado NAP S \_ \_ já está \_ presente**
</dt> <dd> <dl> <dt>

\_\_TYPEDEF \_ de HRESULT (0x0027000DL) 
</dt> <dt>



Um certificado já está presente no repositório de certificados.


</dt> </dl> </dd> <dt>

<span id="NAP_E_ENTITY_DISABLED"></span><span id="nap_e_entity_disabled"></span>**\_entidade E \_ NAP \_ desabilitada**
</dt> <dd> <dl> <dt>

\_\_TYPEDEF \_ de HRESULT (0x8027000EL)
</dt> <dt>



A entidade está desabilitada com o serviço NapAgent.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NETSH_GROUPPOLICY_ERROR"></span><span id="nap_e_netsh_grouppolicy_error"></span>**\_erro de GROUPPOLICY NAP E \_ netsh \_ \_**
</dt> <dd> <dl> <dt>

\_\_TYPEDEF \_ de HRESULT (0x8027000FL)
</dt> <dt>



Política de Grupo não está configurado.


</dt> </dl> </dd> <dt>

<span id="NAP_E_TOO_MANY_CALLS"></span><span id="nap_e_too_many_calls"></span>**NAP \_ E \_ excesso \_ de \_ chamadas**
</dt> <dd> <dl> <dt>

\_\_TYPEDEF \_ de HRESULT (0x80270010L)
</dt> <dt>



Muitas chamadas simultâneas.


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_CONFIG_EXISTED"></span><span id="nap_e_shv_config_existed"></span>**a \_ configuração de NAP E \_ SHV \_ \_ existia**
</dt> <dd> <dl> <dt>

\_\_TYPEDEF \_ de HRESULT (0x80270011L)
</dt> <dt>



A configuração de SHV já existe.

> [!Note]  
> Com suporte no Windows 7 ou posterior.

 


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_CONFIG_NOT_FOUND"></span><span id="nap_e_shv_config_not_found"></span>**configuração de NAP \_ E \_ SHV \_ \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

\_\_TYPEDEF \_ de HRESULT (0x80270012L)
</dt> <dt>



A configuração SHV não foi encontrada.

> [!Note]  
> Com suporte no Windows 7 ou posterior.

 


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_TIMEOUT"></span><span id="nap_e_shv_timeout"></span>**\_tempo limite de NAP E \_ SHV \_**
</dt> <dd> <dl> <dt>

\_\_TYPEDEF \_ de HRESULT (0x80270013L)
</dt> <dt>



O SHV atingiu o tempo limite na solicitação.

> [!Note]  
> Com suporte no Windows 7 ou posterior.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Constantes de NAP**](nap-constants.md)
</dt> </dl>

 

 





