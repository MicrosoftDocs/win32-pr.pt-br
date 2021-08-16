---
title: Trabalhando com os sinks do Writer
description: Trabalhando com os sinks do Writer
ms.assetid: 1ad28684-47d2-4ddb-bf18-22310f0392a0
keywords:
- ASF (Advanced Systems Format), sinks writer
- ASF (Formato de Sistemas Avançados), sinks de writer
- ASF (Advanced Systems Format), sinks
- ASF (Formato de Sistemas Avançados), sinks
- sinks,writer sinks
- sinks writer,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 407e5bf2e87bfbf3084d19f75170a12be693d804d4d902f919096dca5aeab057
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194861"
---
# <a name="working-with-writer-sinks"></a>Trabalhando com os sinks do Writer

O objeto writer do SDK Windows Formato de Mídia processa dados de mídia de entrada em um fluxo de bits. No entanto, o objeto writer não entrega o fluxo de bits para seu destino final (para um arquivo ou um local de rede). Para gravar o conteúdo do ASF em um formato acessível, você deve usar os sinks de gravação.

O objeto writer dá suporte a três tipos de sinks: sinks de arquivo, de rede e de push sinks. Um sink de arquivo grava o conteúdo do ASF em um arquivo ASF no disco. Um sink de rede transmite conteúdo ASF de um endereço de rede. Um sink push fornece dados para um servidor que executa Windows Media Services para que o servidor possa disponibilizar o conteúdo para seu público-alvo. Você também pode criar seus próprios sinks para fornecer dados ASF de qualquer maneira que seja exigido pelo seu aplicativo. Para obter informações sobre os sinks de rede e os sinks de push, consulte [Enviando dados ASF por uma rede.](sending-asf-data-over-a-network.md) O restante desta seção aborda os sinks do autor.

Você pode configurar um ou mais sinks para cada instância do autor usado. Cada sink trata apenas um único destino. Por exemplo, se você quiser gravar três arquivos ao mesmo tempo, deverá criar e configurar um sink de arquivo separado para cada um.

As seções a seguir descrevem o uso de sinks de writer.



| Seção                                                                      | Descrição                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Adicionando os sinks ao writer](adding-sinks-to-the-writer.md)                 | Descreve como adicionar os sinks ao autor.                                        |
| [Enumerando os sinks](enumerating-sinks.md)                                   | Descreve como enumerar os sinks que foram adicionados ao autor.         |
| [Recebendo mensagens de erro de um sink](getting-error-messages-from-a-sink.md) | Descreve como configurar os sinks para entregar mensagens de status ao seu aplicativo. |
| [Uso de coletores de arquivos](using-file-sinks.md)                                     | Descreve como usar um sink de arquivo de writer para criar um arquivo ASF no disco.           |
| [Usando os sinks personalizados](using-custom-sinks.md)                                 | Descreve como criar e usar seus próprios sinks personalizados para fornecer dados ASF.       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMWriterAdvanced Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**IWMWriterSink Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)
</dt> <dt>

[**Escrevendo arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




