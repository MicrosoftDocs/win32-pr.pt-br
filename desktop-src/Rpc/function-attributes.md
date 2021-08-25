---
title: Atributos de função
description: Os atributos \ retorno de chamada\ e \ local\ podem ser aplicados como atributos de função.
ms.assetid: 05e19164-072c-4a5a-878d-845273975854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be36cac561a10ae2e1177c29dfc0e1219f650daf26af8154c47cdbd7e3d2bd57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021016"
---
# <a name="function-attributes"></a>Atributos de função

O **\[** [**retorno de chamada**](/windows/desktop/Midl/callback) **\]** e os **\[** [**atributos**](/windows/desktop/Midl/local) locais **\]** podem ser aplicados como atributos de função.

Um retorno de chamada é uma chamada remota do servidor para o cliente que é executada como parte de um thread de execução única conceitual. Um retorno de chamada sempre é emitido no contexto de uma chamada remota (ou retorno de chamada) e é executado pelo thread que emitiu a chamada remota original (ou retorno de chamada).

Geralmente, é desejável colocar uma declaração de procedimento local no arquivo IDL, pois esse é o local lógico para descrever interfaces para um pacote. O **\[** [**atributo local**](/windows/desktop/Midl/local) indica que uma declaração de procedimento não é, na **\]** verdade, uma função remota, mas um procedimento local. O compilador MIDL não gera stubs para funções com o **\[ atributo local. \]**

É importante observar que o uso de **\[** [**retorno de chamada**](/windows/desktop/Midl/callback) não é recomendado na programação de vários **\]** threads. Como uma função de programação de thread único, ela não é equipado para dar suporte às demandas de segurança que um ambiente de vários threads fornece.

 

 