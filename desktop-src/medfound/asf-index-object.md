---
description: Indexador ASF
ms.assetid: 3f95b0ac-d70f-4bc2-8524-c7de1df34afa
title: Indexador ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c729b547339149ee578a90283c570ec8460b0c57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790503"
---
# <a name="asf-indexer"></a>Indexador ASF

O *indexador* ASF é um componente de camada WMContainer que é usado para ler ou gravar objetos de índice em um arquivo ASF (Advanced Systems Format). Para obter informações sobre a estrutura de um arquivo ASF, consulte [estrutura de arquivo ASF](asf-file-structure.md).

Um aplicativo pode usar o indexador para executar busca com base no tempo de apresentação ou gerar novas entradas de índice para um arquivo ASF. O indexador ASF implementa a interface [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de índice</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Índice baseado em tempo de apresentação</td>
<td>Fornece indexação baseada em tempo de apresentação para fluxos de áudio e vídeo em blocos de índice para tornar a indexação mais eficiente de espaço. Cada bloco de índice faz referência a entradas de índice que contêm um deslocamento de byte. <br/> O deslocamento é a posição do pacote de dados que está sendo buscado, em relação ao início do objeto de dados ASF.<br/> GUID_NULL deve ser usado como o tipo de GUID para o identificador de índice. Para obter mais informações, consulte <a href="using-the-indexer-to-write-a-new-index.md">usando o indexador para gravar um novo índice</a>.<br/></td>
</tr>
<tr class="even">
<td>Índice de código de Code</td>
<td>Facilita a busca por código de meio em fluxos que contêm metadados de código de code. Os códigos de tempo estão em conformidade com um formato SMPTE (<em>horas: minutos: segundos: quadros</em>). Cada bloco de índice faz referência a entradas de índice que contêm um deslocamento de byte. <br/> O deslocamento é a posição do pacote de dados que está sendo buscado, em relação ao início do objeto de dados ASF.<br/>
<blockquote>
[!Note]<br />
No momento, não há suporte para objetos de índice de código de presente.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td>Índice baseado em quadros</td>
<td>Fornece indexação baseada em quadros para fluxos de vídeo. Os índices no índice baseado em quadros estão em termos de números de quadro, com o primeiro quadro para um fluxo no arquivo ASF correspondente à entrada 0 no objeto de índice baseado em quadros. Cada bloco de índice faz referência a entradas de índice que contêm um deslocamento de byte.<br/>
<blockquote>
[!Note]<br />
No momento, não há suporte para objetos de índice baseados em quadros.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

Esta seção contém os seguintes tópicos.



| Tópico                                                                                | Descrição                                                                                                                      |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Criação e configuração do indexador](indexer-creation-and-configuration.md)         | Como criar um objeto de indexador e configurá-lo para ler um índice existente ou para gravar um novo objeto de índice ASF para um arquivo. |
| [Usando o indexador para buscar em um arquivo](using-the-indexer-to-seek.md)                 | Como usar o indexador para buscar em um arquivo ASF.                                                                               |
| [Usando o indexador para gravar um novo índice](using-the-indexer-to-write-a-new-index.md) | Como usar o indexador para gerar entradas de índice e gravar um novo objeto de índice para um arquivo ASF.                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Componentes ASF WMContainer](wmcontainer-asf-components.md)
</dt> <dt>

[Suporte a ASF no Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




