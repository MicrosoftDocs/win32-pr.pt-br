---
description: Os objetos de dados contêm os dados reais ou uma referência a esses dados. Cada objeto de dados tem um modelo correspondente que especifica o tipo de dados. As seções a seguir discutem o formulário e as partes dos objetos de dados.
ms.assetid: 61dbe241-2658-4dd0-af89-3db204b56fad
title: Dados (formato de arquivo X, codificação de texto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1af117a0207ce804ccacd397bb990fe5f43c94
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370240"
---
# <a name="data-x-file-format-text-encoding"></a>Dados (formato de arquivo X, codificação de texto)

Os objetos de dados contêm os dados reais ou uma referência a esses dados. Cada objeto de dados tem um modelo correspondente que especifica o tipo de dados. As seções a seguir discutem o formulário e as partes dos objetos de dados.

## <a name="form-identifier-and-name"></a>Formulário, identificador e nome

Os objetos de dados têm o seguinte formato.


```
        <Identifier> [name] { [<UUID>]
    <member 1>;
...
    <member n>;
}
```



O identificador é obrigatório e deve corresponder a um tipo de dados definido anteriormente ou primitivo. No entanto, o nome é opcional.

## <a name="data-members"></a>Membros de dados

Os membros de dados podem ser um dos seguintes: objeto de dados, referência de dados, lista de inteiros, lista flutuante ou lista de cadeias de caracteres.

Um objeto de dados é um objeto de dados aninhado. Isso permite que a natureza hierárquica do formato de arquivo seja expressa. Os tipos de objetos de dados aninhados permitidos na hierarquia podem ser restritos.

Uma referência de dados é uma referência a um objeto de dados encontrado anteriormente, conforme mostrado no exemplo a seguir.


```
{
  name |
  UUID |
  name UUID
}
```



Uma lista de inteiros é uma lista de inteiros separados por ponto e vírgula, conforme mostrado no exemplo a seguir.


```
1; 2; 3;
```



Uma lista flutuante é uma lista de floats separada por ponto e vírgula, conforme mostrado no exemplo a seguir.


```
1.0; 2.0; 3.0;
```



Uma lista de cadeias de caracteres é uma lista separada por ponto-e-vírgula de cadeias, conforme mostrado no exemplo a seguir.


```
"Moose"; "Goats"; "Sheep";
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificação de Texto](text-encoding.md)
</dt> </dl>

 

 



