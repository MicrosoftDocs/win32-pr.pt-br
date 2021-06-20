---
description: Este aplicativo de exemplo, que demonstra o buffer controlado por temporizador, usa as APIs de áudio principais para processar dados de áudio para um dispositivo de saída especificado pelo usuário.
ms.assetid: eae7d896-77ef-4340-bd77-1f3333166987
title: RenderSharedTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89d2814f359668f8724d3deb65a7c2a9eeff5b06
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410089"
---
# <a name="rendersharedtimerdriven"></a>RenderSharedTimerDriven

Este aplicativo de exemplo usa as APIs de áudio principais para renderizar dados de áudio para um dispositivo de saída especificado pelo usuário. Este exemplo demonstra o buffer controlado por temporizador para um cliente de renderização no modo compartilhado. Para um fluxo de modo compartilhado, o cliente compartilha o buffer de ponto de extremidade com o mecanismo de áudio.

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
-   WASAPI para operações de gerenciamento de fluxo.

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão   |
|----------------------------------------------------------------|-----------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível nos locais a seguir.



| Location    | Caminho/URL                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| SDK do Windows | \\Arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ áudio multimídia \\ \\ RenderSharedTimerDriven \\ ... |



 

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo de RenderSharedTimerDriven, use as seguintes etapas:

1.  Abra o Shell CMD para o SDK do Windows e altere para o diretório de exemplo RenderSharedTimerDriven.
2.  Execute o comando `start WASAPIRenderSharedTimerDriven.sln` no diretório RenderSharedTimerDriven para abrir o projeto WASAPIRenderSharedTimerDriven na janela do Visual Studio.
3.  De dentro da janela, selecione a configuração da solução de **depuração** ou **versão** , selecione o menu **Compilar** na barra de menus e selecione a opção **Compilar** . Se você não abrir o Visual Studio a partir do Shell CMD para o SDK, o Visual Studio não terá acesso ao ambiente de compilação do SDK. Nesse caso, o exemplo não será compilado, a menos que você defina explicitamente a variável de ambiente MSSdk, que é usada no arquivo de projeto, WASAPIRenderSharedTimerDriven. vcproj.

## <a name="running-the-sample"></a>Executando o exemplo

Se você criar o aplicativo de demonstração com êxito, um arquivo executável, WASAPIRenderSharedTimerDriven.exe, será gerado. Para executá-lo, digite `WASAPIRenderSharedTimerDriven` uma janela de comando seguida por argumentos obrigatórios ou opcionais. O exemplo a seguir mostra como executar o exemplo especificando a duração da reprodução no dispositivo multimídia padrão.

`WASAPIRenderSharedTimerDriven.exe -d 20 -multimedia`

A tabela a seguir mostra os argumentos.

| Argumento        | Descrição                                                |
|-----------------|------------------------------------------------------------|
| -?              | Mostra a ajuda.                                                |
| -H              | Mostra a ajuda.                                                |
| -f              | Frequência de onda do seno em Hz.                                 |
| -l              | Latência de renderização de áudio em milissegundos.                      |
| -d              | Duração da onda do seno em segundos.                             |
| -M              | Desabilita o uso do MMCSS.                                 |
| -console        | Use o dispositivo de console padrão.                            |
| -comunicações | Use o dispositivo de comunicação padrão.                      |
| -multimídia     | Use o dispositivo multimídia padrão.                         |
| -ponto de extremidade       | Use o identificador de ponto de extremidade especificado no valor de opção. |



 

Se o aplicativo for executado sem argumentos, ele enumerará os dispositivos disponíveis e solicitará que o usuário selecione um dispositivo para a sessão de renderização. Depois que o usuário especifica um dispositivo, o aplicativo renderiza uma onda de seno a 440 Hz por 10 segundos. Esses valores podem ser modificados especificando-se os valores de opção-f e-d.

RenderSharedTimerDriven demonstra o buffer controlado por temporizador. Nesse modo, o cliente deve aguardar por um período de tempo (metade da latência, especificado pelo valor da opção-d, em milissegundos). Quando o cliente é ativado, metade do período de processamento, ele obtém o próximo conjunto de amostras do mecanismo. Antes de cada passagem de processamento no loop de buffer, o cliente deve descobrir a quantidade de dados a serem renderizados para que os dados não estourem o buffer.

Os dados de áudio a serem reproduzidos no dispositivo especificado podem ser processados habilitando o buffer controlado por eventos. Esse modo é demonstrado no exemplo de [RenderSharedEventDriven](rendersharedeventdriven.md) .

Para obter mais informações sobre como renderizar um fluxo, consulte [renderizando um fluxo](rendering-a-stream.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de SDK que usam as APIs de áudio principal](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



