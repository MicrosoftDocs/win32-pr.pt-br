---
description: Suporte a MPEG-2 no DirectShow
ms.assetid: a4fe4cc9-86a5-4c83-94be-8901b97c8280
title: Suporte a MPEG-2 no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f42b0d49159a28b3ad29a0141c296c0fd0076fdd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500586"
---
# <a name="mpeg-2-support-in-directshow"></a>Suporte a MPEG-2 no DirectShow

Esta seção descreve os componentes que você pode usar para reproduzir conteúdo MPEG-2 no DirectShow.

> [!Note]  
> Embora o vídeo de DVD seja baseado em MPEG-2, esta seção não descreve a reprodução ou a navegação em DVD. Para obter informações sobre o DVD no DirectShow, consulte [aplicativos de DVD](dvd-applications.md).

 

Os dados MPEG-2 podem vir de um arquivo local ou de uma fonte dinâmica, como uma difusão de rede ou um dispositivo D-VHS. A reprodução de arquivo é chamada de *modo de pull* porque o filtro do analisador efetua pull de dados do arquivo para o grafo de filtro. As fontes dinâmicas são chamadas de *modo de push* porque o filtro de origem envia dados por push para o grafo.

O DirectShow fornece dois filtros que podem analisar fluxos de sistema MPEG-2:

-   [Demultiplexador MPEG-2](mpeg-2-demultiplexer.md) ("Demux"): esse filtro dá suporte ao modo de push para fluxos de programa e fluxos de transporte. No Windows XP e posterior, ele também dá suporte ao modo de pull para fluxos de programa.
-   [Divisor MPEG-2](mpeg-2-splitter.md): esse filtro dá suporte ao modo de pull para fluxos de programa em plataformas de nível inferior. Esse filtro foi preterido no Windows XP e versões posteriores.

Para usar o divisor MPEG-2 Demux ou MPEG-2, você deve ter decodificadores de áudio e vídeo MPEG-2 compatíveis com DirectShow que aceitem PES (fluxos elementares) em pacotes.

Esta seção contém os seguintes tópicos:

-   [Visão geral dos sistemas MPEG-2](overview-of-mpeg-2-systems.md)
-   [Usando o demultiplexador MPEG-2](using-the-mpeg-2-demultiplexer.md)
-   [Usando o divisor MPEG-2](using-the-mpeg-2-splitter.md)
-   [Propriedades de exemplo de MPEG](mpeg-sample-properties.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplo de filtro do analisador PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 



