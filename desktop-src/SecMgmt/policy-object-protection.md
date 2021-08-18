---
description: Descreve como o objeto Policy é protegido por padrão.
ms.assetid: e2d65ebf-5fbd-4e25-9862-a8188abb5492
title: Proteção de Objeto de Política
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3317d9cef2a6ff1dfa29753f9a807286d62f31abb0e8c0c9d0150ee10535a1fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894053"
---
# <a name="policy-object-protection"></a>Proteção de Objeto de Política

O [**objeto**](policy-object.md) Policy é protegido por padrão com as seguintes configurações:

-   O grupo local WORLD tem acesso GENERIC \_ EXECUTE.
-   O sistema de ID conhecido é concedido POLICY \_ ALL \_ ACCESS.
-   O grupo local ADMINISTRADOR LOCAL \_ tem acesso GENÉRICO \_ READ, GENERIC WRITE e GENERIC \_ \_ EXECUTE.
-   O grupo ADMINISTRADOR LOCAL \_ é atribuído como proprietário e grupo primário desse objeto.

O [**objeto Policy**](policy-object.md) não pode ser criado ou destruído.

 

 



