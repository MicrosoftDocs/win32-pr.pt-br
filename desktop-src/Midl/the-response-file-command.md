---
title: O comando arquivo de resposta
description: Um arquivo de resposta é um arquivo de texto que contém uma ou mais opções de linha de comando do compilador MIDL.
ms.assetid: ad47ea1a-fe7a-4354-be2f-599ba77685ee
keywords:
- referência de linha de comando MIDL, comando Response File
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26cf4d07ce8465239874ff666537646da2c4c564
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387662"
---
# <a name="the-response-file-command"></a>O comando arquivo de resposta

Um arquivo de resposta é um arquivo de texto que contém uma ou mais opções de linha de comando do compilador MIDL. Ao contrário de uma linha de comando, um arquivo de resposta permite várias linhas de opções e nomes de arquivo. Isso pode ser útil devido a limitações do seu ambiente de compilação ou como uma conveniência para o processo de compilação.

## <a name="switch-options"></a>Opções de comutação

``` syntax
midl @response_file
```

<dl> <dt>

<span id="response_file"></span><span id="RESPONSE_FILE"></span>*arquivo de resposta \_*
</dt> <dd>

Especifica o nome de um arquivo de resposta. O nome do arquivo de resposta deve seguir imediatamente o caractere @. Nenhum espaço em branco é permitido entre o caractere @ e o nome do arquivo de resposta.

</dd> </dl>

## <a name="remarks"></a>Comentários

Como uma alternativa para colocar todas as opções associadas a uma opção na linha de comando, o compilador MIDL aceita arquivos de resposta que contêm opções e argumentos. As opções em um arquivo de resposta são interpretadas como se elas estivessem presentes nesse local na linha de comando MIDL.

Cada argumento em um arquivo de resposta deve começar e terminar na mesma linha. O caractere de barra invertida ( \\ ) não pode ser usado para concatenar linhas. Quando ele faz parte de uma cadeia de caracteres entre aspas no arquivo de resposta, o caractere de barra invertida só pode ser usado antes de outra barra invertida ou antes de um caractere de aspas duplas ("). Quando não faz parte de uma cadeia de caracteres entre aspas, o caractere de barra invertida só pode ser usado antes de um caractere de aspas duplas.

O MIDL dá suporte a argumentos de linha de comando que incluem um ou mais arquivos de resposta combinados com outras opções de linha de comando.

O compilador MIDL não oferece suporte a arquivos de resposta aninhados.

## <a name="examples"></a>Exemplos

**MIDL @midl.rsp**

**MIDL-Oicf @midl1.rsp -env Win32 @midl2.rsp ITF. idl**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




