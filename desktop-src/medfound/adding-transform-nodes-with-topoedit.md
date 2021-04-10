---
description: Adicionando nós de transformação com TopoEdit
ms.assetid: e1725c37-3f04-4208-9c09-56ce9a854138
title: Adicionando nós de transformação com TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97fa39457f8808070f93a4e5de31e181525ca33b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296402"
---
# <a name="adding-transform-nodes-with-topoedit"></a>Adicionando nós de transformação com TopoEdit

Um nó de transformação representa uma Media Foundation transformação (MFT) que processa os dados de mídia recebidos de um nó de origem. Quando estiver pronto, o pipeline o passará para o nó de saída para renderização. Em Media Foundation, codificadores, decodificadores, multiplexadores, desmultiplexadores e efeitos de vídeo de áudio são implementados como MFTs. O TopoEdit dá suporte à adição de nós de transformação que representam MFTs registrados e personalizados.

Para obter informações sobre como adicionar nós de transformação programaticamente usando APIs Media Foundation, consulte [criando nós de transformação](creating-transform-nodes.md).

## <a name="to-add-a-registered-mft-to-the-topology"></a>Para adicionar um MFT registrado à topologia

1.  No menu **topologia** , clique em **Adicionar transformação**.

    A caixa de diálogo **selecionar transformação** é aberta. Ele exibe uma lista categorizada de MFTs registrados que é gerada pela enumeração das entradas registradas no registro chamando a função [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) .

2.  Expanda a categoria e selecione o MFT que você deseja adicionar à topologia.

3.  Clique em **OK** para fechar a caixa de diálogo e retornar ao **painel topologia**.

TopoEdit cria o nó de transformação especificado. O **painel topologia** mostra o nó transformar como uma caixa verde que exibe o nome da MFT.

## <a name="to-add-a-custom-mft-to-the-topology"></a>Para adicionar um MFT personalizado à topologia

1.  No menu **topologia** , clique em **Adicionar MFT personalizado**.

    Isso abre a caixa de diálogo **GUID personalizado de entrada** .

2.  No campo **GUID:** , insira o GUID do MFT que você deseja adicionar à topologia.

    > [!Note]  
    > TopoEdit espera o GUID no formato "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}". Caso contrário, ele não adicionará o nó e exibirá uma mensagem de erro "GUID inválido".

     

3.  Clique em **OK** para fechar a caixa de diálogo e retornar ao **painel topologia**.

TopoEdit cria o nó de transformação especificado. O **painel topologia** mostra o nó transformar como uma caixa verde que exibe o nome da MFT.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando topologias usando TopoEdit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[Transformações de Media Foundation](media-foundation-transforms.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



