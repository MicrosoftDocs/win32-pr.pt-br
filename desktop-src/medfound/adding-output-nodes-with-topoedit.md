---
description: Adicionando nós de saída com TopoEdit
ms.assetid: 23d60fc7-547b-4ef5-b334-5f1b38e58e92
title: Adicionando nós de saída com TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84dc30631332e8138b35e4bbc0ccde75ec9b0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813665"
---
# <a name="adding-output-nodes-with-topoedit"></a>Adicionando nós de saída com TopoEdit

Em uma topologia, um nó de saída representa um coletor de mídia que recebe dados de mídia de um nó de transformação e o apresenta para reprodução. O tipo de nó de saída depende do tipo de mídia do nó de origem.

A tabela a seguir mostra o comando de menu/barra de ferramentas para adicionar um nó de saída à topologia.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de mídia de origem</th>
<th>Comando de menu/barra de ferramentas</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Fluxo de áudio</td>
<td>No menu <strong>topologia</strong> , clique em <strong>Adicionar SAR</strong>.</td>
<td>Cria um nó de saída para o processador de áudio de streaming (SAR) que reproduz um fluxo de áudio por meio de um dispositivo de áudio, como uma placa de som.</td>
</tr>
<tr class="even">
<td>Fluxo de vídeo</td>
<td>No menu <strong>topologia</strong> , clique em <strong>Adicionar EVR</strong>.</td>
<td>Cria um nó de saída para o processador de vídeo avançado (EVR) que exibe quadros para um fluxo de vídeo.</td>
</tr>
<tr class="odd">
<td>Coletor de mídia personalizado</td>
<td><ol>
<li>No menu <strong>topologia</strong> , clique em <strong>Adicionar coletor personalizado</strong>.<br/> A caixa de diálogo <strong>GUID personalizado de entrada</strong> é aberta.<br/></li>
<li><p>No campo <strong>GUID:</strong> , insira o GUID do seu coletor personalizado que você deseja adicionar à topologia.<br/></p>
<blockquote>
[!Note]<br />
TopoEdit espera o GUID no formato &quot; {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} &quot; . Caso contrário, ele não adicionará o nó e exibirá uma &quot; mensagem de erro GUID inválida &quot; .
</blockquote>
<p><br/></p></li>
<li>Clique em <strong>OK</strong>.<br/></li>
</ol></td>
<td>Cria um nó de saída para o coletor de fluxo para uma fonte de mídia personalizada.<br/> O coletor personalizado deve dar suporte a <strong>CoCreateInstance</strong> para que o coletor possa ser especificado com um CLSID.<br/></td>
</tr>
</tbody>
</table>



 

TopoEdit cria o nó de saída especificado. O **painel topologia** mostra o nó de saída como uma caixa verde que mostra o nome do coletor de fluxo.

Para obter informações sobre como adicionar nós de saída programaticamente usando APIs Media Foundation, consulte [criando nós de saída](creating-output-nodes.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando topologias usando TopoEdit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[Processador de streaming de áudio](streaming-audio-renderer.md)
</dt> <dt>

[Processador de vídeo aprimorado](enhanced-video-renderer.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 




