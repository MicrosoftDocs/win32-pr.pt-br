---
title: Vantagens do uso do SIS
description: As vantagens de usar o SIS e a arquitetura de backup do SIS são as seguintes.
ms.assetid: c72a14a1-92ae-4875-ae73-e277ed2b0c0d
keywords:
- Backup de armazenamento de instância única (SIS), vantagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcd1856ce54e817c25830f15f133c7d76c6a80fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004973"
---
# <a name="advantages-of-using-sis"></a>Vantagens do uso do SIS

As vantagens de usar o SIS e a arquitetura de backup do SIS são as seguintes:

-   As conexões entre os links do SIS e os arquivos de backup são mantidas automaticamente pela arquitetura do SIS à medida que os aplicativos de backup chamam as funções da API de backup do SIS.
-   O conteúdo dos pontos de nova análise do SIS é opaco para seus aplicativos de backup e restauração, garantindo que as atualizações para os internos do SIS não exigirão uma alteração na API do SIS ou nos aplicativos de backup e restauração que chamam funções de API do SIS. Você precisa apenas recompilar seu aplicativo com uma nova versão da DLL do SIS, chamada Sisbkup.dll.
-   Como o SIS é implementado como um driver de filtro do sistema de arquivos, ele rastreia constantemente as conexões entre os links do SIS e os arquivos de backup. Quando os arquivos são armazenados em backup e restaurados, o backup do SIS garante que apenas uma instância do arquivo de backup será armazenada em backup e restaurada, independentemente do número de links do SIS que apontam para ele.

 

 




