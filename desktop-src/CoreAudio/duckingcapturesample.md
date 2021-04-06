---
description: Este aplicativo de exemplo demonstra como abrir e fechar fluxos de comunicação e causar eventos de pato que um aplicativo pode obter para implementar a atenuação de fluxo.
ms.assetid: 9a2131b2-ec4a-492a-a277-bd26ec8d67e5
title: DuckingCaptureSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 636fe39e8fa27beee14ab17548f5929d1d937b20
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826675"
---
# <a name="duckingcapturesample"></a>DuckingCaptureSample

Este aplicativo de exemplo demonstra como abrir e fechar fluxos de comunicação e causar eventos de pato que um aplicativo pode obter para implementar a atenuação de fluxo. Esse aplicativo implementa um cliente de chat que usa APIs de áudio de núcleo para ler dados de áudio de um dispositivo de comunicação e reproduzi-lo no dispositivo de saída.

Este tópico inclui as seções a seguir.

-   [Descrição](#description)
-   [Requirements](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)
-   [Tópicos relacionados](#related-topics)

## <a name="description"></a>Descrição

Este exemplo demonstra os recursos a seguir.

-   [API MMDevice](mmdevice-api.md) para enumeração e seleção de dispositivo de multimídia.
-   [WASAPI](wasapi.md) para acessar o dispositivo de captura e processamento de comunicações, operações de gerenciamento de fluxo e manipulação de eventos de pato.
-   [APIs de onda](/previous-versions//ms713499(v=vs.85)) para acessar o dispositivo de comunicações e capturar a entrada de áudio.

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão   |
|----------------------------------------------------------------|-----------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio 2008                                             |           |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível nos locais a seguir.



| Local    | Caminho/URL                                                                                              |
|-------------|-------------------------------------------------------------------------------------------------------|
| SDK do Windows | \\Arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ áudio multimídia \\ \\ DuckingCaptureSample \\ ... |



 

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo de DuckingCaptureSample, use as seguintes etapas:

1.  Abra o DuckingCaptureSample. sln no Visual Studio 2008.
2.  De dentro da janela, selecione a configuração da solução de **depuração** ou **versão** , selecione o menu **Compilar** na barra de menus e selecione a opção **Compilar** . Se você não abrir o Visual Studio a partir do Shell CMD para o SDK, o Visual Studio não terá acesso ao ambiente de compilação do SDK. Nesse caso, o exemplo não será compilado, a menos que você defina explicitamente a variável de ambiente MSSdk, que é usada no arquivo de projeto, DuckingCaptureSample. vcproj.

## <a name="running-the-sample"></a>Executando o exemplo

Se você compilar o aplicativo com êxito, um arquivo executável, DuckingCaptureSample.exe, será gerado. Para executá-lo, selecione **Iniciar Depuração** ou **Iniciar sem Depurar** no menu **depurar** ou digite `DuckingCaptureSample` uma janela de comando.

O DuckingCaptureSample fornece ao usuário duas implementações para capturar áudio do dispositivo de console padrão: WASAPI e APIs de onda. Para iniciar uma sessão de captura, selecione um modo e clique em **Iniciar** na interface do usuário do aplicativo. Para encerrar a sessão, clique em **parar**. Dependendo do dispositivo especificado pelo usuário (entrada ou saída), o aplicativo usa a API MMDevice para obter uma referência ao dispositivo de comunicação de captura ou de renderização padrão. Depois que o usuário inicia uma sessão de bate-papo, o aplicativo executa as seguintes tarefas:

-   Cria e inicializa um cliente de áudio no modo controlado por evento.
-   Associa o cliente ao identificador de evento que sinaliza que as amostras estão prontas para captura ou renderização.
-   Configura um cliente de captura e um cliente de renderização para o transporte.
-   Cria o thread de chat e inicia o mecanismo de áudio.

Para capturar dados de áudio, com cada passagem de processamento, o exemplo usa o cliente de captura para obter a quantidade total de dados capturados que estão disponíveis no buffer, ler dados do dispositivo de entrada padrão e liberar o pacote e disponibilizar o buffer para ler o próximo conjunto de dados capturados.

Para renderização, o aplicativo determina a quantidade de dados que são enfileirados para reprodução no buffer de ponto de extremidade de captura. Portanto, ele grava no buffer e libera o buffer na preparação para o próximo passo de processamento até que todos os dados tenham sido gravados. Para renderização, os quadros silenciosos são inscritos para impedir que o mecanismo de áudio seja reparado na inicialização. DuckingCaptureSample também mostra como ocultar o fluxo de renderização do mixer de volume.

Para obter mais informações sobre o recurso de atenuação de fluxo, consulte [usando um dispositivo de comunicação](using-the-communication-device.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de SDK que usam as APIs de áudio principal](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 
