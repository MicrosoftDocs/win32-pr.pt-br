---
description: Este aplicativo de exemplo demonstra a atenuação de fluxo implementando um player de mídia que mostra o comportamento de atenuação padrão fornecido pelo sistema, opta de eventos de pato e implementa manipulação personalizada quando eventos de pato são recebidos.
ms.assetid: 667c8751-1d17-4b59-8ced-ed5f0c333ae9
title: DuckingMediaPlayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aab5a469ec2a7fb1551980d0a08a758e8e8e8f522831dc2148b2d8fb222ecdfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828277"
---
# <a name="duckingmediaplayer"></a>DuckingMediaPlayer

Este aplicativo de exemplo demonstra a atenuação de fluxo implementando um player de mídia que mostra o comportamento de atenuação padrão fornecido pelo sistema, opta de eventos de pato e implementa manipulação personalizada quando eventos de pato são recebidos. Este exemplo deve ser usado em juntamente com [DuckingCaptureSample](duckingcapturesample.md). Para obter mais informações sobre o pato ou atenuação de fluxo, consulte [experiência de pato padrão](stream-attenuation.md).

Este tópico inclui as seções a seguir.

-   [Descrição](#description)
-   [Requirements](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)
-   [Tópicos relacionados](#related-topics)

## <a name="description"></a>Descrição

Este exemplo demonstra os recursos a seguir.

-   DirectShow reproduzir um arquivo de mídia.
-   [WASAPI](wasapi.md) para gerenciamento de fluxo e manipulação de eventos de pato.

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão   |
|----------------------------------------------------------------|-----------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível nos locais a seguir.



| Localização    | Caminho/URL                                                                                            |
|-------------|-----------------------------------------------------------------------------------------------------|
| SDK do Windows | \\arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ áudio multimídia \\ \\ DuckingMediaPlayer \\ ... |



 

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo de DuckingMediaPlayer, use as seguintes etapas:

1.  abra o DuckingMediaPlayer. sln no Visual Studio 2008.
2.  De dentro da janela, selecione a configuração da solução de **depuração** ou **versão** , selecione o menu **Compilar** na barra de menus e selecione a opção **Compilar** . se você não abrir Visual Studio do shell CMD para o SDK, Visual Studio não terão acesso ao ambiente de compilação do sdk. Nesse caso, o exemplo não será compilado, a menos que você defina explicitamente a variável de ambiente MSSdk, que é usada no arquivo de projeto, DuckingMediaPlayer. vcproj.

## <a name="running-the-sample"></a>Executando o exemplo

Se você compilar o aplicativo com êxito, um arquivo executável, DuckingMediaPlayer.exe, será gerado. Para executá-lo, selecione **Iniciar Depuração** ou **Iniciar sem Depurar** no menu **depurar** ou digite `DuckingMediaPlayer` uma janela de comando.

Para exibir uma demonstração do patoing, você deve executar DuckingMediaPlayer e DuckingCaptureSample simultaneamente. DuckingCaptureSample abre um fluxo de comunicação e sinaliza o sistema para gerar um evento de patoing. O DuckingMediaPlayer é notificado pelo sistema quando ocorre um evento de patoing e o player de mídia executa a ação solicitada pelo usuário.

Para desabilitar o comportamento de pato:

1.  Na janela DuckingCaptureSample, selecione **usar dispositivo de entrada padrão** e clique em **Iniciar** para iniciar uma sessão de captura do dispositivo de comunicação.
2.  No DuckingMediaPlayer, selecione um arquivo de mídia a ser reproduzido e especifique a opção de pato como **recusar o pato**.

Observe que o arquivo de mídia é reproduzido sem nenhuma interrupção. Os eventos gerados pelo sistema quando o fluxo de comunicação aberto são ignorados.

Para demonstrar o comportamento padrão de pato fornecido pelo sistema, faça o seguinte:

1.  Selecione a opção **sons** no painel de controle. Na guia **comunicações** , selecione **reduzir o volume de outros sons em 80%**.
2.  Na janela DuckingCaptureSample, selecione **usar dispositivo de entrada padrão** e clique em **Iniciar** para iniciar uma sessão de captura do dispositivo de comunicação.
3.  No DuckingMediaPlayer, selecione um arquivo de mídia a ser reproduzido, sem escolher nenhuma das opções de pato.
4.  Na janela DuckingCaptureSample, clique em **parar** para interromper o fluxo de comunicação.

Observe que quando o DuckingCaptureSample abre o fluxo de comunicação, o arquivo de mídia jogado por DuckingMediaPlayer é reproduzido sem interrupção, mas o nível de volume é reduzido. Quando a sessão de comunicação é interrompida, o volume é redefinido para a configuração original. Esse comportamento de atenuação de fluxo é o comportamento padrão de pato implementado pelo sistema.

Para exibir um comportamento de pato personalizado implementado pelo Player de mídia:

1.  Na janela DuckingCaptureSample, selecione **usar dispositivo de entrada padrão** e clique em **Iniciar** para iniciar uma sessão de captura do dispositivo de comunicação.
2.  No DuckingMediaPlayer, selecione um arquivo de mídia a ser reproduzido e especifique a opção de pato como **pausa no pato**.
3.  Na janela DuckingCaptureSample, clique em **parar** para interromper o fluxo de comunicação.

Observe que quando o DuckingCaptureSample abre o fluxo de comunicação, o arquivo de mídia jogado por DuckingMediaPlayer é pausado. A reprodução é retomada quando a sessão de comunicação é interrompida. Esse comportamento de atenuação de fluxo é o comportamento de pato implementado pelo Player de mídia.

DuckingMediaPlayer também demonstra como integrar o controle de volume para cada aplicativo com o mixer de volume.

Para obter mais informações sobre o recurso de atenuação de fluxo, consulte [experiência de pato padrão](stream-attenuation.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de SDK que usam as APIs de áudio principal](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



