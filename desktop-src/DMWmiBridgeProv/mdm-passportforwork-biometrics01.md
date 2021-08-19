---
title: MDM_PassportForWork_Biometrics01 classe
description: A classe MDM \_ PassportForWork \_ Biometrics01 define as configurações biométricas.
ms.assetid: 64012526-eac6-4f01-8665-2bd460bc1b93
keywords:
- MDM_PassportForWork_Biometrics01 classe
- MDM_PassportForWork_Biometrics01 classe, descrita
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Biometrics01
- MDM_PassportForWork_Biometrics01.InstanceID
- MDM_PassportForWork_Biometrics01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c22ecbb67499462825e1353d3d8bb8c3b08cedd93c79b1467f40f7c79ebf1f2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084926"
---
# <a name="mdm_passportforwork_biometrics01-class"></a>Classe MDM \_ PassportForWork \_ Biometrics01

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

A **classe MDM \_ PassportForWork \_ Biometrics01** define as configurações biométricas.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Biometrics01
{
  string  InstanceID;
  string  ParentID;
  boolean UseBiometrics;
  boolean FacialFeaturesUseEnhancedAntiSpoofing;
};
```

## <a name="members"></a>Membros

A **classe MDM \_ PassportForWork \_ Biometrics01** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe MDM \_ PassportForWork \_ Biometrics01** tem essas propriedades.

<dl> <dt>

[FacialFeaturesUseEnhancedAntiSpoofing](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
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

Descreve o caminho completo para o nó pai. Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/PassportForWork/"

</dd> <dt>

[UseBiometrics](/windows/client-management/mdm/passportforwork-csp#usebiometrics)
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
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

 

