---
title: Localizando um driver específico
description: Localizando um driver específico
ms.assetid: d48dc313-4606-4f70-b2fe-ed99160e53fc
keywords:
- Gerenciador de compactação de áudio (ACM), localizando drivers
- ACM (Gerenciador de compactação de áudio), localizando drivers
- Exemplos do ACM, localizando drivers
- Localizando drivers
- função acmDriverEnum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d8e8198fdf3bc742c2705e1a83b3ea8036c80f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822937"
---
# <a name="finding-a-specific-driver"></a>Localizando um driver específico

Talvez você queira que seu aplicativo envie uma mensagem diretamente para um driver específico ou para identificar determinados drivers da lista. Por exemplo, talvez você queira que seu aplicativo identifique os drivers que dão suporte a filtros e, em seguida, consulte cada driver para determinar quais marcas de filtro ele suporta. Você pode usar a função [**acmDriverEnum**](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum) para obter um identificador para o driver ou os drivers desejados; Esse identificador pode ser usado para se comunicar com esse driver.

Observe que, quando um aplicativo instala um driver local para seu próprio uso, a função [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) retorna um identificador de driver, que pode ser usado para se comunicar com o driver. Não é necessário usar **acmDriverEnum** nesse caso.

 

 




