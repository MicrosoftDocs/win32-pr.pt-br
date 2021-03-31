---
title: Desenvolvimento versus implantação na rede
description: A maioria dos desenvolvedores escreve e testa seus softwares em uma LAN confiável rápida.
ms.assetid: 9458162c-1046-4554-bafa-b455f2957d58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a83210db66133329d6c6b38b67ec7ecb29c0595
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005394"
---
# <a name="development-vs-deployment-in-the-network"></a>Desenvolvimento versus implantação na rede

A maioria dos desenvolvedores escreve e testa seus softwares em uma LAN confiável rápida. O cliente e o servidor geralmente estão no mesmo segmento de rede. Em tais circunstâncias, a rede raramente não responde e a conectividade raramente foi perdida. No entanto, quando implantado em um ambiente de cliente, o cliente e o servidor geralmente estão em diferentes segmentos de rede, possivelmente geograficamente remotos, e o servidor é muito carregado com outros clientes. Em outras palavras: não é possível supor a capacidade de resposta da rede.

Este artigo explica como construir arquiteturas robustas de cliente/servidor diante de incertezas introduzidas por uma rede intrinsecamente confiável e servidores potencialmente indisponíveis.

 

 




