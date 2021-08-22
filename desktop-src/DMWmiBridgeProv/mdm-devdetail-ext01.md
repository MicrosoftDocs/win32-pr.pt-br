---
title: MDM_DevDetail_Ext01 classe
description: A classe MDM DevDetail Ext01 trata o objeto de gerenciamento que fornece parâmetros específicos do dispositivo para o \_ \_ servidor de DM do OMA.
ms.assetid: 8b8cb8e8-a299-4a87-8206-a846a79dd647
keywords:
- MDM_DevDetail_Ext01 classe
- MDM_DevDetail_Ext01 classe , descrita
topic_type:
- apiref
api_name:
- MDM_DevDetail_Ext01
- MDM_DevDetail_Ext01.InstanceID
- MDM_DevDetail_Ext01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 159647863ab9964c3b137332a66603c9bf4eb12f2cc24c79f9029e4414b200a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077300"
---
# <a name="mdm_devdetail_ext01-class"></a>Classe MDM \_ DevDetail \_ Ext01

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

A **classe MDM \_ DevDetail \_ Ext01** trata o objeto de gerenciamento que fornece parâmetros específicos do dispositivo para o servidor de DM do OMA. Esses parâmetros de dispositivo não são enviados do cliente para o servidor automaticamente, mas podem ser consultados por servidores usando comandos de DM OMA.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DevDetail_Ext01
{
  string InstanceID;
  string ParentID;
  string DeviceHardwareData;
  string WLANMACAddress;
};
```

## <a name="members"></a>Membros

A **classe MDM \_ DevDetail \_ Ext01** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe MDM \_ DevDetail \_ Ext01** tem essas propriedades.

<dl> <dt>

[DeviceHardwareData](/windows/client-management/mdm/devdetail-csp#devicehardwaredata)
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

Identifica o nome do nó pai. Para essa classe, a cadeia de caracteres é "Ext"

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descreve o caminho completo para o nó pai. Para essa classe, a cadeia de caracteres é "./DevDetail/"

</dd> <dt>

[WLANMACAddress](/windows/client-management/mdm/devdetail-csp#ext-wlanmacaddress)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Namespace<br/>                | \\Cimv2 \\ mdm \\ dmmap raiz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Como usar os scripts do PowerShell com o provedor de ponte WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

