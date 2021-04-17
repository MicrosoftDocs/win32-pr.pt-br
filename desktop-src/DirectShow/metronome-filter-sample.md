---
description: Exemplo de filtro Metronome
ms.assetid: bb279898-875a-4ce4-ac69-6c58f640fbbd
title: Exemplo de filtro Metronome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 361b46aafa84590243cfcc05445d91a56ce56e83
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105780142"
---
# <a name="metronome-filter-sample"></a>Exemplo de filtro Metronome

## <a name="description"></a>Descrição

Este filtro de exemplo mostra como implementar um relógio de referência. O filtro usa a entrada de microfone padrão para escutar picos de áudio (como cliques, mão Claps ou coughs), que é usado para determinar uma taxa de relógio.

## <a name="usage"></a>Uso

Crie o projeto de exemplo e copie a DLL de filtro (Metronom.ax) para o diretório do sistema do Windows. Execute o arquivo Metronom. reg para registrar a DLL.

Para usar o filtro:

1.  Crie um gráfico de filtro no GraphEdit que renderiza um fluxo de vídeo.
2.  Exclua todos os fluxos de áudio renderizados.
3.  Adicione o filtro Metronome ao grafo. Ele aparece na categoria filtros do DirectShow.
4.  Execute o grafo. O vídeo começará a ser reproduzido em velocidade normal.
5.  Clape suas mãos ou use um Metronome para definir uma nova velocidade.

## <a name="programming-notes"></a>Notas de programação

Esse filtro funciona apenas para vídeo. O processador de áudio não é capaz de sincronizar para taxas de clock radicalmente diferentes.

Se você clap 92 vezes por minuto (uma vez a cada ~ 652 MS), o vídeo será reproduzido na taxa normal. Você pode alterar esse padrão alterando o valor da constante `BPM` em Metronom. cpp.

Se você parar o Clapping por um período de tempo e, em seguida, iniciar o Clapping novamente, deverá começar novamente com aproximadamente a mesma velocidade ou o filtro irá ignorá-lo. Além disso, a taxa de reprodução de vídeo é limitada pela velocidade da CPU. Se você exceder o limite para qualquer período de tempo, o filtro deixará de responder às alterações de taxa. Se isso acontecer, pare o grafo e reinicie.

Se você implementar seu próprio relógio, as regras mais importantes são que os relógios de referência não devem retroceder. Ou seja, eles nunca devem relatar um valor de tempo menor que o valor de tempo anterior.

## <a name="downloading-the-sample"></a>Baixando o exemplo

Para baixar os exemplos do SDK do DirectShow, instale a versão mais recente do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este exemplo é instalado no seguinte caminho: exemplo de *\[ raiz \] do SDK* \\ amostras de multimídia do \\ \\ DirectShow \\ \\ Metronome.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> <dt>

[Amostras do DirectShow](directshow-samples.md)
</dt> </dl>

 

 



