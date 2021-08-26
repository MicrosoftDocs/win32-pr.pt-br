---
title: Escolhendo o conteúdo para propriedades descritivas
description: Embora o conteúdo de algumas propriedades seja específico, o conteúdo de outras propriedades consiste em texto descritivo que é deixado para o desenvolvedor do servidor fornecer.
ms.assetid: 3f399451-e9c5-4901-9b6e-198aa0c2deab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5215a6592d11272223654184340c4df8b299b88edb5b5f4addbd2c8d4712ab74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071846"
---
# <a name="choosing-the-content-for-descriptive-properties"></a>Escolhendo o conteúdo para propriedades descritivas

Embora o conteúdo de algumas propriedades seja específico, o conteúdo de outras propriedades consiste em texto descritivo que é deixado para o desenvolvedor do servidor fornecer. Além disso, o tipo de informações para cada propriedade varia dependendo do objeto . A tabela a seguir fornece sugestões para escolher o conteúdo dessas propriedades descritivas.



| Propriedade                                        | Sugestão de conteúdo                                                                                                                                                                                                                                                    |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nome**](name-property.md)                   | Um rótulo que descreve e identifica brevemente o objeto em seu contêiner, como o texto em um botão de push, o nome de um item de menu ou um rótulo exibido ao lado de um controle de edição.                                                                              |
| [**Defaultaction**](defaultaction-property.md) | A interação padrão com o objeto . A cadeia de caracteres retornada por essa propriedade é um único verbo, como "Pressionar" para um botão de barra de ferramentas ou uma frase curta que começa com um verbo.                                                                               |
| [**Valor**](value-property.md)                 | Informações contidas no objeto, como o texto em um controle de edição ou o nome de arquivo de um link HTML. O conteúdo da propriedade [**Value**](value-property.md) pode mudar, enquanto o conteúdo da [**propriedade Name**](name-property.md) não é altere. |
| [**Descrição**](description-property.md)     | Descreve a aparência do objeto.                                                                                                                                                                                                                                    |
| [**Ajuda**](help-property.md)                   | Informações de estilo de balão ou dica de ferramenta usadas para descrever o que o objeto faz ou como usá-lo.                                                                                                                                                                   |
| [**Helptopic**](helptopic-property.md)         | Um identificador de contexto de [um tópico winHelp](/windows/win32/api/winuser/nf-winuser-winhelpa) que documenta o objeto .                                                                                                                                                 |



 

Use um dos valores de função de [objeto](object-roles.md) predefinidos para [**a Função**](role-property.md) e a combinação apropriada de [constantes](object-state-constants.md) de estado do objeto para o [**Estado**](state-property.md).

O conteúdo das propriedades para controles personalizados deve corresponder ao conteúdo das propriedades para os controles fornecidos pelo sistema que os controles personalizados emular. Para obter informações sobre as propriedades com suporte pelos controles fornecidos pelo sistema, consulte Apêndice A: Referência de [elementos Interface do Usuário com suporte.](appendix-a--supported-user-interface-elements-reference.md)

 

 