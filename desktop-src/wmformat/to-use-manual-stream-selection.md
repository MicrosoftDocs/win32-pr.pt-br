---
title: Para usar a seleção de fluxo manual
description: Para usar a seleção de fluxo manual
ms.assetid: 49ec283f-670a-4a0e-9477-c60a80919a1e
keywords:
- ASF (Advanced Systems Format), seleção de fluxo manual
- ASF (formato de sistemas avançados), seleção de fluxo manual
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (formato de sistemas avançados), leitores assíncronos
- ASF (Advanced Systems Format), seleção de fluxo
- ASF (formato de sistemas avançados), seleção de fluxo
- ASF (Advanced Systems Format), exclusão mútua
- ASF (formato de sistemas avançados), exclusão mútua
- leitores assíncronos, seleção de fluxo manual
- leitores assíncronos, seleção de fluxo
- fluxos, seleção manual
- exclusão mútua, seleção de fluxo manual
- fluxos, leitores assíncronos
- exclusão mútua, leitores assíncronos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87c493bc8f41bc2a03ba15832ed402939adbeff
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105770649"
---
# <a name="to-use-manual-stream-selection"></a>Para usar a seleção de fluxo manual

Ao fornecer exemplos não compactados com o objeto leitor, você pode entregá-los somente pelo número de saída. No caso de fluxos mutuamente exclusivos, isso significa que você pode receber amostras somente de um fluxo na exclusão mútua de cada vez. O processo de escolher qual fluxo mutuamente exclusivo a ser entregue é chamado de seleção de fluxo.

Para a exclusão mútua de taxa de bits, o leitor faz seleções de fluxo automaticamente com base nas condições no computador host na reprodução. Para outros tipos de exclusão mútua, o leitor fornecerá exemplos do fluxo padrão, a menos que você selecione manualmente um fluxo diferente. Também pode haver instâncias em que você deseja selecionar um fluxo manualmente de uma exclusão mútua de taxa de bits.

A seleção de fluxo manual está ativada ou desativada para o arquivo inteiro. Se um arquivo contiver exclusão mútua de taxa de bits e algum outro tipo de exclusão mútua, você deverá selecionar manualmente os fluxos com base na taxa de bits.

Para selecionar um fluxo mutuamente exclusivo manualmente, você deve executar as etapas a seguir.

1.  Recupere um ponteiro para a interface [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) do objeto leitor chamando **IWMReader:: QueryInterface**.
2.  Habilite a seleção de fluxo manual chamando [**IWMReaderAdvanced:: SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection).
3.  Para descobrir se um fluxo específico está selecionado, chame [**IWMReaderAdvanced:: GetStreamSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected). Você deve passar um ponteiro para uma variável do tipo de enumeração de [**\_ \_ seleção de fluxo WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection) . Quando a chamada retorna, o valor na variável descreverá o tipo de seleção atual do fluxo.
4.  Para selecionar um fluxo, chame [**IWMReaderAdvanced:: SetStreamsSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected). Esse método permite que você especifique vários fluxos ao mesmo tempo para a alternância de fluxo sincronizada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Lendo arquivos com o leitor assíncrono**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




