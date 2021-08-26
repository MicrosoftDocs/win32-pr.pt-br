---
description: A \_ classe CIM HostedService representa uma associação entre um serviço e o sistema no qual a funcionalidade reside.
ms.assetid: 23bb385d-dd22-4126-aea9-d2f22527223e
ms.tgt_platform: multiple
title: Classe CIM_HostedService (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedService
- CIM_HostedService.Dependent
- CIM_HostedService.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7e70f7dea8fe6f5be0da7d76b37cf99ba4dcc7397c09cf27b542129232212286
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921596"
---
# <a name="cim_hostedservice-class-cimwin32-wmi-providers"></a>Classe CIM_HostedService (provedores WMI CIMWin32)

A classe **CIM \_ HostedService** representa uma associação entre um serviço e o sistema no qual a funcionalidade reside. Um sistema pode hospedar muitos serviços, o que adia para o sistema de hospedagem. O modelo não representa serviços hospedados em vários sistemas.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{83B2A7AA-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedService : CIM_Dependency
{
  CIM_Service REF Dependent;
  CIM_System  REF Antecedent;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ HostedService** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ HostedService** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ sistema CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Um [**\_ sistema CIM**](cim-system.md) que descreve o sistema de hospedagem.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ serviço CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**fraco**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Um [**\_ serviço CIM**](cim-service.md) que descreve o serviço hospedado no sistema.

</dd> </dl>

## <a name="remarks"></a>Comentários

**CIM \_ O HostedService** é derivado [**da \_ dependência CIM**](cim-dependency.md).

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

 

