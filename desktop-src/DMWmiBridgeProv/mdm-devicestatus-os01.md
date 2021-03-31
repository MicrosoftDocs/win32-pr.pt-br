---
title: Classe MDM_DeviceStatus_OS01
description: A \_ classe MDM DeviceStatus \_ OS01 é usada pela empresa para consultar o sistema operacional em dispositivos com suas políticas corporativas.
ms.assetid: 887dc453-f6b5-4f09-8ce1-b87f71dd8396
keywords:
- Classe MDM_DeviceStatus_OS01
- Classe MDM_DeviceStatus_OS01, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_OS01
- MDM_DeviceStatus_OS01.InstanceID
- MDM_DeviceStatus_OS01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01bff7a57d71b3d651ea2b97a0eac5b2ccd94255
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085996"
---
# <a name="mdm_devicestatus_os01-class"></a>\_ \_ Classe OS01 do MDM DeviceStatus

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

A classe **MDM \_ DeviceStatus \_ OS01** é usada pela empresa para consultar o sistema operacional em dispositivos com suas políticas corporativas.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_OS01
{
  string InstanceID;
  string ParentID;
  string Edition;
};
```

## <a name="members"></a>Membros

A **classe \_ \_ OS01 de MDM DeviceStatus** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ \_ OS01 do MDM DeviceStatus** tem essas propriedades.

<dl> <dt>

[Edição](/windows/client-management/mdm/devicestatus-csp#devicestatus-os-edition)
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

Nó para a consulta do sistema operacional.

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



 

