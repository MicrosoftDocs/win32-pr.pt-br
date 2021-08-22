---
description: Contém um resumo de informações sobre o sistema de computador virtual especificado.
ms.assetid: ab31d5db-a8d3-47bc-a024-0f4c4b93a34b
title: Msvm_ComputerSystemSummaryInformation classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystemSummaryInformation
- Msvm_ComputerSystemSummaryInformation.Antecedent
- Msvm_ComputerSystemSummaryInformation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 78ac2b89336a415bedd23e0ca4ecd6589abdefbf75a54900d716c78152d34d4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531756"
---
# <a name="msvm_computersystemsummaryinformation-class"></a>Classe Msvm \_ ComputerSystemSummaryInformation

Contém um resumo de informações sobre o sistema de computador virtual especificado.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Association, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ComputerSystemSummaryInformation : CIM_ElementView
{
  CIM_ComputerSystem          REF Antecedent;
  Msvm_SummaryInformationBase REF Dependent;
};
```

## <a name="members"></a>Membros

A **classe Msvm \_ ComputerSystemSummaryInformation** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ ComputerSystemSummaryInformation** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ ComputerSystem**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Chave**](/windows/desktop/WmiSdk/key-qualifier), [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecessor")
</dt> </dl>

Um [**objeto \_ COMPUTERSystem cim**](cim-computersystem.md) que é uma instância na representação normalizada do recurso gerenciado.

> [!Note]
>
> Tipo de dados atualizado do [**Msvm \_ ComputerSystem**](msvm-computersystem.md) Windows 10, versão 1703.

 

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Msvm \_ SummaryInformationBase**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Chave**](/windows/desktop/WmiSdk/key-qualifier), [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependente")
</dt> </dl>

Uma instância de [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) que representa uma exibição des normalizada ou agregada do recurso gerenciado representado pelo [**Msvm \_ ComputerSystem**](msvm-computersystem.md) referenciado pela propriedade Antecedent.

> [!Note]
>
> Datatype atualizado de [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) no Windows 10, versão 1703.

 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento \_ CIMView**](cim-elementview.md)
</dt> </dl>

 

