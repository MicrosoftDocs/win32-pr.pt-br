---
title: " Diretiva include"
description: Diretiva de pré-processador que insere o conteúdo do arquivo especificado no programa de origem no ponto em que a diretiva é exibida.
ms.assetid: 24796d89-5690-469b-950e-df56783aa05a
keywords:
- incluir diretiva HLSL
topic_type:
- apiref
api_name:
- include Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a844459234200ca99233eb3f64a2a1c30449cdcc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988672"
---
# <a name="include-directive"></a>\#Diretiva include

Diretiva de pré-processador que insere o conteúdo do arquivo especificado no programa de origem no ponto em que a diretiva é exibida.


| \#incluir "*filename*"       |
|------------------------------|
| \#incluir *nome de arquivo* <> |

## <a name="parameters"></a>Parâmetros

| Item | Descrição |
|------|-------------|
| *filename* | Nome do arquivo a ser incluído, opcionalmente precedido por uma especificação de diretório. O filename deve especificar um arquivo existente. |

## <a name="remarks"></a>Comentários

A \# diretiva include causa a substituição da diretiva pelo conteúdo inteiro do arquivo especificado. O pré-processador para de Pesquisar assim que encontrar um arquivo com o nome especificado; Se você especificar uma especificação de caminho completa e não ambígua para o arquivo, o pré-processador pesquisará apenas o caminho especificado.

> [!NOTE]
> A [ferramenta de compilador de efeito](/windows/desktop/direct3dtools/fxc) tem um manipulador de inclusão interno usando a opção/i. No entanto, ao executar o compilador da API, você pode fornecer um manipulador de inclusão personalizado implementando a interface ID3DXInclude.

A diferença entre as duas formas de sintaxe é a ordem na qual o pré-processador procura por arquivos de cabeçalho quando o caminho é especificado incompletamente, conforme mostrado na tabela a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Formato de sintaxe</th>
<th>Padrão de pesquisa de pré-processador</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>#incluir <b>&quot;</b> <em>nome de arquivo</em><b>&quot;</b></td>
<td>Procura o arquivo de inclusão:
<ol>
<li>no mesmo diretório que o arquivo que contém a diretiva #include.</li>
<li>nos diretórios de todos os arquivos que contêm uma diretiva #include para o arquivo que contém a diretiva #include.</li>
<li>em caminhos especificados pela opção de compilador/I, na ordem em que são listados.</li>
<li><p>em caminhos especificados pela variável de ambiente INCLUDE, na ordem em que eles são listados.</p>
<blockquote>
[!NOTE]<br />
A variável de ambiente INCLUDE é ignorada em um ambiente de desenvolvimento. Consulte a documentação do ambiente de desenvolvimento para obter informações sobre como definir os caminhos de inclusão para o seu projeto.
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
<tr class="even">
<td>#incluir <b><</b> <em>nome de arquivo</em><b>></b></td>
<td>Procura o arquivo de inclusão:
<ol>
<li>em caminhos especificados pela opção de compilador/I, na ordem em que são listados.</li>
<li><p>em caminhos especificados pela variável de ambiente INCLUDE, na ordem em que eles são listados.</p>
<blockquote>
[!NOTE]<br />
A variável de ambiente INCLUDE é ignorada em um ambiente de desenvolvimento. Consulte a documentação do ambiente de desenvolvimento para obter informações sobre como definir os caminhos de inclusão para o seu projeto.
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="examples"></a>Exemplos

O exemplo a seguir faz com que o pré-processador substitua a \# diretiva include pelo conteúdo de stdio. h. Como o exemplo usa o formato de colchete angular, o pré-processador pesquisará o arquivo somente nos diretórios listados pela opção de compilador/I e a variável de ambiente INCLUDE.

```cpp
#include <stdio.h>
```

## <a name="see-also"></a>Confira também

- [Diretivas de pré-processador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)

- [Interface ID3D10Include](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))

- [Efeito-ferramenta do compilador](/windows/desktop/direct3dtools/fxc)