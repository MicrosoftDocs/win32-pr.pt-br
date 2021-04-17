---
description: Streaming é o processo de manutenção de apenas uma pequena parte de um arquivo de áudio de reprodução na memória. Isso permite que arquivos de áudio grandes, como música em segundo plano, sejam reproduzidos, e não ocupam uma grande quantidade de memória.
ms.assetid: 7a938ea6-15ef-66b1-0276-88eabf9a722b
title: Dados de áudio de streaming XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1766b20f539f8bbe4d11204b681b7eddca58578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762424"
---
# <a name="xaudio2-streaming-audio-data"></a>Dados de áudio de streaming XAudio2

Streaming é o processo de manutenção de apenas uma pequena parte de um arquivo de áudio de reprodução na memória. Isso permite que arquivos de áudio grandes, como música em segundo plano, sejam reproduzidos, e não ocupam uma grande quantidade de memória.

Quando um arquivo de áudio é transmitido, seus dados são lidos do disco em partes em vez de carregar todo o arquivo ao mesmo tempo. O streaming é feito por meio da leitura assíncrona de dados de áudio em uma fila de buffers de disco. Cada buffer é preenchido e enviado para uma voz de origem. Depois que a voz termina de reproduzir um buffer, o buffer fica disponível para leitura novamente. O loop pelos buffers de disco dessa maneira permite que um arquivo de áudio grande seja reproduzido enquanto apenas uma parte de seus dados é carregada. O código de streaming deve ser colocado em um thread separado, no qual ele pode dormir enquanto aguarda a conclusão de operações de disco e áudio de execução demorada. Uma classe de retorno de chamada é usada para ativar o thread disparando eventos quando as operações de áudio são concluídas.

Para obter um exemplo de como o streaming pode ser realizado com o XAudio2, consulte [como transmitir um som do disco](how-to--stream-a-sound-from-disk.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Transmitindo dados de áudio](streaming-audio-data.md)
</dt> <dt>

[Guia de Programação em XAudio2](programming-guide.md)
</dt> </dl>

 

 



