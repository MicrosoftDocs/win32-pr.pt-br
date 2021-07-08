---
description: O sistema de propriedades contém uma propriedade chamada System.Kind, que divide itens em tipos de acordo com a extensão de nome de arquivo e com quais usuários finais podem se identificar facilmente.
ms.assetid: 1466b4c7-49ea-417a-ac94-7b45515ccb96
title: Usando nomes de tipo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dca36d7c1de587efd8d96f0c18aaca9457721714
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481871"
---
# <a name="using-kind-names"></a>Usando nomes de tipo

O sistema de propriedades contém uma propriedade chamada , que divide os itens em tipos de acordo com a extensão de nome de arquivo e com a qual os usuários finais `System.Kind` podem se identificar facilmente.

Este tópico é organizado da seguinte forma:

-   [Sobre a propriedade System.Kind](#about-the-systemkind-property)
-   [Hierarquia e registro de valor de tipo](#kind-value-hierarchy-and-registration)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="about-the-systemkind-property"></a>Sobre a propriedade System.Kind

O tipo foi introduzido no Windows Vista para expressar uma noção mais amigável de tipo de arquivo. A propriedade divide itens em tipos e fornece um Nome de tipo com o qual os usuários finais podem se identificar, como `System.Kind` Documentos, Música, Imagens e assim por diante. Portanto, os Nomes de tipo vêm a ser conhecidos como amigáveis. Como a propriedade é definida com o mesmo valor para itens do mesmo tipo de arquivo e associa itens que têm características semelhantes a uma propriedade comum, o sistema e o usuário podem agir no grupo como `System.Kind` um todo. Por exemplo, a propriedade pode ser usada para limitar uma pesquisa a itens de um tipo específico, exibir as propriedades mais relevantes para um item na exibição Conteúdo ou agrupar itens `System.Kind` semelhantes.

Como Kind é uma propriedade de cadeia de caracteres de vários valores, você pode ter `audio;video` um valor `link;document` ou Kind. Um `System.Kind` valor é uma lista ordenada de valores de cadeia de caracteres. Em alguns casos, pode haver apenas um elemento nessa lista. Em outros casos, um item pode pertencer a mais de um Tipo. Para obter um exemplo de um item que pertence a mais de um Kind, consulte o exemplo de chave do Registro neste tópico. Os valores de cadeia de caracteres são de um conjunto predefinido de valores conhecidos. Os valores são comparados usando funções de comparação de cadeia de caracteres não sensíveis a maiúsculas e minúsculas e sem valor de localidade. Essas cadeias de caracteres não são localizadas.

Alguns nomes kind já estão associados a propriedades e padrões de layout. Por exemplo, itens associados a e itens associados a exibem propriedades diferentes mesmo quando estão na mesma exibição, devido às propriedades e padrões de layout que já estão associados a esses dois `Kind.Picture` `Kind.Document` Nomes de tipo. Cada tipo de item pode ser associado a um dos quatro padrões de layout exclusivos que define o número de propriedades exibidas para cada item e seu layout. Para obter mais informações, consulte [Exibição de conteúdo com base no tipo de arquivo ou associação de tipo](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85)).

## <a name="kind-value-hierarchy-and-registration"></a>Hierarquia e registro de valor de tipo

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

Os manipuladores de propriedades podem declarar sua propriedade estaticamente por meio do Registro ou podem fornecer o valor dinamicamente por meio de seu código, como faria `System.Kind` com uma propriedade padrão.

Para definir estaticamente a propriedade , uma entrada de valor REG SZ é adicionada sob a chave do Registro `Kind` **KindMap,** conforme mostrado no exemplo a **\_** seguir.

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

Observe que o `Kind` pode ser um único valor ou vários valores em uma cadeia de caracteres delimitada por ponto e vírgula. Ao fornecer vários valores, o valor mais `Kind` específico é listado primeiro com o valor menos específico a seguir. No exemplo, Contact é nomeado primeiro porque é hierarquicamente mais específico do que Communications. O valor **Item** é assumido e não deve ser fornecido explicitamente.

## <a name="additional-resources"></a>Recursos adicionais

-   Para a documentação de referência sobre propriedades, [consulte System.Kind](./props-system-kind.md) e [System.KindText](./props-system-kindtext.md).
-   Para obter mais informações sobre como criar novos ou usar tipos de arquivo existentes, consulte [Tipos de arquivo](../shell/fa-file-types.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Noções básicas sobre manipuladores de propriedade](./building-property-handlers-properties.md)
</dt> <dt>

[Usando listas de propriedades](./building-property-handlers-property-lists.md)
</dt> <dt>

[Inicializando manipuladores de propriedades](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registrando e distribuindo manipuladores de propriedade](./prophand-reg-dist.md)
</dt> <dt>

[Práticas recomendadas e perguntas frequentes do manipulador de propriedades](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
