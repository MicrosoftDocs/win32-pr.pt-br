---
description: Transição de compositor
ms.assetid: 7903ecd7-88fb-4277-82ee-a7f71cae0412
title: Transição de compositor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75488e9dbdea4926c515f52352b42f68a2bfa679
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104563386"
---
# <a name="compositor-transition"></a>Transição de compositor

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A transição do compositor compõe um subretângulo do primeiro plano em um retângulo designado em segundo plano, sem alterar o restante do plano de fundo. Use essa transição para criar efeitos da tela de divisão ou imagem em imagem.

A imagem a seguir mostra a transição do compositor:

![transição de compositor](images/trans-compositor.png)

ID de classe (CLSID): {BB44391D-6ABD-422f-9E2E-385C9DFF51FC}

Nome da variável CLSID: CLSID \_ DxtCompositor

Nome amigável: "DxtCompositor"

Propriedades



| Propriedade   | Type | Padrão | Descrição                                                    |
|------------|------|---------|----------------------------------------------------------------|
| Altura     | long | 0       | Altura do retângulo de destino, em pixels.                     |
| OffsetX    | long | 0       | Deslocamento horizontal do retângulo de destino, em pixels.          |
| OffsetY    | long | 0       | Deslocamento vertical do retângulo de destino, em pixels.            |
| SrcHeight  | long | 0       | A altura do subretângulo na origem, em pixels.       |
| SrcOffsetX | long | 0       | A coordenada x do subretângulo na origem, em pixels. |
| SrcOffsetY | long | 0       | A coordenada y do subretângulo na origem, em pixels. |
| SrcWidth   | long | 0       | A largura do subretângulo na origem, em pixels.        |
| Largura      | long | 0       | Largura do retângulo de destino, em pixels.                      |



 

O diagrama a seguir ilustra essas propriedades:

![Propriedades do compositor](images/compmeasure.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Transições e efeitos](transitions-and-effects.md)
</dt> </dl>

 

 



