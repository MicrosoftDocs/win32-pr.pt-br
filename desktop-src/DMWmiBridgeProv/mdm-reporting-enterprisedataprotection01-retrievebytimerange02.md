---
title: Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
description: A \_ classe EnterpriseDataProtection01 RetrieveByTimeRange02 de relatórios do MDM \_ \_ é usada para recuperar os logs que existem dentro de StartTime e StopTime.
ms.assetid: 6abec00e-901f-4f79-840d-a4ef3a4d392d
keywords:
- Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
- Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02, descrita
topic_type:
- apiref
api_name:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02.InstanceID
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec266e68bbaaafb1f1e3a78fba7ea6b91805096a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008899"
---
# <a name="mdm_reporting_enterprisedataprotection01_retrievebytimerange02-class"></a>\_Classe RetrieveByTimeRange02 de relatórios MDM \_ EnterpriseDataProtection01 \_

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

A **classe \_ \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02 de relatórios do MDM** é usada para recuperar os logs que existem dentro de StartTime e StopTime. StartTime e StopTime são expressos no formato ISO 8601. Se StartTime e StopTime não forem especificados, os valores serão interpretados como a primeira hora existente ou a última.

Estes são os outros cenários possíveis:

-   Se StartTime e StopTime não forem especificados, ele retornará todos os logs existentes.
-   Se o StopTime for especificado, mas o StartTime não for especificado, todos os logs existentes antes de StopTime serão retornados.
-   Se StartTime for especificado, mas o StopTime não for especificado, todos os logs que existirem de StartTime serão retornados.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
{
  string InstanceID;
  string ParentID;
  string Logs;
  string StartTime;
  string StopTime;
  sint32 Type;
};
```

## <a name="members"></a>Membros

A **classe \_ RetrieveByTimeRange02 de relatórios do MDM \_ EnterpriseDataProtection01 \_** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ RetrieveByTimeRange02 de relatório do MDM \_ EnterpriseDataProtection01 \_** tem essas propriedades.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica o nome do nó pai. Para essa classe, a cadeia de caracteres é "RetrieveByTimeRange".

</dd> <dt>

[Logs](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
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

Descreve o caminho completo para o nó pai. Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/EnterpriseDataProtection"

</dd> <dt>

[StartTime](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[StopTime](/windows/client-management/mdm/reporting-csp#stoptime)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[Tipo](/windows/client-management/mdm/reporting-csp#type)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                            |
| Namespace<br/>                | \\Dmmap de \\ MDM \\ cimv2 raiz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>\\DMWmiBridgeProv.dllMOFs</dt> </dl> |



 

