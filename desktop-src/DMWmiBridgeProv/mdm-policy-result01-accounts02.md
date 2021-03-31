---
title: Classe MDM_Policy_Result01_Accounts02
description: A \_ classe Result01 Accounts02 de política de MDM \_ \_ representa políticas relacionadas a contas.
ms.assetid: 581d63de-6ea8-4c4a-8b94-06228ed07371
keywords:
- Classe MDM_Policy_Result01_Accounts02
- Classe MDM_Policy_Result01_Accounts02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Accounts02
- MDM_Policy_Result01_Accounts02.InstanceID
- MDM_Policy_Result01_Accounts02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e5c240f9cd4d3703122c0ea051f35ec8326e2df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644691"
---
# <a name="mdm_policy_result01_accounts02-class"></a>\_Classe MDM \_ Result01 \_ Accounts02

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

A **classe \_ \_ Result01 \_ Accounts02 de política de MDM** representa políticas relacionadas a contas.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Accounts02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMicrosoftAccountConnection;
  sint32 AllowMicrosoftAccountSignInAssistant;
  sint32 AllowAddingNonMicrosoftAccountsManually;
  string DomainNamesForEmailSync;
};
```

## <a name="members"></a>Membros

A **classe \_ \_ Result01 \_ Accounts02 da política MDM** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ \_ Result01 \_ Accounts02 da política MDM** tem essas propriedades.

<dl> <dt>

[AllowAddingNonMicrosoftAccountsManually](/windows/client-management/mdm/policy-csp-accounts#accounts-allowaddingnonmicrosoftaccountsmanually)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[AllowMicrosoftAccountConnection](/windows/client-management/mdm/policy-csp-accounts#accounts-allowmicrosoftaccountconnection)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[AllowMicrosoftAccountSignInAssistant](/windows/client-management/mdm/policy-csp-accounts#accounts-allowmicrosoftaccountsigninassistant)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

DomainNamesForEmailSync
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

Identifica o nome do nó pai. Para essa classe, a cadeia de caracteres é "contas".

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descreve o caminho completo para o nó pai. Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Result"

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Namespace<br/>                | \\DMMap de \\ MDM \\ CIMv2 raiz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Como usar os scripts do PowerShell com o provedor de ponte WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

