---
title: Container-Specific interfaces privadas
description: Container-Specific interfaces privadas
ms.assetid: 429cf71c-9b9d-4d0b-b5de-91fbe1dde3cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c6569a79e9f1801c6fd82543bc40408903c780
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292779"
---
# <a name="container-specific-private-interfaces"></a>Container-Specific interfaces privadas

Alguns contêineres fornecem interfaces privadas específicas de contêiner para funcionalidade adicional ou desempenho aprimorado. Os controles que dependem dessas interfaces específicas de contêiner devem, se possível, funcionar sem essas interfaces específicas de contêiner presentes para que o controle funcione em diferentes contêineres. Por exemplo, Visual Basic implementa interfaces privadas que fornecem funcionalidade de formatação de cadeia de caracteres a controles. Se um controle usa essas interfaces de formatação privada, ele deve ser capaz de executar com suporte de formatação padrão se essas interfaces não estiverem disponíveis. Se o controle puder funcionar sem as interfaces privadas, ele deverá executar a ação apropriada (como avisar o usuário sobre a funcionalidade reduzida), mas continuar a trabalhar. Se essa não for uma opção, uma categoria de componente deverá ser registrada conforme necessário para que somente os contêineres que dão suporte a essa funcionalidade possam hospedar esses controles.

 

 




