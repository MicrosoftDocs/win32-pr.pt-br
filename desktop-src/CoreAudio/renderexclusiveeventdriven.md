---
description: Este aplicativo de exemplo usa as APIs de áudio principais para renderizar dados de áudio para um dispositivo de saída especificado pelo usuário.
ms.assetid: 3a2e3fa6-2d6a-4ab0-a531-d1c968458e96
title: RenderExclusiveEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3b94fa423cd4d4e7dc7121e927696529bfadf9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010214"
---
# <a name="renderexclusiveeventdriven"></a>RenderExclusiveEventDriven

Este aplicativo de exemplo usa as APIs de áudio principais para renderizar dados de áudio para um dispositivo de saída especificado pelo usuário. Este exemplo demonstra o buffer controlado por eventos para um cliente de renderização em modo exclusivo. Para um fluxo de modo exclusivo, o cliente compartilha o buffer de ponto de extremidade com o dispositivo de áudio.

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



| Local    | Caminho/URL                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| SDK do Windows | \\Arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ áudio multimídia \\ \\ RenderExclusiveEventDriven \\ ... |



 

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo de RenderExclusiveEventDriven, use as seguintes etapas:

1.  Abra o Shell CMD para o SDK do Windows e altere para o diretório de exemplo RenderExclusiveEventDriven.
2.  Execute o comando `start WASAPIRenderExclusiveEventDriven.sln` no diretório RenderExclusiveEventDriven para abrir o projeto WASAPIRenderExclusiveEventDriven na janela do Visual Studio.
3.  De dentro da janela, selecione a configuração da solução de **depuração** ou **versão** , selecione o menu **Compilar** na barra de menus e selecione a opção **Compilar** . Se você não abrir o Visual Studio a partir do Shell CMD para o SDK, o Visual Studio não terá acesso ao ambiente de compilação do SDK. Nesse caso, o exemplo não será compilado, a menos que você defina explicitamente a variável de ambiente MSSdk, que é usada no arquivo de projeto, WASAPIRenderExclusiveEventDriven. vcproj.

## <a name="running-the-sample"></a>Executando o exemplo

Se você criar o aplicativo de demonstração com êxito, um arquivo executável, WASAPIRenderExclusiveEventDriven.exe, será gerado. Para executá-lo, digite `WASAPIRenderExclusiveEventDriven` uma janela de comando seguida por argumentos obrigatórios ou opcionais. O exemplo a seguir mostra como executar o exemplo especificando a duração da reprodução no dispositivo multimídia padrão.

`WASAPIRenderExclusiveEventDriven.exe -d 20 -multimedia`

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

O exemplo RenderExclusiveEventDriven demonstra o buffer controlado por evento. O exemplo mostra como:

-   Crie uma instância de um cliente de áudio, configure-o para ser executado em modo exclusivo e habilite o buffer controlado por evento definindo o sinalizador **AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK** na chamada para [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).
-   Associe o cliente com os exemplos que estão prontos para serem renderizados fornecendo um identificador de evento ao sistema chamando o método [**IAudioClient:: SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) .
-   Crie um thread de renderização para processar exemplos do mecanismo de áudio.
-   Alinhe os buffers corretamente em um limite de 128 bytes antes de enviá-los para o dispositivo. Isso é feito ajustando a periodicidade do mecanismo.
-   Verifique o formato de combinação do ponto de extremidade do dispositivo para determinar se os exemplos podem ser renderizados. Se o dispositivo não oferecer suporte ao formato Mix, os dados serão convertidos em PCM.
-   Manipular a alternância de fluxo.

Depois que a sessão de renderização começa e o fluxo é iniciado, o mecanismo de áudio sinaliza o identificador de evento fornecido para notificar o cliente sempre que um buffer se tornar pronto para o cliente processar. Os dados de áudio também podem ser processados em um loop controlado por temporizador. Esse modo é demonstrado no exemplo de [RenderExclusiveTimerDriven](renderexclusivetimerdriven.md) .

Para obter mais informações sobre como renderizar um fluxo, consulte [renderizando um fluxo](rendering-a-stream.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de SDK que usam as APIs de áudio principal](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



