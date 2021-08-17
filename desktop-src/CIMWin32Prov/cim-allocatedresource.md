---
description: A classe CIM AllocatedResource representa uma associação entre dispositivos lógicos e recursos do sistema e indica que o recurso \_ é atribuído ao dispositivo.
ms.assetid: e1702635-32f5-4280-8c02-3940fd858106
ms.tgt_platform: multiple
title: CIM_AllocatedResource classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AllocatedResource
- CIM_AllocatedResource.Dependent
- CIM_AllocatedResource.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2caf51e4b6a76693a64253e1046ea74c6ec19b8f5895618419aa693a10260f56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322696"
---
# <a name="cim_allocatedresource-class"></a>Classe CIM \_ AllocatedResource

A **classe CIM \_ AllocatedResource** representa uma associação entre dispositivos lógicos e recursos do sistema e indica que o recurso é atribuído ao dispositivo.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) modelo CIM DMTF são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{8502C579-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_AllocatedResource : CIM_Dependency
{
  CIM_LogicalDevice  REF Dependent;
  CIM_SystemResource REF Antecedent;
};
```

## <a name="members"></a>Membros

A **classe CIM \_ AllocatedResource** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe CIM \_ AllocatedResource** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ SystemResource**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecessor")
</dt> </dl>

Um [**\_ SystemResource cim**](cim-systemresource.md) que descreve o recurso.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ LogicalDevice**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependente")
</dt> </dl>

Um [**\_ LogicalDevice cim**](cim-logicaldevice.md) que contém o dispositivo lógico ao qual o recurso é atribuído.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe CIM \_ AllocatedResource** é derivada da [**\_ Dependência CIM.**](cim-dependency.md)

O WMI não implementa essa classe. Para obter mais informações sobre classes derivadas de **CIM \_ AllocatedResource**, consulte [Classes Win32](win32-provider.md).

Esta documentação é derivada das descrições da classe CIM publicadas pelo DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, estar em conformidade com os padrões de documentação do SDK da Microsoft ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Dependência cim \_**](cim-dependency.md)
</dt> </dl>

 

