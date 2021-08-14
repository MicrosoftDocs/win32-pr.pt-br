---
description: A \_ classe WMI de associação DependentService do Win32 relaciona dois serviços base interdependentes.
ms.assetid: ba21fce3-f8f9-4886-b09d-a9e830376364
ms.tgt_platform: multiple
title: Classe Win32_DependentService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DependentService
- Win32_DependentService.TypeOfDependency
- Win32_DependentService.Antecedent
- Win32_DependentService.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 391db343723af04536ac970e1d8beb0d7c7fb4bb1fe47ac15846a877999f4e6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118417619"
---
# <a name="win32_dependentservice-class"></a>\_Classe Win32 DependentService

A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ DependentService do Win32** relaciona dois serviços base interdependentes.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FA-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DependentService : CIM_ServiceServiceDependency
{
  uint16                TypeOfDependency;
  Win32_BaseService REF Antecedent;
  Win32_BaseService REF Dependent;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ DependentService** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ DependentService** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ BaseService**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ BaseService")
</dt> </dl>

Um [**\_ BaseService Win32**](win32-baseservice.md) que representa o serviço base de acordo com a propriedade **dependent** dessa classe.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ BaseService**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ BaseService")
</dt> </dl>

Um [**\_ BaseService Win32**](win32-baseservice.md) que representa o serviço base que é dependente da propriedade **Antecedent** dessa classe.

</dd> <dt>

**TypeOfDependency**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Natureza da dependência entre serviços. Essa propriedade indica que o serviço associado deve ter sido concluído, deve ser iniciado ou não deve ser iniciado para que o serviço funcione.

Essa propriedade é herdada do [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>

<span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>O **serviço deve ter sido concluído** (2)


</dt> <dd>

O serviço deve ter sido concluído.

</dd> <dt>

<span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>

<span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>O **serviço deve ser iniciado** (3)


</dt> <dd>

O serviço deve ser iniciado.

</dd> <dt>

<span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>

<span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>O **serviço não deve ser iniciado** (4)


</dt> <dd>

O serviço não deve ser iniciado.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ DependentService** é derivada de [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md).

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

[**\_SERVICESERVICEDEPENDENCY CIM**](cim-serviceservicedependency.md)
</dt> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

