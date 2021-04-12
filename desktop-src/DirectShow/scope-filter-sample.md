---
description: Exemplo de filtro de escopo
ms.assetid: f967d4c7-94d2-440b-9e52-423feefec66d
title: Exemplo de filtro de escopo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74ba823e68da1cd1faadd3e1e3acc4e613e2f42
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456574"
---
# <a name="scope-filter-sample"></a>Exemplo de filtro de escopo

## <a name="description"></a>Descrição

O filtro de escopo é um filtro de renderizador que exibe dados de som como formulários de onda.

## <a name="usage"></a>Uso

Para usar esse filtro, abra GraphEdit e processe um arquivo de áudio (ou um arquivo de vídeo com um fluxo de áudio). Desconecte o processador de áudio temporariamente e insira o filtro de exemplo Infinite-Pin t ([exemplo de filtro InfTee](inftee-filter-sample.md)). Reconecte o processador de áudio. Em seguida, conecte o segundo pino de saída do filtro de "t Infinite-Pin" ao filtro de escopo. Agora, execute o grafo.

A janela escopo é implementada como uma caixa de diálogo, não como uma janela real. Os desenvolvedores que criam painéis de controle para alterar parâmetros de filtro em tempo real podem querer usar uma técnica como esta, em vez de páginas de propriedades.

O filtro de escopo demonstra a configuração de um thread separado para processar dados. Nesse caso, os dados são copiados apenas para um buffer separado no método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) e, em seguida, são desenhados na janela Scope no thread separado.

O filtro de escopo também permite que você monitore a saída de áudio para determinar se está recortando, para que você possa ajustar o lucro.

Esse filtro aparece em GraphEdit como "Oscilloscope".

## <a name="downloading-the-sample"></a>Baixando o exemplo

Para baixar os exemplos do SDK do DirectShow, instale a versão mais recente do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este exemplo é instalado no seguinte caminho: exemplos de *\[ raiz \] do SDK* \\ modelos de filtros do \\ \\ DirectShow multimídia \\ \\ .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Amostras do DirectShow](directshow-samples.md)
</dt> </dl>

 

 



