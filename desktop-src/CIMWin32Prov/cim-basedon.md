---
description: A classe CIM BasedOn representa uma associação que descreve como as extensão de armazenamento podem ser \_ montadas de extensão de nível inferior.
ms.assetid: 82132012-5851-4be8-82db-edbdb50b70e5
ms.tgt_platform: multiple
title: CIM_BasedOn classe (Provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BasedOn
- CIM_BasedOn.Dependent
- CIM_BasedOn.Antecedent
- CIM_BasedOn.EndingAddress
- CIM_BasedOn.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0a6bdd4c61628c71dbcb58b7b1d177cf7e936f802165aa9beed0aa195aeef4a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119439256"
---
# <a name="cim_basedon-class-cimwin32-wmi-providers"></a>CIM_BasedOn classe (Provedores WMI CIMWin32)

A **classe CIM \_ BasedOn** representa uma associação que descreve como as extensão de armazenamento podem ser montadas de extensão de nível inferior. Por exemplo, as extensão físicas incluem as extensão de espaço protegida. Portanto, os conjuntos de volumes são montados de uma ou mais extensão de espaço físico ou protegido. A memória de cache pode ser definida independentemente e realizada em um elemento físico ou pode ser baseada em extensão de armazenamento volátil ou não volátil.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) modelo CIM DMTF são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{8502C53E-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_BasedOn : CIM_Dependency
{
  CIM_StorageExtent REF Dependent;
  CIM_StorageExtent REF Antecedent;
  uint64                EndingAddress;
  uint64                StartingAddress;
};
```

## <a name="members"></a>Membros

A **classe CIM \_ BasedOn** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe CIM \_ BasedOn** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ StorageExtent**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecessor")
</dt> </dl>

Um [**\_ StorageExtent cim**](cim-storageextent.md) que descreve a extensão de armazenamento de nível inferior.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ StorageExtent**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependente")
</dt> </dl>

Um [**\_ StorageExtent cim**](cim-storageextent.md) que descreve a extensão de armazenamento de nível superior.

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o final da extensão de alto nível no armazenamento de nível inferior. Essa propriedade é útil ao mapear as extensão não contíguas para um grupo de nível superior.

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o início da extensão de alto nível no armazenamento de nível inferior.

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ Cim BasedOn** é derivada da [**\_ Dependência CIM.**](cim-dependency.md)

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

[**Dependência cim \_**](cim-dependency.md)
</dt> </dl>

 

