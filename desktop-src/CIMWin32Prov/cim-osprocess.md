---
description: A \_ classe CIM OSProcess associa o sistema operacional e um ou mais processos em execução no contexto do sistema operacional.
ms.assetid: 59d52b29-9d97-464f-bbbc-4191305df8c7
ms.tgt_platform: multiple
title: Classe CIM_OSProcess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OSProcess
- CIM_OSProcess.PartComponent
- CIM_OSProcess.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 62cb209f37a89fd0d2456c2f9760060a69af8cbb45d2dd15b608a1201409c509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921306"
---
# <a name="cim_osprocess-class"></a>\_Classe CIM OSProcess

A classe **CIM \_ OSProcess** associa o sistema operacional e um ou mais processos em execução no contexto do sistema operacional.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{A361A7AE-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_OSProcess : CIM_Component
{
  CIM_Process         REF PartComponent;
  CIM_OperatingSystem REF GroupComponent;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ OSProcess** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ OSProcess** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: sistema **\_ operacional CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Um [**\_ OperatingSystem CIM**](cim-operatingsystem.md) que descreve o sistema operacional.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ processo CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**fraca**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Um [**\_ processo CIM**](cim-process.md) que descreve o processo em execução no contexto do sistema operacional

</dd> </dl>

## <a name="remarks"></a>Comentários

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

[**\_Componente CIM**](cim-component.md)
</dt> </dl>

 

