---
description: A classe LogicalDiskBasedOnPartition cim associa um disco lógico à partição de disco \_ na qual ele reside.
ms.assetid: 264b62ed-2af2-42dc-9cd2-41b26cc85ca4
ms.tgt_platform: multiple
title: CIM_LogicalDiskBasedOnPartition classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDiskBasedOnPartition
- CIM_LogicalDiskBasedOnPartition.EndingAddress
- CIM_LogicalDiskBasedOnPartition.StartingAddress
- CIM_LogicalDiskBasedOnPartition.Dependent
- CIM_LogicalDiskBasedOnPartition.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 27e0805d4fa3a4a59d59423b30b3644e78ccc6138509b2b0f71cdecb435ffc7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118679868"
---
# <a name="cim_logicaldiskbasedonpartition-class"></a>Classe CIM \_ LogicalDiskBasedOnPartition

A **classe \_ LogicalDiskBasedOnPartition cim** associa um disco lógico à partição de disco na qual ele reside.

Por exemplo, a unidade C de um computador pode estar localizada em uma partição na mídia física local, o que determina que um disco lógico não pode abranger mais de uma partição. Quando um disco lógico pode abranger mais de uma partição, no entanto, o disco lógico é baseado na configuração raid (por exemplo, um espelho ou conjunto de faixas). Nesse caso, o disco lógico é baseado no volume de armazenamento. Para evitar o uso da associação **\_ LogicalDiskBasedOnPartition** cim incorretamente, o qualificador **Max(1)** foi colocado na referência **antecedente** à partição de disco.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) modelo CIM DMTF são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{8502C53F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalDiskBasedOnPartition : CIM_BasedOn
{
  uint64                EndingAddress;
  uint64                StartingAddress;
  CIM_LogicalDisk   REF Dependent;
  CIM_DiskPartition REF Antecedent;
};
```

## <a name="members"></a>Membros

A **classe \_ CIM LogicalDiskBasedOnPartition** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ LogicalDiskBasedOnPartition cim** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ DiskPartition**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecessor"), [**Máx.**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Um [**\_ DiskPartition cim**](cim-diskpartition.md) que descreve a partição de disco.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ LogicalDisk**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependente")
</dt> </dl>

Um [**\_ LogicalDisk cim**](cim-logicaldisk.md) que descreve o disco lógico criado na partição.

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o final da extensão de alto nível no armazenamento de nível inferior. Essa propriedade é útil ao mapear as extensão não contíguas para um grupo de nível superior.

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Essa propriedade é herdada de [**CIM \_ BasedOn.**](cim-basedon.md)

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o início da extensão de alto nível no armazenamento de nível inferior.

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Essa propriedade é herdada de [**CIM \_ BasedOn.**](cim-basedon.md)

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ CIM LogicalDiskBasedOnPartition** é derivada de [**CIM \_ BasedOn**](cim-basedon.md).

O WMI não implementa essa classe. Para classes derivadas de **\_ LOGICALDiskBasedOnPartition** cim , consulte [Classes Win32](win32-provider.md).

Esta documentação é derivada das descrições da classe CIM publicadas pelo DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, estar em conformidade com os padrões de documentação do SDK da Microsoft ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**CIM \_ BasedOn**](cim-basedon.md)
</dt> </dl>

 

