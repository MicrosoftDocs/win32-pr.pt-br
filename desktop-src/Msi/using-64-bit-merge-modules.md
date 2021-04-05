---
description: Siga estas diretrizes ao criar um módulo de mesclagem de 64 bits.
ms.assetid: 326c274b-981e-4b21-a4fb-0060c178a01e
title: Usando módulos de mesclagem de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bfeec3f77e497fac0686cd6aeb44b69e987655
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662590"
---
# <a name="using-64-bit-merge-modules"></a>Usando módulos de mesclagem de 64 bits

Um módulo de mesclagem de 64 bits tem qualquer uma das características identificadas neste tópico.

-   O módulo de mesclagem contém pelo menos um componente que foi compilado para sistemas operacionais de 64 bits.
-   O módulo de mesclagem não contém nenhum componente de 64 bits, mas destina-se ao uso somente com pacotes [de Windows Installer de 64 bits](64-bit-windows-installer-packages.md) .

Os módulos de mesclagem podem ser usados da seguinte maneira:

-   Um módulo de mesclagem de 64 bits pode ser mesclado em um pacote de [Windows Installer de 64 bits](64-bit-windows-installer-packages.md) . As propriedades de [**Resumo do modelo**](template-summary.md) no módulo de mesclagem e no pacote de Windows Installer devem ser definidas para o mesmo tipo de processador de 64 bits. Um módulo de mesclagem x64 pode ser mesclado somente em pacotes x64 e um módulo de mesclagem Intel64 pode ser mesclado somente em pacotes Intel64.
-   Um módulo de mesclagem de 32 bits pode ser mesclado em pacotes de Windows Installer de 32 bits ou [64 bits](64-bit-windows-installer-packages.md) .
-   Um módulo de mesclagem de 64 bits pode ser mesclado em um pacote de 64 bits em um sistema operacional de 32 bits.

Siga o seguinte ao criar um módulo de mesclagem de 64 bits:

-   Use o mesmo procedimento geral de criação de módulos de mesclagem de 32 bits. Para obter informações, consulte [sobre módulos de mesclagem](about-merge-modules.md) e [criação de módulos de mesclagem](authoring-merge-modules.md).
-   Você deve definir a propriedade de [**Resumo do modelo**](template-summary.md) com o valor Intel64 se estiver executando um sistema Intel64. Você deve definir a propriedade de **Resumo do modelo** com o valor x64 se estiver executando um sistema x64. Para obter informações, consulte [referência de fluxo de informações de resumo do módulo de mesclagem](merge-module-summary-information-stream-reference.md).
-   Quando existirem módulos de mesclagem de 32 bits e 64 bits para o mesmo componente, é recomendável que os módulos tenham assinaturas diferentes. Isso permitirá que um pacote contenha as duas versões do componente.

Para obter mais informações, consulte [Windows Installer em sistemas operacionais de 64 bits](windows-installer-on-64-bit-operating-systems.md).

 

 



