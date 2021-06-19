---
description: Este aplicativo de exemplo, que demonstra o buffer orientado a eventos, usa as APIs de Áudio Principal para renderizar dados de áudio em um dispositivo de saída especificado pelo usuário.
ms.assetid: 3a2e3fa6-2d6a-4ab0-a531-d1c968458e96
title: RenderExclusiveEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75553496219d0a4ddaf6685089de802e034f94cb
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405129"
---
# <a name="renderexclusiveeventdriven"></a>RenderExclusiveEventDriven

Este aplicativo de exemplo usa as APIs de Áudio Core para renderizar dados de áudio para um dispositivo de saída especificado pelo usuário. Este exemplo demonstra o buffer orientado a eventos para um cliente de renderização no modo exclusivo. Para um fluxo de modo exclusivo, o cliente compartilha o buffer de ponto de extremidade com o dispositivo de áudio.

Este tópico inclui as seções a seguir.

-   [Descrição](#description)
-   [Requirements](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)
-   [Tópicos relacionados](#related-topics)

## <a name="description"></a>Descrição

Este exemplo demonstra os recursos a seguir.

-   [API MMDevice para](mmdevice-api.md) enumeração e seleção de dispositivo multimídia.
-   WASAPI para operações de gerenciamento de fluxo.

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão   |
|----------------------------------------------------------------|-----------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível nos locais a seguir.



| Location    | Caminho/URL                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| SDK do Windows | \\Arquivos de \\ Programas Microsoft SDKs \\ Windows \\ v7.0 Amostras Renderização de Áudio \\ \\ \\ \\ MultimídiaExclusiveEventDriven... \\ |



 

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo RenderExclusiveEventDriven, use as seguintes etapas:

1.  Abra o shell do CMD para o SDK do Windows e altere para o diretório de exemplo RenderExclusiveEventDriven.
2.  Execute o comando no `start WASAPIRenderExclusiveEventDriven.sln` diretório RenderExclusiveEventDriven para abrir o projeto WASAPIRenderExclusiveEventDriven na janela Visual Studio.
3.  Na janela, selecione a configuração **de solução Depurar** ou Liberar, selecione o menu **Build** na barra de menus e selecione a **opção Build.**  Se você não abrir Visual Studio shell do CMD para o SDK, Visual Studio terá acesso ao ambiente de build do SDK. Nesse caso, o exemplo não será criado, a menos que você de definir explicitamente a variável de ambiente MSSdk, que é usada no arquivo de projeto WASAPIRenderExclusiveEventDriven.vcproj.

## <a name="running-the-sample"></a>Executando o exemplo

Se você criar o aplicativo de demonstração com êxito, um arquivo executável, WASAPIRenderExclusiveEventDriven.exe, será gerado. Para executar, digite `WASAPIRenderExclusiveEventDriven` uma janela de comando seguida por argumentos obrigatórios ou opcionais. O exemplo a seguir mostra como executar o exemplo especificando a duração da reprodução no dispositivo multimídia padrão.

`WASAPIRenderExclusiveEventDriven.exe -d 20 -multimedia`

A tabela a seguir mostra os argumentos.

| Argumento        | Descrição                                                |
|-----------------|------------------------------------------------------------|
| -?              | Mostra a ajuda.                                                |
| -H              | Mostra a ajuda.                                                |
| -f              | Frequência de onda seno em Hz.                                 |
| -l              | Latência de renderização de áudio em milissegundos.                      |
| -d              | Duração da onda seno em segundos.                             |
| -M              | Desabilita o uso do MMCSS.                                 |
| -console        | Use o dispositivo de console padrão.                            |
| -communications | Use o dispositivo de comunicação padrão.                      |
| -multimídia     | Use o dispositivo multimídia padrão.                         |
| -endpoint       | Use o identificador de ponto de extremidade especificado no valor da opção. |



 

Se o aplicativo for executado sem argumentos, ele enumera os dispositivos disponíveis e solicita que o usuário selecione um dispositivo para a sessão de renderização. Depois que o usuário especifica um dispositivo, o aplicativo renderiza uma onda seno a 440 Hz por 10 segundos. Esses valores podem ser modificados especificando -f e -d valores de opção.

O exemplo RenderExclusiveEventDriven demonstra o buffer orientado a eventos. O exemplo mostra como:

-   Insinue um cliente de áudio, configure-o para ser executado no modo exclusivo e habilita o buffer orientado a eventos definindo o sinalizador **AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK** na chamada para [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).
-   Associe o cliente aos exemplos que estão prontos para serem renderizados, fornecendo um alçamento de evento ao sistema chamando o [**método IAudioClient::SetEventHandle.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle)
-   Crie um thread de renderização para processar exemplos do mecanismo de áudio.
-   Alinhe os buffers corretamente em um limite de 128 byte antes de enviá-los ao dispositivo. Isso é feito ajustando a periodicidade do mecanismo.
-   Verifique o formato de combinação do ponto de extremidade do dispositivo para determinar se os exemplos podem ser renderizados. Se o dispositivo não dá suporte ao formato de combinação, os dados são convertidos em PCM.
-   Manipular a alternação de fluxo.

Depois que a sessão de renderização é iniciada e o fluxo é iniciado, o mecanismo de áudio sinaliza o handle de evento fornecido para notificar o cliente sempre que um buffer se torna pronto para o cliente processar. Os dados de áudio também podem ser processados em um loop orientado por temporizador. Esse modo é demonstrado no exemplo [RenderExclusiveTimerDriven.](renderexclusivetimerdriven.md)

Para obter mais informações sobre como renderizar um fluxo, consulte [Renderizar um fluxo](rendering-a-stream.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de SDK que usam as APIs de áudio principais](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



