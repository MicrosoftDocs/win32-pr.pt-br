---
description: Exemplo de VMRPlayer
ms.assetid: 7fc893a6-afa5-4ada-9295-29122b43b21e
title: Exemplo de VMRPlayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2214d94628a90daf0dd543f4e3a7f0166f4968a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827529"
---
# <a name="vmrplayer-sample"></a>Exemplo de VMRPlayer

## <a name="description"></a>Descrição

Este exemplo usa o filtro de processador de mixagem de vídeo 9 (VMR-9) para alfa Blend um ou dois vídeos em execução e uma imagem estática.

## <a name="usage"></a>Uso

Para abrir o primeiro vídeo, escolha **abrir fluxo primário** no menu **arquivo** . Para abrir um segundo vídeo, escolha **abrir fluxo secundário** no menu **arquivo** (você deve abrir primeiro o fluxo primário). Para reproduzir o vídeo, clique no botão **reproduzir** .

Você pode definir a posição, o tamanho e os valores Alfa dos vídeos selecionando fluxo **principal** ou **Secondard Stream** no menu de **Propriedades do VMR** .

Para adicionar um bitmap estático no vídeo, escolha **imagem estática do aplicativo** no menu de **Propriedades do VMR** e clique na caixa **Exibir imagem do aplicativo** . Você pode usar a mesma caixa de diálogo para controlar a posição, o tamanho e o valor alfa do bitmap.

Para capturar a imagem de vídeo mesclada, escolha **Capturar imagem de bitmap** no menu de **Propriedades do VMR** .

Você também pode especificar o fluxo da imagem primária na linha de comando:

**VMRPlayer** **/p** *nome do arquivo*

## <a name="downloading-the-sample"></a>Baixando o exemplo

Para baixar os exemplos do SDK do DirectShow, instale a versão mais recente do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Amostras do DirectShow](directshow-samples.md)
</dt> </dl>

 

 



