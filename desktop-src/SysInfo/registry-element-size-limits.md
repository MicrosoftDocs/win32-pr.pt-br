---
description: A tabela a seguir identifica os limites de tamanho para os vários elementos do registro.
ms.assetid: a6d3a884-f181-46a5-b655-226c68792e08
title: Limites de tamanho de elemento do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c76a11abc80f80a13e0643d7745d211168ecba8bcf06446af9ac842f8351567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885229"
---
# <a name="registry-element-size-limits"></a>Limites de tamanho de elemento do registro

A tabela a seguir identifica os limites de tamanho para os vários elementos do registro.



| Elemento do registro | Limite de tamanho                                                                                                                                            |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome da chave         | 255 caracteres. O nome da chave inclui o caminho absoluto da chave no registro, sempre Iniciando em uma chave base, por exemplo, HKEY \_ local \_ Machine. |
| Nome do valor       | 16.383 caracteres **Windows 2000:** 260 caracteres ANSI ou 16.383 caracteres Unicode.<br/>                                                       |
| Valor            | Memória disponível (formato mais recente) 1 MB (formato padrão)<br/>                                                                                     |
| Árvore             | Uma árvore do registro pode ter 512 níveis de profundidade. Você pode criar até 32 níveis por vez por meio de uma única chamada à API do registro.                                  |



 

Valores longos (mais de 2.048 bytes) devem ser armazenados em um arquivo e o local do arquivo deve ser armazenado no registro. Isso ajuda o registro a ser executado com eficiência.

O local do arquivo pode ser o nome de um valor ou os dados de um valor. Cada barra invertida na cadeia de caracteres de localização deve ser precedida por outra barra invertida como um caractere de escape. Por exemplo, especifique "C: \\ \\ mydir \\ \\ MyFile" para armazenar a cadeia de caracteres "c: \\ mydir \\ MyFile". Um local de arquivo também pode ser o nome de uma chave se estiver dentro do limite de 255 caracteres para nomes de chave e não contiver barras invertidas, que não são permitidas em nomes de chave.

 

 




