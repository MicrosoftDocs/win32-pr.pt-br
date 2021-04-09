---
title: Estrutura de MPSIGUPDATE_DATA (MpClient. h)
description: Dados de notificação passados para a função de retorno de chamada de atualização de assinatura.
ms.assetid: E999ABC2-CC72-43CC-86D9-4F29E9128E1A
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPSIGUPDATE_DATA
- Ponteiro de estrutura de PMPSIGUPDATE_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPSIGUPDATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 442b19da394043b6fc6b8693f51c5f150233f970
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085842"
---
# <a name="mpsigupdate_data-structure"></a>\_Estrutura de dados MPSIGUPDATE

Dados de notificação passados para a função de retorno de chamada de atualização de assinatura.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPSIGUPDATE_DATA {
  DWORD                 dwPercentComplete;
  DWORD                 dwTotalUpdates;
  DWORD                 dwCurrentUpdateIndex;
  MPSIGUPDATE_TYPE      eType;
  MP_UPDATE_STAGE       Stage;
  MP_MIDL_STRING LPWSTR Path;
} MPSIGUPDATE_DATA, *PMPSIGUPDATE_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwPercentComplete**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Uma estimativa da porcentagem em todas as atualizações que foram baixadas e/ou instaladas.

</dd> <dt>

**dwTotalUpdates**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Número total de atualizações a serem baixadas e/ou instaladas.

</dd> <dt>

**dwCurrentUpdateIndex**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Valor de índice com base em zero que especifica qual atualização entre esses necessários está sendo baixada e/ou instalada no momento.

</dd> <dt>

**eType**
</dt> <dd>

Tipo: **\_ tipo de MPSIGUPDATE**

</dd> <dd>

Tipo de atualização. Um dos seguintes valores possíveis:



| Valor                                                                                                                                                                                                                             | Significado                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="MPSIGUPDATE_TYPE_NONE"></span><span id="mpsigupdate_type_none"></span><dl> <dt>**MPSIGUPDATE \_ tipo \_ nenhum**</dt> </dl>                                            |                                                                             |
| <span id="MPSIGUPDATE_TYPE_MANAGED"></span><span id="mpsigupdate_type_managed"></span><dl> <dt>**tipo de MPSIGUPDATE \_ \_ gerenciado**</dt> </dl>                                   | Atualização do WSUS. Cancelar requer direitos de administrador.<br/>               |
| <span id="MPSIGUPDATE_TYPE_HTTP"></span><span id="mpsigupdate_type_http"></span><dl> <dt>**MPSIGUPDATE \_ tipo \_ http**</dt> </dl>                                            | Atualização de HTTP. Direitos de administrador não necessários para cancelar.<br/>          |
| <span id="MPSIGUPDATE_TYPE_HTTP_SRV"></span><span id="mpsigupdate_type_http_srv"></span><dl> <dt>**MPSIGUPDATE \_ tipo \_ http \_ SRV**</dt> </dl>                               | HTTP do serviço. Cancelar requer direitos de administrador.<br/>         |
| <span id="MPSIGUPDATE_TYPE_UNC"></span><span id="mpsigupdate_type_unc"></span><dl> <dt>**MPSIGUPDATE de \_ tipo \_ UNC**</dt> </dl>                                               | Compartilhamento UNC. Direitos de administrador não necessários para cancelar.<br/>            |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED"></span><span id="mpsigupdate_type_unmanaged"></span><dl> <dt>**tipo de MPSIGUPDATE \_ \_ não gerenciado**</dt> </dl>                             | Atualização do MU/WU. Cancelar requer direitos de administrador.<br/>              |
| <span id="MPSIGUPDATE_TYPE_MANAGED_PLATFORM"></span><span id="mpsigupdate_type_managed_platform"></span><dl> <dt>**\_ \_ plataforma gerenciada do tipo MPSIGUPDATE \_**</dt> </dl>       | Atualização do WSUS para plataforma. Cancelar requer direitos de administrador.<br/>  |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED_PLATFORM"></span><span id="mpsigupdate_type_unmanaged_platform"></span><dl> <dt>**\_ \_ plataforma não gerenciada do tipo MPSIGUPDATE \_**</dt> </dl> | Atualização do MU/WU para plataforma. Cancelar requer direitos de administrador.<br/> |



 

</dd> <dt>

**Estágio**
</dt> <dd>

Tipo: **\_ \_ estágio de atualização do MP**

</dd> <dd>

Estágio de atualização. Um dos seguintes valores possíveis:



| Valor                                                                                                                                                                         | Significado                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="MP_STAGE_UNKNOWN"></span><span id="mp_stage_unknown"></span><dl> <dt>**\_estágio MP \_ desconhecido**</dt> </dl>       | Estágio de atualização desconhecido.<br/>  |
| <span id="MP_SEARCH_UPDATE"></span><span id="mp_search_update"></span><dl> <dt>**\_atualização de pesquisa de PG \_**</dt> </dl>       | Atualizar estágio de pesquisa.<br/>   |
| <span id="MP_DOWNLOAD_UPDATE"></span><span id="mp_download_update"></span><dl> <dt>**\_atualização de download do MP \_**</dt> </dl> | Atualizar estágio de download.<br/> |
| <span id="MP_INSTALL_UPDATE"></span><span id="mp_install_update"></span><dl> <dt>**\_atualização de instalação do MP \_**</dt> </dl>    | Atualizar estágio de instalação.<br/>  |



 

</dd> <dt>

**Caminho**
</dt> <dd>

Tipo: **PG \_ MIDL \_ String LPWSTR**

</dd> <dd>

Caminho de atualização.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





