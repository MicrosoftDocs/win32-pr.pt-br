---
title: criando um arquivo a partir de Fluxos existentes
description: criando um arquivo a partir de Fluxos existentes
ms.assetid: 5149a766-7809-42b7-8e5c-b67b847b9218
keywords:
- Função AVISave
- Função AVISaveV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a15a6ad3770f93bc2fb77dcb79975e1e9aa1fc8da7319e34c140baf488a69554
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498006"
---
# <a name="creating-a-file-from-existing-streams"></a>criando um arquivo a partir de Fluxos existentes

Uma maneira de criar um arquivo que contém fluxos de dados é combinar fluxos existentes em um novo arquivo. Os fluxos que fornecem dados para o novo arquivo podem residir na memória ou em um ou mais arquivos.

Você pode criar um arquivo de vários fluxos usando a função [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) . Essa função cria um arquivo e grava os fluxos de dados especificados em sua sequência de chamada para o arquivo. A sequência de chamada para **AVISave** usa um número variável de argumentos que incluem interfaces para os fluxos combinados no novo arquivo.

Você também pode combinar fluxos de dados em um novo arquivo usando a função [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) . Essa função fornece a mesma funcionalidade que **AVISave**, mas quando você usa **AVISaveV**, seu aplicativo especifica os fluxos de dados como uma matriz, não como um número variável de argumentos.

Você pode criar uma caixa de diálogo na qual o usuário pode selecionar configurações de compactação para o novo arquivo usando a função [**AVISaveOptions**](/windows/desktop/api/Vfw/nf-vfw-avisaveoptions) . A caixa de diálogo exibe as configurações de compactação atuais e permite que o usuário as edite. As alterações de configuração de compactação são armazenadas em uma estrutura [**AVICOMPRESSOPTIONS**](/windows/desktop/api/Vfw/ns-vfw-avicompressoptions) .

Você também pode incluir uma função de retorno de chamada com [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) e [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) que seu aplicativo pode usar para exibir o progresso da gravação do arquivo e, se necessário, permitir que o usuário cancele a operação de salvamento. Você pode incluir o endereço da função de chamada de retorno na sequência de chamada de **AVISave** ou **AVISaveV**.

Você pode permitir que o usuário selecione um nome de arquivo para o novo arquivos usando a função [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) . Essa função exibe a caixa de diálogo Salvar como na qual o usuário pode visualizar o primeiro fluxo (normalmente o fluxo de vídeo) de um arquivo AVI.

Você pode criar um ponteiro de interface de arquivo (e um arquivo virtual) para um grupo de fluxos usando a função [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) . Outras funções AVIFile podem usar o ponteiro de interface de arquivo retornado por essa função para acessar os fluxos no arquivo virtual. Depois de terminar de usar o arquivo virtual, exclua o ponteiro de interface de arquivo usando a função [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) .

> [!Note]  
> Para minimizar a degradação da imagem e do áudio, evite compactar um arquivo AVI mais de uma vez. Combine pedaços de vídeo não compactados em seu sistema de edição e, em seguida, compacte o produto final. Para obter informações sobre opções de compactação, consulte [Gerenciador de compactação de vídeo](video-compression-manager.md).

 

 

 




