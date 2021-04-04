---
description: Cada assembly lado a lado deve ter uma versão.
ms.assetid: 0b78ecf6-fbff-4172-9b0d-09f993666db1
title: Versões de assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c9e32ecc0990572f17264edd2ff51c205a01c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662427"
---
# <a name="assembly-versions"></a>Versões de assembly

Cada assembly lado a lado deve ter uma versão. Cada versão do assembly é associada a um número de versão com quatro partes separadas por pontos: *Major. Minor. Build. Revision*. Se uma alteração for feita em um assembly, o que o torna incompatível com as versões existentes, as partes *principais* ou *secundárias* do número de versão devem ser alteradas. Um número de versão que é alterado somente nas partes de *compilação* ou *revisão* indica que o assembly é compatível com versões anteriores.

A versão deve ser especificada em elementos **AssemblyIdentity** de [manifestos](manifests.md). Use o formato de versão de quatro partes: mmmmm. NNNNN. Ooooo. ppppp. Cada uma das partes separadas por períodos pode ser de 0-65535 inclusive.

 

 



