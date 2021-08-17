---
description: Dados Flow no Navegador de DVD
ms.assetid: 14f9cfa3-5ef6-419c-9196-2e4060549c03
title: Dados Flow no Navegador de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e649edfacf0a1fad56cfbe8e73a5e1e9aaf099b9c17463858bf776ab06605c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953355"
---
# <a name="data-flow-in-the-dvd-navigator"></a>Dados Flow no Navegador de DVD

O Navegador de DVD tem métodos para parar e pausar a reprodução. Esses métodos são semelhantes , mas não idênticos, aos métodos **Stop** e **Pause** no [**IMediaControl.**](/windows/desktop/api/Control/nn-control-imediacontrol) Esta é a diferença entre eles:

-   Os **métodos IDvdControl2** alteram o que o Navegador de DVD lê do disco. Eles não alteram o estado do grafo.
-   Os **métodos IMediaControl** alteram o estado do grafo. Eles não alteram o que o Navegador de DVD lê do disco. (Há uma exceção importante, explicada na próxima seção, relacionada ao **método Stop.)**

Por exemplo, [**o método IDvdControl2::P ause**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause) emite o comando Anexo J "Pausar Em", mas não \_ pausa o grafo de filtro. O [**método IMediaControl::P ause,**](/windows/desktop/api/Control/nf-control-imediacontrol-pause) por outro lado, pausa o grafo, mas não em nenhum comando de DVD.

Em geral, use os métodos **IMediaControl::P ause** e **Stop** em vez dos métodos **IDvdControl2** correspondentes. Os **métodos IMediaControl** têm latências muito pequenas, enquanto os métodos **IDvdControl2** podem ter até dois segundos de latência.

Interrompendo a reprodução

O comportamento de [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) depende de um sinalizador que você pode definir com o [**método IDvdControl2::SetOption.**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption)

-   Se o sinalizador RESETOnStop do DVD for \_ **FALSE,** **IMediaControl::Stop** interromperá o grafo, mas não alterará o domínio do Navegador de DVD. Quando você chama executar novamente, a reprodução é retomada da posição atual.
-   Se DVD \_ ResetOnStop for **TRUE,** **IMediaControl::Stop** faz com que o Navegador de DVD seja redefinido. Quando você chama [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) novamente, o Navegador de DVD é executado do domínio First Play, como se você estivesse inserindo o DVD pela primeira vez.

O sinalizador \_ RESETOnStop de DVD é **TRUE** por padrão, para compatibilidade com aplicativos mais antigos. Em geral, no entanto, você deve substituir o padrão e definir o sinalizador como **FALSE.** O motivo é que determinados eventos podem fazer com que o grafo pare durante a reprodução. Por exemplo, se a resolução de exibição mudar, o grafo de filtro será interrompido, reconectará o renderador de vídeo e reiniciará. Se DVD \_ ResetOnStop for **TRUE,** a reprodução será reiniciada desde o início do disco. Isso provavelmente não é o que o usuário espera.

No início do aplicativo, portanto, chame **SetOption com** DVD \_ ResetOnStop definido como **FALSE.** Se você quiser interromper a reprodução e retomá-la do mesmo local, chame **IMediaControl::Stop** ou **IMediaControl::P ause**. Se você quiser interromper a reprodução e redefinir o disco, chame **SetOption** com DVD ResetOnStop igual a \_ **TRUE;** em seguida, chame **IMediaControl::Stop**; por fim, chame **SetOption** novamente e redefinir ResetOnStop de DVD \_ como **FALSE.**

Pausando a reprodução

Se você der ao Navegador de DVD um comando enquanto o grafo estiver em pausa, o comando poderá não ser concluído até que o grafo seja executado novamente. Em algumas situações, isso pode causar um deadlock em seu aplicativo. Há duas regras que você deve seguir para evitar deadlocks:

-   Enquanto estiver em pausa, não emito mais de um comando de DVD assíncrono.
-   Enquanto estiver em pausa, não bloqueie o thread de interface do usuário do aplicativo ou o thread que altera o estado do grafo.

A segunda regra vale a pena examinar mais detalhadamente. Aqui estão alguns cenários específicos que podem causar um deadlock:

-   **Cenário:** enquanto estiver em pausa, o aplicativo emite um comando de DVD com o sinalizador de bloqueio. Isso poderá causar um deadlock se o thread que emite o comando DVD for o mesmo thread que emite o comando run. O comando DVD é bloco até que o grafo seja executado, mas o grafo não pode ser executado até que o comando seja concluído.

    **Recomendação**: emita o comando DVD em um thread de trabalho separado ou não use o sinalizador de bloqueio.

-   **Cenário:** enquanto estiver em pausa, o aplicativo emite um comando dvd e, em seguida, chama [**IDvdCmd::WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) no objeto de comando. Essa situação é equivalente ao exemplo anterior. Se você chamar **Wait** do thread da interface do usuário, o thread da interface do usuário não poderá executar o grafo até que o método **Wait** seja desbloqueado, mas o método **Wait** não será desbloqueado até que o grafo seja executado.

    **Recomendação:** chame **Wait** em um thread de trabalho.

-   **Cenário:** enquanto o grafo está em execução, o aplicativo emite um comando de DVD com o sinalizador de bloqueio e, em seguida, chama pause de outro thread. Essa é uma condição de corrida possível porque o grafo pode pausar antes que o comando seja emitido. Se um dos dois threads for o thread da interface do usuário, você poderá causar um deadlock semelhante aos dois exemplos anteriores. Este exemplo ilustra a importância de escrever código thread-safe se seu aplicativo usar vários threads.

    **Recomendação**: se você usar threads de trabalho, certifique-se de que seu código é thread-safe.

-   **Cenário:** enquanto pausado, o aplicativo desabilita o comando run da interface do usuário e emite um comando de DVD assíncrono. Esse caso não é estritamente um deadlock, porque o thread do aplicativo ainda está em execução. No entanto, o usuário agora é impedido de executar o grafo e, portanto, o comando nunca será concluído.

    **Recomendação:** ao pausar, sempre deixe o comando executar habilitado.

Buscando um DVD para um horário especificado

Para buscar com precisão um horário especificado em um disco, chame [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run). Em seguida, [**chame IDvdControl2::P layAtTime**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattime), especificando a hora e definindo *dwFlags* como Dvd \_ CMD \_ FLAG \_ Flush.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 



