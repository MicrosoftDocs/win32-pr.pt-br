---
title: MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02 classe
description: A classe MDM \_ Reporting \_ EnterpriseDataProtection01 RetrieveByTimeRange02 é usada para recuperar os logs existentes em \_ StartTime e StopTime.
ms.assetid: 6abec00e-901f-4f79-840d-a4ef3a4d392d
keywords:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02 classe
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02 classe , descrita
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
ms.openlocfilehash: 60952e10f437b75edb4edf5a9465d4926b7e0615cc736f19f31520e02997d5f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045606"
---
# <a name="mdm_reporting_enterprisedataprotection01_retrievebytimerange02-class"></a>Classe MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

A **classe MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02** é usada para recuperar os logs existentes em StartTime e StopTime. StartTime e StopTime são expressos no formato ISO 8601. Se StartTime e StopTime não são especificados, os valores são interpretados como o primeiro tempo existente ou o último existente.

Aqui estão os outros cenários possíveis:

-   Se StartTime e StopTime não são especificados, ele retorna todos os logs existentes.
-   Se StopTime for especificado, mas StartTime não for especificado, todos os logs existentes antes do StopTime serão retornados.
-   Se StartTime for especificado, mas StopTime não for especificado, todos os logs existentes do StartTime serão retornados.

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

A **classe MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02** tem essas propriedades.

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

Tipo de acesso: Leitura/gravação
</dt> </dl>

</dd> <dt>

**Parentid**
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

Tipo de acesso: Leitura/gravação
</dt> </dl>

</dd> <dt>

[StopTime](/windows/client-management/mdm/reporting-csp#stoptime)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

</dd> <dt>

[Tipo](/windows/client-management/mdm/reporting-csp#type)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                            |
| Namespace<br/>                | \\Cimv2 \\ mdm \\ dmmap raiz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1.mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Mofs \\DMWmiBridgeProv.dll</dt> </dl> |



 

