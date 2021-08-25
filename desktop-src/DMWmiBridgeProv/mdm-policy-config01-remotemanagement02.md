---
title: Classe MDM_Policy_Config01_RemoteManagement02
description: A política de MDM \_ \_ Config01 \_ RemoteManagement02 políticas de gerenciamento remoto.
ms.assetid: 2eabbf72-00a4-4c61-9ae1-ff49067cb502
keywords:
- Classe MDM_Policy_Config01_RemoteManagement02
- Classe MDM_Policy_Config01_RemoteManagement02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteManagement02
- MDM_Policy_Config01_RemoteManagement02.InstanceID
- MDM_Policy_Config01_RemoteManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba9113d435e828b0c1ddf45e67fb71ee4e39372f3d9b804bded4e97be01e47f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694756"
---
# <a name="mdm_policy_config01_remotemanagement02-class"></a>\_Classe MDM \_ Config01 \_ RemoteManagement02

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

A política de MDM \_ \_ Config01 \_ RemoteManagement02 políticas de gerenciamento remoto.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteManagement02
{
  string InstanceID;
  string ParentID;
  string AllowBasicAuthentication_Client;
  string AllowBasicAuthentication_Service;
  string AllowCredSSPAuthenticationClient;
  string AllowCredSSPAuthenticationService;
  string AllowRemoteServerManagement;
  string AllowUnencryptedTraffic_Client;
  string AllowUnencryptedTraffic_Service;
  string DisallowDigestAuthentication;
  string DisallowNegotiateAuthenticationClient;
  string DisallowNegotiateAuthenticationService;
  string DisallowStoringOfRunAsCredentials;
  string SpecifyChannelBindingTokenHardeningLevel;
  string TrustedHosts;
  string TurnOnCompatibilityHTTPListener;
  string TurnOnCompatibilityHTTPSListener;
};
```

## <a name="members"></a>Membros

A **classe \_ \_ Config01 \_ RemoteManagement02 da política MDM** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ \_ Config01 \_ RemoteManagement02 da política MDM** tem essas propriedades.

<dl> <dt>

[\_Cliente AllowBasicAuthentication](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowbasicauthentication-client)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[\_Serviço AllowBasicAuthentication](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowbasicauthentication-service)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[AllowCredSSPAuthenticationClient](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowcredsspauthenticationclient)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[AllowCredSSPAuthenticationService](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowcredsspauthenticationservice)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[AllowRemoteServerManagement](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowremoteservermanagement)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[\_Cliente AllowUnencryptedTraffic](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowunencryptedtraffic-client)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[\_Serviço AllowUnencryptedTraffic](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowunencryptedtraffic-service)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[DisallowDigestAuthentication](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallowdigestauthentication)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[DisallowNegotiateAuthenticationClient](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallownegotiateauthenticationclient)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[DisallowNegotiateAuthenticationService](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallownegotiateauthenticationservice)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[DisallowStoringOfRunAsCredentials](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallowstoringofrunascredentials)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
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

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> <dt>

[SpecifyChannelBindingTokenHardeningLevel](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-specifychannelbindingtokenhardeninglevel)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[TrustedHosts](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-trustedhosts)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[TurnOnCompatibilityHTTPListener](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-turnoncompatibilityhttplistener)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[TurnOnCompatibilityHTTPSListener](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-turnoncompatibilityhttpslistener)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Namespace<br/>                | \\Dmmap de \\ MDM \\ cimv2 raiz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

