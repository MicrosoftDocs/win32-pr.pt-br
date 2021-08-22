---
description: A classe CIM ComputerSystemMappedIO representa uma associação entre um sistema de computador e suas portas de E/S mapeadas \_ em memória disponíveis.
ms.assetid: 5df9db36-67ad-4a94-a7db-150b58977af1
ms.tgt_platform: multiple
title: CIM_ComputerSystemMappedIO classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemMappedIO
- CIM_ComputerSystemMappedIO.GroupComponent
- CIM_ComputerSystemMappedIO.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bf81632bd380756e49cde1804f7e35d3115b8575460ce04772e8d153255d6777
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322036"
---
# <a name="cim_computersystemmappedio-class"></a>Classe CIM \_ ComputerSystemMappedIO

A **classe CIM \_ ComputerSystemMappedIO representa** uma associação entre um sistema de computador e suas portas de E/S mapeadas em memória disponíveis.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) modelo CIM DMTF são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{A2EFC897-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemMappedIO : CIM_ComputerSystemResource
{
  CIM_ComputerSystem REF GroupComponent;
  CIM_MemoryMappedIO REF PartComponent;
};
```

## <a name="members"></a>Membros

A **classe CIM \_ ComputerSystemMappedIO** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe CIM \_ ComputerSystemMappedIO** tem essas propriedades.

<dl> <dt>

**Groupcomponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ ComputerSystem**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)
</dt> </dl>

Um [**\_ ComputerSystem cim**](cim-computersystem.md) que descreve o sistema de computador mapeado para a porta de E/S.

Essa propriedade é herdada de [ **\_ ComputerSystemResource do CIM**](cim-computersystemresource.md)

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **Memória \_ CIMMappedIO**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Fraco**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Um [**Cim \_ MemoryMappedIO**](cim-memorymappedio.md) que descreve uma porta de E/S mapeada em memória do sistema de computador.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe CIM \_ ComputerSystemMappedIO** é derivada de [**CIM \_ ComputerSystemResource**](cim-computersystemresource.md).

O WMI não implementa essa classe.

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

[**CIM \_ ComputerSystemResource**](cim-computersystemresource.md)
</dt> </dl>

 

