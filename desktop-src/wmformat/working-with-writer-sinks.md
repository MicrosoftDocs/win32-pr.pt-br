---
title: Trabalhando com coletores de gravador
description: Trabalhando com coletores de gravador
ms.assetid: 1ad28684-47d2-4ddb-bf18-22310f0392a0
keywords:
- ASF (Advanced Systems Format), coletores de gravador
- ASF (formato de sistemas avançados), coletores de gravador
- ASF (Advanced Systems Format), coletores
- ASF (formato de sistemas avançados), coletores
- coletores, coletores de gravador
- coletores de gravador, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 407e5bf2e87bfbf3084d19f75170a12be693d804d4d902f919096dca5aeab057
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194861"
---
# <a name="working-with-writer-sinks"></a>Trabalhando com coletores de gravador

o objeto do gravador do SDK do formato de mídia Windows processa dados de mídia de entrada em um fluxo de bits. No entanto, o objeto Writer não entrega o fluxo de bits para seu destino final (seja para um arquivo ou um local de rede). Para gravar o conteúdo do ASF em um formato utilizável, você deve usar coletores de gravador.

O objeto Writer dá suporte a três tipos de coletores: coletores de arquivos, coletores de rede e coletores de push. Um coletor de arquivos grava o conteúdo ASF em um arquivo ASF no disco. Um coletor de rede transmite o conteúdo do ASF de um endereço de rede. um coletor de push entrega dados a um servidor executando Windows Media Services para que o servidor possa disponibilizar o conteúdo para seu público-alvo. Você também pode criar seus próprios coletores para fornecer dados de ASF de qualquer maneira que seja necessária para seu aplicativo. Para obter informações sobre coletores de rede e coletores de push, consulte [enviando dados de ASF por meio de uma rede](sending-asf-data-over-a-network.md). O restante desta seção aborda os coletores de gravador.

Você pode configurar um ou mais coletores para cada instância do gravador que você usa. Cada coletor manipula apenas um único destino. Por exemplo, se você quiser escrever três arquivos ao mesmo tempo, deverá criar e configurar um coletor de arquivo separado para cada um.

As seções a seguir descrevem o uso de coletores de gravador.



| Seção                                                                      | Descrição                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Adicionando coletores ao gravador](adding-sinks-to-the-writer.md)                 | Descreve como adicionar coletores ao gravador.                                        |
| [Enumerando coletores](enumerating-sinks.md)                                   | Descreve como enumerar os coletores que foram adicionados ao gravador.         |
| [Obtendo mensagens de erro de um coletor](getting-error-messages-from-a-sink.md) | Descreve como configurar coletores para fornecer mensagens de status ao seu aplicativo. |
| [Uso de coletores de arquivos](using-file-sinks.md)                                     | Descreve como usar um coletor de arquivos do Writer para criar um arquivo ASF no disco.           |
| [Usando coletores personalizados](using-custom-sinks.md)                                 | Descreve como criar e usar seus próprios coletores personalizados para fornecer dados ASF.       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Interface IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)
</dt> <dt>

[**Gravando arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




