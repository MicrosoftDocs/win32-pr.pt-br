---
title: Para pausar ou parar a reprodução
description: Para pausar ou parar a reprodução
ms.assetid: 8e43ea80-36c7-4530-8ed3-dfdb64a3a2e3
keywords:
- ASF (Advanced Systems Format), pausando a reprodução
- ASF (Formato de Sistemas Avançados), pausando a reprodução
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (Formato de Sistemas Avançados), leitores assíncronos
- ASF (Advanced Systems Format), interrompendo a reprodução
- ASF (Formato de Sistemas Avançados), interrompendo a reprodução
- ASF (Advanced Systems Format), reprodução pausando ou parando
- ASF (Formato de Sistemas Avançados), pausa ou interrupção de reprodução
- leitores assíncronos, pausando a reprodução
- leitores assíncronos, interrompendo a reprodução
- leitores assíncronos, pausando ou parando de reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7ae7f3c1dd2c045a35b8d3ee8950ace849a032136371f9da7ff1bcc2b12de27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845361"
---
# <a name="to-pause-or-stop-playback"></a>Para pausar ou parar a reprodução

Quando você chama [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) para começar a reprodução de um arquivo, o leitor assíncrono continuará izando em seus próprios threads separados até que o final do arquivo seja atingido. Você pode pausar ou interromper a entrega de exemplos usando os métodos [**IWMReader::P ause**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-pause) ou [**IWMReader::Stop,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop) respectivamente.

## <a name="pausing"></a>Pausando

Quando você chama **IWMReader::P ause** para pausar a reprodução de um arquivo, o leitor acompanha a posição atual no arquivo. Para retomar a reprodução após pausar, chame [**IWMReader::Resume**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-resume). A reprodução será retomada a partir do ponto em que ela foi pausada.

## <a name="stopping"></a>Parando

Quando você chama **IWMReader::Stop** para interromper a reprodução de um arquivo, o leitor não acompanha nenhuma informação sobre o progresso da reprodução. Para usar **Parar** e retornar posteriormente ao ponto de interrupção, você deve economizar o tempo de apresentação do último exemplo entregue e usá-lo em sua chamada para **IWMReader::Start**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMReader Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Lendo arquivos com o Leitor Assíncrono**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




