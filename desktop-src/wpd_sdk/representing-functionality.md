---
description: Representando a funcionalidade
ms.assetid: 34a4a015-614d-4fac-98d8-29ae43165798
title: Representando a funcionalidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f969bcf6352cd4eef02c1580a93bebcbf769953e2ae658243b4499e6d1ca763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842698"
---
# <a name="representing-functionality"></a>Representando a funcionalidade

Existem objetos funcionais para identificar ou agrupar logicamente os recursos de recurso de um dispositivo. Por exemplo, um aplicativo pode ver que um dispositivo dá suporte ao SMS procurando o objeto funcional do SMS. Da mesma forma, o aplicativo pode ver que um dispositivo tem recursos de câmera procurando o objeto funcional de captura de imagem ainda.

Essa representação de objeto flexível ajuda a habilitar o suporte fácil para dispositivos com recursos de várias funções. Os drivers podem simplesmente expor quaisquer objetos funcionais que representam seu dispositivo, o que é mais granular do que usar classes de dispositivo tradicionais. A representação do objeto também ajuda a isolar partes funcionais sobrepostas; por exemplo, alguns telefones podem ter duas câmeras ou quatro armazenamentos.

no sistema operacional Windows 7, os serviços estendem objetos funcionais fornecendo consultas avançadas de recursos e um agrupamento abstrato de conteúdo. Os aplicativos podem usar os serviços para descobrir recursos do dispositivo e interagir com o conteúdo com mais eficiência. Por exemplo, um aplicativo pode ver que um dispositivo dá suporte aos recursos de sincronização de contatos procurando por um objeto de serviço de contatos e pode localizar todos os contatos como objetos filho do objeto de serviço, sem precisar pesquisar recursivamente a hierarquia de armazenamento.

Os serviços também permitem que os aplicativos descubram e invoquem o comportamento personalizado em um dispositivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Visão geral do aplicativo**](application-overview.md)
</dt> </dl>

 

 



