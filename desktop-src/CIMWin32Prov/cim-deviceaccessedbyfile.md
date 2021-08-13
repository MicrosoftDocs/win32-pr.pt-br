---
description: A classe de associação DeviceAccessedByFile cim especifica o dispositivo lógico acessado usando a \_ classe DeviceFile CIM \_ referenciada.
ms.assetid: 8ba44f40-8b84-4f5c-b719-aded10877654
ms.tgt_platform: multiple
title: CIM_DeviceAccessedByFile classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceAccessedByFile
- CIM_DeviceAccessedByFile.Dependent
- CIM_DeviceAccessedByFile.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 24526d7743b1f4939f2240c751f7da2bfecfacfe13d2ddf3cbc7fdd73c1d260e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119321636"
---
# <a name="cim_deviceaccessedbyfile-class"></a>Classe \_ DeviceAccessedByFile cim

A **classe de associação \_ DeviceAccessedByFile cim** especifica o dispositivo lógico acessado usando a classe [**DeviceFile CIM \_ referenciada.**](cim-devicefile.md)

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) modelo CIM DMTF são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{05D1FFF2-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceAccessedByFile : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_DeviceFile    REF Antecedent;
};
```

## <a name="members"></a>Membros

A **classe \_ DeviceAccessedByFile cim** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ DeviceAccessedByFile cim** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ DeviceFile CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecessor")
</dt> </dl>

Um [**\_ DeviceFile CIM**](cim-devicefile.md) que descreve o arquivo de dispositivo.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ LogicalDevice**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")
</dt> </dl>

Um [**\_ LogicalDevice cim**](cim-logicaldevice.md) que descreve o dispositivo que é acessado usando o arquivo de dispositivo.

</dd> </dl>

## <a name="remarks"></a>Comentários

O WMI não implementa essa classe.

A **classe \_ DeviceAccessedByFile CIM** é derivada da [**\_ Dependência CIM.**](cim-dependency.md)

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

 

