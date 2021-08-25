---
title: Coletores
description: Coletores
ms.assetid: 6781a326-a30a-4d4d-96db-332d0f681a31
keywords:
- Windows SDK de Formato de Mídia, sinks
- Windows SDK de Formato de Mídia, sinks de arquivos
- ASF (Advanced Systems Format), sinks
- ASF (Formato de Sistemas Avançados), sinks
- FORMATO DE SISTEMAS Avançados (ASF), sinks de arquivos
- ASF (Formato de Sistemas Avançados), sinks de arquivos
- Windows SDK de Formato de Mídia, sinks de rede
- Windows SDK de Formato de Mídia, sinks push
- ASF (Advanced Systems Format), sinks de rede
- ASF (Formato de Sistemas Avançados), sinks de rede
- ASF (Advanced Systems Format), por push sinks
- ASF (Formato de Sistemas Avançados), efetuar push de sinks
- sinks,about
- sinks de arquivo, sobre
- sinks de rede
- por push sinks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb72479a231c3db508efcea7db54528c0b1bf9635afba8b842a4c23add0456cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807896"
---
# <a name="sinks"></a>Coletores

O objeto writer do SDK Windows Formato de Mídia fornece conteúdo processado para os sinks. Cada sink é um objeto que fornece dados. O ponto de entrega depende do tipo de sink. Há três tipos de sinks: sinks de arquivo, sinks de rede e de push sinks.

## <a name="file-sinks"></a>Sinks de arquivos

Os sinks de arquivos escrevem conteúdo ASF em um arquivo em uma unidade local ou de rede. Quando você usa o objeto writer para gravar um arquivo sem adicionar explicitamente um sink de arquivo, o autor criará um para você usando o nome que você passa para [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename). Você pode atribuir vários sinks de arquivo a um objeto de gravação para gravar o conteúdo em vários arquivos de uma só vez.

Usando um sink de arquivo, você pode controlar muitos aspectos do arquivo. Os recursos a seguir estão disponíveis por meio de um sink de arquivo.

-   Monitoramento de estatísticas de arquivo. Você pode monitorar o tamanho e a duração do arquivo enquanto ele está sendo criado.
-   Criação parcial de arquivo de conteúdo. Os sinks de arquivos podem ser configurados para começar a escrever conteúdo em um momento específico e terminar de escrever em um momento específico. Isso permite que você crie vários arquivos contendo seções diferentes do mesmo conteúdo na mesma passagem de escrita.

## <a name="network-sinks"></a>Sinks de rede

Os sinks de rede transmitem conteúdo para um endereço de rede. Os clientes de leitura podem se conectar ao endereço para receber a difusão.

## <a name="push-sinks"></a>Push Sinks

Os sinks push entregam conteúdo do autor para um servidor que executa Windows Media Services. Normalmente, os sinks push são usados em cenários em que um computador codifica conteúdo ao vivo e o entrega a um ou mais servidores para distribuição ampla. O uso de um sink push permite dedicar computadores a tarefas específicas, economizando largura de banda e habilitando o processamento em cada servidor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de escrita de arquivo**](file-writing-features.md)
</dt> <dt>

[**Trabalhando com os sinks do Writer**](working-with-writer-sinks.md)
</dt> </dl>

 

 




