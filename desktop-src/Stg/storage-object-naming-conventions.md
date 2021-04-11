---
title: Convenções de nomenclatura de objeto de armazenamento
description: Os objetos de armazenamento e fluxo são nomeados de acordo com um conjunto de convenções.
ms.assetid: 72e87c6a-cce5-4456-8336-c657e65c0a34
keywords:
- Armazenamento estruturado Strctd STG, conceitos básicos, convenções de nomenclatura de objeto de armazenamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e828674f4165bdb54dc2ec06748ab4165e75e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363739"
---
# <a name="storage-object-naming-conventions"></a>Convenções de nomenclatura de objeto de armazenamento

Os objetos de armazenamento e fluxo são nomeados de acordo com um conjunto de convenções.

O nome de um objeto de armazenamento raiz é o nome real do arquivo no sistema de arquivos subjacente. Ele está em conformidade com as convenções e restrições que o sistema de arquivos impõe. As cadeias de caracteres de nome de arquivo passadas para métodos e funções relacionados ao armazenamento são passadas, não interpretadas e inalteradas, para o sistema de arquivos.

O nome de um elemento aninhado contido em um objeto de armazenamento é gerenciado pela implementação do objeto de armazenamento específico. Todas as implementações de objetos de armazenamento devem oferecer suporte a nomes de elementos aninhados 32 caracteres de comprimento (incluindo o terminador **nulo** ), embora algumas implementações possam dar suporte a nomes mais longos. Se o objeto de armazenamento faz qualquer conversão de caso é definido pela implementação. Como resultado, os aplicativos que definem nomes de elementos devem escolher nomes que são aceitáveis independentemente de a conversão de maiúsculas e minúsculas ser executada. A implementação COM de arquivos compostos dá suporte a nomes com um comprimento máximo de 32 caracteres e não executa nenhuma conversão de maiúsculas e minúsculas.

 

 




