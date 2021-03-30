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
ms.openlocfilehash: 1d5b690d9e1ab25d15f7c1e8612bf20e32f87c81
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640113"
---
# <a name="working-with-writer-sinks"></a>Trabalhando com coletores de gravador

O objeto gravador do SDK do Windows Media Format processa dados de mídia de entrada em um fluxo de bits. No entanto, o objeto Writer não entrega o fluxo de bits para seu destino final (seja para um arquivo ou um local de rede). Para gravar o conteúdo do ASF em um formato utilizável, você deve usar coletores de gravador.

O objeto Writer dá suporte a três tipos de coletores: coletores de arquivos, coletores de rede e coletores de push. Um coletor de arquivos grava o conteúdo ASF em um arquivo ASF no disco. Um coletor de rede transmite o conteúdo do ASF de um endereço de rede. Um coletor de push entrega dados a um servidor que executa os serviços de mídia do Windows para que o servidor possa disponibilizar o conteúdo para seu público-alvo. Você também pode criar seus próprios coletores para fornecer dados de ASF de qualquer maneira que seja necessária para seu aplicativo. Para obter informações sobre coletores de rede e coletores de push, consulte [enviando dados de ASF por meio de uma rede](sending-asf-data-over-a-network.md). O restante desta seção aborda os coletores de gravador.

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

 

 




