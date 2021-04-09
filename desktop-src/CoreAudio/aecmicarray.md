---
description: Este exemplo usa as APIs de áudio principais para capturar um fluxo de voz de alta qualidade. O exemplo dá suporte a AEC (cancelamento de eco acústico) e ao processamento de matriz de microfone usando o AEC DMO, também chamado de DSP de captura de voz, fornecido pela Microsoft.
ms.assetid: 932d3442-1beb-4938-9382-031c61cd9b05
title: AECMicArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe72351b9f8f61d939a9f73eaf85022d7f487bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089635"
---
# <a name="aecmicarray"></a>AECMicArray

Este exemplo usa as APIs de áudio principais para capturar um fluxo de voz de alta qualidade. O exemplo dá suporte a AEC (cancelamento de eco acústico) e ao processamento de matriz de microfone usando o AEC DMO, também chamado de DSP de captura de voz, fornecido pela Microsoft.

Este tópico contém as seções a seguir.

-   [Descrição](#description)
-   [Requirements](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)
-   [Tópicos relacionados](#related-topics)

## <a name="description"></a>Descrição

Este exemplo demonstra os recursos a seguir.

-   [MMDevice](mmdevice-api.md) para enumeração e seleção de dispositivo de multimídia.
-   [WASAPI](wasapi.md) para operações de gerenciamento de fluxo, como iniciar e interromper o fluxo, alternando o fluxo.
-   [DeviceTopology](devicetopology-api.md) para enumerar adaptadores de áudio.
-   [EndpointVolume](endpointvolume-api.md) controle os níveis de volume de [sessões de áudio](audio-sessions.md).

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão                     |
|----------------------------------------------------------------|-----------------------------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows Vista ou posterior      |
| Visual Studio                                                  | 2005 (edições não Express) |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível nos locais a seguir.



| Local    | Caminho/URL                                                                                     |
|-------------|----------------------------------------------------------------------------------------------|
| SDK do Windows | \\Arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ áudio multimídia \\ \\ AECMicArray \\ ... |



 

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo de AecSDKDemo, use as seguintes etapas:

1.  Abra uma janela de comando do SDK.
2.  Digite **CD% MSSDK% \\ Setup**.
3.  Execute VCIntegrate.exe.

    Deste ponto em diante, as janelas de comando terão as configurações de ambiente adequadas para criar um aplicativo que aproveita o SDK.

4.  Compile o exemplo.

## <a name="running-the-sample"></a>Executando o exemplo

Se você criar o aplicativo de demonstração com êxito, um arquivo executável AecSDKDemo.exe será gerado. Para executá-lo, digite `AecSDKDemo` uma janela de comando seguida por argumentos obrigatórios ou opcionais, conforme descrito abaixo.

`AecSDKDemo -out mic_out.pcm -mod system_mode [-option value] `

A tabela a seguir mostra os argumentos.

| Argumento  | Descrição                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| -out      | Obrigatórios. Especifica o nome do arquivo de saída.                                                                                                 |
| -mod      | Obrigatórios. Especifica o modo do sistema de captura de voz. Consulte a seção "Configurando a captura de voz DMO" no Leiame de exemplo para obter detalhes. |
| -feito     | Opcional. Ativa o modo de recurso em (1) ou desativado (0).                                                                                       |
| -NS       | Opcional. Ativa a supressão de ruído em (1) ou off (0). O modo de recurso deve estar ativado para especificar isso.                                     |
| -agc      | Opcional. Transforma AGC digital em (1) ou off (0). O modo de recurso deve estar ativado para especificar isso.                                           |
| -cntrclip | Opcional. Desativa o recorte de centro em (1) ou desativado (0). O modo de recurso deve estar ativado para especificar isso.                                       |
| -spkdev   | Opcional. Especifica o índice do dispositivo do orador. Se não for especificado, o usuário será solicitado a selecionar.                                         |
| -micdev   | Opcional. Especifica o índice do dispositivo de microfone. Se não for especificado, o usuário será solicitado a selecionar.                                      |
| -duração | Opcional. Especifica por quanto tempo o aplicativo é executado.                                                                                    |



 

Este aplicativo de exemplo não executa sinais. Para executar a demonstração corretamente para os modos habilitados para AEC (modo 0 e 4), os usuários devem reproduzir alguns sinais de áudio por meio do mesmo dispositivo de alto-falante especificado para o DMO (ou seja, o dispositivo especificado pela opção "-spkdev"), que simula a voz de ponta em um cenário de bate-papo bidirecional. Os usuários podem usar qualquer jogador para reproduzir sinais de áudio. Se não houver nenhum fluxo de renderização ativo no dispositivo de alto-falante selecionado, o DMO falhará ao processar.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de SDK que usam as APIs de áudio principal](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



