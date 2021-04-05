---
description: A \_ classe CIM CollectionSetting representa a associação entre um CIM \_ CollectionOfMSEs e a classe de configuração definida para eles.
ms.assetid: f09bd656-5fdd-4ab1-8ef9-52d431a5117d
ms.tgt_platform: multiple
title: Classe CIM_CollectionSetting
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
ms.openlocfilehash: c290225ee38008f0345b695af794e57f311f2998
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826500"
---
# <a name="cim_collectionsetting-class"></a>\_Classe CIM CollectionSetting

A classe **CIM \_ CollectionSetting** representa a associação entre um [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) e a classe de configuração definida para eles.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

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

A classe **CIM \_ CollectionSetting** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ CollectionSetting** tem essas propriedades.

<dl> <dt>

**Coleção**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ CollectionOfMSEs**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência à classe [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) .

</dd> <dt>

**Configuração**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ configuração de CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência ao objeto de **configuração** associado à propriedade de **coleção** .

</dd> </dl>

## <a name="remarks"></a>Comentários

O WMI não implementa essa classe. Para obter mais informações sobre classes WMI derivadas do **CIM \_ CollectionSetting**, consulte [classes Win32](win32-provider.md).

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




