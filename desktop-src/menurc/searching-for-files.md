---
title: Procurando arquivos
description: Por padrão, o RC procura arquivos de cabeçalho e arquivos de recursos (como arquivos de ícone e cursor) primeiro no diretório atual e, em seguida, nos diretórios especificados pela variável de ambiente INCLUDE.
ms.assetid: 6c8c905d-b0f6-4665-9a93-62617ff30137
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078a04a4cf2f3461d03c7026e0f1d73d8fd38665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105765702"
---
# <a name="searching-for-files"></a>Procurando arquivos

Por padrão, o RC procura arquivos de cabeçalho e arquivos de recursos (como arquivos de ícone e cursor) primeiro no diretório atual e, em seguida, nos diretórios especificados pela variável de ambiente INCLUDE. (A variável de ambiente PATH não tem nenhum efeito sobre quais diretórios RC pesquisa.)

## <a name="adding-a-directory-to-search"></a>Adicionando um diretório para pesquisa

Você pode usar a opção **/i** para adicionar um diretório à lista de pesquisas de diretórios RC. O compilador então pesquisa os diretórios na seguinte ordem:

1.  O diretório atual
2.  O diretório ou diretórios que você especifica usando a opção **/i** , na ordem em que aparecem na linha de comando RC
3.  A lista de diretórios especificada pela variável de ambiente INCLUDE, na ordem em que a variável as lista, a menos que você especifique a opção **/x**

O exemplo a seguir compila o arquivo de definição de recurso MyApp. rc:

**RC/i c: \\ origem \\ itens/i d: \\ recursos MyApp. rc**

Ao compilar o script MyApp. rc, o RC procura arquivos de cabeçalho e arquivos de recursos primeiro no diretório atual, em C: \\ Source it \\ e D: \\ Resources e, em seguida, nos diretórios especificados pela variável de ambiente INCLUDE.

## <a name="ignoring-the-include-environment-variable"></a>Ignorando a variável de ambiente INCLUDE

Você pode impedir que o RC use a variável de ambiente INCLUDE ao determinar os diretórios a serem pesquisados. Para fazer isso, use a opção **/x** . O compilador então procura arquivos somente no diretório atual e em todos os diretórios que você especificar usando a opção **/i** .

O comando a seguir compila o arquivo de script MyApp. rc:

**RC/x/i c: \\ origem \\ coisas MyApp. rc**

Ao compilar o script MyApp. rc, o RC procura arquivos de cabeçalho e arquivos de recursos primeiro no diretório atual e, em seguida, em C: \\ Source \\ . Ele não pesquisa os diretórios especificados pela variável de ambiente INCLUDE.

 

 




