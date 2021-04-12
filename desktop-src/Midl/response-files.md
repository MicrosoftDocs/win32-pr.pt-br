---
title: Arquivos de resposta
description: Como uma alternativa para colocar todas as opções na linha de comando, o compilador MIDL aceita arquivos de resposta que contêm opções e argumentos.
ms.assetid: 53ee9ad2-1ab4-421f-99c9-66186da4bd9d
keywords:
- MIDL do compilador MIDL, arquivos de resposta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd949a3704b0669fd37c5629307a59df9742010
ms.sourcegitcommit: ad8bd914e19508a67af232d8d59c0e0ee9c3948b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/07/2019
ms.locfileid: "104364524"
---
# <a name="response-files"></a>Arquivos de resposta

Como uma alternativa para colocar todas as opções na linha de comando, o compilador MIDL aceita arquivos de resposta que contêm opções e argumentos. Um arquivo de resposta é um arquivo de texto que contém uma ou mais opções de linha de comando do compilador MIDL. Ao contrário de uma linha de comando, um arquivo de resposta permite várias linhas de opções e nomes de arquivo. Isso pode ser útil devido a limitações do seu ambiente de compilação ou como uma conveniência para o processo de compilação. Você pode especificar um arquivo de resposta MIDL como:

 **\@ nome de arquivo** MIDL

<dl> <dt>

<span id="filename"></span><span id="FILENAME"></span>*nome do arquivo*
</dt> <dd>

Especifica o nome do arquivo de resposta. O nome do arquivo de resposta deve seguir imediatamente o caractere @ sem espaço em branco entre o caractere @ e o nome do arquivo de resposta.

</dd> </dl>

As opções em um arquivo de resposta são interpretadas como se estivessem presentes nesse local na linha de comando MIDL. Cada argumento em um arquivo de resposta deve começar e terminar na mesma linha. Não é possível usar o caractere de barra invertida ( \) para concatenar linhas.

O MIDL dá suporte a argumentos de linha de comando que incluem um ou mais arquivos de resposta, combinados com outras opções de linha de comando:

**MIDL-Oicf @midl1.rsp -envwin32 @midl2.rsp ITF. idl**

O compilador MIDL não oferece suporte a arquivos de resposta aninhados.

 

 




