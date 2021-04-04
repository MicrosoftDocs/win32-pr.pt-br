---
title: Classe MDM_Update_ApprovedUpdates01_01
description: A \_ classe MDM update \_ ApprovedUpdates01 \_ 01 é usada para gerenciar e controlar a distribuição de atualizações aprovadas.
ms.assetid: 3903dbc1-c745-4e9a-a7f7-455338b77563
keywords:
- Classe MDM_Update_ApprovedUpdates01_01
- Classe MDM_Update_ApprovedUpdates01_01, descrita
topic_type:
- apiref
api_name:
- MDM_Update_ApprovedUpdates01_01
- MDM_Update_ApprovedUpdates01_01.InstanceID
- MDM_Update_ApprovedUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e6e12700b04f6e48fdf746cb27953da5849169d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918017"
---
# <a name="mdm_update_approvedupdates01_01-class"></a>\_ \_ Classe ApprovedUpdates01 01 de atualização \_ do MDM

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

A classe **MDM \_ Update \_ ApprovedUpdates01 \_ 01** é usada para gerenciar e controlar a distribuição de atualizações aprovadas.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_ApprovedUpdates01_01
{
  string   InstanceID;
  string   ParentID;
  datetime ApprovedTime;
};
```

## <a name="members"></a>Membros

A classe **MDM \_ Update \_ ApprovedUpdates01 \_ 01** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **MDM \_ Update \_ ApprovedUpdates01 \_ 01** tem essas propriedades.

<dl> <dt>

[Aprovadotime](/windows/client-management/mdm/update-csp#approvedupdates-approved-update-guid-approvedtime)
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
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

Identifica o nome do nó pai. Para essa classe, a cadeia de caracteres é o GUID da atualização aprovada.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descreve o caminho completo para o nó pai. Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Update/ApprovedUpdates"

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                            |
| Namespace<br/>                | \\Dmmap de \\ MDM \\ cimv2 raiz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>\\DMWmiBridgeProv.dllMOFs</dt> </dl> |



 

