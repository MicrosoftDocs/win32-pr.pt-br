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
# <a name="describing-a-wmi-namespace-object-path"></a><span data-ttu-id="280f7-104">Descrevendo um caminho de objeto de namespace do WMI</span><span class="sxs-lookup"><span data-stu-id="280f7-104">Describing a WMI Namespace Object Path</span></span>

<span data-ttu-id="280f7-105">Um caminho de objeto de namespace descreve o local de um namespace específico em um servidor.</span><span class="sxs-lookup"><span data-stu-id="280f7-105">A namespace object path describes the location of a particular namespace on a server.</span></span> <span data-ttu-id="280f7-106">Um caminho de objeto de namespace contém elementos de servidor e namespace e é formatado usando barras para frente ou para trás.</span><span class="sxs-lookup"><span data-stu-id="280f7-106">A namespace object path contains server and namespace elements, and is formatted using either forward or backward slashes.</span></span>

<span data-ttu-id="280f7-107">O elemento Server especifica o nome de rede do computador que está hospedando o namespace, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="280f7-107">The server element specifies the network name of the computer that is hosting the namespace, as shown in the following example.</span></span>

``` syntax
\\Server\Namespace
```

<span data-ttu-id="280f7-108">\- ou –</span><span class="sxs-lookup"><span data-stu-id="280f7-108">\- or -</span></span>

``` syntax
//Server/Namespace
```

<span data-ttu-id="280f7-109">Se o servidor for o computador local, use um único ponto em vez do nome do servidor, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="280f7-109">If the server is the local computer, use a single dot instead of the server name, as shown in the following example.</span></span>

``` syntax
\\.\Namespace
```

<span data-ttu-id="280f7-110">O elemento namespace Especifica qualquer namespace válido.</span><span class="sxs-lookup"><span data-stu-id="280f7-110">The namespace element specifies any valid namespace.</span></span> <span data-ttu-id="280f7-111">Um namespace é representado por uma cadeia de caracteres hierárquica contendo elementos delimitados por barras invertidas simples, como raiz \\ cimv2.</span><span class="sxs-lookup"><span data-stu-id="280f7-111">A namespace is represented with a hierarchical string containing elements delimited by single backslashes, such as root\\cimv2.</span></span> <span data-ttu-id="280f7-112">Não é possível usar barras invertidas em nomes de namespace.</span><span class="sxs-lookup"><span data-stu-id="280f7-112">You cannot use forward slashes within namespace names.</span></span>

 

 



