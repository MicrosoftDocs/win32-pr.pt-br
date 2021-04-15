---
description: Antes que as funções de instalação possam acessar informações no INF, você deve abri-las com uma chamada para a função SetupOpenInfFile. Essa função retorna um identificador para o arquivo INF.
ms.assetid: d838c05c-51e4-49a8-b773-af4924bff7e2
title: Abrindo e fechando um arquivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893b72d000f433fb4da7ecfee0db4d856f878814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505951"
---
# <a name="opening-and-closing-an-inf-file"></a>Abrindo e fechando um arquivo INF

Antes que as funções de instalação possam acessar informações no INF, você deve abri-las com uma chamada para a função [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) . Essa função retorna um identificador para o arquivo INF.

Se você não souber o nome do arquivo INF que precisa abrir, poderá usar a função [**SetupGetInfFileList**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista) para obter uma lista de arquivos INF em um diretório.

Depois de abrir um arquivo INF, você pode acrescentar outros arquivos INF ao arquivo INF aberto usando a função [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) . Isso é funcionalmente semelhante a uma instrução include. Quando as funções de configuração subsequentes fazem referência a um arquivo INF aberto, elas também poderão acessar todas as informações armazenadas nos arquivos acrescentados.

Se você não especificar um arquivo INF durante a chamada para a função [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) , o **SetupOpenAppendInfFile** acrescentará os arquivos especificados pela chave **layoutfile** na seção **versão** do arquivo inf aberto.

Quando você não precisar mais das informações no arquivo INF, chame a função [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) para liberar os recursos alocados durante a chamada para [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea).

 

 



