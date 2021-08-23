---
title: Expondo uma interface de modelo de objeto nativo
description: Se um elemento de interface do usuário dá suporte a um modelo de objeto nativo diferente de Microsoft Active Accessibility ou Automação da Interface do Usuário, ele pode expor a interface personalizada respondendo a mensagens GETOBJECT WM que incluem o identificador de objeto \_ \_ OBJID NATIVEOM.
ms.assetid: 430abeaf-e5ca-48c4-aa35-8d52a8cee2f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 701ed721e8259aa3b707fa1d7a6f2e80b9da13a3760b9850edef22b169d772e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644916"
---
# <a name="exposing-a-native-object-model-interface"></a>Expondo uma interface de modelo de objeto nativo

Se um elemento de interface do usuário dá suporte a um modelo de objeto nativo diferente de Microsoft Active Accessibility ou Automação da Interface do Usuário, ele pode expor a interface personalizada respondendo a [**mensagens \_ GETOBJECT WM**](wm-getobject.md) que incluem o identificador de objeto [**\_ OBJID NATIVEOM.**](object-identifiers.md) Para responder, o elemento de interface do usuário deve retornar o valor recuperado por uma chamada para a [**função LresultFromObject.**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)

Um cliente pode recuperar uma interface de um elemento de interface do usuário que dá suporte a um modelo de objeto nativo chamando a função [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) e especificando [**OBJID \_ NATIVEOM**](object-identifiers.md) como o segundo parâmetro.

 

 




