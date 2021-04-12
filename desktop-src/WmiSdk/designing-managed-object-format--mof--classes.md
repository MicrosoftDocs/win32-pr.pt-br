---
description: Um provedor WMI consiste em um arquivo formato MOF (MOF) e um arquivo DLL. O arquivo MOF define as classes para as quais a implementação do provedor fornece dados.
ms.assetid: 20ef6b88-2aaa-4e86-bc4a-bebc34069672
ms.tgt_platform: multiple
title: Criando classes formato MOF (MOF)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 201f8c45f7a247fbca5695baa6dd440fc5dc323f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170389"
---
# <a name="designing-managed-object-format-mof-classes"></a>Criando classes formato MOF (MOF)

Um [*provedor WMI*](gloss-p.md) consiste em um arquivo formato MOF (MOF) e um arquivo dll. O arquivo MOF define as classes para as quais a implementação do provedor fornece dados.

As definições de classe do MOF são compiladas pelo utilitário [**Mofcomp**](mofcomp.md) e armazenadas no [*repositório WMI*](gloss-w.md), também conhecido como repositório de modelo CIM (CIM). Uma maneira menos comum de criar classes é por meio dos métodos da [API com para o WMI](com-api-for-wmi.md).

> [!Note]  
> Para garantir que todas as definições de classe WMI para objetos gerenciados sejam restauradas no [*repositório WMI*](gloss-w.md) se o WMI tiver uma falha e reiniciar, use a instrução de pré-processador de [**\# AutoRecuperação pragma**](pragma-autorecover.md) em seu arquivo MOF.

 

As seções a seguir são discutidas neste tópico:

-   [Definindo os objetos a serem gerenciados](#defining-the-objects-to-manage)
-   [Definindo propriedades ou métodos](#defining-properties-or-methods)
-   [Relacionando objetos entre si](#relating-objects-to-each-other)
-   [Tópicos relacionados](#related-topics)

## <a name="defining-the-objects-to-manage"></a>Definindo os objetos a serem gerenciados

Depois de identificar a parte de sua empresa a ser gerenciada, defina os objetos a serem gerenciados. A definição deve incluir os dados necessários e permitir que você implemente as regras de negócios relevantes com precisão. Você pode definir objetos em um nível granular, mas é melhor decidir entre o nível de detalhe contido na definição e a necessidade de fornecer detalhes suficientes para ser útil. Os atalhos no início do processo podem economizar tempo, mas podem causar mais trabalho no futuro.

O tutorial do CIM no site da DMTF (Distributed Management Task Force) contém informações excelentes sobre o processo de design. Para obter mais informações, consulte [www.dmtf.org](https://www.dmtf.org/).

Considere os seguintes fatores ao desenvolver e implementar um design de esquema:

-   Qualificadores

    Os qualificadores fornecem informações sobre como descrever classes, objetos, propriedades, métodos e parâmetros; e eles são aplicados às definições de classe e propriedade. No código MOF, os qualificadores são colocados entre colchetes e podem incluir \[ chave \] ou \[ Associação \] . Para obter mais informações, consulte [adicionando um qualificador](adding-a-qualifier.md) e [qualificadores WMI](wmi-qualifiers.md).

-   Namespace

    Um namespace é uma unidade lógica para agrupar classes e objetos e controlar o escopo e a visibilidade. Normalmente, um namespace contém um conjunto de classes e objetos que representam objetos gerenciados em um ambiente específico. Para obter mais informações, consulte [Criando hierarquias no WMI](creating-hierarchies-within-wmi.md).

-   Objeto

    Um objeto modelado pode ser um elemento físico ou lógico do esquema. Por exemplo, você pode modelar uma unidade de disco físico, como uma unidade de disco rígido, ou um disco lógico que possa ser uma partição em um disco físico. Um design que usa uma classe para modelar uma unidade de disco físico e, em seguida, estende essa classe para modelar um disco lógico é mais extensível do que uma que tenta criar uma classe separada para cada tipo de disco.

-   Dados

    Os dados podem ser dinâmicos ou estáticos. Se os dados forem dinâmicos, você deverá criar um provedor de classes para ele.

    Para permitir que o usuário modifique dados, você deve determinar se deseja ou não que uma propriedade seja diretamente gravável ou modificável usando um método chamado pelo usuário.

## <a name="defining-properties-or-methods"></a>Definindo propriedades ou métodos

Em geral, uma propriedade de classe WMI é semelhante a uma propriedade em uma classe C++. Se as únicas ações que seu código implementa para a parte dos dados são obter o valor ou definir o valor, os dados devem ser definidos como uma propriedade da classe WMI.

Um método WMI geralmente executa uma ação que altera o estado de um objeto gerenciado. Por exemplo, se a ação for habilitar ou desabilitar a operação de um objeto de hardware, um método provavelmente será preferível a criar uma propriedade de leitura/gravação. Você também pode optar por criar uma propriedade que exibe o estado do hardware.

Ao criar uma classe ou uma instância, você pode incluir comentários. Use essa técnica para documentar sua classe ou explicar suas técnicas de programação. Para obter mais informações, consulte [criando um comentário](creating-a-comment.md). Além disso, você pode adicionar dados para qualificar a finalidade de um objeto de dados. Para obter mais informações, consulte [adicionando um qualificador](adding-a-qualifier.md).

## <a name="relating-objects-to-each-other"></a>Relacionando objetos entre si

Há duas maneiras de relacionar objetos entre si: Criando objetos separados e um objeto de associação que os relaciona ou inserindo um objeto no outro. O CIM não dá suporte a objetos incorporados, portanto, para ser compatível com o CIM, você deve usar o primeiro método. No entanto, o WMI dá suporte a objetos inseridos, portanto, use qualquer um dos métodos para representar uma relação entre objetos. Você pode encontrar exemplos de objetos inseridos nas [classes do Win32](/windows/desktop/CIMWin32Prov/win32-provider). Por exemplo, o [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) tem o objeto inserido [**Win32 \_ Ace**](/previous-versions/windows/desktop/secrcw32prov/win32-ace), que tem outro objeto incorporado, o [**\_ confiança do Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee).

Considere o seguinte ao decidir como representar relações entre objetos:

-   Se uma instância for útil por si mesma, uma associação funcionará melhor. Por exemplo, [**Win32 \_ process**](/windows/desktop/CIMWin32Prov/win32-process) e [**Win32 \_ USERACCOUNT**](/windows/desktop/CIMWin32Prov/win32-useraccount). Para obter mais informações, consulte [declarando uma classe de associação](declaring-an-association-class.md).
-   Se uma instância não existir fora do objeto pai, um objeto incorporado funcionará melhor. Por exemplo, [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) e [**Win32 \_ Ace**](/previous-versions/windows/desktop/secrcw32prov/win32-ace). Para obter mais informações, consulte [inserindo objetos em uma classe](embedded-objects.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvendo um provedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Fornecendo dados ao WMI](providing-data-to-wmi.md)
</dt> <dt>

[Tipos de dados MOF](mof-data-types.md)
</dt> </dl>

 

 
