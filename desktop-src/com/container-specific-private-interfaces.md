---
title: Container-Specific interfaces privadas
description: Container-Specific interfaces privadas
ms.assetid: 429cf71c-9b9d-4d0b-b5de-91fbe1dde3cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a426ae67d3722406ca6c1428d46d0bc3b4a937a1bcdd105de6f376bbe53a5ccd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118550630"
---
# <a name="container-specific-private-interfaces"></a>Container-Specific interfaces privadas

Alguns contêineres fornecem interfaces privadas específicas de contêiner para funcionalidade adicional ou desempenho aprimorado. Os controles que dependem dessas interfaces específicas de contêiner devem, se possível, funcionar sem essas interfaces específicas de contêiner presentes para que o controle funcione em diferentes contêineres. por exemplo, Visual Basic implementa interfaces privadas que fornecem funcionalidade de formatação de cadeia de caracteres a controles. Se um controle usa essas interfaces de formatação privada, ele deve ser capaz de executar com suporte de formatação padrão se essas interfaces não estiverem disponíveis. Se o controle puder funcionar sem as interfaces privadas, ele deverá executar a ação apropriada (como avisar o usuário sobre a funcionalidade reduzida), mas continuar a trabalhar. Se essa não for uma opção, uma categoria de componente deverá ser registrada conforme necessário para que somente os contêineres que dão suporte a essa funcionalidade possam hospedar esses controles.

 

 




