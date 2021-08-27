---
title: MDM_VPNv2_AppTriggerList02_App04 classe
description: A classe MDM \_ VPNv2AppTriggerList02 App04 descreve uma lista de \_ aplicativos definidos para disparar a VPN.
ms.assetid: d17ec7b9-8a66-47da-8373-81b56168b495
keywords:
- MDM_VPNv2_AppTriggerList02_App04 classe
- MDM_VPNv2_AppTriggerList02_App04 classe , descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_AppTriggerList02_App04
- MDM_VPNv2_AppTriggerList02_App04.InstanceID
- MDM_VPNv2_AppTriggerList02_App04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 067e23f747ff5fdc6b3e9c848a5d8f4b8463b716c14cadd5cac9d89bfe2ab746
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109236"
---
# <a name="mdm_vpnv2_apptriggerlist02_app04-class"></a>Classe MDM \_ VPNv2 \_ AppTriggerList02 \_ App04

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

A **classe MDM \_ VPNv2AppTriggerList02 \_ App04** descreve uma lista de aplicativos definidos para disparar a VPN.

Se qualquer um desses aplicativos for lançado e o perfil VPN for o perfil ativo no momento, esse perfil vpn será disparado para se conectar.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_AppTriggerList02_App04
{
  string InstanceID;
  string ParentID;
  string Id;
  string Type;
};
```

## <a name="members"></a>Membros

A **classe MDM \_ VPNv2 \_ AppTriggerList02 \_ App04** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe MDM \_ VPNv2 \_ AppTriggerList02 \_ App04** tem essas propriedades.

<dl> <dt>

[Id](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-app-id)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nó do Aplicativo na ID da Linha.

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descreve o caminho completo para o nó pai. Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/VPNv2/*ProfileName*/AppTriggerList/*appTriggerRowId*"

</dd> <dt>

[Tipo](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apptriggerlist-apptriggerrowid-app-type)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Namespace<br/>                | \\DMMap de \\ MDM cimv2 \\ raiz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Como usar os scripts do PowerShell com o provedor de ponte WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

