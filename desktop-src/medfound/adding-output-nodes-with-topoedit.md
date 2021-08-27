---
description: Adicionando nós de saída com TopoEdit
ms.assetid: 23d60fc7-547b-4ef5-b334-5f1b38e58e92
title: Adicionando nós de saída com TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e975e332a464218f8629363f34a2d3fbef0e5a49
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481972"
---
# <a name="adding-output-nodes-with-topoedit"></a>Adicionando nós de saída com TopoEdit

Em uma topologia, um nó de saída representa um coletor de mídia que recebe dados de mídia de um nó de transformação e o apresenta para reprodução. O tipo de nó de saída depende do tipo de mídia do nó de origem.

A tabela a seguir mostra o comando de menu/barra de ferramentas para adicionar um nó de saída à topologia.




| Tipo de mídia de origem | Comando de menu/barra de ferramentas | Descrição | 
|-------------------|----------------------|-------------|
| Fluxo de áudio | No menu <strong>topologia</strong> , clique em <strong>Adicionar SAR</strong>. | Cria um nó de saída para o processador de áudio de streaming (SAR) que reproduz um fluxo de áudio por meio de um dispositivo de áudio, como uma placa de som. | 
| Fluxo de vídeo | No menu <strong>topologia</strong> , clique em <strong>Adicionar EVR</strong>. | Cria um nó de saída para o processador de vídeo avançado (EVR) que exibe quadros para um fluxo de vídeo. | 
| Coletor de mídia personalizado | <ol><li>No menu <strong>topologia</strong> , clique em <strong>Adicionar coletor personalizado</strong>.<br /> A caixa de diálogo <strong>GUID personalizado de entrada</strong> é aberta.<br /></li><li><p>No campo <strong>GUID:</strong> , insira o GUID do seu coletor personalizado que você deseja adicionar à topologia.<br /></p><blockquote>[!Note]<br />TopoEdit espera o GUID no formato "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}". Caso contrário, ele não adicionará o nó e exibirá uma mensagem de erro "GUID inválido".</blockquote><p><br /></p></li><li>Clique em <strong>OK</strong>.<br /></li></ol> | Cria um nó de saída para o coletor de fluxo para uma fonte de mídia personalizada.<br /> O coletor personalizado deve dar suporte a <strong>CoCreateInstance</strong> para que o coletor possa ser especificado com um CLSID.<br /> | 




 

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

 

 




