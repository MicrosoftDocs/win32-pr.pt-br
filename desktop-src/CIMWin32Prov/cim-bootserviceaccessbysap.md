---
description: A \_ classe CIM BootServiceAccessBySAP associa um serviço de inicialização e seus pontos de acesso.
ms.assetid: 993469dd-fb9c-4d21-99e0-03c4b19eb7fd
ms.tgt_platform: multiple
title: Classe CIM_BootServiceAccessBySAP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootServiceAccessBySAP
- CIM_BootServiceAccessBySAP.Dependent
- CIM_BootServiceAccessBySAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90548be52defbcf3419d6c7defc21395da5cfbfe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646429"
---
# <a name="cim_bootserviceaccessbysap-class"></a>\_Classe CIM BootServiceAccessBySAP

A classe **CIM \_ BootServiceAccessBySAP** associa um serviço de inicialização e seus pontos de acesso.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[UUID("{6EDF1DD2-DB35-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BootServiceAccessBySAP : CIM_ServiceAccessBySAP
{
  CIM_BootSAP     REF Dependent;
  CIM_BootService REF Antecedent;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ BootServiceAccessBySAP** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ BootServiceAccessBySAP** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ DS**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Um [**\_ DS CIM**](cim-bootservice.md) que descreve o serviço de inicialização.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ BootSAP**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")
</dt> </dl>

Um [**\_ BootSAP CIM**](cim-bootsap.md) que descreve um ponto de acesso para o serviço de inicialização.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **CIM \_ BootServiceAccessBySAP** é derivada de [**\_ ServiceAccessBySAP CIM**](cim-serviceaccessbysap.md).

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

[**\_SERVICEACCESSBYSAP CIM**](cim-serviceaccessbysap.md)
</dt> </dl>

 

