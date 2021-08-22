---
description: Exemplo de VMRPlayer
ms.assetid: 7fc893a6-afa5-4ada-9295-29122b43b21e
title: Exemplo de VMRPlayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c6281147e2c140541ade480e5b2a5e0f0a1d4146dde59b4871441b68fec6f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071910"
---
# <a name="vmrplayer-sample"></a>Exemplo de VMRPlayer

## <a name="description"></a>Descrição

Este exemplo usa o filtro VMR-9 (Video Mixing Renderer 9) para uma combinação alfa de um ou dois vídeos em execução e uma imagem estática.

## <a name="usage"></a>Uso

Para abrir o primeiro vídeo, escolha **Abrir Fluxo Primário** no menu Arquivo.  Para abrir um segundo vídeo, escolha **Abrir Fluxo Secundário** no menu Arquivo (você deve abrir o fluxo primário primeiro).  Para reproduzir o vídeo, clique no **botão** Reproduzir.

Você pode definir a posição, o tamanho e os  valores alfa dos vídeos selecionando **Fluxo** Primário ou Fluxo Secundário no menu **Propriedades da VMR.**

Para adicionar um bitmap estático  sobre o vídeo, escolha Imagem do Aplicativo Estático no menu Propriedades da **VMR** e clique na **caixa Exibir Imagem do** Aplicativo. Você pode usar a mesma caixa de diálogo para controlar a posição, o tamanho e o valor alfa do bitmap.

Para capturar a imagem de vídeo mesclada, escolha **Capturar Imagem de Bitmap** no menu **Propriedades da VMR.**

Você também pode especificar o fluxo de imagem primária na linha de comando:

**VMRPlayer** **/P** *filename*

## <a name="downloading-the-sample"></a>Baixando o exemplo

Para baixar os DirectShow exemplos do SDK, instale a versão mais recente do [SDK Windows .](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Amostras](directshow-samples.md)
</dt> </dl>

 

 



