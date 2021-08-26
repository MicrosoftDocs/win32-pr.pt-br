---
description: Cada assembly lado a lado deve ter uma versão.
ms.assetid: 0b78ecf6-fbff-4172-9b0d-09f993666db1
title: Versões de assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e555035bf7b43f53d3a68f249005928867f453b78522f70dd45f3b5379c75e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885566"
---
# <a name="assembly-versions"></a>Versões de assembly

Cada assembly lado a lado deve ter uma versão. Cada versão do assembly é associada a um número de versão que tem quatro partes separadas por períodos: *major.minor.build.revision.* Se uma alteração for feita em um assembly tornando-o  incompatível com as versões existentes, as partes principais ou secundárias do número de versão deverão ser alteradas.  Um número de versão que  muda somente nas partes *de build* ou revisão indica que o assembly é compatível com versões anteriores.

A versão deve ser especificada em **elementos assemblyIdentity** dos [manifestos](manifests.md). Use o formato de versão de quatro partes: mmmmm.nnnnn.ooooo.ppppp. Cada uma das partes separadas por períodos pode ser de 0 a 65535, inclusive.

 

 



