---
title: Classe MDM_AppLocker_CodeIntegrity03
description: A \_ classe CodeIntegrity03 do MDM AppLocker \_ define a política para a integridade do código.
ms.assetid: 8e7649b4-2e89-4d79-923e-3767e5b0ea52
keywords:
- Classe MDM_AppLocker_CodeIntegrity03
- Classe MDM_AppLocker_CodeIntegrity03, descrita
topic_type:
- apiref
api_name:
- MDM_AppLocker_CodeIntegrity03
- MDM_AppLocker_CodeIntegrity03.InstanceID
- MDM_AppLocker_CodeIntegrity03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff702f2887f47c1cc5fcebeb4b8ec9a08c450b8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644575"
---
# <a name="mdm_applocker_codeintegrity03-class"></a>\_ \_ Classe CODEINTEGRITY03 do MDM AppLocker

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

A **classe \_ \_ CodeIntegrity03 do MDM AppLocker** define a política para a integridade do código.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_CodeIntegrity03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a>Membros

A **classe \_ \_ CodeIntegrity03 do MDM AppLocker** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ \_ CodeIntegrity03 do MDM AppLocker** tem essas propriedades.

<dl> <dt>

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

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descreve o caminho completo para o nó pai. Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"

</dd> <dt>

[**Política**](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: **octetstring**
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



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Como usar os scripts do PowerShell com o provedor de ponte WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

