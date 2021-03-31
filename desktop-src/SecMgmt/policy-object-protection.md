---
description: Descreve como o objeto de política é protegido por padrão.
ms.assetid: e2d65ebf-5fbd-4e25-9862-a8188abb5492
title: Proteção de objeto de política
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 802fea6ce37a070c8230c3c9993df78a45f439bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646997"
---
# <a name="policy-object-protection"></a>Proteção de objeto de política

O objeto de [**política**](policy-object.md) é protegido por padrão com as seguintes configurações:

-   O mundo do grupo local tem \_ acesso genérico de execução.
-   O sistema de ID conhecido recebe \_ todos os \_ acessos à política.
-   O administrador LOCAL do grupo local \_ tem \_ acesso genérico de leitura, \_ gravação genérica e \_ execução genérica.
-   O administrador LOCAL do grupo \_ é atribuído como proprietário e grupo primário deste objeto.

O objeto de [**política**](policy-object.md) não pode ser criado ou destruído.

 

 



