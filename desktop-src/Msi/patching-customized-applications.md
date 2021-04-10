---
description: Ao instalar um patch e uma ou mais transformações de personalização em um aplicativo, o patch é normalmente instalado primeiro, seguido pelas transformações de personalização.
ms.assetid: 39a58174-fa62-42e3-a0aa-4cc541c2e36b
title: Aplicação de patch em aplicativos personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289685ebc390de750ea9c47ddfae6ef58ec87116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296759"
---
# <a name="patching-customized-applications"></a>Aplicação de patch em aplicativos personalizados

Ao instalar um patch e uma ou mais transformações de personalização em um aplicativo, o patch é normalmente instalado primeiro, seguido pelas transformações de personalização. Por design, o patch não é interrompido pela instalação subsequente da personalização. No entanto, instalar as transformações primeiro e, em seguida, o patch, pode interromper a personalização.

Por exemplo, uma interrupção na personalização pode ocorrer quando um patch é usado para atualizar um produto da versão 1 para a versão 2 e uma transformação de personalização que funciona para a versão 1 não funciona para a versão 2. Nesse caso, o patch de atualização de versão não pode ser aplicado a um produto personalizado sem primeiro desinstalar e reinstalar o produto original.

 

 



