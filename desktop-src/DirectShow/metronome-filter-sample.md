---
description: Exemplo de filtro de metronome
ms.assetid: bb279898-875a-4ce4-ac69-6c58f640fbbd
title: Exemplo de filtro de metronome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ea1b321dd2602829697862e2716c9017573a44b6162b355e78e586e14d85003
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072980"
---
# <a name="metronome-filter-sample"></a>Exemplo de filtro de metronome

## <a name="description"></a>Descrição

Este filtro de exemplo mostra como implementar um relógio de referência. O filtro usa sua entrada de microfone padrão para escutar picos de áudio (como cliques, reações de mão ou reações), que ele usa para determinar uma taxa de relógio.

## <a name="usage"></a>Uso

Crie o projeto de exemplo e copie a DLL de filtro (Metronom.ax) para o Windows do sistema. Execute o arquivo Metronom.reg para registrar a DLL.

Para usar o filtro:

1.  Crie um grafo de filtro no GraphEdit que renderiza um fluxo de vídeo.
2.  Exclua quaisquer fluxos de áudio renderizados.
3.  Adicione o filtro Metronome ao grafo. Ele aparece na categoria DirectShow Filtros.
4.  Execute o grafo. O vídeo começará a ser gravado em velocidade normal.
5.  Agilizar as mãos ou usar um metronome para definir uma nova velocidade.

## <a name="programming-notes"></a>Notas de programação

Esse filtro funciona apenas para vídeo. O renderador de áudio não é capaz de sincronizar com taxas de relógio radicalmente diferentes.

Se você 92 vezes por minuto (uma vez a cada ~652 ms), o vídeo será reproduzir na taxa normal. Você pode alterar esse padrão alterando o valor da constante `BPM` em Metronom.cpp.

Se você parar de se desalocar por um período de tempo e, em seguida, começar a falar novamente, deverá iniciar novamente aproximadamente na mesma velocidade ou o filtro o ignorará. Além disso, a taxa de reprodução de vídeo é limitada pela velocidade da CPU. Se você exceder o limite por qualquer período de tempo, o filtro interromperá a resposta às alterações de taxa. Se isso acontecer, pare o grafo e reinicie.

Se você implementar seu próprio relógio, as regras mais importantes são que os relógios de referência não devem voltar. Ou seja, eles nunca devem relatar um valor de hora menor que o valor de hora anterior.

## <a name="downloading-the-sample"></a>Baixando o exemplo

Para baixar os DirectShow exemplos do SDK do DirectShow, instale a versão mais recente [do SDK Windows .](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

Este exemplo é instalado no seguinte caminho: *\[ SDK \] Root* \\ Samples Multimedia DirectShow Filters \\ \\ \\ \\ Metronome.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> <dt>

[DirectShow Amostras](directshow-samples.md)
</dt> </dl>

 

 



