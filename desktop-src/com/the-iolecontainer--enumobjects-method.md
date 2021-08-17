---
title: O método EnumObjects IOleContainer
description: O método EnumObjects IOleContainer
ms.assetid: 29562d0e-dc8b-49cd-a58f-1f3125a438ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbd74e4916eec4d58240f702a09fd8376008fe0bb352113e1512bd2882d8dee9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462316"
---
# <a name="the-iolecontainerenumobjects-method"></a>O método IOleContainer::EnumObjects

Esse método é usado para enumerar todos os objetos OLE contidos em um documento ou formulário, retornando um ponteiro de interface para cada objeto OLE. O contêiner deve retornar ponteiros para cada objeto OLE que compartilha o mesmo contêiner. Formulários aninhados ou controles aninhados também devem ser enumerados.

Alguns contêineres implementam controles de extensor, que envolvem controles não ActiveX e retornam ponteiros para esses controles extensor à medida que um formulário é enumerado. Esse comportamento permite que ActiveX controles e ActiveX contêineres de controle se integrem bem a controles não ActiveX e, portanto, é recomendado, mas não é necessário.

 

 




