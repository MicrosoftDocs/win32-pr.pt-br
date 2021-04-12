---
title: Redimensionando a caixa de diálogo de aquisição de licença
description: Redimensionando a caixa de diálogo de aquisição de licença
ms.assetid: e091d981-1574-4ffc-bdc4-b92f74396cb7
keywords:
- Windows Media Player, caixa de diálogo redimensionar a aquisição de licença
- Caixa de diálogo Windows Media Player, aquisição de licença
- Windows Media Player, DRM_LicenseAcqURL atributo
- caixa de diálogo redimensionar a aquisição de licença
- Caixa de diálogo aquisição de licença
- DRM_LicenseAcqURL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440683ce65417653251bbed58d59c4d9a34dbc57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364200"
---
# <a name="resizing-the-license-acquisition-dialog-box"></a>Redimensionando a caixa de diálogo de aquisição de licença

Você pode acrescentar parâmetros de cadeia de caracteres de consulta à URL fornecida para o atributo **\_ LicenseAcqURL do DRM** para especificar um tamanho para a caixa de diálogo de aquisição de licença do Windows Media Player 10 ou posterior. A tabela a seguir lista os parâmetros.



| Parâmetro | Descrição                                        |
|-----------|----------------------------------------------------|
| *DlgX*    | Especifica a largura da caixa de diálogo, em pixels.  |
| *DlgY*    | Especifica a altura da caixa de diálogo, em pixels. |



 

Por exemplo, a seguinte URL de aquisição de licença faria com que a caixa de diálogo de aquisição de licença fosse aberta com um tamanho de 800 por 600 pixels:


```C++
https://www.proseware.com/license/lic_acq.htm?DlgX=800&DlgY=600

```



O tamanho máximo da caixa de diálogo nunca excederá as dimensões da tela atual menos 20 pixels. O tamanho mínimo é 333 x 210 pixels (o tamanho padrão).

Esse recurso requer o Windows Media Player 10 ou posterior.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 




