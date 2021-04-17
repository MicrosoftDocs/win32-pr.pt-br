---
title: Para pausar ou parar a reprodução
description: Para pausar ou parar a reprodução
ms.assetid: 8e43ea80-36c7-4530-8ed3-dfdb64a3a2e3
keywords:
- ASF (Advanced Systems Format), pausando a reprodução
- ASF (formato de sistemas avançados), pausando a reprodução
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (formato de sistemas avançados), leitores assíncronos
- ASF (Advanced Systems Format), parando a reprodução
- ASF (formato de sistemas avançados), parando a reprodução
- ASF (Advanced Systems Format), reprodução Pausando ou parando
- ASF (formato de sistemas avançados), pausando ou parando reprodução
- leitores assíncronos, pausando a reprodução
- leitores assíncronos, parando a reprodução
- leitores assíncronos, pausando ou parando a reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728ce4c58f9198f605764d0f19d0d5f55c7f6c6b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104498980"
---
# <a name="to-pause-or-stop-playback"></a>Para pausar ou parar a reprodução

Quando você chama [**IWMReader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) para começar a reproduzir um arquivo, o leitor assíncrono continuará a ser processado em seus próprios threads separados até que o final do arquivo seja atingido. Você pode pausar ou parar a entrega de amostras usando os métodos [**IWMReader::P ause**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-pause) ou [**IWMReader:: Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop) , respectivamente.

## <a name="pausing"></a>Pausando

Quando você chama **IWMReader::P ause** para pausar a reprodução de um arquivo, o leitor controla a posição atual no arquivo. Para retomar a reprodução após a pausa, chame [**IWMReader:: resume**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-resume). A reprodução será retomada do ponto em que está em pausa.

## <a name="stopping"></a>Parando

Quando você chama **IWMReader:: Stop** para interromper a reprodução de um arquivo, o leitor não controla nenhuma informação sobre o progresso da reprodução. Para usar **parar** e depois retornar ao ponto de interrupção, você deve salvar o tempo de apresentação do último exemplo entregue e usá-lo em sua chamada para **IWMReader:: Start**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Lendo arquivos com o leitor assíncrono**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




