---
description: O CIM é um modelo de dados orientado a objeto e extensível que contém informações sobre diferentes partes de uma empresa.
ms.assetid: 3e619cb7-18a9-40ff-82fe-c10eb5090a93
ms.tgt_platform: multiple
title: Modelo CIM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53e4e2dc06e03a1f19b5b47ba0b94d7a866a5e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011445"
---
# <a name="common-information-model"></a>Modelo CIM

O CIM é um modelo de dados orientado a objeto e extensível que contém informações sobre diferentes partes de uma empresa. O [CIM](https://www.dmtf.org/standards/cim) é um padrão de plataforma cruzada mantido pela[DMTF](https://www.dmtf.org/)(Distributed Management Task Force). Por meio da WMI, um desenvolvedor pode usar o CIM para criar classes que representam discos rígidos, aplicativos, roteadores de rede ou, até mesmo, tecnologias definidas pelo usuário, como um ar condicionado conectado em rede. Ao exibir e fazer alterações em uma classe do CIM, um gerente pode controlar diferentes aspectos da empresa. Por exemplo, um gerente poderá consultar uma instância de classe do CIM que representa uma estação de trabalho desktop. Em seguida, o gerente poderá executar um script para modificar a instância da estação de trabalho do CIM. A WMI converterá qualquer alteração na instância da classe do CIM da estação de trabalho em uma alteração na estação de trabalho real.

O CIM é um modelo de programação independente de linguagem que usa técnicas orientadas a objeto para descrever uma empresa. Usando três níveis de herança pai/filho, o CIM pode descrever aspectos gerais e específicos de uma empresa. O CIM também usa uma técnica chamada "Association" para vincular diferentes partes do modelo empresarial e usa esquemas para distinguir diferentes ambientes de gerenciamento.

O CIM foi projetado para apresentar uma exibição consistente de objetos lógicos e físicos em um ambiente de gerenciamento. O CIM representa objetos gerenciados usando uma construção orientada a objeto chamada "Class". Como uma classe C++ ou COM, uma classe CIM pode incluir propriedades para descrever os dados e métodos para descrever o comportamento. Como um conjunto de classes COM, o CIM não está vinculado a nenhuma plataforma. No entanto, o WMI inclui uma extensão para o CIM que descreve as plataformas do sistema operacional Microsoft Windows.

O CIM define três níveis de classes:

-   Core

    Classes de núcleo representam objetos gerenciados que se aplicam a todas as áreas de gerenciamento. Essas classes fornecem um vocabulário básico para analisar e descrever sistemas gerenciados. As classes [**\_ \_ Parameters**](--parameters.md) e [**\_ \_ SystemSecurity**](--systemsecurity.md) são exemplos de classes de núcleo.

-   Comum

    Classes comuns representam objetos gerenciados que se aplicam a áreas de gerenciamento específicas. No entanto, as classes comuns são independentes de uma implementação ou tecnologia específica. As classes comuns são uma extensão das classes principais. A classe [**CIM \_ UnitaryComputerSystem**](/windows/desktop/CIMWin32Prov/cim-unitarycomputersystem) é um exemplo de uma classe comum.

-   Estendido

    Classes estendidas representam objetos gerenciados que são adições específicas de tecnologia às classes comuns. Uma classe estendida normalmente se aplica a uma plataforma específica, como UNIX ou o ambiente Microsoft Win32. A classe [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) é um exemplo de uma classe estendida.

Um desenvolvedor pode derivar uma classe de outra classe. Uma classe derivada representa um caso especial da classe pai e herda todas as propriedades e métodos do pai. Por exemplo, [**o \_ sistema de ComputerSystem do Win32**](/windows/desktop/CIMWin32Prov/win32-computersystem) herda do [**CIM \_ UnitaryComputerSystem**](/windows/desktop/CIMWin32Prov/cim-unitarycomputersystem). As relações de herança podem ser determinadas usando a **\_ \_ derivação** de propriedades do sistema, **\_ \_ dinastia** e **\_ \_ superclasse**. A propriedade do sistema de **\_ \_ derivação** é uma matriz de cadeias de caracteres que lista toda a cadeia de herança até e incluindo a classe raiz, que também está incluída no **\_ \_ dinastia**. A propriedade sistema de **\_ \_ superclasse** mostra o pai imediato da classe atual.

O WMI também oferece suporte a associações. Uma associação é uma relação entre duas ou mais classes WMI diferentes. Por exemplo, uma estação de trabalho em execução geralmente tem um processador. A classe de associação WMI [Win32 \_ ComputerSystemProcessor](/windows/desktop/CIMWin32Prov/win32-computersystemprocessor) associa a estação de trabalho [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) com o [**\_ processador**](/windows/desktop/CIMWin32Prov/win32-processor)de classe de processador Win32. No entanto, uma classe de associação não precisa vincular duas classes dependentes juntas. Na verdade, a principal finalidade de uma classe de associação é mostrar as relações entre as classes que não são necessariamente dependentes umas das outras. Para obter mais informações, consulte [declarando uma classe de associação](declaring-an-association-class.md).

Por fim, o WMI dá suporte ao conceito de esquemas. No contexto do WMI, um esquema é um grupo de classes que descreve um ambiente de gerenciamento específico. O SDK (Software Development Kit) do Microsoft Windows usa dois esquemas: o esquema CIM e o esquema Win32. Os nomes de classe de esquema CIM começam com [CIM \_](cimclas.md)e os nomes de classe de esquema Win32 começam com o [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-provider). O esquema CIM contém as definições para as classes básicas e comuns, enquanto o esquema Win32 contém as definições para as classes estendidas que são comuns ao ambiente do Win32. No entanto, um fornecedor terceirizado pode criar seus próprios esquemas para descrever os requisitos específicos do fornecedor. Como os esquemas são projetados para ser infinitamente extensíveis, um desenvolvedor sempre pode adicionar novas classes para descrever novos objetos gerenciados em um ambiente existente. Para simplificar, no entanto, a maioria dos fornecedores opta por criar esquemas que herdam propriedades dos esquemas CIM ou Win32.

 

 
