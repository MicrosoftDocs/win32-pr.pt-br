---
description: Fluxo de dados no navegador de DVD
ms.assetid: 14f9cfa3-5ef6-419c-9196-2e4060549c03
title: Fluxo de dados no navegador de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29a981d2d7b528163abb53478e9e8f2ab88d46c0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646131"
---
# <a name="data-flow-in-the-dvd-navigator"></a>Fluxo de dados no navegador de DVD

O navegador de DVD tem métodos para parar e pausar a reprodução. Esses métodos são semelhantes, mas não idênticos, aos métodos **Stop** e **Pause** em [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol). Aqui está a diferença entre eles:

-   Os métodos **IDvdControl2** alteram o que o navegador de DVD lê do disco. Eles não alteram o estado do grafo.
-   Os métodos **IMediaControl** alteram o estado do grafo. Eles não alteram o que o navegador de DVD lê do disco. (Há uma exceção importante, explicada na próxima seção, relacionada ao método **Stop** ).

Por exemplo, [**IDvdControl2::P método ause**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause) emite o comando anexo J "Pausar \_ ", mas não pausa o gráfico de filtro. O método [**IMediaControl::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause) , por outro lado, pausa o grafo, mas não emite nenhum comando de DVD.

Em geral, use os métodos **IMediaControl::P ause** e **Stop** em vez dos métodos **IDvdControl2** correspondentes. Os métodos **IMediaControl** têm latências muito pequenas, enquanto os métodos **IDvdControl2** podem ter até dois segundos de latência.

Parando a reprodução

O comportamento de [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) depende de um sinalizador que você pode definir com o método [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) .

-   Se o \_ sinalizador ResetOnStop de DVD for **false**, **IMediaControl:: Stop** interromperá o grafo, mas não alterará o domínio do navegador de DVD. Quando você chamar executar novamente, a reprodução será retomada da posição atual.
-   Se \_ o DVD ResetOnStop for **true**, **IMediaControl:: Stop** fará com que o navegador de DVD seja redefinido. Quando você chama [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) novamente, o navegador de DVD é reproduzido do primeiro domínio de reprodução, como se você estivesse inserindo o DVD pela primeira vez.

O \_ sinalizador DVD ResetOnStop é **true** por padrão, para compatibilidade com aplicativos mais antigos. No entanto, em geral, você deve substituir o padrão e definir o sinalizador como **false**. O motivo é que determinados eventos podem fazer com que o grafo pare durante a reprodução. Por exemplo, se a resolução de vídeo for alterada, o gráfico de filtro será interrompido, reconectará o processador de vídeo e reiniciará. Se o DVD \_ ResetOnStop for **true**, a reprodução será reiniciada a partir do início do disco. Isso provavelmente não é o que o usuário espera.

No início do seu aplicativo, portanto, chame **SetOption** com o DVD \_ ResetOnStop definido como **false**. Se você quiser parar a reprodução e retomá-la do mesmo local, chame **IMediaControl:: Stop** ou **IMediaControl::P ause**. Se você quiser parar a reprodução e redefinir o disco, chame **SetOption** com DVD \_ ResetOnStop igual a **true**; em seguida, chame **IMediaControl:: Stop**; finalmente, chame **SetOption** novamente e redefina o DVD \_ ResetOnStop como **false**.

Pausando reprodução

Se você der ao navegador de DVD um comando enquanto o grafo estiver em pausa, o comando poderá não ser concluído até que o grafo seja executado novamente. Em algumas situações, isso pode causar um deadlock em seu aplicativo. Há duas regras que você deve seguir para evitar deadlocks:

-   Enquanto estiver em pausa, não emita mais de um comando de DVD assíncrono.
-   Enquanto estiver em pausa, não bloqueie o thread da interface do usuário do aplicativo ou o thread que altera o estado do grafo.

A segunda regra vale a pena examinar mais detalhadamente. Aqui estão alguns cenários específicos que podem causar um deadlock:

-   **Cenário**: enquanto está em pausa, o aplicativo emite um comando de DVD com o sinalizador de bloqueio. Isso pode causar um deadlock se o thread que emite o comando de DVD for o mesmo thread que emite o comando de execução. O comando de DVD é bloqueado até que o grafo seja executado, mas o grafo não pode ser executado até que o comando seja concluído.

    **Recomendação**: emita o comando DVD em um thread de trabalho separado ou não use o sinalizador de bloqueio.

-   **Cenário**: enquanto está em pausa, o aplicativo emite um comando de DVD e, em seguida, chama [**IDvdCmd:: WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) no objeto Command. Essa situação é equivalente ao exemplo anterior. Se você chamar **Wait** no thread da interface do usuário, o thread da interface do usuário não poderá executar o grafo até que o método **Wait** desbloqueie, mas o método **Wait** não será desbloqueado até que o grafo seja executado.

    **Recomendação**: chamada **Wait** em um thread de trabalho.

-   **Cenário**: enquanto o grafo está em execução, o aplicativo emite um comando de DVD com o sinalizador de bloqueio e, em seguida, chama a pausa de outro thread. Essa é uma possível condição de corrida porque o grafo pode pausar antes de o comando ser emitido. Se um dos dois threads for o thread da interface do usuário, você poderá causar um deadlock semelhante aos dois exemplos anteriores. Este exemplo ilustra a importância de escrever código de thread-safe se seu aplicativo usar vários threads.

    **Recomendação**: se você usar threads de trabalho, verifique se seu código é thread-safe.

-   **Cenário**: enquanto estiver em pausa, o aplicativo desabilitará o comando executar da interface do usuário e emitirá um comando DVD assíncrono. Esse caso não é estritamente um deadlock, porque o thread do aplicativo ainda está em execução. No entanto, o usuário agora é impedido de executar o grafo e, portanto, o comando nunca será concluído.

    **Recomendação**: ao pausar, sempre deixe o comando executar habilitado.

Procurando um DVD em um horário especificado

Para buscar com precisão um horário especificado em um disco, chame [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run). Em seguida, chame [**IDvdControl2::P layattime**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattime), especificando a hora e a configuração de *dwFlags* para o sinalizador de cmd de DVD \_ \_ \_ flush.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 



