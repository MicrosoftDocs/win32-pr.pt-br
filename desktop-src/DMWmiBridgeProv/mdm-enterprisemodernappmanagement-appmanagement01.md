---
title: Classe MDM_EnterpriseModernAppManagement_AppManagement01
description: A \_ classe MDM EnterpriseModernAppManagement \_ AppManagement01 inicia o Windows Update examina e relata o último erro de verificação.
ms.assetid: f579a7c9-2e98-4e34-b45b-db8a4d553c57
keywords:
- Classe MDM_EnterpriseModernAppManagement_AppManagement01
- Classe MDM_EnterpriseModernAppManagement_AppManagement01, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01
- MDM_EnterpriseModernAppManagement_AppManagement01.InstanceID
- MDM_EnterpriseModernAppManagement_AppManagement01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be1f2a3739fe16d4a13e409d7d152645d4653336
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163600"
---
# <a name="mdm_enterprisemodernappmanagement_appmanagement01-class"></a>\_ \_ Classe APPMANAGEMENT01 do MDM EnterpriseModernAppManagement

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

A classe **MDM \_ EnterpriseModernAppManagement \_ AppManagement01** inicia o Windows Update examina e relata o último erro de verificação.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppManagement01
{
  string InstanceID;
  string ParentID;
  sint32 LastScanError;
  string AppInventoryQuery;
  string AppInventoryResults;
  string RemovePackage;
};
```

## <a name="members"></a>Membros

A **classe \_ \_ AppManagement01 de MDM EnterpriseModernAppManagement** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ \_ AppManagement01 do MDM EnterpriseModernAppManagement** tem esses métodos.



| Método                                                                                               | Descrição                                             |
|:-----------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| [**RemovePackageMethod**](mdm-enterprisemodernappmanagement-appmanagement01-removepackagemethod.md) | Método para remover pacotes.<br/>                |
| [**UpdateScanMethod**](mdm-enterprisemodernappmanagement-appmanagement01-updatescanmethod.md)       | Método para iniciar a verificação de Windows Update.<br/> |



 

### <a name="properties"></a>Propriedades

A **classe \_ \_ AppManagement01 do MDM EnterpriseModernAppManagement** tem essas propriedades.

<dl> <dt>

[AppInventoryQuery](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-appinventoryquery)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[AppInventoryResults](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-appinventoryresults)
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

Identifica o nome do nó pai. Para essa classe, a cadeia de caracteres é "AppManagement".

</dd> <dt>

[LastScanError](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-lastscanerror)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
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

Descreve o caminho completo para o nó pai. Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/EnterpriseModernAppManagement/"

</dd> <dt>

[RemovePackage](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-removepackage)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

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

 

