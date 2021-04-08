---
title: Classe MDM_Policy_Config01_CredentialsUI02
description: A \_ classe Config01 CredentialsUI02 de política de MDM \_ \_ configura as políticas de provedor de credenciais disponíveis.
ms.assetid: 508b8dc8-cc89-4260-9346-30deeac606fd
keywords:
- Classe MDM_Policy_Config01_CredentialsUI02
- Classe MDM_Policy_Config01_CredentialsUI02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_CredentialsUI02
- MDM_Policy_Config01_CredentialsUI02.InstanceID
- MDM_Policy_Config01_CredentialsUI02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e0fcb9b736adfabbf2b3de12d576ef76652e17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009173"
---
# <a name="mdm_policy_config01_credentialsui02-class"></a>\_Classe MDM \_ Config01 \_ CredentialsUI02

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

A \_ classe Config01 CredentialsUI02 de política de MDM \_ \_ configura as políticas de provedor de credenciais disponíveis.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_CredentialsUI02
{
  string InstanceID;
  string ParentID;
  string DisablePasswordReveal;
  string EnumerateAdministrators;
};
```

## <a name="members"></a>Membros

A **classe \_ \_ Config01 \_ CredentialsUI02 da política MDM** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ \_ Config01 \_ CredentialsUI02 da política MDM** tem essas propriedades.

<dl> <dt>

[DisablePasswordReveal](/windows/client-management/mdm/policy-csp-credentialsui#credentialsui-disablepasswordreveal)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[EnumerateAdministrators](/windows/client-management/mdm/policy-csp-credentialsui#credentialsui-enumerateadministrators)
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

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Namespace<br/>                | \\Dmmap de \\ MDM \\ cimv2 raiz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

