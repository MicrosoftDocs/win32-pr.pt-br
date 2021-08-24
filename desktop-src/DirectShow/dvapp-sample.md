---
description: Exemplo de DVApp
ms.assetid: 80375170-d0d6-4371-abe3-078703e158b1
title: Exemplo de DVApp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72067c04e108354c1706690bc71e8b339ad5af071c46cc0e4102ae10e9a3643f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148719"
---
# <a name="dvapp-sample"></a>Exemplo de DVApp

## <a name="description"></a>Descrição

Aplicativo de captura de DV (Vídeo Digital).

Este exemplo demonstra como criar vários tipos de grafos de filtro para controlar as gravações DV. Ele também mostra como executar o controle de captura, visualização, transmissão e dispositivo com uma gravação DV.

### <a name="usage"></a>Uso

O aplicativo DVApp dá suporte aos seguintes modos:

-   Versão prévia: renderiza DV da câmera de vídeo para uma janela de vídeo.
-   DV para o arquivo type-1: captura dados DV da gravação para um arquivo DV de tipo 1.
-   Arquivo type-1 para DV: transmite dados de um arquivo DV de tipo 1 para a câmera.
-   DV para o arquivo type-2: captura dados DV da gravação para um arquivo DV do tipo 2.
-   Arquivo type-2 para DV: transmite dados de um arquivo DV type-2 para a câmera.

Os modos de captura e transmissão também executam a versão prévia. Cada um desses modos também tem uma **opção Sem Visualização,** que desabilita a visualização. A captura sem visualização é mais eficiente e pode reduzir o número de quadros descartados.

O aplicativo é iniciado no modo de visualização. Para selecionar outro modo, escolha um modo no menu **Graph Modo.** Para cada modo, DVApp cria um grafo de filtro que dá suporte à funcionalidade desse modo. Para salvar o grafo como um arquivo GraphEdit (.grf), selecione Salvar Graph **arquivo** **no** menu Arquivo. Saia do DVApp antes de abrir o arquivo em GraphEdit.

Para capturar em um arquivo:

1.  No menu **Arquivo,** escolha **Definir Arquivo de Saída** e insira um nome de arquivo.
2.  No menu **Graph,** selecione um *DV* para Modo de arquivo (tipo 1 ou tipo 2, com ou sem versão prévia).
3.  Clique **em Registrar**.
4.  Se a câmera estiver no modo VTR, clique em **Reproduzir**.
5.  Para interromper a captura, clique em **Parar**.

Para transmitir de um arquivo para a câmera:

1.  No menu **Arquivo,** clique em **Definir Arquivo de Entrada** e selecione um arquivo DV. O arquivo deve corresponder ao modo selecionado (tipo 1 ou tipo 2).
2.  No menu **Graph,** selecione um modo Arquivo para *DV* (tipo 1 ou tipo 2, com ou sem versão prévia).
3.  Clique em **Reproduzir**.
4.  Para registrar os dados em fita, clique em **Registrar**.
5.  Para interromper a transmissão, clique em **Parar**.

Se a câmera estiver no modo VTR, o usuário poderá controlar o mecanismo de transporte por meio dos botões de estilo VCR do aplicativo. Para buscar a fita, insira o código de tempo de destino e clique no botão buscar.

Para limitar a quantos dados o aplicativo captura, escolha **Tamanho da Captura** no menu Arquivo. 

Para verificar o formato de fita (NTSC ou PAL), escolha **Verificar** Fita **no** menu Opções.

Para alterar o tamanho da janela de visualização, escolha **Alterar Tamanho da Decodificar** **no** menu Opções.

### <a name="programming-notes"></a>Notas de programação

A principal finalidade desse aplicativo é mostrar como criar vários grafos de captura e transmissão de DV.

### <a name="device-arrival-and-removal"></a>Chegada e remoção do dispositivo

O aplicativo lida com a chegada e a remoção do dispositivo, usando duas técnicas diferentes. Para a chegada do dispositivo, o loop de mensagens do aplicativo responde às mensagens \_ WM DEVICECHANGE. Para a remoção do dispositivo, o aplicativo responde aos [**eventos EC \_ DEVICE \_ LOST**](ec-device-lost.md) do gerenciador de grafo de filtro. Qualquer abordagem funciona, embora o evento EC \_ DEVICE \_ LOST dependa da existência do dispositivo no grafo de filtro.

O aplicativo trata apenas um dispositivo por vez. Se o dispositivo atual for removido, o aplicativo procura outro dispositivo DV no sistema.

Em algumas gravações DV, o usuário deve desligar o dispositivo ao alternar entre o modo de câmera e o modo VTR, o que dispara uma mensagem perdida pelo dispositivo. O aplicativo responde habilitando ou desabilitando os comandos de menu apropriados. No entanto, se o usuário alternar rapidamente entre modos, a câmera poderá não gerar uma mensagem perdida pelo dispositivo. Você pode forçar os menus a atualizar escolhendo **Atualizar Modo** **no** menu Opções. Algumas câmeras dv podem alternar modos sem desligar, mas enviam uma mensagem perdida pelo dispositivo somente quando alternam para o modo VTR.

### <a name="device-control"></a>Controle de dispositivo

A funcionalidade do botão **Reproduzir** **e Registrar** depende do modo atual:

-   Versão prévia: o grafo de filtro é executado automaticamente. O **botão** Reproduzir inicia o transporte.
-   Capturar no arquivo: o **botão Registrar** executa o grafo e o **botão Reproduzir** inicia o transporte.
-   Transmitir para o dispositivo: o **botão Reproduzir** executa o grafo e o **botão Registrar** inicia o transporte.

O aplicativo de exemplo não executa captura com precisão de quadro. Em vários pontos, o aplicativo chama a **função Sleep** para aguardar a resposta do dispositivo. As gravações DV mais novas enviam uma notificação quando o estado do dispositivo muda. Dispositivos mais antigos podem não dar suporte à notificação; para fins de um exemplo, chamar **Sleep** é uma solução mais simples.

## <a name="downloading-the-sample"></a>Baixando o exemplo

Para baixar os exemplos DirectShow SDK, instale a versão mais recente do [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este exemplo é instalado no seguinte caminho: *\[ SDK \] Root* \\ Samples Multimedia DirectShow Capture \\ \\ \\ \\ DVApp.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controlando uma dvcorder](controlling-a-dv-camcorder.md)
</dt> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[DirectShow Amostras](directshow-samples.md)
</dt> </dl>

 

 



