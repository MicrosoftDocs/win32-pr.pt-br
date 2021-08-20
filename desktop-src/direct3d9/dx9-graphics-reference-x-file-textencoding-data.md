---
description: Os objetos de dados contêm os dados reais ou uma referência a esses dados. Cada objeto de dados tem um modelo correspondente que especifica o tipo de dados. As seções a seguir discutem a forma e as partes dos objetos de dados.
ms.assetid: 61dbe241-2658-4dd0-af89-3db204b56fad
title: Dados (formato de arquivo X, codificação de texto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0acd4222e2878b882b8777e3ba22e28f2d213fb5f3550686baf29b4ed6719e5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730197"
---
# <a name="data-x-file-format-text-encoding"></a>Dados (formato de arquivo X, codificação de texto)

Os objetos de dados contêm os dados reais ou uma referência a esses dados. Cada objeto de dados tem um modelo correspondente que especifica o tipo de dados. As seções a seguir discutem a forma e as partes dos objetos de dados.

## <a name="form-identifier-and-name"></a>Formulário, Identificador e Nome

Os objetos de dados têm o formulário a seguir.


```
        <Identifier> [name] { [<UUID>]
    <member 1>;
...
    <member n>;
}
```



O identificador é primitivo e deve corresponder a um tipo de dados ou primitivo definido anteriormente. No entanto, o nome é opcional.

## <a name="data-members"></a>Membros de dados

Os membros de dados podem ser um dos seguintes: objeto de dados, referência de dados, lista de inteiros, lista float ou lista de cadeias de caracteres.

Um objeto de dados é um objeto de dados aninhado. Isso permite que a natureza hierárquica do formato de arquivo seja expressa. Os tipos de objetos de dados aninhados permitidos na hierarquia podem ser restritos.

Uma referência de dados é uma referência a um objeto de dados encontrado anteriormente, conforme mostrado no exemplo a seguir.


```
{
  name |
  UUID |
  name UUID
}
```



Uma lista de inteiros é uma lista separada por ponto e vírgula de inteiros, conforme mostrado no exemplo a seguir.


```
1; 2; 3;
```



Uma lista float é uma lista separada por ponto e vírgula de floats, conforme mostrado no exemplo a seguir.


```
1.0; 2.0; 3.0;
```



Uma lista de cadeias de caracteres é uma lista separada por ponto e vírgula de cadeias de caracteres, conforme mostrado no exemplo a seguir.


```
"Moose"; "Goats"; "Sheep";
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificação de texto](text-encoding.md)
</dt> </dl>

 

 



