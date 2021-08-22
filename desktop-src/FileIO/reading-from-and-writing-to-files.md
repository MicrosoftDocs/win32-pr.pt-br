---
description: Um aplicativo lê e grava em um arquivo usando as funções ReadFile, ReadFileEx, WriteFile e WriteFileEx.
ms.assetid: 14ecb06c-3f80-47b8-9964-6a2c3b572300
title: Lendo e gravando em arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b88de3510a681839a9592bed4755de6249f79db117d94985ddb00320381b92c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119533316"
---
# <a name="reading-from-and-writing-to-files"></a>Lendo e gravando em arquivos

Um aplicativo lê e grava em um arquivo usando as funções [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex), [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)e [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) . Essas funções exigem um identificador para um arquivo a ser aberto para leitura e gravação, respectivamente. Eles lêem e gravam um número especificado de bytes no local indicado pelo ponteiro do arquivo. Os dados são lidos e gravados exatamente como especificado; as funções não formatam Os dados.

Quando o ponteiro do arquivo atingir o final de um arquivo e o aplicativo tentar ler o arquivo, nenhum erro ocorrerá, mas nenhum byte será lido. Portanto, a leitura de zero bytes sem um erro significa que o aplicativo atingiu o final do arquivo. Escrever zero bytes não faz nada.

Para obter mais informações, consulte estes tópicos.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                                                           | Descrição                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Posicionando um ponteiro de arquivo](positioning-a-file-pointer.md)<br/>                                                                         | Windows usa um ponteiro de arquivo para controlar os bytes lidos ou gravados.<br/>                                                       |
| [Lendo ou gravando em arquivos usando um esquema de Scatter-Gather](reading-from-or-writing-to-files-using-a-scatter-gather-scheme.md)<br/> | Descreve um esquema de dispersão-coleta para leitura ou gravação de partes não contíguas de dados em uma única operação.<br/>                   |
| [Liberando dados de e/s de System-Buffered para O disco](flushing-system-buffered-i-o-data-to-disk.md)<br/>                                           | o Windows armazena os dados em operações de gravação e leitura de arquivo em buffers de dados mantidos pelo sistema para otimizar o desempenho do disco.<br/> |
| [Truncando ou estendendo arquivos](truncating-or-extending-files.md)<br/>                                                                   | Um aplicativo pode truncar ou estender um arquivo chamando [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).<br/>                             |



 

 

 




