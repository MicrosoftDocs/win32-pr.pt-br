---
description: Depois de criar um documento HTML de origem do ERP (página de referência de evento), você deve nomeá-lo antes que Monitor de Rede possa exibi-lo no Visualizador de Eventos.
ms.assetid: 0c668a8b-94a5-4996-8214-4629a24a8337
title: Nomeando uma página de referência de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 569991c5e5ac24e18476fe27727f4fad1c310c8fd4e9439062fdf91bfb344005
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799686"
---
# <a name="naming-an-event-reference-page"></a>Nomeando uma página de referência de evento

Depois de criar um documento HTML de origem do ERP (página de referência de evento), você deve nomeá-lo antes que Monitor de Rede possa exibi-lo no Visualizador de Eventos.

Monitor de nome e arquivos ERP de especialistas com este formato:

``` syntax
<ExpertName><EventIdent>.htm (or <MonitorName><EventIdent>.htm)
```

<dl> <dt>

<span id="ExpertName"></span><span id="expertname"></span><span id="EXPERTNAME"></span>**Especialistaname**
</dt> <dd>

Nome do arquivo DLL, excluindo a extensão de nome de arquivo.

</dd> <dt>

<span id="EventIdent"></span><span id="eventident"></span><span id="EVENTIDENT"></span>**EventIdent**
</dt> <dd>

Identificador de evento do especialista em ERP.

O identificador de evento também é encontrado no membro **EventIdent** da estrutura **NMEVENTDATA** .

</dd> </dl>

Para obter mais informações sobre como criar um ERP, consulte os seguintes tópicos:

-   [Criando páginas de referência de evento expert e monitor](creating-expert-and-monitor-event-reference-pages.md)
-   [Escrevendo uma página de referência de evento](writing-an-event-reference-page.md)
-   [Testando uma página de referência de evento](testing-an-event-reference-page.md)

 

 



