---
description: O sistema de propriedades contém uma propriedade chamada System. Kind, que divide os itens em tipos de acordo com a extensão de nome de arquivo e quais usuários finais podem facilmente identificar com o.
ms.assetid: 1466b4c7-49ea-417a-ac94-7b45515ccb96
title: Usando nomes de tipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f358306deaeb04d4ea30b10b0665cdc8323b4d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296612"
---
# <a name="using-kind-names"></a>Usando nomes de tipos

O sistema de propriedades contém uma propriedade chamada `System.Kind` , que divide os itens em tipos de acordo com a extensão de nome de arquivo e quais usuários finais podem facilmente identificar com o.

Este tópico é organizado da seguinte maneira:

-   [Sobre a propriedade System. Kind](#about-the-systemkind-property)
-   [Tipo de hierarquia e registro de valor](#kind-value-hierarchy-and-registration)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="about-the-systemkind-property"></a>Sobre a propriedade System. Kind

O tipo foi introduzido no Windows Vista para expressar uma noção mais amigável do tipo de arquivo. A `System.Kind` Propriedade divide itens em tipos e fornece um nome de tipo que os usuários finais podem identificar, como documentos, música, imagens e assim por diante. Portanto, os nomes de espécie vêm para serem conhecidos como amigáveis para o usuário. Como a `System.Kind` propriedade é definida com o mesmo valor para itens do mesmo tipo de arquivo e associa itens que têm características semelhantes com uma propriedade comum, o sistema e o usuário podem agir no grupo como um todo. Por exemplo, a `System.Kind` propriedade pode ser usada para limitar uma pesquisa a itens de um tipo específico, exibir as propriedades mais relevantes para um item no modo de exibição de conteúdo ou agrupar itens semelhantes.

Como Kind é uma propriedade de cadeia de caracteres com vários valores, você pode ter um `audio;video` valor ou um `link;document` tipo. Um `System.Kind` valor é uma lista ordenada de valores de cadeia de caracteres. Em alguns casos, pode haver apenas um elemento nessa lista. Em outros casos, um item pode pertencer a mais de um tipo. Para obter um exemplo de um item que pertence a mais de um tipo, consulte o exemplo de chave do registro neste tópico. Os valores de cadeia de caracteres são de um conjunto predefinido de valores conhecidos. Os valores são comparados usando funções de comparação de cadeia de caracteres e não diferenciam maiúsculas de minúsculas. Essas cadeias de caracteres não estão localizadas.

Alguns nomes de tipo já estão associados a propriedades e padrões de layout. Por exemplo, itens associados a `Kind.Picture` e itens associados a `Kind.Document` Exibir propriedades diferentes mesmo quando estão na mesma exibição, devido às propriedades e padrões de layout que já estão associados a esses dois tipos de nomes. Cada tipo de item pode ser associado a um dos quatro padrões de layout exclusivos que definem o número de propriedades exibidas para cada item e seu layout. Para obter mais informações, consulte [exibição de conteúdo com base na associação de tipo de arquivo ou](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85))tipo.

## <a name="kind-value-hierarchy-and-registration"></a>Tipo de hierarquia e registro de valor

Um `Kind` valor deve representar um dos valores na lista a seguir.

```
Item
   Folder
   Program
   Game
   WebHistory
   Feed
   Document
   Link
   Movie
   Music
   RecordedTV
   Video
   Picture
   Communications
      Calendar
      Contact
      E-Mail
      Task
      Journal
      Note
      InstantMessage
```

Manipuladores de propriedade podem declarar sua `System.Kind` Propriedade estaticamente por meio do registro ou podem fornecer o valor dinamicamente por meio de seu código como faria com uma propriedade padrão.

Para definir estaticamente a `Kind` propriedade, uma entrada de valor **\_ sz do reg** é adicionada sob a chave do registro **KindMap** , conforme mostrado no exemplo a seguir.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  KindMap
                     .recipe = Document
                     .ccc = Contact; Communications
```

Observe que o `Kind` pode ser um único valor ou vários valores em uma cadeia de caracteres delimitada por ponto e vírgula. Ao fornecer vários valores, o valor mais específico `Kind` é listado primeiro com o menos específico a seguir. No exemplo, o contato é nomeado primeiro porque é hierarquicamente mais específico do que as comunicações. O **Item** de valor é assumido e não deve ser fornecido explicitamente.

## <a name="additional-resources"></a>Recursos adicionais

-   Para obter a documentação de referência sobre propriedades, consulte [System. Kind](./props-system-kind.md) e [System. KindText](./props-system-kindtext.md).
-   Para obter mais informações sobre como criar novos ou usar tipos de arquivo existentes, consulte [tipos de arquivo](../shell/fa-file-types.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Noções básicas sobre manipuladores de propriedade](./building-property-handlers-properties.md)
</dt> <dt>

[Usando listas de propriedades](./building-property-handlers-property-lists.md)
</dt> <dt>

[Inicializando manipuladores de propriedade](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registrando e distribuindo manipuladores de propriedade](./prophand-reg-dist.md)
</dt> <dt>

[Práticas recomendadas e perguntas frequentes do manipulador de propriedades](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
