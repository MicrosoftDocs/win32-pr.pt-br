---
description: Uma família de fontes é um conjunto de fontes com características de largura de traço e de serifa comuns. Há cinco famílias de fontes. Uma sexta família permite que um aplicativo use a fonte padrão. A tabela a seguir descreve as famílias de fontes.
ms.assetid: 3c462000-4f65-43d0-8937-059081a8c417
title: Famílias de fontes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dfda200967b5efbf773fadc17d5093a856d0317
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988817"
---
# <a name="font-families"></a>Famílias de fontes

Uma *família de fontes* é um conjunto de fontes com características de largura de traço e de serifa comuns. Há cinco famílias de fontes. Uma sexta família permite que um aplicativo use a fonte padrão. A tabela a seguir descreve as famílias de fontes.



| Família de fontes | Description                                                                                                                                   |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Decorativa  | Especifica uma fonte novidade. Um exemplo é antigo inglês.                                                                                          |
| DontCare    | Especifica um nome de família genérico. Esse nome é usado quando as informações sobre uma fonte não existem ou não são importantes. A fonte padrão é usada. |
| Moderna      | Especifica uma fonte monospace com ou sem serifas. As fontes monospace são normalmente modernas; Os exemplos incluem paica, elite e Courier New.         |
| Roman       | Especifica uma fonte proporcional com serifas. Um exemplo é Times New Roman.                                                                     |
| Script      | Especifica uma fonte que é criada para parecer como manuscrito; Os exemplos incluem script e cursivo.                                              |
| Suíço       | Especifica uma fonte proporcional sem serifas. Um exemplo é Arial.                                                                            |



 

Essas famílias de fontes correspondem às constantes encontradas no arquivo WinGDI. h: FF \_ decorate, FF \_ DONTCARE, FF \_ moderno, FF \_ Romano, FF \_ script e FF \_ suíço. Um aplicativo usa essas constantes ao criar uma fonte, seleciona uma fonte ou recupera informações sobre uma fonte.

As fontes de uma família são diferenciadas por tamanho (10 pontos, 24 pontos e assim por diante) e estilo (regular, itálico e assim por diante).

 

 



