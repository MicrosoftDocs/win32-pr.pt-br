---
title: Classe MDM_EnterpriseAPN_Settings01
description: A \_ classe MDM EnterpriseAPN \_ Settings01 é usada pela empresa para alterar as configurações globais do APN.
ms.assetid: 3f2d3d38-c389-4945-b519-5f2d7dedb86c
keywords:
- Classe MDM_EnterpriseAPN_Settings01
- Classe MDM_EnterpriseAPN_Settings01, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseAPN_Settings01
- MDM_EnterpriseAPN_Settings01.InstanceID
- MDM_EnterpriseAPN_Settings01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6150e86f798e9408117daac5966f1efdecae4063ae3c4665b3f7577c1e2f31e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053526"
---
# <a name="mdm_enterpriseapn_settings01-class"></a>\_ \_ Classe SETTINGS01 do MDM EnterpriseAPN

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

A classe **MDM \_ EnterpriseAPN \_ Settings01** é usada pela empresa para alterar as configurações globais do APN.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseAPN_Settings01
{
  string  InstanceID;
  string  ParentID;
  boolean AllowUserControl;
  boolean HideView;
};
```

## <a name="members"></a>Membros

A **classe \_ \_ Settings01 de MDM EnterpriseAPN** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ \_ Settings01 do MDM EnterpriseAPN** tem essas propriedades.

<dl> <dt>

[AllowUserControl](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-settings-allowusercontrol)
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[HideView](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-settings-hideview)
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

Nó que contém configurações globais do APN.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descreve o caminho completo para o nó pai. para essa classe, a cadeia de caracteres é "./Vendor/MSFT/EnterpriseAPN/Configurações"

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Namespace<br/>                | \\Dmmap de \\ MDM \\ cimv2 raiz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

