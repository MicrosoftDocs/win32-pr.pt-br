---
description: Amostras do DirectShow
ms.assetid: 4166d5ca-5e02-49f6-bcb1-d448f8175a0c
title: Amostras do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f58c10615aaaa4305a30934e32ef9b11efb18c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500673"
---
# <a name="directshow-samples"></a>Amostras do DirectShow

Os exemplos do DirectShow estão incluídos no [SDK do Windows](https://msdn.microsoft.com/windows/aa904949.aspx). Elas estão localizadas no caminho \[ raiz do SDK \] \\ exemplos de \\ multimídia \\ DirectShow.

A tabela a seguir lista todos os exemplos do DirectShow fornecidos no SDK do Windows. Para obter instruções sobre como criar os exemplos, consulte a documentação fornecida na SDK do Windows.

Se houver documentação adicional para um exemplo, a primeira coluna desta tabela será vinculada a ela.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Amostra</th>
<th>Área</th>
<th>Descrição</th>
<th>Dependências adicionais</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="directshow-base-classes.md">Classes base do DirectShow</a></td>
<td>Biblioteca de classes base</td>
<td>Classes C++ e funções de utilitário projetadas para implementar filtros do DirectShow.</td>

</tr>
<tr class="even">
<td><a href="amcap-sample.md">Exemplo de AmCap</a></td>
<td>Capturar</td>
<td>Aplicativo de captura de vídeo.</td>
<td>Strmbase. lib</td>
</tr>
<tr class="odd">
<td><a href="dvapp-sample.md">Exemplo de DVApp</a></td>
<td>Capturar</td>
<td>Aplicativo de captura de vídeo digital (DV).</td>

</tr>
<tr class="even">
<td><a href="playcap-sample.md">Exemplo de PlayCap</a></td>
<td>Capturar</td>
<td>Aplicativo de captura simples.</td>

</tr>
<tr class="odd">
<td><a href="dmo-demo-sample.md">Exemplo de demonstração de DMO</a></td>
<td>DMO</td>
<td>Transmite dados de áudio de um arquivo WAV por meio de um efeito de áudio DMO.</td>
<td>SDK do DirectX</td>
</tr>
<tr class="even">
<td>Exemplo de DVD</td>
<td>DVD</td>
<td>Demonstra a reprodução e a navegação de DVD básica, além de recursos avançados, como gerenciamento de nível pai, indicadores, karaokê e sincronização de comando.</td>

</tr>
<tr class="odd">
<td><a href="inftee-filter-sample.md">Exemplo de filtro InfTee</a></td>
<td>Filtros, diversos</td>
<td>Exemplo de implementação do filtro de <a href="infinite-pin-tee-filter.md">t de PIN infinito</a> .</td>
<td>Strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="metronome-filter-sample.md">Exemplo de filtro Metronome</a></td>
<td>Filtros, diversos</td>
<td>Mostra como implementar um relógio de referência.</td>
<td>Strmbase. lib</td>
</tr>
<tr class="odd">
<td><a href="psi-parser-filter-sample.md">Exemplo de filtro do analisador PSI</a></td>
<td>Filtros, diversos</td>
<td>Recebe tabelas de informações específicas do programa (PSI) de um fluxo de transporte MPEG-2 e extrai informações do programa.</td>
<td>Strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="dump-filter-sample.md">Exemplo de filtro de despejo</a></td>
<td>Filtros, renderizador</td>
<td>Grava exemplos de mídia recebidos em um arquivo de texto.</td>
<td>Strmbase. lib</td>
</tr>
<tr class="odd">
<td>Filtro de SampVid</td>
<td>Filtros, renderizador</td>
<td>Filtro de renderização de vídeo.</td>
<td>Strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="scope-filter-sample.md">Exemplo de filtro de escopo</a></td>
<td>Filtros, renderizador</td>
<td>Exibe dados de som como formulários de onda.</td>
<td>Strmbase. lib</td>
</tr>
<tr class="odd">
<td><a href="async-filter-sample.md">Exemplo de filtro assíncrono</a></td>
<td>Filtros, origem</td>
<td>Filtro de leitor de arquivo que dá suporte ao download progressivo.</td>
<td>Strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="ball-filter-sample.md">Exemplo de filtro de bola</a></td>
<td>Filtros, origem</td>
<td>Filtro de fonte de vídeo que produz uma imagem de uma bola saltando.</td>
<td>Strmbase. lib</td>
</tr>
<tr class="odd">
<td><a href="push-source-filters-sample.md">Exemplo de filtros de origem de push</a></td>
<td>Filtros, origem</td>
<td>Filtros de origem que fornecem os seguintes dados como um fluxo de vídeo: um único bitmap, um conjunto de bitmaps, uma cópia da imagem da área de trabalho atual.</td>
<td>Strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="synth-filter-sample.md">Exemplo de filtro de sintetizador</a></td>
<td>Filtros, origem</td>
<td>Filtro de origem que gera as ondas de áudio. Este exemplo demonstra a criação dinâmica de gráficos.</td>
<td>Strmbase. lib</td>
</tr>
<tr class="odd">
<td><a href="ezrgb24-filter-sample.md">Exemplo de filtro EZRGB24</a></td>
<td>Filtros, transformação</td>
<td>Filtro de processamento de imagem.</td>
<td>Strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="gargle-filter-sample.md">Exemplo de filtro Gargle</a></td>
<td>Filtros, transformação</td>
<td>Filtro de efeito de áudio.</td>
<td>Strmbase. lib</td>
</tr>
<tr class="odd">
<td><a href="wavdest-filter-sample.md">Exemplo de filtro WavDest</a></td>
<td>Filtros, transformação</td>
<td>Grava um fluxo de áudio em um arquivo WAV.</td>
<td>Strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="dmoenum-sample.md">Exemplo de DMOEnum</a></td>
<td>Diversos</td>
<td>Mostra como enumerar o <a href="directx-media-objects.md">DirectX Media Objects</a> (DMOs).</td>

</tr>
<tr class="odd">
<td><a href="mapper-sample.md">Exemplo de mapeador</a></td>
<td>Diversos</td>
<td>Mostra como usar o <a href="filter-mapper.md">mapeador de filtro</a> para localizar filtros no registro.</td>

</tr>
<tr class="even">
<td>Exemplo de SysEnum</td>
<td>Diversos</td>
<td>Demonstra como usar o <a href="system-device-enumerator.md">enumerador de dispositivo do sistema</a> para enumerar dispositivos e filtros.</td>

</tr>
<tr class="odd">
<td><a href="cutscene-sample.md">Exemplo de CutScene</a></td>
<td>Reprodução</td>
<td>Reproduz um arquivo de vídeo no modo de tela inteira.</td>

</tr>
<tr class="even">
<td>Exemplo de DDrawXCL</td>
<td>Reprodução</td>
<td>Reproduz o vídeo no modo de tela inteira exclusivo do DirectDraw, usando a interface <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a> no filtro de <a href="overlay-mixer-filter.md">mixer de sobreposição</a> .</td>

</tr>
<tr class="odd">
<td>Exemplo de DShowPlayer</td>
<td>Reprodução</td>
<td>Aplicativo de reprodução de vídeo.</td>

</tr>
<tr class="even">
<td>Exemplo de EVRPlayer</td>
<td>Reprodução</td>
<td>Demonstra como usar o filtro EVR do DirectShow.
<blockquote>
[!Note]<br />
Requer o Windows Vista ou posterior.
</blockquote>
<br/> <br/> Este exemplo está disponível no SDK do Windows para Windows Server 2008 ou posterior.<br/></td>
<td>Strmbase. lib</td>
</tr>
<tr class="odd">
<td>Exemplo de Texture3D9</td>
<td>Reprodução</td>
<td>Desenha vídeo em uma superfície de textura do Microsoft DirectX 9,0.</td>
<td>Strmbase. lib, SDK do DirectX</td>
</tr>
<tr class="even">
<td><a href="ticker-sample.md">Exemplo de marca</a></td>
<td>VMR-9</td>
<td>Usa o VMR-9 para misturar vídeo e texto.</td>

</tr>
<tr class="odd">
<td>Exemplo de VMR9Allocator</td>
<td>VMR-9</td>
<td>Implementa um apresentador de alocador personalizado para o VMR-9.</td>
<td>Strmbase. lib</td>
</tr>
<tr class="even">
<td>Exemplo de VMR9Compositor</td>
<td>VMR-9</td>
<td>Implementa um mixer personalizado para o VMR-9.</td>

</tr>
<tr class="odd">
<td><a href="vmrplayer-sample.md">Exemplo de VMRPlayer</a></td>
<td>VMR-9</td>
<td>Usa o VMR-9 para misturar um ou dois vídeos em execução e uma imagem estática.</td>

</tr>
<tr class="even">
<td>Exemplo de marca d' água</td>
<td>VMR-9</td>
<td>Combina um bitmap estático em um vídeo durante a reprodução, usando o VMR-9.</td>

</tr>
<tr class="odd">
<td><a href="windowless-sample.md">Exemplo sem janela</a></td>
<td>VMR-9</td>
<td>Demonstra o modo sem janela no VMR-9.</td>

</tr>
</tbody>
</table>



 

## <a name="additional-dependencies"></a>Dependências adicionais

Alguns dos exemplos são vinculados à biblioteca de classes base do DirectShow. Para criar esses exemplos, você deve primeiro compilar a biblioteca de classes base. Para obter mais informações, consulte [classes base do DirectShow](directshow-base-classes.md). A biblioteca de classes base é necessária para todos os filtros de exemplo.

Alguns dos exemplos também exigem o SDK do DirectX, além do SDK do Windows. Para criar esses exemplos, você deve instalar o SDK do DirectX e definir a variável de ambiente% DXSDK \_ dir%, igual ao seu caminho de instalação do SDK do DirectX.

Muitos dos exemplos do DirectShow usam um conjunto de cabeçalhos comuns e arquivos de origem localizados nos exemplos de raiz do SDK do directrory \[ \] \\ \\ multimídia do \\ DirectShow \\ comum. Se você copiar uma pasta de exemplo para outro diretório, certifique-se de copiar a pasta comum também.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando o ambiente de compilação](setting-up-the-build-environment.md)
</dt> </dl>

 

 




