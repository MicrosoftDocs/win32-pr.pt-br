---
title: Escolhendo o conteúdo para propriedades descritivas
description: Embora o conteúdo de algumas propriedades seja específico, o conteúdo de outras propriedades consiste em um texto descritivo que é deixado para o desenvolvedor do servidor a ser fornecido.
ms.assetid: 3f399451-e9c5-4901-9b6e-198aa0c2deab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b77860eaefeb4e371c69fdf6acd205c77d763c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641765"
---
# <a name="choosing-the-content-for-descriptive-properties"></a>Escolhendo o conteúdo para propriedades descritivas

Embora o conteúdo de algumas propriedades seja específico, o conteúdo de outras propriedades consiste em um texto descritivo que é deixado para o desenvolvedor do servidor a ser fornecido. Além disso, o tipo de informações para cada propriedade varia dependendo do objeto. A tabela a seguir fornece sugestões para escolher o conteúdo dessas propriedades descritivas.



| Propriedade                                        | Sugestão de conteúdo                                                                                                                                                                                                                                                    |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nomes**](name-property.md)                   | Um rótulo que descreve brevemente e identifica o objeto dentro de seu contêiner, como o texto em um botão de ação, o nome de um item de menu ou um rótulo exibido ao lado de um controle de edição.                                                                              |
| [**DefaultAction**](defaultaction-property.md) | A interação padrão com o objeto. A cadeia de caracteres retornada por essa propriedade é um único verbo, como "pressionar" para um botão da barra de ferramentas ou uma frase curta que começa com um verbo.                                                                               |
| [**Valor**](value-property.md)                 | As informações contidas no objeto, como o texto em um controle de edição ou o nome de arquivo de um link HTML. O conteúdo da propriedade [**Value**](value-property.md) pode ser alterado, enquanto o conteúdo da propriedade [**Name**](name-property.md) não é alterado. |
| [**Descrição**](description-property.md)     | Descreve a aparência do objeto.                                                                                                                                                                                                                                    |
| [**Ajuda**](help-property.md)                   | Informações de dica de ferramenta ou estilo de balão usadas para descrever o que o objeto faz ou como usá-lo.                                                                                                                                                                   |
| [**HelpTopic**](helptopic-property.md)         | Um identificador de contexto de um tópico do [WinHelp](/windows/win32/api/winuser/nf-winuser-winhelpa) que documenta o objeto.                                                                                                                                                 |



 

Use um dos valores de [função de objeto](object-roles.md) predefinidos para a [**função**](role-property.md) e a combinação apropriada de [constantes de estado de objeto](object-state-constants.md) para o [**estado**](state-property.md).

O conteúdo das propriedades de controles personalizados deve corresponder ao conteúdo das propriedades dos controles fornecidos pelo sistema que os controles personalizados emulam. Para obter informações sobre as propriedades com suporte pelos controles fornecidos pelo sistema, consulte [o apêndice A: referência de elementos da interface do usuário com suporte](appendix-a--supported-user-interface-elements-reference.md).

 

 