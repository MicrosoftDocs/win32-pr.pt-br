---
title: Para escrever exemplos
description: Para escrever exemplos
ms.assetid: 9ce10a77-9e80-45e0-a7e7-2ffdf8b57773
keywords:
- ASF (Advanced Systems Format), exemplos de gravação
- ASF (formato de sistemas avançados), escrevendo exemplos
- ASF (Advanced Systems Format), passando amostras para o gravador
- ASF (formato de sistemas avançados), passando amostras para o gravador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 738014b3c42441e878105d12a8ebf23ce4b266f7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365555"
---
# <a name="to-write-samples"></a>Para escrever exemplos

Quando você tiver identificado e configurado as entradas para o arquivo que está gravando, poderá começar a passar amostras para o gravador. Você deve passar os exemplos na ordem de tempo de apresentação, se possível, para tornar o processo de gravação mais eficiente.

Antes de passar qualquer amostra, você deve definir o gravador para aceitá-las chamando [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

Para passar um exemplo para o gravador, execute as seguintes etapas:

1.  Aloque um buffer e recupere um ponteiro para a interface [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) chamando [**IWMWriter:: AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).
2.  Recupere o endereço do buffer criado na etapa 1 chamando [**INSSBuffer:: GetBuffer**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbuffer).
3.  Copie os dados de exemplo para o local do buffer, certificando-se de que o exemplo passado caiba no buffer alocado. Você pode usar qualquer função de cópia de memória para copiar seus dados. Uma opção comum é o memcpy, que está incluído na biblioteca padrão de tempo de execução do C.
4.  Atualize a quantidade de dados usados no buffer para refletir o tamanho real do exemplo chamando [**INSSBuffer:: SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).
5.  Passe a interface de buffer para o gravador junto com o número de entrada e o tempo de amostra usando o método [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) . Todos os exemplos de áudio de uma entrada representam a mesma duração do conteúdo, de modo que você pode calcular o tempo de amostra adicionando a duração de amostra a um total em execução. Para vídeo, você precisa calcular a hora com base na taxa de quadros.

O **WriteSample** funciona de forma assíncrona e pode não terminar de gravar os dados do buffer antes que seu aplicativo esteja pronto para chamar o método novamente. Portanto, é importante chamar **AllocateSample** uma vez para cada chamada para **WriteSample**. No entanto, você pode liberar a interface **INSSBuffer** imediatamente após chamar **WriteSample**.

Quando terminar de passar amostras, chame [**IWMWriter:: redação**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting).

**Observação** É importante que amostras de todos os fluxos no arquivo sejam passadas para o gravador em sincronização entre si. Ou seja, sempre que possível, você deve passar amostras para o gravador em ordem de tempo de apresentação dentro da tolerância de sincronização especificada em [**IWMWriterAdvanced:: SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance). Os melhores resultados são obtidos quando os dados são entregues a cada fluxo em unidades de um segundo ou menos.

Os fluxos também devem terminar quase ao mesmo tempo. Por exemplo, você não deve gravar um arquivo com um fluxo de áudio com 45 segundos de comprimento e um fluxo de vídeo que tenha 50 segundos de comprimento. Se você codificar esse arquivo com entradas inalteradas, alguns dos dados de áudio no final do fluxo serão descartados (mesmo que seja o fluxo mais curto). Para fazer com que a codificação do arquivo funcione, você deve adicionar 5 segundos de silêncio à entrada de áudio para que um fluxo não termine vários segundos antes de outro. Não é necessário que os tipos de fluxo com amostras intermitentes, como fluxos de texto ou de imagem, sejam preenchidos dessa maneira. Fluxos de comando de script também devem seguir todas essas regras.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[**Interface IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Gravando arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




