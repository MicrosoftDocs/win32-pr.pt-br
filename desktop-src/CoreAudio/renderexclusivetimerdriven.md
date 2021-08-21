---
description: Este aplicativo de exemplo usa as APIs de áudio principais para renderizar dados de áudio para um dispositivo de saída especificado pelo usuário. Este exemplo demonstra o buffer controlado por temporizador para um cliente de renderização em modo exclusivo.
ms.assetid: 9dcfccd2-a709-4b4e-bbb3-4c68a15cce03
title: RenderExclusiveTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6876c448aa7737683aff4e495416020af7def54cb01109c3d6ad2d1c26d20780
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077440"
---
# <a name="renderexclusivetimerdriven"></a>RenderExclusiveTimerDriven

Este aplicativo de exemplo usa as APIs de áudio principais para renderizar dados de áudio para um dispositivo de saída especificado pelo usuário. Este exemplo demonstra o buffer controlado por temporizador para um cliente de renderização em modo exclusivo. Para um fluxo de modo exclusivo, o cliente compartilha o buffer de ponto de extremidade com o dispositivo de áudio.

Este tópico inclui as seções a seguir.

-   [Descrição](#description)
-   [Requirements](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Exibir os arquivos de exemplo](#view-the-sample-files)
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



| Localização    | Caminho/URL                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| SDK do Windows | \\arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ áudio multimídia \\ \\ RenderExclusiveTimerDriven \\ ... |



 

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo de RenderExclusiveTimerDriven, use as seguintes etapas:

1.  abra o shell CMD para o SDK do Windows e altere para o diretório de exemplo RenderExclusiveTimerDriven.
2.  execute o comando `start WASAPIRenderExclusiveTimerDriven.sln` no diretório RenderExclusiveTimerDriven para abrir o projeto WASAPIRenderExclusiveTimerDriven na janela Visual Studio.
3.  De dentro da janela, selecione a configuração da solução de **depuração** ou **versão** , selecione o menu **Compilar** na barra de menus e selecione a opção **Compilar** . se você não abrir Visual Studio do shell CMD para o SDK, Visual Studio não terão acesso ao ambiente de compilação do sdk. Nesse caso, o exemplo não será compilado, a menos que você defina explicitamente a variável de ambiente MSSdk, que é usada no arquivo de projeto, WASAPIRenderExclusiveTimerDriven. vcproj.

## <a name="view-the-sample-files"></a>Exibir os arquivos de exemplo

Se você criar o aplicativo de demonstração com êxito, um arquivo executável, WASAPIRenderExclusiveTimerDriven.exe, será gerado. Para executá-lo, digite `WASAPIRenderExclusiveTimerDriven` uma janela de comando seguida por argumentos obrigatórios ou opcionais. O exemplo a seguir mostra como executar o exemplo por uma duração de reprodução especificando no dispositivo de console padrão.

`WASAPIRenderExclusiveTimerDriven.exe -d 20 -console`

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

RenderExclusiveTimerDriven demonstra o buffer controlado por temporizador. Nesse modo, o cliente deve aguardar por um período de tempo (metade da latência, especificado pelo valor da opção-d, em milissegundos). Quando o cliente é ativado, metade do período de processamento, ele obtém o próximo conjunto de amostras do mecanismo. Antes de cada passagem de processamento no loop de buffer, o cliente deve descobrir a quantidade de dados a serem renderizados para que os dados não estourem o buffer.

Os dados de áudio a serem reproduzidos no dispositivo especificado podem ser processados habilitando o buffer controlado por eventos. Esse modo é demonstrado no exemplo de RenderExclusiveTimerDriven.

Para obter mais informações sobre como renderizar um fluxo, consulte [renderizando um fluxo](rendering-a-stream.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de SDK que usam as APIs de áudio principal](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



