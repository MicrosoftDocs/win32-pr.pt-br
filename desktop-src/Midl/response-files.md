---
title: Arquivos de resposta
description: Como uma alternativa para colocar todas as opções na linha de comando, o compilador MIDL aceita arquivos de resposta que contêm opções e argumentos.
ms.assetid: 53ee9ad2-1ab4-421f-99c9-66186da4bd9d
keywords:
- MIDL do compilador MIDL, arquivos de resposta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60a565c6178b3f671cccb391124297b07bb344c08d1cf7125ed26ba4f1b0704
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822106"
---
# <a name="response-files"></a>Arquivos de resposta

Como uma alternativa para colocar todas as opções na linha de comando, o compilador MIDL aceita arquivos de resposta que contêm opções e argumentos. Um arquivo de resposta é um arquivo de texto que contém uma ou mais opções de linha de comando do compilador MIDL. Ao contrário de uma linha de comando, um arquivo de resposta permite várias linhas de opções e nomes de arquivo. Isso pode ser útil devido a limitações do seu ambiente de compilação ou como uma conveniência para o processo de compilação. Você pode especificar um arquivo de resposta MIDL como:

 **\@ nome de arquivo** MIDL

<dl> <dt>

<span id="filename"></span><span id="FILENAME"></span>*nome do arquivo*
</dt> <dd>

Especifica o nome do arquivo de resposta. O nome do arquivo de resposta deve seguir imediatamente o caractere @ sem espaço em branco entre o caractere @ e o nome do arquivo de resposta.

</dd> </dl>

As opções em um arquivo de resposta são interpretadas como se estivessem presentes nesse local na linha de comando MIDL. Cada argumento em um arquivo de resposta deve começar e terminar na mesma linha. Não é possível usar o caractere de barra invertida ( \\ ) para concatenar as linhas.

O MIDL dá suporte a argumentos de linha de comando que incluem um ou mais arquivos de resposta, combinados com outras opções de linha de comando:

**MIDL-Oicf @midl1.rsp -envwin32 @midl2.rsp ITF. idl**

O compilador MIDL não oferece suporte a arquivos de resposta aninhados.

 

 




