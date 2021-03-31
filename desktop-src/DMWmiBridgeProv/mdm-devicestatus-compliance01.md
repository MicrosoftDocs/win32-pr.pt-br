---
title: Classe MDM_DeviceStatus_Compliance01
description: A \_ classe MDM DeviceStatus \_ Compliance01 permite consultar se o dispositivo está em conformidade com a política de criptografia corporativa.
ms.assetid: 99c4cb9b-ae53-432c-b970-d61fb8496123
keywords:
- Classe MDM_DeviceStatus_Compliance01
- Classe MDM_DeviceStatus_Compliance01, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Compliance01
- MDM_DeviceStatus_Compliance01.InstanceID
- MDM_DeviceStatus_Compliance01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf606b7f10fbe7abc196622ee54b271e5285f2c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085998"
---
# <a name="mdm_devicestatus_compliance01-class"></a>\_ \_ Classe COMPLIANCE01 do MDM DeviceStatus

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

A classe **MDM \_ DeviceStatus \_ Compliance01** permite consultar se o dispositivo está em conformidade com a política de criptografia corporativa.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Compliance01
{
  string  InstanceID;
  string  ParentID;
  boolean EncryptionCompliance;
};
```

## <a name="members"></a>Membros

A **classe \_ \_ Compliance01 de MDM DeviceStatus** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ \_ Compliance01 do MDM DeviceStatus** tem essas propriedades.

<dl> <dt>

[EncryptionCompliance](/windows/client-management/mdm/devicestatus-csp#devicestatus-compliance-encryptioncompliance)
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
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

Nó para consultas sobre conformidade.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descreve o caminho completo para o nó pai. Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/DeviceStatus"

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Namespace<br/>                | \\Dmmap de \\ MDM \\ cimv2 raiz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Como usar os scripts do PowerShell com o provedor de ponte WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

