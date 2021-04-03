---
title: Expondo uma interface de modelo de objeto nativo
description: Se um elemento de interface do usuário oferecer suporte a um modelo de objeto nativo diferente do Microsoft Acessibilidade Ativa ou da automação da interface do usuário, ele poderá expor a interface personalizada respondendo às \_ mensagens do WM GetObject que incluem o \_ identificador de objeto OBJID NATIVEOM.
ms.assetid: 430abeaf-e5ca-48c4-aa35-8d52a8cee2f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e52543908e89a1cea57c981d60bf7cb2b9fbd1fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005748"
---
# <a name="exposing-a-native-object-model-interface"></a>Expondo uma interface de modelo de objeto nativo

Se um elemento de interface do usuário oferecer suporte a um modelo de objeto nativo diferente do Microsoft Acessibilidade Ativa ou da automação da interface do usuário, ele poderá expor a interface personalizada respondendo às mensagens do [**WM \_ GetObject**](wm-getobject.md) que incluem o identificador de objeto [**OBJID \_ NATIVEOM**](object-identifiers.md) . Para responder, o elemento de interface do usuário deve retornar o valor recuperado por uma chamada para a função [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .

Um cliente pode recuperar uma interface de um elemento de interface do usuário que dá suporte a um modelo de objeto nativo chamando a função [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) e especificando [**OBJID \_ NATIVEOM**](object-identifiers.md) como o segundo parâmetro.

 

 




