---
title: O comando de arquivo de resposta
description: Um arquivo de resposta é um arquivo de texto que contém uma ou mais opções de linha de comando do compilador MIDL.
ms.assetid: ad47ea1a-fe7a-4354-be2f-599ba77685ee
keywords:
- referência de linha de comando MIDL , comando de arquivo de resposta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9c40d8f4255b15a7b95b9bdca9e72ae2cba8e7ea1d42281f441326090a9529d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013524"
---
# <a name="the-response-file-command"></a>O comando de arquivo de resposta

Um arquivo de resposta é um arquivo de texto que contém uma ou mais opções de linha de comando do compilador MIDL. Ao contrário de uma linha de comando, um arquivo de resposta permite várias linhas de opções e nomes de arquivo. Isso pode ser útil devido a limitações do seu ambiente de build ou como uma conveniência para o processo de build.

## <a name="switch-options"></a>Opções de opção

``` syntax
midl @response_file
```

<dl> <dt>

<span id="response_file"></span><span id="RESPONSE_FILE"></span>*arquivo \_ de resposta*
</dt> <dd>

Especifica o nome de um arquivo de resposta. O nome do arquivo de resposta deve seguir imediatamente o caractere @. Nenhum espaço em branco é permitido entre o caractere @ e o nome do arquivo de resposta.

</dd> </dl>

## <a name="remarks"></a>Comentários

Como alternativa à colocação de todas as opções associadas a uma opção na linha de comando, o compilador MIDL aceita arquivos de resposta que contêm opções e argumentos. As opções em um arquivo de resposta são interpretadas como se elas estivesse presentes nesse local na linha de comando MIDL.

Cada argumento em um arquivo de resposta deve começar e terminar na mesma linha. O caractere de faixa invertida ( \\ ) não pode ser usado para concatenar linhas. Quando faz parte de uma cadeia de caracteres entre aspas no arquivo de resposta, o caractere de faixa invertida só pode ser usado antes de outra faixa invertida ou antes de um caractere de aspas duplas ("). Quando não faz parte de uma cadeia de caracteres entre aspas, o caractere de linha invertida só pode ser usado antes de um caractere de aspas duplas.

O MIDL dá suporte a argumentos de linha de comando que incluem um ou mais arquivos de resposta combinados com outras opções de linha de comando.

O compilador MIDL não dá suporte a arquivos de resposta aninhados.

## <a name="examples"></a>Exemplos

**Midl @midl.rsp**

**midl -Oicf @midl1.rsp -env win32 @midl2.rsp itf.idl**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sintaxe geral da linha de comando MIDL](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




