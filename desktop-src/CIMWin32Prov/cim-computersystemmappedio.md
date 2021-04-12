---
description: A \_ classe CIM ComputerSystemMappedIO representa uma associação entre um sistema de computador e suas portas de e/s mapeadas de memória disponíveis.
ms.assetid: 5df9db36-67ad-4a94-a7db-150b58977af1
ms.tgt_platform: multiple
title: Classe CIM_ComputerSystemMappedIO
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
ms.openlocfilehash: ce7d00950038c7d94f97f9a6938b9190846f6ff0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089349"
---
# <a name="cim_computersystemmappedio-class"></a>\_Classe CIM ComputerSystemMappedIO

A classe **CIM \_ ComputerSystemMappedIO** representa uma associação entre um sistema de computador e suas portas de e/s mapeadas de memória disponíveis.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

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

A classe **CIM \_ ComputerSystemMappedIO** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ ComputerSystemMappedIO** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ sistema de ComputerSystem CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)
</dt> </dl>

Um [**computador \_ CIM**](cim-computersystem.md) que descreve o sistema de computadores mapeado para a porta de e/s.

Esta propriedade é herdada do [ **CIM \_ ComputerSystemResource**](cim-computersystemresource.md)

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ MemoryMappedIO**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**fraca**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Um [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md) que descreve uma porta de e/s mapeada da memória do sistema de computador.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **CIM \_ ComputerSystemMappedIO** é derivada de [**\_ ComputerSystemResource CIM**](cim-computersystemresource.md).

O WMI não implementa essa classe.

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_COMPUTERSYSTEMRESOURCE CIM**](cim-computersystemresource.md)
</dt> </dl>

 

