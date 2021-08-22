---
description: Faz referência às informações de compatibilidade para uma VM (máquina virtual) (quando executado em um sistema de computador VM) ou um host (quando executado em um sistema de computador host).
ms.assetid: A3DB75BF-91C8-444E-B273-25DF8A5BFA7B
title: Classe Msvm_CompatibilityVector
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CompatibilityVector
- Msvm_CompatibilityVector.VectorId
- Msvm_CompatibilityVector.CompareOperation
- Msvm_CompatibilityVector.CompatibilityInfo
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 976e6b7bd9bf69e483b987da4d8055ffc102e89c67ed83bab6aa09c4e586b1ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531836"
---
# <a name="msvm_compatibilityvector-class"></a>\_Classe Msvm CompatibilityVector

Faz referência às informações de compatibilidade para uma VM (máquina virtual) (quando executado em um sistema de computador VM) ou um host (quando executado em um sistema de computador host).

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CompatibilityVector
{
  uint32 VectorId;
  uint32 CompareOperation;
  uint64 CompatibilityInfo;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ CompatibilityVector** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ CompatibilityVector** tem essas propriedades.

<dl> <dt>

**CompareOperation**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identifica a operação de comparação que retornará true se e somente se dois vetores forem compatíveis. Os dados da VM estão no lado esquerdo da comparação, e os dados do host estão no lado direito.

<dt>

<span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>

**Igual** (0)


</dt> <dd></dd> <dt>

<span id="Superset"></span><span id="superset"></span><span id="SUPERSET"></span>

**Superconjunto** (1)


</dt> <dd></dd> <dt>

<span id="Subset"></span><span id="subset"></span><span id="SUBSET"></span>

**Subconjunto** (2)


</dt> <dd></dd> <dt>

<span id="Disjoint"></span><span id="disjoint"></span><span id="DISJOINT"></span>

Não **contíguo** (3)


</dt> <dd></dd> <dt>

<span id="GreaterThan"></span><span id="greaterthan"></span><span id="GREATERTHAN"></span>

**GreaterThan** (4)


</dt> <dd></dd> <dt>

<span id="GreaterThanOrEqual"></span><span id="greaterthanorequal"></span><span id="GREATERTHANOREQUAL"></span>

**GreaterThanOrEqual** (5)


</dt> <dd></dd> <dt>

<span id="LessThan"></span><span id="lessthan"></span><span id="LESSTHAN"></span>

**LessThan** (6)


</dt> <dd></dd> <dt>

<span id="LessThanOrEqual"></span><span id="lessthanorequal"></span><span id="LESSTHANOREQUAL"></span>

**LessThanOrEqual** (7)


</dt> <dd></dd> <dt>

<span id="Multiple"></span><span id="multiple"></span><span id="MULTIPLE"></span>

**Múltiplo** (8)


</dt> <dd></dd> <dt>

<span id="Divisible"></span><span id="divisible"></span><span id="DIVISIBLE"></span>

**Divisível** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**CompatibilityInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Os dados de atributo de compatibilidade reais que são usados para comparação.

</dd> <dt>

**Vetorid**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identifica um vetor de compatibilidade que representa um atributo específico. Essa propriedade é usada para corresponder os vetores correspondentes entre um host e uma VM.

</dd> </dl>

## <a name="remarks"></a>Comentários

O método [**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) da classe [**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) retorna uma matriz de instâncias de **Msvm \_ CompatibilityVector** para o host (se executado no host) ou uma VM (se executado na VM). Cada entrada **Msvm \_ CompatibilityVector** na lista descreve um vetor de atributo de compatibilidade. Para que uma VM seja compatível com um host, todos os seus atributos de compatibilidade devem ser compatíveis com os atributos do host.

Cada **entrada \_ CompatibilityVector Msvm** tem estas propriedades:

<dl> <dt>

**Vetorid**
</dt> <dd>

Identifica exclusivamente o vetor de compatibilidade. Isso é usado para corresponder os vetores para comparar entre um host e uma VM.

</dd> <dt>

**CompareOperation**
</dt> <dd>

Identifica a operação de comparação que determina se os vetores são compatíveis.

</dd> <dt>

**CompatibilityInfo**
</dt> <dd>

Contém o atributo de compatibilidade real; Isso é efetivamente a carga de atributo (por exemplo, máscara de recurso de processador, tamanho de liberação de linha de cache, etc.)

</dd> </dl>

O conjunto de operações definido para **CompareOperation** envolve a comparação de inteiros básico e a lógica bit-a-bit. Isso permite que o conteúdo real de **CompatibilityInfo** permaneça opaco. O conjunto de operações inclui:



| CompareOperation | Descrição                                      | Comparação de pseudocódigo                |
|------------------|--------------------------------------------------|--------------------------------------|
| VmCcEqual        | VmAttr deve ser igual a HostAttr                       | If (VmAttr = = HostAttr)              |
| VmCcSuperSet     | VmAttr deve ser um superconjunto de HostAttr            | If (VmAttr & HostAttr) = = HostAttr) |
| VmCcSubSet       | VmAttr deve ser um subconjunto de HostAttr              | If (VmAttr & HostAttr) = = VmAttr)   |
| VmCcDisjointSet  | VmAttr deve ser um conjunto não contíguo de HostAttr      | If ((VmAttr & HostAttr) = = 0)        |
| VmCcGreater      | VmAttr deve ser maior que HostAttr             | If (VmAttr > HostAttr)            |
| VmCcGreaterEqual | VmAttr deve ser maior ou igual a HostAttr | If (VmAttr >= HostAttr)           |
| VmCcLess         | VmAttr deve ser menor que HostAttr                | If (VmAttr < HostAttr)            |
| VmCcLessEqual    | VmAttr deve ser menor ou igual a HostAttr    | If (VmAttr <= HostAttr)           |
| VmCcMultiple     | VmAttr deve ser um múltiplo de HostAttr            | If ((VmAttr% HostAttr) = = 0)        |
| VmCcDivisor      | VmAttr deve ser um divisor de HostAttr             | If ((HostAttr% VmAttr) = = 0)        |



 

O SCVMM precisa executar estas etapas para determinar se uma VM é compatível com um host.

**Para determinar se uma VM é compatível com um host**

1.  Iterar em todos os elementos **Msvm \_ CompatibilityVector** para a VM.
2.  Para cada elemento **Msvm \_ CompatibilityVector** , use a operação de compatibilidade especificada em **CompareOperation** para comparar o vetor de compatibilidade de hardware de VM s com o vetor de compatibilidade correspondente para o host.
3.  Se todos os elementos **Msvm \_ COMPATIBILITYVECTOR** da VM forem considerados compatíveis, a VM será compatível com o host (da perspectiva do recurso do processador).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ somente aplicativos da área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Somente aplicativos da área de trabalho R2\]<br/>                                                 |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




