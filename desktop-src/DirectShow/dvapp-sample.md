---
description: Exemplo de DVApp
ms.assetid: 80375170-d0d6-4371-abe3-078703e158b1
title: Exemplo de DVApp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86653781d08921bf638e7798fb34f3a86e8d34a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087708"
---
# <a name="dvapp-sample"></a>Exemplo de DVApp

## <a name="description"></a>Descrição

Aplicativo de captura de vídeo digital (DV).

Este exemplo demonstra como criar vários tipos de grafos de filtro para controlar camcorders DV. Ele também mostra como executar a captura, a visualização, a transmissão e o controle de dispositivo com uma camcorder DV.

### <a name="usage"></a>Uso

O aplicativo DVApp dá suporte aos seguintes modos:

-   Visualização: renderiza o DV da camcorder em uma janela de vídeo.
-   DV para o arquivo do tipo-1: captura dados de DV da camcorder para um arquivo DV de tipo 1.
-   Tipo-1 arquivo para DV: transmite dados de um arquivo DV tipo-1 para a camcorder.
-   DV para o arquivo do tipo-2: captura dados de DV da camcorder para um arquivo de DV tipo 2.
-   Tipo-2 arquivo para DV: transmite dados de um arquivo DV tipo-2 para a camcorder.

Os modos de captura e transmissão também executam a visualização. Cada um desses modos também tem uma opção **sem visualização** , que desabilita a visualização. A captura sem visualização é mais eficiente e pode reduzir o número de quadros descartados.

O aplicativo é iniciado no modo de visualização. Para selecionar outro modo, escolha um modo no menu **modo de gráfico** . Para cada modo, o DVApp cria um grafo de filtro que dá suporte à funcionalidade desse modo. Para salvar o grafo como um arquivo GraphEdit (. GRF), selecione **salvar grafo em arquivo** no menu **arquivo** . Saia do DVApp antes de abrir o arquivo em GraphEdit.

Para capturar para um arquivo:

1.  No menu **arquivo** , escolha **definir arquivo de saída** e insira um nome de arquivo.
2.  No menu **modo de gráfico** , selecione um *DV para* o modo de arquivo (tipo 1 ou 2, com ou sem visualização).
3.  Clique em **gravar**.
4.  Se a camcorder estiver no modo VTR, clique em **reproduzir**.
5.  Para parar a captura, clique em **parar**.

Para transmitir de um arquivo para a camcorder:

1.  No menu **arquivo** , clique em **definir arquivo de entrada** e selecione um arquivo DV. O arquivo deve corresponder ao modo selecionado (tipo 1 ou tipo 2).
2.  No menu **modo de gráfico** , selecione um *arquivo para* o modo DV (tipo 1 ou tipo 2, com ou sem visualização).
3.  Clique em **Reproduzir**.
4.  Para registrar os dados em fita, clique em **gravar**.
5.  Para interromper a transmissão, clique em **parar**.

Se a camcorder estiver no modo VTR, o usuário poderá controlar o mecanismo de transporte por meio dos botões de estilo VCR do aplicativo. Para buscar a fita, insira o código de padirecionamento de destino e clique no botão buscar.

Para limitar a quantidade de dados capturados pelo aplicativo, escolha **capturar tamanho** no menu **arquivo** .

Para verificar o formato de fita (NTSC ou PAL), escolha **verificar fita** no menu de **Opções** .

Para alterar o tamanho da janela de visualização, escolha **alterar tamanho de decodificação** no menu **Opções** .

### <a name="programming-notes"></a>Notas de programação

A principal finalidade desse aplicativo é mostrar como criar vários grafos de transmissão e captura de DV.

### <a name="device-arrival-and-removal"></a>Chegada e remoção de dispositivo

O aplicativo lida com a chegada e remoção de dispositivos usando duas técnicas diferentes. Para a chegada do dispositivo, o loop de mensagem do aplicativo responde às mensagens do WM \_ DEVICECHANGE. Para a remoção do dispositivo, o aplicativo responde aos eventos [**\_ \_ perdidos do dispositivo EC**](ec-device-lost.md) do Gerenciador do grafo de filtro. Qualquer abordagem funciona, embora o \_ evento de perda do dispositivo EC \_ dependa da existência do dispositivo no grafo de filtro.

O aplicativo lida apenas com um dispositivo de cada vez. Se o dispositivo atual for removido, o aplicativo procurará outro dispositivo de vídeo digital no sistema.

Em algumas filmadoras de vídeo digital, o usuário deve desligar o dispositivo ao alterá-lo entre o modo de câmera e o modo VTR, que dispara uma mensagem de perda de dispositivo. O aplicativo responde habilitando ou desabilitando os comandos de menu apropriados. No entanto, se o usuário alternar rapidamente entre os modos, a camcorder poderá não gerar uma mensagem de perda de dispositivo. Você pode forçar os menus a serem atualizados escolhendo o **modo de atualização** no menu de **Opções** . Algumas camcorders DV podem alternar modos sem desligamento, mas enviar uma mensagem de dispositivo perdido somente quando eles mudarem para o modo VTR.

### <a name="device-control"></a>Controle de dispositivo

A funcionalidade do botão **reproduzir** e **gravar** depende do modo atual:

-   Visualização: o grafo de filtro é executado automaticamente. O botão **reproduzir** inicia o transporte.
-   Capturar para arquivo: o botão **gravar** executa o grafo e o botão **reproduzir** inicia o transporte.
-   Transmitir para o dispositivo: o botão **reproduzir** executa o grafo e o botão **gravar** inicia o transporte.

O aplicativo de exemplo não executa captura precisa de quadro. Em vários pontos, o aplicativo chama a função de **suspensão** para aguardar que o dispositivo responda. Camcorders DV mais recentes enviam uma notificação quando o estado do dispositivo é alterado. Dispositivos mais antigos podem não dar suporte à notificação; para os fins de um exemplo, chamar **Sleep** é uma solução mais simples.

## <a name="downloading-the-sample"></a>Baixando o exemplo

Para baixar os exemplos do SDK do DirectShow, instale a versão mais recente do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este exemplo é instalado no seguinte caminho: exemplo de *\[ raiz \] do SDK* \\ \\ multimídia DirectShow de \\ \\ captura \\ DVApp.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controlando uma camcorder DV](controlling-a-dv-camcorder.md)
</dt> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Amostras do DirectShow](directshow-samples.md)
</dt> </dl>

 

 



