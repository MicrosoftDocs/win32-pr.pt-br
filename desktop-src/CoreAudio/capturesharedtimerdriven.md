---
description: Este aplicativo de exemplo usa as APIs de áudio principais para capturar dados de áudio de um dispositivo de entrada especificado pelo usuário e grava-os em um arquivo. wav nomeado exclusivamente no diretório atual. Este exemplo demonstra o buffer controlado por temporizador.
ms.assetid: 06124b99-89b3-4dfa-b989-a54746ecd697
title: CaptureSharedTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6d9e8cbd686bdd71804ed067a5b3d9ff36ed8271c8b0edb04b8077ca162fbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957375"
---
# <a name="capturesharedtimerdriven"></a>CaptureSharedTimerDriven

Este aplicativo de exemplo usa as APIs de áudio principais para capturar dados de áudio de um dispositivo de entrada especificado pelo usuário e grava-os em um arquivo. wav nomeado exclusivamente no diretório atual. Este exemplo demonstra o buffer controlado por temporizador.

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
-   [WASAPI](wasapi.md) para operações de gerenciamento de fluxo.

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão   |
|----------------------------------------------------------------|-----------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível nos locais a seguir.



| Localização    | Caminho/URL                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| SDK do Windows | \\arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ áudio multimídia \\ \\ CaptureSharedTimerDriven \\ ... |



 

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo de CaptureSharedTimerDriven, use as seguintes etapas:

1.  abra o shell CMD para o SDK do Windows e altere para o diretório de exemplo CaptureSharedTimerDriven.
2.  execute o comando `start WASAPICaptureSharedTimerDriven.sln` no diretório CaptureSharedTimerDriven para abrir o projeto WASAPICaptureSharedTimerDriven na janela Visual Studio.
3.  De dentro da janela, selecione a configuração da solução de **depuração** ou **versão** , selecione o menu **Compilar** na barra de menus e selecione a opção **Compilar** . se você não abrir Visual Studio do shell CMD para o SDK, Visual Studio não terão acesso ao ambiente de compilação do sdk. Nesse caso, o exemplo não será compilado, a menos que você defina explicitamente a variável de ambiente MSSdk, que é usada no arquivo de projeto, WASAPICaptureSharedTimerDriven. vcproj.

## <a name="running-the-sample"></a>Executando o exemplo

Se você criar o aplicativo de demonstração com êxito, um arquivo executável, WASAPICaptureSharedTimerDriven.exe, será gerado. Para executá-lo, digite `WASAPICaptureSharedTimerDriven` uma janela de comando seguida por argumentos obrigatórios ou opcionais. O exemplo a seguir mostra como executar o exemplo especificando a duração da captura no dispositivo multimídia padrão.

`WASAPICaptureSharedTimerDriven.exe -d 20 -multimedia`

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

CaptureSharedTimerDriven demonstra o buffer controlado por temporizador. Nesse modo, o cliente deve aguardar por um período de tempo (metade da latência, especificado pelo valor da opção-d, em milissegundos). Quando o cliente é ativado, metade do período de processamento, ele obtém o próximo conjunto de amostras do mecanismo. Antes de cada passagem de processamento no loop de buffer, o cliente deve descobrir a quantidade de dados de captura disponíveis para que os dados não estourem o buffer de captura. Os dados de áudio que são capturados do dispositivo especificado podem ser processados habilitando o buffer controlado por eventos. Esse modo é demonstrado no exemplo de [CaptureSharedEventDriven](capturesharedeventdriven.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de SDK que usam as APIs de áudio principal](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



