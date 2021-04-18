---
title: O identificador do objeto OBJID_QUERYCLASSNAMEIDX
description: O Microsoft Acessibilidade Ativa usa o \_ identificador de objeto OBJID QUERYCLASSNAMEIDX com a mensagem do WM \_ GetObject para determinar a classe à qual pertence um controle padrão do Windows ou o controle comum.
ms.assetid: 2167df6d-5df3-40b7-bebe-142f4bd98cd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d73a152380411ef0b230de8f0e3372a6718b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105764378"
---
# <a name="the-objid_queryclassnameidx-object-identifier"></a>O \_ identificador de objeto OBJID QUERYCLASSNAMEIDX

O Microsoft Acessibilidade Ativa usa o identificador de objeto [**OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md) com a mensagem do [**WM \_ GetObject**](wm-getobject.md) para determinar a classe à qual pertence um controle padrão do Windows ou o controle comum. Um controle responde a essa mensagem retornando um valor que o Microsoft Acessibilidade Ativa mapeia para o nome de classe do controle. O Microsoft Acessibilidade Ativa usa essas informações para fornecer suporte de acessibilidade para controles padrão do Windows e controles comuns.

Em geral, somente os controles padrão do Windows e os controles comuns respondem ao identificador de objeto [**OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md) . No entanto, um controle personalizado também pode responder se ele inclui toda a mesma funcionalidade de um controle padrão do Windows ou controle comum. Isso permite que o controle personalizado tenha suporte de um dos objetos de proxy padrão fornecidos pelo Microsoft Acessibilidade Ativa.

Para obter mais informações, consulte o [Apêndice F: valores de identificador de objeto para OBJID \_ QUERYCLASSNAMEIDX](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).

 

 




