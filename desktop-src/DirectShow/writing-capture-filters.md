---
description: Gravando filtros de captura
ms.assetid: 7dfd1009-da09-49dc-a200-3d7a9f1c70c1
title: Gravando filtros de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de1a64de2b56dbc0728432307036fc46387f539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105767663"
---
# <a name="writing-capture-filters"></a>Gravando filtros de captura

Não é recomendável escrever um filtro de captura de áudio ou vídeo para o DirectShow. Em vez disso, o DirectShow fornece suporte automático para dispositivos de captura de áudio e vídeo, usando filtros de wrapper e o [enumerador de dispositivo do sistema](system-device-enumerator.md). Para obter mais informações sobre como implementar um driver de dispositivo, consulte a documentação do Windows Driver Kit (WDK).

Esta seção destina-se apenas a desenvolvedores que precisam capturar algum tipo de dados personalizados de um dispositivo de hardware incomum.

Este artigo inclui as seções a seguir:

-   [Requisitos de PIN para filtros de captura](pin-requirements-for-capture-filters.md)
-   [Implementando um PIN de visualização (opcional)](implementing-a-preview-pin--optional.md)
-   [Produzindo dados em um filtro de captura](producing-data-in-a-capture-filter.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando filtros do DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



