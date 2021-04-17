---
description: 'Para que um aplicativo de Tablet PC opere com tinta com eficiência, esse aplicativo deve ser capaz de:'
ms.assetid: 64a7b773-35c9-42f7-aec4-7fed34fa84d9
title: Cenários importantes de interoperabilidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6dca3bcbf52d673131122615fa5a08317dbf10c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749918"
---
# <a name="important-interoperability-scenarios"></a>Cenários importantes de interoperabilidade

Para que um aplicativo de Tablet PC opere com tinta com eficiência, esse aplicativo deve ser capaz de:

-   Salve um documento no formato binário nativo do aplicativo sem perder a tinta do documento.
-   Salvar um documento em qualquer formato com o qual o aplicativo normalmente dá suporte (por exemplo, HTML ou Rich Text Format (RTF)) sem perder a tinta do documento.
-   Copiar tinta de um aplicativo para outro usando a área de transferência. Isso funcionará se o outro aplicativo reconhecer apenas um formato específico, como HTML, RTF ou bitmap (BMP). Também funciona se o aplicativo de destino reconhece a tinta. Se ele reconhecer tinta, o aplicativo de destino será capaz de interpretar a tinta que foi copiada como tinta e não apenas como uma imagem.
-   Copiar tinta, juntamente com texto, entre dois aplicativos que reconhecem tinta, cada um com mais de um objeto de [**tinta**](inkdisp-class.md) . Isso requer HTML, RTF ou um formato semelhante.
-   Copiar tinta entre dois aplicativos, cada um deles com um objeto de [**tinta**](inkdisp-class.md) . O ISF (Ink serializado Format) é suficiente para isso.
-   Copie a tinta de um aplicativo que tenha mais de um objeto de [**tinta**](inkdisp-class.md) para um aplicativo que tenha apenas um objeto de **tinta** . Nesse caso, o aplicativo que tem mais de um objeto de **tinta** deve ser capaz de produzir o formato serializado da tinta (ISF).
-   Copie a tinta de um aplicativo que tenha um objeto de [**tinta**](inkdisp-class.md) para um aplicativo que tenha mais de um objeto de **tinta** . Nesse caso, o aplicativo que tem mais de um objeto de **tinta** deve ser capaz de reconhecer ISF.

 

 



