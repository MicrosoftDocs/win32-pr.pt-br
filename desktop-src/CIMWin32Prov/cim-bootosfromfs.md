---
description: A \_ classe CIM BootOSFromFS associa o sistema operacional e os sistemas de arquivos dos quais o sistema operacional é carregado.
ms.assetid: c5697e9c-9031-4787-a03d-cf713c961cdf
ms.tgt_platform: multiple
title: Classe CIM_BootOSFromFS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootOSFromFS
- CIM_BootOSFromFS.Dependent
- CIM_BootOSFromFS.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 91247872045920eacf9d00664731effe48a8ce22cf14e3e1a4086bbaf4b92c5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119284536"
---
# <a name="cim_bootosfromfs-class"></a>\_Classe CIM BootOSFromFS

A classe **CIM \_ BootOSFromFS** associa o sistema operacional e os sistemas de arquivos dos quais o sistema operacional é carregado. A associação é muitos-para-muitos; um sistema operacional distribuído pode depender de vários sistemas de arquivos para serem carregados de forma correta e completa.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{5F5B101E-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_BootOSFromFS : CIM_Dependency
{
  CIM_OperatingSystem REF Dependent;
  CIM_FileSystem      REF Antecedent;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ BootOSFromFS** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ BootOSFromFS** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ sistema de arquivos CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

O sistema de arquivos do qual o sistema operacional é carregado.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: sistema **\_ operacional CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")
</dt> </dl>

O sistema operacional.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **CIM \_ BootOSFromFS** é derivada da [**\_ dependência CIM**](cim-dependency.md).

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

[**\_Dependência CIM**](cim-dependency.md)
</dt> </dl>

 

