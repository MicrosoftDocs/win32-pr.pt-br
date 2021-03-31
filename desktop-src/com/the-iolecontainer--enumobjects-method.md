---
title: O método IOleContainer EnumObjects
description: O método IOleContainer EnumObjects
ms.assetid: 29562d0e-dc8b-49cd-a58f-1f3125a438ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a2dff2331374299abbc13cdd595aa709ec1aa74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159399"
---
# <a name="the-iolecontainerenumobjects-method"></a>O método IOleContainer:: EnumObjects

Esse método é usado para enumerar todos os objetos OLE contidos em um documento ou formulário, retornando um ponteiro de interface para cada objeto OLE. O contêiner deve retornar ponteiros para cada objeto OLE que compartilha o mesmo contêiner. Formulários aninhados ou controles aninhados também devem ser enumerados.

Alguns contêineres implementam controles de extensor, que encapsulam controles não ActiveX e, em seguida, retornam ponteiros para esses controles de extensor, pois um formulário é enumerado. Esse comportamento permite que controles ActiveX e contêineres de controle ActiveX se integrem bem com controles não ActiveX e, portanto, são recomendados, mas não obrigatórios.

 

 




