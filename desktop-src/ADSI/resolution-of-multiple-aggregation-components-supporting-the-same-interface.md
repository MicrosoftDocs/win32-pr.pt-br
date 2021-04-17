---
title: Resolução de vários componentes de agregação com suporte para a mesma interface
description: Não é comum que duas extensões exponham a mesma interface para ADSI.
ms.assetid: 87cb1a17-04f7-4ad0-989a-a9506dfdca05
ms.tgt_platform: multiple
keywords:
- Resolução de vários componentes de agregação que dão suporte à mesma interface ADSI
- resolução de vários componentes de agregação que dão suporte à mesma interface ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f58b7b606a05543444a172e2f76b436f6048431
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105752984"
---
# <a name="resolution-of-multiple-aggregation-components-supporting-the-same-interface"></a>Resolução de vários componentes de agregação com suporte para a mesma interface

Não é comum que duas extensões exponham a mesma interface para ADSI. Se isso acontecer, as seguintes regras se aplicam:

-   Se uma interface, como **IMinhaInterface**, for suportada pelo agregador (ADSI) e por qualquer objeto de extensão, **QueryInterface** sempre retornará o **IMinhaInterface** para ADSI.
-   Se uma interface, como **IMinhaInterface**, não tiver suporte do agregador (ADSI), mas tiver suporte de mais de um objeto de extensão, **QueryInterface** retornará o **IMinhaInterface** do primeiro objeto de extensão listado no registro que dá suporte à interface.

Lembre-se de que a ordem dos componentes no registro também afeta a resolução de conflitos de nomes na automação. Para obter mais informações, consulte [resolução de conflitos de nome de função/Propriedade em automação em extensões](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).

 

 




