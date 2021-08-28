---
title: Classe MDM_Policy_Config01_Printers02
description: A \_ classe Config01 Printers02 de política de MDM \_ \_ configura as políticas de impressora.
ms.assetid: c0e6dc53-5f84-4cef-a4c4-08db6486784a
keywords:
- Classe MDM_Policy_Config01_Printers02
- Classe MDM_Policy_Config01_Printers02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Printers02
- MDM_Policy_Config01_Printers02.InstanceID
- MDM_Policy_Config01_Printers02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04fd3a0070a11659b9a9549cf28b89463032c792b1cc4e01bbee1a9e9a5dfcc8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834006"
---
# <a name="mdm_policy_config01_printers02-class"></a>\_Classe MDM \_ Config01 \_ Printers02

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

A \_ classe Config01 Printers02 de política de MDM \_ \_ configura as políticas de impressora.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Printers02
{
  string InstanceID;
  string ParentID;
  string PointAndPrintRestrictions;
  string PublishPrinters;
};
```

## <a name="members"></a>Membros

A **classe \_ \_ Config01 \_ Printers02 da política MDM** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ \_ Config01 \_ Printers02 da política MDM** tem essas propriedades.

<dl> <dt>

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

</dd> <dt>

[PointAndPrintRestrictions](/windows/client-management/mdm/policy-csp-printers#printers-pointandprintrestrictions)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[PublishPrinters](/windows/client-management/mdm/policy-csp-printers#printers-publishprinters)
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
| Namespace<br/>                | \\Dmmap de \\ MDM \\ cimv2 raiz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

