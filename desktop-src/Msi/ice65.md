---
description: ICE65 verifica se a tabela de ambiente não tem valores de acréscimo ou de prefixo inválidos.
ms.assetid: 95d4e618-9a19-40db-910a-daab105559ae
title: ICE65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 543c75f3abe6cb44a405f41bcb788dc71adf85ae954f013244bfc1cded4e6d27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946583"
---
# <a name="ice65"></a>ICE65

ICE65 verifica se a [tabela de ambiente](environment-table.md) não tem valores de acréscimo ou de prefixo inválidos.

Falha ao corrigir um aviso ou erro relatado por ICE65 geralmente leva a problemas na instalação, na desinstalação ou no reparo da variável de ambiente. Por exemplo, somente alguns valores de uma variável específica poderão ser removidos se um ou mais dos valores dessa variável tiverem um separador à direita.

## <a name="result"></a>Resultado

ICE65 lançará um aviso ou um erro se a tabela de ambiente tiver valores de prefixo ou acréscimo inválidos.

## <a name="example"></a>Exemplo

ICE65 relata o seguinte erro e aviso para o exemplo mostrado.

``` syntax
The environment variable 'Var3' has a separator beginning or ending its value.
```

O nulo à direita no final do valor ( \[ ~ \] ) marca esse valor como sendo anexado a qualquer valor existente. O caractere imediatamente antes de NULL (ponto-e-vírgula) torna-se o separador desse valor. Esse valor também tem um ponto e vírgula no início da cadeia de caracteres.

Para corrigir esse erro, basta excluir o ponto-e-vírgula à esquerda.

``` syntax
WARNING: The environment variable 'Var2' has an alphanumeric separator
```

O nulo à esquerda no valor ( \[ ~ \] ) marca esse valor a ser anexado a qualquer valor existente. O caractere imediatamente após NULL torna-se o separador desse valor. Nesse caso, esse caractere é a letra "e", que também ocorre no meio da cadeia de caracteres a ser acrescentada. Essa condição (com um separador igual a um caractere dentro da cadeia de caracteres a ser acrescentada) pode causar resultados imprevisíveis.

A letra "e", sendo uma letra comum, provavelmente será encontrada no valor. Uma opção melhor seria ";" ou algum outro caractere não alfanumérico. (No entanto, se o valor for um caminho, ":" e " \\ " e "." são opções arriscadas.)

Para corrigir esse aviso, use um caractere separador diferente.

[Tabela de ambiente](environment-table.md)



| Componente | Diretório | Atributos         | KeyPath       |
|-----------|-----------|--------------------|---------------|
| Var1      | TestVar   | \[~\]; AppendThis   | TestComponent |
| Var2      | TestVar   | \[~\]eAppendThis   | TestComponent |
| Var3      | TestVar   | ; PrependThis;\[~\] | TestComponent |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



