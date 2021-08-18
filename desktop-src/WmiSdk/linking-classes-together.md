---
description: Os provedores WMI são geralmente projetados para fornecer informações sobre um objeto gerenciado específico em um único computador.
ms.assetid: 9f23d599-ac37-4bfb-a3dc-0cef67e68b05
ms.tgt_platform: multiple
title: Vinculando classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da48ab6b816eece1184915026ca32ed152b896f0555ca6c546d0b8ed4d6a7640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131218"
---
# <a name="linking-classes-together"></a>Vinculando classes

Os provedores WMI são geralmente projetados para fornecer informações sobre um objeto gerenciado específico em um único computador. Se houver uma propriedade comum que possa servir como uma chave para identificar exclusivamente todas as instâncias de origem diferentes, use o provedor de [exibição](view-provider.md) para combinar Propriedades de diferentes classes, namespaces ou computadores em uma única classe.

Primeiro, você deve [registrar o provedor de exibição](registering-the-view-provider.md). Após o registro, você pode criar os seguintes tipos de classes de exibição:

-   [Modo de exibição de junção](creating-a-new-instance-from-old-properties.md)

    Instâncias de classes diferentes conectadas por um valor de propriedade comum.

-   [Exibição de associação](associating-instances-between-namespaces.md)

    Exibições de classes de associação existentes no limite do namespace.

-   [Exibição de União](creating-a-union-view-class.md)

    União de uma ou mais instâncias.

 

 



