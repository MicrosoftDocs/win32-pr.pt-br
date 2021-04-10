---
title: Classe MDM_Policy_User_Result01_Settings02
description: A \_ classe Result01 Settings02 do usuário da política de MDM \_ \_ \_ Obtém as configurações para calendários adicionais na barra de tarefas.
ms.assetid: 84121b24-590a-4b0b-946f-8a107eaed6c6
keywords:
- Classe MDM_Policy_User_Result01_Settings02
- Classe MDM_Policy_User_Result01_Settings02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Settings02
- MDM_Policy_User_Result01_Settings02.InstanceID
- MDM_Policy_User_Result01_Settings02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b38956121d6391433fd2727048ce95eb0b5646
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008905"
---
# <a name="mdm_policy_user_result01_settings02-class"></a>Result01 de usuário de política de MDM- \_ \_ \_ \_ classe Settings02

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

A \_ classe Result01 Settings02 do usuário da política de MDM \_ \_ \_ Obtém as configurações para calendários adicionais na barra de tarefas.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Settings02
{
  string InstanceID;
  string ParentID;
  sint32 ConfigureTaskbarCalendar;
};
```

## <a name="members"></a>Membros

A **classe \_ \_ \_ Result01 \_ Settings02 do usuário da política MDM** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ \_ \_ Result01 \_ Settings02 do usuário da política MDM** tem essas propriedades.

<dl> <dt>

[ConfigureTaskbarCalendar](/windows/client-management/mdm/policy-csp-settings#settings-configuretaskbarcalendar)
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



 

