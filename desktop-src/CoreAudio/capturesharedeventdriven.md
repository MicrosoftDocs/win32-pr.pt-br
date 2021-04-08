---
description: Este aplicativo de exemplo usa as APIs de áudio principais para capturar dados de áudio de um dispositivo de entrada especificado pelo usuário e grava-os em um arquivo. wav nomeado exclusivamente no diretório atual. Este exemplo demonstra o buffer controlado por eventos.
ms.assetid: 6ff3bc23-550e-41b7-b37c-35d552b29e20
title: CaptureSharedEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 339bd02fcb94f65be558c2dce767747ebf4fab98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089249"
---
# <a name="capturesharedeventdriven"></a>CaptureSharedEventDriven

Este aplicativo de exemplo usa as APIs de áudio principais para capturar dados de áudio de um dispositivo de entrada especificado pelo usuário e grava-os em um arquivo. wav nomeado exclusivamente no diretório atual. Este exemplo demonstra o buffer controlado por eventos.

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
-   [WASAPI](wasapi.md) para operações de gerenciamento de fluxo, como iniciar e interromper o fluxo e alternar o fluxo.

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão   |
|----------------------------------------------------------------|-----------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível nos locais a seguir.



| Local    | Caminho/URL                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| SDK do Windows | \\Arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ áudio multimídia \\ \\ CaptureSharedEventDriven \\ ... |



 

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo de CaptureSharedEventDriven, use as seguintes etapas:

1.  Abra o Shell CMD para o SDK do Windows e altere para o diretório de exemplo CaptureSharedEventDriven.
2.  Execute o comando `start WASAPICaptureSharedEventDriven.sln` no diretório CaptureSharedEventDriven para abrir o projeto WASAPICaptureSharedEventDriven na janela do Visual Studio.
3.  De dentro da janela, selecione a configuração da solução de **depuração** ou **versão** , selecione o menu **Compilar** na barra de menus e selecione a opção **Compilar** . Se você não abrir o Visual Studio a partir do Shell CMD para o SDK, o Visual Studio não terá acesso ao ambiente de compilação do SDK. Nesse caso, o exemplo não será compilado, a menos que você defina explicitamente a variável de ambiente MSSdk, que é usada no arquivo de projeto, WASAPICaptureSharedEventDriven. vcproj.

## <a name="running-the-sample"></a>Executando o exemplo

Se você criar o aplicativo de demonstração com êxito, um arquivo executável, WASAPICaptureSharedEventDriven.exe, será gerado. Para executá-lo, digite `WASAPICaptureSharedEventDriven` uma janela de comando seguida por argumentos obrigatórios ou opcionais. O exemplo a seguir mostra como executar o exemplo especificando a duração da captura no dispositivo multimídia padrão.

`WASAPICaptureSharedEventDriven.exe -d 20 -multimedia`

A tabela a seguir mostra os argumentos.

| Argumento        | Descrição                                                |
|-----------------|------------------------------------------------------------|
| -?              | Mostra a ajuda.                                                |
| -H              | Mostra a ajuda.                                                |
| -l              | Latência de captura de áudio em milissegundos.                     |
| -d              | Duração da captura de áudio em segundos.                         |
| -M              | Desabilita o uso do MMCSS.                                 |
| -console        | Use o dispositivo de console padrão.                            |
| -comunicações | Use o dispositivo de comunicação padrão.                      |
| -multimídia     | Use o dispositivo multimídia padrão.                         |
| -ponto de extremidade       | Use o identificador de ponto de extremidade especificado no valor de opção. |



 

Se o aplicativo for executado sem argumentos, ele enumerará os dispositivos disponíveis e solicitará que o usuário selecione um dispositivo para a sessão de captura. Os dispositivos de console, comunicação e multimídia padrão são listados seguidos por dispositivos e os identificadores de ponto de extremidade. Se nenhuma duração for especificada, o fluxo de áudio do dispositivo especificado será capturado por 10 segundos. O aplicativo grava os dados capturados em um arquivo. wav nomeado exclusivamente.

CaptureSharedEventDriven demonstra o buffer controlado por eventos. O cliente de áudio instanciado para este exemplo está configurado para ser executado no modo compartilhado e o processamento do cliente do buffer de áudio é feito com eventos definindo o sinalizador **AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK** na chamada para [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize). O exemplo mostra como o cliente deve fornecer um identificador de evento ao sistema chamando o método [**IAudioClient:: SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) . Depois que a sessão de captura começa e o fluxo é iniciado, o mecanismo de áudio sinaliza o identificador de evento fornecido para notificar o cliente sempre que um buffer se tornar pronto para o cliente processar. Os dados de áudio também podem ser processados em um loop controlado por temporizador. Esse modo é demostrated no exemplo de [CaptureSharedTimerDriven](capturesharedtimerdriven.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de SDK que usam as APIs de áudio principal](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



