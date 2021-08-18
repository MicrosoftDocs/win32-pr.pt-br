---
description: Este aplicativo de exemplo demonstra como abrir e fechar fluxos de comunicação e causar eventos de rebaixamento que um aplicativo pode obter para implementar atenuação de fluxo.
ms.assetid: 9a2131b2-ec4a-492a-a277-bd26ec8d67e5
title: DuckingCaptureSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76515f9d20e31bf4583b715e09da38c29bfdac34f6c975087f64bf2617696542
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018454"
---
# <a name="duckingcapturesample"></a>DuckingCaptureSample

Este aplicativo de exemplo demonstra como abrir e fechar fluxos de comunicação e causar eventos de rebaixamento que um aplicativo pode obter para implementar atenuação de fluxo. Esse aplicativo implementa um cliente de chat que usa APIs de áudio principais para ler dados de áudio de um dispositivo de comunicação e reproduzi-los no dispositivo de saída.

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
-   [WASAPI para](wasapi.md) acessar a captura de comunicações e renderizar dispositivo, operações de gerenciamento de fluxo e manipulação de eventos de ressarma.
-   [APIs WAVE para](/previous-versions//ms713499(v=vs.85)) acessar o dispositivo de comunicações e capturar a entrada de áudio.

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão   |
|----------------------------------------------------------------|-----------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio 2008                                             |           |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível nos locais a seguir.



| Localização    | Caminho/URL                                                                                              |
|-------------|-------------------------------------------------------------------------------------------------------|
| SDK do Windows | \\Arquivos de \\ Programas SDKs da Microsoft Windows \\ \\ exemplos v7.0 De áudio \\ \\ \\ \\ multimídiaCaptureSample... \\ |



 

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo Dep. deCaptureSample, use as seguintes etapas:

1.  Abra o DuckingCaptureSample.sln no Visual Studio 2008.
2.  Na janela, selecione a configuração **de solução Depurar** ou Liberar, selecione o menu **Build** na barra de menus e selecione a **opção Build.**  Se você não abrir Visual Studio shell do CMD para o SDK, Visual Studio terá acesso ao ambiente de build do SDK. Nesse caso, o exemplo não será criado, a menos que você desmarque explicitamente a variável de ambiente MSSdk, que é usada no arquivo de projeto, DuckingCaptureSample.vcproj.

## <a name="running-the-sample"></a>Executando o exemplo

Se você criar o aplicativo com êxito, um arquivo executável, DuckingCaptureSample.exe, será gerado. Para executar, selecione **Iniciar Depuração** ou Iniciar Sem **Depuração** no menu **Depurar** ou digite `DuckingCaptureSample` em uma janela de comando.

O DuckingCaptureSample fornece ao usuário duas implementações para capturar áudio do dispositivo de console padrão: WASAPI e APIs wave. Para iniciar uma sessão de captura, selecione um modo e clique **em** Iniciar na interface do usuário do aplicativo. Para encerrar a sessão, clique em **Parar**. Dependendo do dispositivo especificado pelo usuário (entrada ou saída), o aplicativo usa a API MMDevice para obter uma referência ao dispositivo de comunicação de renderização ou captura padrão. Depois que o usuário inicia uma sessão de chat, o aplicativo executa as seguintes tarefas:

-   Cria e inicializa um cliente de áudio no modo orientado a eventos.
-   Associa o cliente ao alça de evento que sinaliza que os exemplos estão prontos para captura ou renderização.
-   Configura um cliente de captura e um cliente de renderização para o transporte.
-   Cria a conversa de chat e inicia o mecanismo de áudio.

Para capturar dados de áudio, com cada passagem de processamento, o exemplo usa o cliente de captura para obter a quantidade total de dados capturados disponíveis no buffer, ler dados do dispositivo de entrada padrão e liberar o pacote e disponibilizar o buffer para ler o próximo conjunto de dados capturados.

Para renderização, o aplicativo determina a quantidade de dados que estão na fila para reproduzir no buffer do ponto de extremidade de captura. Ele grava de acordo no buffer e libera o buffer em preparação para a próxima passagem de processamento até que todos os dados foram gravados. Para renderização, os quadros silenciosos são pré-gravados para impedir que o mecanismo de áudio falha na inicialização. O DuckingCaptureSample também mostra como ocultar o fluxo de renderização do mixer de volume.

Para obter mais informações sobre o recurso de atenuação de fluxo, consulte [Usando um dispositivo de comunicação](using-the-communication-device.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de SDK que usam as APIs de áudio principais](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 
