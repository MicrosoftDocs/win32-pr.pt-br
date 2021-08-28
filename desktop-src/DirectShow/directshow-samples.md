---
description: DirectShow Amostras
ms.assetid: 4166d5ca-5e02-49f6-bcb1-d448f8175a0c
title: DirectShow Amostras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87687905d53f91339202af2b08bffa79902e100d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467353"
---
# <a name="directshow-samples"></a>DirectShow Amostras

Os DirectShow exemplos são incluídos com o [SDK Windows .](https://msdn.microsoft.com/windows/aa904949.aspx) Eles estão localizados no caminho \[ SDK Root \] \\ Samples \\ Multimedia \\ DirectShow.

A tabela a seguir lista todos os DirectShow exemplos fornecidos no SDK do Windows. Para obter instruções sobre como criar os exemplos, consulte a documentação fornecida no SDK do Windows.

Se houver documentação adicional para um exemplo, a primeira coluna dessa tabela será vinculada a ela.




| Amostra | Área | Descrição | Dependências adicionais | 
|--------|------|-------------|-------------------------|
| <a href="directshow-base-classes.md">DirectShow Base Classes</a> | Biblioteca de classes base | Classes C++ e funções de utilitário projetadas para implementar DirectShow filtros. | 
| <a href="amcap-sample.md">Exemplo de AmCap</a> | Capturar | Aplicativo de captura de vídeo. | strmbase.lib | 
| <a href="dvapp-sample.md">Exemplo de DVApp</a> | Capturar | Aplicativo de captura de DV (Vídeo Digital). | 
| <a href="playcap-sample.md">Exemplo de PlayCap</a> | Capturar | Aplicativo de captura simples. | 
| <a href="dmo-demo-sample.md">DMO Exemplo de demonstração</a> | DMO | Fluxos dados de áudio de um arquivo WAV por meio de um efeito de áudio DMO. | DirectX SDK | 
| Exemplo de DVD | DVD | Demonstra a reprodução e a navegação básicas de DVD, além de recursos avançados, como gerenciamento de nível dos pais, indicadores, sinalização e sincronização de comandos. | 
| <a href="inftee-filter-sample.md">Exemplo de filtro infTee</a> | Filtros, diversos | Implementação de exemplo do filtro <a href="infinite-pin-tee-filter.md">Tee de Pino</a> Infinito. | strmbase.lib | 
| <a href="metronome-filter-sample.md">Exemplo de filtro de metronome</a> | Filtros, diversos | Mostra como implementar um relógio de referência. | strmbase.lib | 
| <a href="psi-parser-filter-sample.md">Exemplo de filtro do analisador PSI</a> | Filtros, diversos | Recebe tabelas PSI (Informações Específicas do Programa) de um fluxo de transporte MPEG-2 e extrai informações do programa. | strmbase.lib | 
| <a href="dump-filter-sample.md">Exemplo de filtro de despejo</a> | Filtros, renderdor | Grava exemplos de mídia recebidos em um arquivo de texto. | strmbase.lib | 
| Filtro SampVid | Filtros, renderdor | Filtro do renderador de vídeo. | strmbase.lib | 
| <a href="scope-filter-sample.md">Exemplo de filtro de escopo</a> | Filtros, renderdor | Exibe dados de som como formulários de onda. | strmbase.lib | 
| <a href="async-filter-sample.md">Exemplo de filtro assíncrono</a> | Filtros, origem | Filtro de leitor de arquivo que dá suporte ao download progressivo. | strmbase.lib | 
| <a href="ball-filter-sample.md">Exemplo de filtro de bola</a> | Filtros, origem | Filtro de fonte de vídeo que produz uma imagem de uma bola de salto. | strmbase.lib | 
| <a href="push-source-filters-sample.md">Exemplo de filtros de origem por push</a> | Filtros, origem | Filtros de origem que fornecem os seguintes dados como um fluxo de vídeo: um único bitmap, um conjunto de bitmaps, uma cópia da imagem da área de trabalho atual. | strmbase.lib | 
| <a href="synth-filter-sample.md">Exemplo de filtro do Synth</a> | Filtros, origem | Filtro de origem que gera forma de onda de áudio. Este exemplo demonstra a criação dinâmica de grafo. | strmbase.lib | 
| <a href="ezrgb24-filter-sample.md">Exemplo de filtro EZRGB24</a> | Filtros, transformação | Filtro de processamento de imagem. | strmbase.lib | 
| <a href="gargle-filter-sample.md">Exemplo de filtro de gargle</a> | Filtros, transformação | Filtro de efeito de áudio. | strmbase.lib | 
| <a href="wavdest-filter-sample.md">Exemplo de filtro wavdest</a> | Filtros, transformação | Grava um fluxo de áudio em um arquivo WAV. | strmbase.lib | 
| <a href="dmoenum-sample.md">Exemplo de DMOEnum</a> | Diversos | Mostra como enumerar DMOs <a href="directx-media-objects.md">(Objetos de Mídia DirectX).</a> | 
| <a href="mapper-sample.md">Exemplo de mapeado</a> | Diversos | Mostra como usar o <a href="filter-mapper.md">Mapeado de Filtros</a> para encontrar filtros no Registro. | 
| Exemplo de SysEnum | Diversos | Demonstra o uso do <a href="system-device-enumerator.md">Enumerador de Dispositivo do Sistema</a> para enumerar dispositivos e filtros. | 
| <a href="cutscene-sample.md">Exemplo de CutScene</a> | Reprodução | Reproduz um arquivo de vídeo no modo de tela inteira. | 
| Exemplo de DDrawXCL | Reprodução | Reproduz vídeo no modo de tela inteira exclusivo do DirectDraw, usando a <a href="overlay-mixer-filter.md"></a> interface <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a> no filtro Mixer sobreposição. | 
| Exemplo de DShowPlayer | Reprodução | Aplicativo de reprodução de vídeo. | 
| Exemplo de EVRPlayer | Reprodução | Demonstra como usar o filtro DirectShow EVR.<blockquote>[!Note]<br />Requer Windows Vista ou posterior.</blockquote><br /><br /> Este exemplo está disponível no SDK do Windows para Windows Server 2008 ou posterior.<br /> | strmbase.lib | 
| Amostra Texture3D9 | Reprodução | Desenha vídeo em uma superfície de textura do Microsoft DirectX 9.0. | strmbase.lib, SDK do DirectX | 
| <a href="ticker-sample.md">Exemplo de tique</a> | VMR-9 | Usa a VMR-9 para combinar vídeo e texto. | 
| Exemplo de VMR9Allocator | VMR-9 | Implementa um alocador-presenter personalizado para a VMR-9. | strmbase.lib | 
| Exemplo de VMR9Compositor | VMR-9 | Implementa um mixer personalizado para a VMR-9. | 
| <a href="vmrplayer-sample.md">Exemplo de VMRPlayer</a> | VMR-9 | Usa a VMR-9 para combinar um ou dois vídeos em execução e uma imagem estática. | 
| Exemplo de marca-d'água | VMR-9 | Combina um bitmap estático em um vídeo durante a reprodução, usando a VMR-9. | 
| <a href="windowless-sample.md">Exemplo sem janela</a> | VMR-9 | Demonstra o modo sem janela na VMR-9. | 




 

## <a name="additional-dependencies"></a>Dependências adicionais

Alguns dos exemplos vinculam-se à biblioteca DirectShow classe base. Para criar esses exemplos, primeiro você deve criar a biblioteca de classes base. Para obter mais informações, [consulte DirectShow classes base](directshow-base-classes.md). A biblioteca de classes base é necessária para todos os filtros de exemplo.

Alguns dos exemplos também exigem o SDK do DirectX, além do SDK do Windows. Para criar esses exemplos, você deve instalar o SDK do DirectX e definir a variável de ambiente %DXSDK DIR% igual ao caminho de instalação do \_ SDK do DirectX.

Muitos dos exemplos DirectShow usam um conjunto de arquivos de origem e de headers comuns localizados na multimídia de exemplos raiz do SDK do directrory \[ \] \\ \\ DirectShow \\ \\ Comum. Se você copiar uma pasta de exemplo para outro diretório, copie a pasta Comum também.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando o ambiente de build](setting-up-the-build-environment.md)
</dt> </dl>

 

 




