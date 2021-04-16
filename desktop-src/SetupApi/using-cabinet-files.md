---
description: As funções de instalação manipulam os gabinetes internamente. Para enumerar explicitamente e extrair arquivos de um gabinete, você pode chamar a função SetupIterateCabinet.
ms.assetid: 14bd925a-e7fe-48a3-9ed6-4e42ce796290
title: Usando arquivos de gabinete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03467f6591b4503cb13935cca550f8c1ba1dff81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754100"
---
# <a name="using-cabinet-files"></a>Usando arquivos de gabinete

As funções de instalação manipulam os gabinetes internamente. Para enumerar explicitamente e extrair arquivos de um gabinete, você pode chamar a função [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) .

O tópico a seguir descreve o processamento de gabinete interno para as funções de instalação e como usar o [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta). Também são discutidas as notificações enviadas pelo **SetupIterateCabinet** e o formato necessário de uma rotina de retorno de chamada de gabinete para processar essas notificações.

-   [Extraindo arquivos de gabinetes](extracting-files-from-cabinets.md)
-   [Criando uma rotina de retorno de chamada de gabinete](creating-a-cabinet-callback-routine.md)

 

 



