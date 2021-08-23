---
description: A caneta, o pincel, o bitmap, a paleta, a região e o caminho associados a um controlador de domínio são chamados de objetos gráficos. Os atributos a seguir estão associados a cada um desses objetos.
ms.assetid: 95c82efa-257e-4718-9853-7ef10cdfd76c
title: Objetos gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cf256cd8eafd6ee346c12f6658a7c3dd388c94fb4107b010528e47c126fce2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831956"
---
# <a name="graphic-objects"></a>Objetos gráficos

A caneta, o pincel, o bitmap, a paleta, a região e o caminho associados a um controlador de domínio são chamados de objetos gráficos. Os atributos a seguir estão associados a cada um desses objetos.



| Objeto gráfico | Atributos associados                                                               |
|----------------|-------------------------------------------------------------------------------------|
| Bitmap         | Tamanho, em bytes; dimensões, em pixels; formato de cor; esquema de compactação; e assim por diante. |
| Pincel          | Estilo, cor, padrão e origem.                                                  |
| Paleta        | Cores e tamanho (ou número de cores).                                              |
| Fonte           | Nome da face de tipos, largura, altura, peso, conjunto de caracteres e assim por diante.                     |
| Caminho           | La.                                                                              |
| Caneta            | Estilo, largura e cor.                                                            |
| Região         | Local e dimensões.                                                            |



 

Quando um aplicativo cria um controlador de domínio, o sistema armazena automaticamente um conjunto de objetos padrão nele (não há bitmap ou caminho padrão). Um aplicativo pode examinar os atributos dos objetos padrão chamando as funções [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) e [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) . O aplicativo pode alterar esses padrões criando um novo objeto e selecionando-o no controlador de domínio. Um objeto é selecionado em um controlador de domínio chamando a função [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) .

Um aplicativo pode definir a cor do pincel atual com um valor de cor especificado com [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor).

A função [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) retorna a cor do pincel do DC. A função [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor) define a cor da caneta para um valor de cor especificado. A função [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor) retorna a cor da caneta do DC.

 

 



