---
title: Classe MDM_Update
description: A classe de atualização do MDM \_ é usada para gerenciar e controlar a distribuição de novas atualizações.
ms.assetid: 503884fd-190c-482d-b600-1a15363891f3
keywords:
- Classe MDM_Update
- Classe MDM_Update, descrita
topic_type:
- apiref
api_name:
- MDM_Update
- MDM_Update.InstanceID
- MDM_Update.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8c3b2c03d9ffcea84b21c1d135388141c26b24bbe2fdcc6973ae33fa74d71fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077030"
---
# <a name="mdm_update-class"></a>Classe de atualização do MDM \_

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

A classe de **\_ atualização do MDM** é usada para gerenciar e controlar a distribuição de novas atualizações.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update
{
  string   InstanceID;
  string   ParentID;
  datetime LastSuccessfulScanTime;
  sint32   DeferUpgrade;
};
```

## <a name="members"></a>Membros

A classe de **\_ atualização do MDM** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ atualização do MDM** tem essas propriedades.

<dl> <dt>

[DeferUpgrade](/windows/client-management/mdm/update-csp#deferupgrade)
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

Identifica o nome do nó pai. Para essa classe, a cadeia de caracteres é "Update".

</dd> <dt>

[LastSuccessfulScanTime](/windows/client-management/mdm/update-csp#lastsuccessfulscantime)
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
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

Descreve o caminho completo para o nó pai. Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/"

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                            |
| Namespace<br/>                | \\Dmmap de \\ MDM \\ cimv2 raiz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>\\DMWmiBridgeProv.dllMOFs</dt> </dl> |



 

