---
title: Identificadores de contexto estrito e de tipo estrito
description: Use o \_ atributo de identificador de contexto estrito \_ para todos os identificadores de contexto.
ms.assetid: 2483aa76-0814-4f63-9c38-0aa050d73772
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a45b4e7914034e315f2275e1d928293332012fc4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454209"
---
# <a name="strict-and-type-strict-context-handles"></a>Identificadores de contexto estrito e de tipo estrito

Use o atributo de [**\_ \_ identificador de contexto estrito**](/windows/desktop/Midl/strict-context-handle) para todos os identificadores de contexto. Por padrão, um identificador de contexto não está associado a uma interface, o que significa que um identificador de contexto pode ser criado em uma interface e, em seguida, passado para outro. Esse é um ataque fácil, e muitos servidores RPC falham ao impedi-lo.

Se duas interfaces coexistirem no mesmo processo, um invasor poderá abrir um identificador de contexto em uma interface e passá-lo para outro, o que pode passar pelos dados inesperados. Muitos desenvolvedores acreditam que seu software é a única interface em um processo, mas com muita frequência que não é o caso, porque o sistema e muitos componentes de terceiros usam o RPC internamente, e essas interfaces podem criar identificadores de contexto. Quando o atributo de [**\_ \_ identificador de contexto estrito**](/windows/desktop/Midl/strict-context-handle) é usado, o tempo de execução de RPC garante que um contexto criado em uma interface possa ser passado como um argumento somente para métodos dessa interface.

Em situações em que um aplicativo é desenvolvido para o Windows Vista, o uso do [**\_ identificador de \_ contexto \_ de tipo estrito**](/windows/desktop/Midl/type-strict-context-handle) está disponível e recomendado. Os identificadores de contexto não são associados a um tipo específico por padrão. Quando vários tipos de identificadores de contexto são usados no mesmo processo, é possível que um cliente mal-intencionado passe um identificador de contexto em vez de outro para produzir resultados indesejáveis. O uso do **\_ identificador de \_ contexto \_ de tipo estrito** permite que os aplicativos imponham a consistência de tipo de identificador de contexto e evitem qualquer uso de tipo de identificador de contexto incompatível.

 

 