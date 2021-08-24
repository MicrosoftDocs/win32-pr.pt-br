---
title: MDM_DeviceManageability_Provider01_01 classe
description: A classe \_ DeviceManageability Provider01 01 do MDM é usada para recuperar as informações gerais sobre os recursos de configuração \_ \_ de MDM no dispositivo.
ms.assetid: 080e5cdd-4509-42d6-b5f8-36df6f8d9b45
keywords:
- MDM_DeviceManageability_Provider01_01 classe
- MDM_DeviceManageability_Provider01_01, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceManageability_Provider01_01
- MDM_DeviceManageability_Provider01_01.InstanceID
- MDM_DeviceManageability_Provider01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e45fa96c71902bae9f6c7a98be8004b6f632fa0dad04952720f9a9c598879a03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825736"
---
# <a name="mdm_devicemanageability_provider01_01-class"></a>Classe MDM \_ DeviceManageability \_ Provider01 \_ 01

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

A classe \_ DeviceManageability Provider01 01 do MDM é usada para recuperar as informações gerais sobre os recursos de configuração \_ \_ de MDM no dispositivo.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_DeviceManageability_Provider01_01
{
  string InstanceID;
  string ParentID;
  string ConfigInfo;
  string EnrollmentInfo;
};
```

## <a name="members"></a>Membros

A **classe \_ DeviceManageability \_ Provider01 \_ 01 do MDM** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ DeviceManageability \_ Provider01 \_ 01 do MDM** tem essas propriedades.

<dl> <dt>

[ConfigInfo](/windows/client-management/mdm/devicemanageability-csp#capabilities-cspversions)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Você deve definir o valor como Servidor de \_ Ponte WMI. \_ O chamador não pode definir dinamicamente a ID do Provedor.

</dd> <dt>

[EnrollmentInfo](/windows/client-management/mdm/devicemanageability-csp#capabilities-cspversions)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
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

**Parentid**
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
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                     |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                       |
| Namespace<br/>                | \\Cimv2 \\ mdm \\ dmmap raiz<br/>                                                              |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl>  |



 

