---
title: Desenvolvimento versus implantação na rede
description: A maioria dos desenvolvedores escreve e testa seus softwares em uma LAN confiável rápida.
ms.assetid: 9458162c-1046-4554-bafa-b455f2957d58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ff9da31ecd80b9e0a699d9ec0eb450e885a423b9380b85e2015e9ef7c1af7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930616"
---
# <a name="development-vs-deployment-in-the-network"></a>Desenvolvimento versus implantação na rede

A maioria dos desenvolvedores escreve e testa seus softwares em uma LAN confiável rápida. O cliente e o servidor geralmente estão no mesmo segmento de rede. Em tais circunstâncias, a rede raramente não responde e a conectividade raramente foi perdida. No entanto, quando implantado em um ambiente de cliente, o cliente e o servidor geralmente estão em diferentes segmentos de rede, possivelmente geograficamente remotos, e o servidor é muito carregado com outros clientes. Em outras palavras: não é possível supor a capacidade de resposta da rede.

Este artigo explica como construir arquiteturas robustas de cliente/servidor diante de incertezas introduzidas por uma rede intrinsecamente confiável e servidores potencialmente indisponíveis.

 

 




