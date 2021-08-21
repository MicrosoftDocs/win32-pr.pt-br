---
title: Lendo arquivos ASF
description: Lendo arquivos ASF
ms.assetid: e0aabe05-b317-42ac-85fc-5a75165722d4
keywords:
- Windows Media Format SDK, lendo arquivos ASF
- Windows SDK do formato de mídia, formato de sistemas avançados (ASF)
- ASF (Advanced Systems Format), lendo arquivos
- ASF (formato de sistemas avançados), lendo arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e01f417cafad4e125c6c176ac35e95ff3ab8f08c4f600b811865a9fb6ae51362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197507"
---
# <a name="reading-asf-files"></a>Lendo arquivos ASF

o SDK do formato de mídia Windows pode ser usado para fornecer amostras de mídia de um arquivo ASF. Dois objetos são usados para recuperar amostras, o objeto leitor e o objeto leitor síncrono.

o objeto leitor é o objeto de leitura original no SDK do formato de mídia Windows. O objeto leitor usa uma arquitetura assíncrona para enviar amostras por push a um aplicativo. Os aplicativos criados usando o objeto leitor devem implementar funções de retorno de chamada que respondam às várias mensagens e eventos resultantes desse modelo multi-threaded. Para maior clareza, esta seção fará referência ao objeto leitor como o leitor assíncrono.

o objeto leitor síncrono é novo para esta versão do SDK do formato de mídia Windows. O leitor síncrono não usa vários threads no processamento de amostras de arquivos ASF. Um aplicativo criado usando o leitor síncrono recupera amostras sob demanda, em vez de esperar que o leitor as envie.

Ao criar um aplicativo para ler arquivos ASF, você deve escolher qual objeto de leitor usar. em geral, os aplicativos criados para fornecer Windows conteúdo baseado em mídia devem ser criados usando o leitor assíncrono, enquanto os aplicativos criados para editar arquivos ASF devem ser criados com o leitor síncrono.

A tabela a seguir lista os principais recursos de ambos os objetos do leitor. Use esta tabela para ajudar a determinar qual objeto usar para seu aplicativo.



| Recurso                                                                    | Leitor assíncrono | Leitor de sincronização |
|----------------------------------------------------------------------------|--------------|-------------|
| Ler amostras não compactadas por número de saída                                 | Sim          | Sim         |
| Ler amostras compactadas por número de fluxo                                   | Sim          | Sim         |
| Ler amostras não compactadas por número de fluxo                                 | Não           | Sim         |
| Ler do site da Internet                                                    | Sim          | Não          |
| Ler metadados                                                              | Sim          | Sim         |
| Buscar na hora da apresentação                                                  | Sim          | Sim         |
| Buscar para quadro                                                              | Sim          | Sim         |
| Buscar para o marcador                                                             | Sim          | Não          |
| Alternar entre a entrega de amostra compactada e não compactada durante a reprodução | Não           | Sim         |
| Abrir arquivos usando a interface **IStream**                                     | Sim          | Sim         |



 

As seções a seguir fornecem mais informações sobre como trabalhar com os dois objetos do leitor.



| Seção                                                                                      | Descrição                                                                                                                             |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [Trabalhando com saídas](working-with-outputs.md)                                             | Descreve como usar e manipular saídas. Aplica-se a ambos os objetos do leitor.                                                            |
| [Alocando buffers para leitura de arquivo](allocating-buffers-for-file-reading.md)               | Descreve como usar seu próprio pool de buffers para manter amostras entregues pelo leitor ou leitor síncrono.                            |
| [Lendo metadados na reprodução](reading-metadata-at-playback.md)                             | Descreve como aproveitar o suporte a metadados na reprodução. Aplica-se a ambos os objetos do leitor.                                        |
| [Obtendo informações de perfil na reprodução](getting-profile-information-at-playback.md)       | Descreve como acessar informações de perfil para arquivos abertos. Aplica-se a ambos os objetos do leitor.                                           |
| [Lendo áudio de multicanal](reading-multichannel-audio.md)                                 | Descreve como configurar o gravador para decodificar corretamente o áudio de multicanal.                                                            |
| [Renderizando conteúdo](rendering-content.md)                                                   | Discute os problemas relacionados à renderização de amostras não compactadas. Aplica-se a ambos os objetos do leitor.                                         |
| [Obtendo o melhor desempenho de busca de vídeo](getting-the-best-video-seeking-performance.md) | Descreve maneiras de melhorar o desempenho de busca de vídeo.                                                                                    |
| [Lendo arquivos com o leitor assíncrono](reading-files-with-the-asynchronous-reader.md) | Descreve como ler arquivos ASF usando o objeto leitor assíncrono.                                                                   |
| [Lendo arquivos com o leitor síncrono](reading-files-with-the-synchronous-reader.md)   | Descreve como ler arquivos ASF usando o objeto leitor síncrono.                                                                    |
| [Habilitando a aceleração de vídeo do DirectX](enabling-directx-video-acceleration.md)               | Descreve como implementar a aceleração de vídeo do DirectX para usar os recursos de aceleração de hardware de algumas placas de vídeo para decodificar vídeo. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação**](programming-guide.md)
</dt> <dt>

[**Objeto de leitor**](reader-object.md)
</dt> <dt>

[**Objeto de leitor síncrono**](synchronous-reader-object.md)
</dt> </dl>

 

 




