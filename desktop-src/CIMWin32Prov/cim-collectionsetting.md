---
description: A classe \_ CollectionSetting cim representa a associação entre uma \_ Coleção CIMOfMSEs e a classe de configuração definida para eles.
ms.assetid: f09bd656-5fdd-4ab1-8ef9-52d431a5117d
ms.tgt_platform: multiple
title: CIM_CollectionSetting classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionSetting
- CIM_CollectionSetting.Collection
- CIM_CollectionSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d3f8e1c57301c3357ff4d28a056cb92bc4572eb29b62b6414a0064113189173a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119700886"
---
# <a name="cim_collectionsetting-class"></a>Classe Cim \_ CollectionSetting

A **classe \_ CollectionSetting cim** representa a associação entre uma Coleção [**\_ CIMOfMSEs**](cim-collectionofmses.md) e a classe de configuração definida para eles.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class CIM_CollectionSetting
{
  CIM_CollectionOfMSEs REF Collection;
  CIM_Setting          REF Setting;
};
```

## <a name="members"></a>Membros

A **classe Cim \_ CollectionSetting** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ CollectionSetting cim** tem essas propriedades.

<dl> <dt>

**Coleção**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ Coleção CIMOfMSEs**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência à [**classe CIM \_ CollectionOfMSEs.**](cim-collectionofmses.md)

</dd> <dt>

**Configuração**
</dt> <dd> <dl> <dt>

Tipo de dados: **Configuração cim \_**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência ao **objeto Setting** associado à **propriedade** Collection.

</dd> </dl>

## <a name="remarks"></a>Comentários

O WMI não implementa essa classe. Para obter mais informações sobre classes WMI derivadas de **\_ CollectionSetting cim**, consulte [Classes Win32](win32-provider.md).

Esta documentação é derivada das descrições da classe CIM publicadas pelo DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, estar em conformidade com os padrões de documentação do SDK da Microsoft ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




