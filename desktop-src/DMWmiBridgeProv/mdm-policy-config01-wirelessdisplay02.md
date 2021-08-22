---
title: Classe MDM_Policy_Config01_WirelessDisplay02
description: A \_ classe MDM Policy \_ Config01 \_ WirelessDisplay02 representa as políticas de exibição sem fio disponíveis.
ms.assetid: 24b72ed9-cc14-4318-a9d1-597976083242
keywords:
- Classe MDM_Policy_Config01_WirelessDisplay02
- Classe MDM_Policy_Config01_WirelessDisplay02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_WirelessDisplay02
- MDM_Policy_Config01_WirelessDisplay02.InstanceID
- MDM_Policy_Config01_WirelessDisplay02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489b465a77ccd10aef2e7ec58f3ac17a2464db005cb114cb3fe2eae6a5869a8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587956"
---
# <a name="mdm_policy_config01_wirelessdisplay02-class"></a>\_Classe MDM \_ Config01 \_ WirelessDisplay02

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

A classe **MDM \_ Policy \_ Config01 \_ WirelessDisplay02** representa as políticas de exibição sem fio disponíveis.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_WirelessDisplay02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMdnsDiscovery;
  sint32 AllowMdnsAdvertisement;
  sint32 AllowProjectionFromPCOverInfrastructure;
  sint32 AllowProjectionFromPC;
  sint32 AllowProjectionToPC;
  sint32 AllowProjectionToPCOverInfrastructure;
  sint32 AllowUserInputFromWirelessDisplayReceiver;
  sint32 RequirePinForPairing;
};
```

## <a name="members"></a>Membros

A **classe \_ \_ Config01 \_ WirelessDisplay02 da política MDM** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ \_ Config01 \_ WirelessDisplay02 da política MDM** tem essas propriedades.

<dl> <dt>

[AllowMdnsAdvertisement](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowmdnsadvertisement)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[AllowMdnsDiscovery](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowmdnsdiscovery)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[AllowProjectionFromPC](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectionfrompc)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[AllowProjectionFromPCOverInfrastructure](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectionfrompcoverinfrastructure)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[AllowProjectionToPC](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectiontopc)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[AllowProjectionToPCOverInfrastructure](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectiontopcoverinfrastructure)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[AllowUserInputFromWirelessDisplayReceiver](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowuserinputfromwirelessdisplayreceiver)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
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

Identifica o nome do nó pai. Para essa classe, a cadeia de caracteres é "WirelessDisplay".

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descreve o caminho completo para o nó pai. Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Config"

</dd> <dt>

[RequirePinForPairing](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-requirepinforpairing)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                            |
| Namespace<br/>                | \\Dmmap de \\ MDM \\ cimv2 raiz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>\\DMWmiBridgeProv.dllMOFs</dt> </dl> |



 

