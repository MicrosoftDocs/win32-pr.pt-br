---
description: Um caminho de objeto de namespace descreve o local de um namespace específico em um servidor. Um caminho de objeto de namespace contém elementos de servidor e namespace e é formatado usando barras para frente ou para trás.
ms.assetid: 6d8da19e-0914-4267-870e-c203176b895e
ms.tgt_platform: multiple
title: Descrevendo um caminho de objeto de namespace do WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586104a1c193f1c229b0fbb27437d22e3686585b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010818"
---
# <a name="describing-a-wmi-namespace-object-path"></a>Descrevendo um caminho de objeto de namespace do WMI

Um caminho de objeto de namespace descreve o local de um namespace específico em um servidor. Um caminho de objeto de namespace contém elementos de servidor e namespace e é formatado usando barras para frente ou para trás.

O elemento Server especifica o nome de rede do computador que está hospedando o namespace, conforme mostrado no exemplo a seguir.

``` syntax
\\Server\Namespace
```

\- ou –

``` syntax
//Server/Namespace
```

Se o servidor for o computador local, use um único ponto em vez do nome do servidor, conforme mostrado no exemplo a seguir.

``` syntax
\\.\Namespace
```

O elemento namespace Especifica qualquer namespace válido. Um namespace é representado por uma cadeia de caracteres hierárquica contendo elementos delimitados por barras invertidas simples, como raiz \\ cimv2. Não é possível usar barras invertidas em nomes de namespace.

 

 



