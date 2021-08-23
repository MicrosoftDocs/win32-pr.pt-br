---
description: Antes que as funções de instalação possam acessar informações no INF, você deve abri-la com uma chamada para a função SetupOpenInfFile. Essa função retorna um handle para o arquivo INF.
ms.assetid: d838c05c-51e4-49a8-b773-af4924bff7e2
title: Abrindo e fechando um arquivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e05500b473a904a3834fa507cff0d22c466153f4e08d95f75d0c076c66d86675
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665546"
---
# <a name="opening-and-closing-an-inf-file"></a>Abrindo e fechando um arquivo INF

Antes que as funções de instalação possam acessar informações no INF, você deve abri-la com uma chamada para a [**função SetupOpenInfFile.**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) Essa função retorna um handle para o arquivo INF.

Se você não sabe o nome do arquivo INF que precisa abrir, pode usar a função [**SetupGetInfFileList**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista) para obter uma lista de arquivos INF em um diretório.

Depois de abrir um arquivo INF, você pode anexar arquivos INF adicionais ao arquivo INF aberto usando a [**função SetupOpenAppendInfFile.**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) Isso é funcionalmente semelhante a uma instrução include. Quando as funções de instalação subsequentes referenciam um arquivo INF aberto, elas também poderão acessar todas as informações armazenadas nos arquivos anexados.

Se você não especificar um arquivo INF durante a chamada para a função [**SetupOpenAppendInfFile,**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) **SetupOpenAppendInfFile** anexa os arquivos especificados pela chave **LayoutFile** na seção **Versão** do arquivo INF aberto.

Quando você não precisar mais das informações no arquivo INF, chame a função [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) para liberar recursos alocados durante a chamada para [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea).

 

 



