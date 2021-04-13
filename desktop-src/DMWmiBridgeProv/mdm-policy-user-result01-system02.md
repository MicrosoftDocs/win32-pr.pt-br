---
title: Classe MDM_Policy_User_Result01_System02
description: A \_ classe Result01 System02 do usuário da política de MDM \_ \_ \_ representa as políticas de telemetria disponíveis.
ms.assetid: ed16474c-3bbb-41d8-9806-81dbd95c608d
keywords:
- Classe MDM_Policy_User_Result01_System02
- Classe MDM_Policy_User_Result01_System02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_System02
- MDM_Policy_User_Result01_System02.InstanceID
- MDM_Policy_User_Result01_System02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ce5e01429a648d265904d3b3996be9fb7a3faa5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369252"
---
# <a name="mdm_policy_user_result01_system02-class"></a>Result01 de usuário de política de MDM- \_ \_ \_ \_ classe System02

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

A \_ classe Result01 System02 do usuário da política de MDM \_ \_ \_ representa as políticas de telemetria disponíveis.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_System02
{
  string InstanceID;
  string ParentID;
  sint32 AllowTelemetry;
};
```

## <a name="members"></a>Membros

A **classe \_ \_ \_ Result01 \_ System02 do usuário da política MDM** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ \_ \_ Result01 \_ System02 do usuário da política MDM** tem essas propriedades.

<dl> <dt>

[AllowTelemetry](/windows/client-management/mdm/policy-csp-system#system-allowtelemetry)
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



 

