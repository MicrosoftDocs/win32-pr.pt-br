---
title: Arquivos de resposta
description: Como alternativa à colocação de todas as opções na linha de comando, o compilador MIDL aceita arquivos de resposta que contêm opções e argumentos.
ms.assetid: 53ee9ad2-1ab4-421f-99c9-66186da4bd9d
keywords:
- MIDL compiler MIDL , arquivos de resposta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c9b4d079e92dff3c25f8a38c6c73073a548ea91
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387065"
---
# <a name="response-files"></a>Arquivos de resposta

Como alternativa à colocação de todas as opções na linha de comando, o compilador MIDL aceita arquivos de resposta que contêm opções e argumentos. Um arquivo de resposta é um arquivo de texto que contém uma ou mais opções de linha de comando do compilador MIDL. Ao contrário de uma linha de comando, um arquivo de resposta permite várias linhas de opções e nomes de arquivo. Isso pode ser útil devido a limitações do seu ambiente de build ou como uma conveniência para o processo de build. Você pode especificar um arquivo de resposta MIDL como:

**midl** **\@ filename**

<dl> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Filename*
</dt> <dd>

Especifica o nome do arquivo de resposta. O nome do arquivo de resposta deve seguir imediatamente o caractere @ sem espaço em branco entre o caractere @ e o nome do arquivo de resposta.

</dd> </dl>

As opções em um arquivo de resposta são interpretadas como se elas estavam presentes nesse local na linha de comando MIDL. Cada argumento em um arquivo de resposta deve começar e terminar na mesma linha. Não é possível usar o caractere de linha invertida ( \\ ) para concatenar linhas.

O MIDL dá suporte a argumentos de linha de comando que incluem um ou mais arquivos de resposta, combinados com outras opções de linha de comando:

**midl -Oicf @midl1.rsp -envwin32 @midl2.rsp itf.idl**

O compilador MIDL não dá suporte a arquivos de resposta aninhados.

 

 




