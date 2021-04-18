---
title: Classe MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03
description: A \_ classe MDM AppLocker \_ ApplicationLaunchRestrictions01 \_ StoreApps03 permite que você ESPECIFIQUE quais aplicativos exe são permitidos ou despermitidos para a proteção de dados empresariais.
ms.assetid: de5ceaea-589a-4ed7-8dd6-eb9477d68e0e
keywords:
- Classe MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03
- Classe MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03, descrita
topic_type:
- apiref
api_name:
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03.InstanceID
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54c58610c10e672a6fbc1406b2d022b8ce211871
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769024"
---
# <a name="mdm_applocker_applicationlaunchrestrictions01_storeapps03-class"></a>\_Classe StoreApps03 do MDM AppLocker \_ ApplicationLaunchRestrictions01 \_

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

A classe **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ StoreApps03** permite que você especifique quais aplicativos exe são permitidos ou despermitidos para a proteção de dados empresariais.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
};
```

## <a name="members"></a>Membros

A classe **StoreApps03 do MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **StoreApps03 do MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_** tem essas propriedades.

<dl> <dt>

[**Imposiçãomode**](/windows/client-management/mdm/applocker-csp)
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

Define as restrições para a execução de aplicativos da Windows Store.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descreve o caminho completo para o nó pai. Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/*GROUPING*"

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Namespace<br/>                | \\DMMap de \\ MDM \\ CIMv2 raiz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Como usar os scripts do PowerShell com o provedor de ponte WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

