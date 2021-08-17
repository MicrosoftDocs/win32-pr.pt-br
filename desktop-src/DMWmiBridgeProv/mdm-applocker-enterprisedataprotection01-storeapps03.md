---
title: Classe MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
description: a \_ classe MDM AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03 captura a lista de aplicativos Windows que têm permissão para lidar com dados corporativos. Deve ser usado em conjunto com as configurações em./Vendor/MSFT/Policy/ConfigSource/DataProtection.
ms.assetid: f37fe52d-dbe1-45b7-acd5-5047c46d9bd0
keywords:
- Classe MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
- Classe MDM_AppLocker_EnterpriseDataProtection01_StoreApps03, descrita
topic_type:
- apiref
api_name:
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03.InstanceID
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5b0c3af455e501695cb7a2093b841159f5755ac54e1de97a370c7dc7f2d6fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077401"
---
# <a name="mdm_applocker_enterprisedataprotection01_storeapps03-class"></a>\_Classe StoreApps03 do MDM AppLocker \_ EnterpriseDataProtection01 \_

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

a classe **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03** captura a lista de aplicativos Windows que têm permissão para lidar com dados corporativos. Deve ser usado em conjunto com as configurações em./Vendor/MSFT/Policy/ConfigSource/DataProtection.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a>Membros

A classe **StoreApps03 do MDM \_ AppLocker \_ EnterpriseDataProtection01 \_** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **StoreApps03 do MDM \_ AppLocker \_ EnterpriseDataProtection01 \_** tem essas propriedades.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

define as restrições para a execução de aplicativos do Windows Store.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descreve o caminho completo para o nó pai. Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*GROUPING*"

</dd> <dt>

[**Política**](/windows/client-management/mdm/applocker-csp)
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
| Namespace<br/>                | \\DMMap de \\ MDM \\ CIMv2 raiz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Como usar os scripts do PowerShell com o provedor de ponte WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

