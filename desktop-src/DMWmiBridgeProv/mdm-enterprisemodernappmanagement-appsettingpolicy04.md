---
title: Classe MDM_EnterpriseModernAppManagement_AppSettingPolicy04
description: A \_ classe MDM EnterpriseModernAppManagement \_ AppSettingPolicy04 especifica todos os valores de configuração de aplicativo gerenciado.
ms.assetid: 65e2d2aa-31fd-4733-a1f7-8a572700a562
keywords:
- Classe MDM_EnterpriseModernAppManagement_AppSettingPolicy04
- Classe MDM_EnterpriseModernAppManagement_AppSettingPolicy04, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04.InstanceID
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba82be4653266c94465917857eb47b014399594525a6f0f18264e4f73651684
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077250"
---
# <a name="mdm_enterprisemodernappmanagement_appsettingpolicy04-class"></a>\_ \_ Classe APPSETTINGPOLICY04 do MDM EnterpriseModernAppManagement

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

A classe **MDM \_ EnterpriseModernAppManagement \_ AppSettingPolicy04** especifica todos os valores de configuração de aplicativo gerenciado.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppSettingPolicy04
{
  string  InstanceID;
  string  ParentID;
  string  Value;
  boolean IsVariableLeaf;
};
```

## <a name="members"></a>Membros

A **classe \_ \_ AppSettingPolicy04 de MDM EnterpriseModernAppManagement** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ \_ AppSettingPolicy04 do MDM EnterpriseModernAppManagement** tem essas propriedades.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica o nome do nó pai. Para essa classe, a cadeia de caracteres "AppSettingPolicy".

</dd> <dt>

[IsVariableLeaf](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

adicionado em Windows 10, versão 1511. O **configurador** e os dados representam um par chave-valor a ser configurado para o aplicativo. O nó representa o nome da chave e os dados representam o valor. Você pode encontrar esse valor em LocalSettings no Managed.App. Configurações contêiner.

Essa configuração só funciona para aplicativos que dão suporte ao recurso e só tem suporte no contexto do usuário.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descreve o caminho completo para o nó pai. Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/AppStore/*PackageFamilyName*"

</dd> <dt>

[**Valor**](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
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



## <a name="see-also"></a>Confira também

<dl> <dt>

[Como usar os scripts do PowerShell com o provedor de ponte WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

