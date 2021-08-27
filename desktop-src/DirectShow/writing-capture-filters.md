---
description: Gravando filtros de captura
ms.assetid: 7dfd1009-da09-49dc-a200-3d7a9f1c70c1
title: Gravando filtros de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa4807f381dc925a68fa3c60e45d5c8c5c444653230f366895b370e97aaccb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049086"
---
# <a name="writing-capture-filters"></a>Gravando filtros de captura

não é recomendável escrever um filtro de captura de áudio ou vídeo para o DirectShow. em vez disso, DirectShow fornece suporte automático para dispositivos de captura de áudio e vídeo, usando filtros de wrapper e o [enumerador de dispositivo do sistema](system-device-enumerator.md). para obter mais informações sobre como implementar um driver de dispositivo, consulte a documentação do WDK (Windows driver Kit).

Esta seção destina-se apenas a desenvolvedores que precisam capturar algum tipo de dados personalizados de um dispositivo de hardware incomum.

Este artigo inclui as seções a seguir:

-   [Requisitos de PIN para filtros de captura](pin-requirements-for-capture-filters.md)
-   [Implementando um PIN de visualização (opcional)](implementing-a-preview-pin--optional.md)
-   [Produzindo dados em um filtro de captura](producing-data-in-a-capture-filter.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[gravando filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



