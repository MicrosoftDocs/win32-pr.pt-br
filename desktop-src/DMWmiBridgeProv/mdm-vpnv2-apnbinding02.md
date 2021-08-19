---
title: Classe MDM_VPNv2_APNBinding02
description: Reservado para uso futuro. | Classe MDM_VPNv2_APNBinding02
ms.assetid: ef530e79-b9cc-4bee-8d7b-45227ed55dbe
keywords:
- Classe MDM_VPNv2_APNBinding02
- Classe MDM_VPNv2_APNBinding02, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_APNBinding02
- MDM_VPNv2_APNBinding02.InstanceID
- MDM_VPNv2_APNBinding02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff62d5a2280a28292289e6e6a1374615f066a66463eef9a8c0e3db58383874ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084806"
---
# <a name="mdm_vpnv2_apnbinding02-class"></a>\_ \_ Classe APNBINDING02 do MDM VPNv2

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Reservado para uso futuro

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_APNBinding02
{
  string  InstanceID;
  string  ParentID;
  string  ProviderId;
  string  AccessPointName;
  string  UserName;
  string  Password;
  boolean IsCompressionEnabled;
  string  AuthenticationType;
};
```

## <a name="members"></a>Membros

A **classe \_ \_ APNBinding02 de MDM VPNv2** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ \_ APNBinding02 do MDM VPNv2** tem essas propriedades.

<dl> <dt>

[AccessPointName](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-accesspointname)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[AuthenticationType](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-authenticationtype)
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

Reservado para uso futuro.

</dd> <dt>

[IsCompressionEnabled](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-iscompressionenabled)
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
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

Reservado para uso futuro.

</dd> <dt>

[Senha](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-password)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[ProviderId](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-providerid)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[UserName](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-username)
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



## <a name="see-also"></a>Confira também

<dl> <dt>

[Como usar os scripts do PowerShell com o provedor de ponte WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

