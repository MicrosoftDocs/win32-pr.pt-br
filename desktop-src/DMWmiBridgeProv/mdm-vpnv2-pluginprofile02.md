---
title: MDM_VPNv2_PluginProfile02 classe
description: A classe MDM \_ VPNv2 PlugInProfile02 descreve as informações necessárias ao usar um \_ plug-in VPN Windows Store.
ms.assetid: 522c32e5-74f9-46b2-b590-ca6ade241e97
keywords:
- MDM_VPNv2_PluginProfile02 classe
- MDM_VPNv2_PluginProfile02 classe, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_PluginProfile02
- MDM_VPNv2_PluginProfile02.InstanceID
- MDM_VPNv2_PluginProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5833440924af2c8a3682a50cb066c892ce3e9c428711f21f149c70f4c0db8859
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795726"
---
# <a name="mdm_vpnv2_pluginprofile02-class"></a>Classe \_ PluginProfile02 do VPNv2 \_ MDM

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

A **classe MDM \_ VPNv2 \_ PlugInProfile02** descreve as informações necessárias ao usar um plug-in VPN Windows Store.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_PluginProfile02
{
  string InstanceID;
  string ParentID;
  string ServerUrlList;
  string CustomConfiguration;
  string PluginPackageFamilyName;
  string CustomStoreUrl;
};
```

## <a name="members"></a>Membros

A **classe MDM \_ VPNv2 \_ PluginProfile02** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe MDM \_ VPNv2 \_ PluginProfile02** tem essas propriedades.

<dl> <dt>

[CustomConfiguration](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-customconfiguration)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

</dd> <dt>

[CustomStoreUrl](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-customstoreurl)
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

Identifica o nome do nó pai.

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descreve o caminho completo para o nó pai. Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/VPNv2/*ProfileName"*

</dd> <dt>

[PluginPackageFamilyName](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-pluginpackagefamilyname)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

</dd> <dt>

[ServerUrlList](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-serverurllist)
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

 

