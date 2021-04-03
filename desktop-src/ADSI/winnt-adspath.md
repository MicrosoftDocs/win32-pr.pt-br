---
title: ADsPath do WinNT
description: Este tópico contém exemplos de cadeias de caracteres a serem usadas para o ADsPath do WinNT.
ms.assetid: 0fad4b34-5287-43a0-a172-a08955b8b132
ms.tgt_platform: multiple
keywords:
- ADSI do provedor de serviços WinNT, ADsPath do WinNT
- ADsPath ADSI, WinNT, descrição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906ea2c3db1b5234fb07045d921858766a105c4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915874"
---
# <a name="winnt-adspath"></a><span data-ttu-id="ec5d1-105">ADsPath do WinNT</span><span class="sxs-lookup"><span data-stu-id="ec5d1-105">WinNT ADsPath</span></span>

<span data-ttu-id="ec5d1-106">A cadeia de caracteres ADsPath do provedor ADSI WinNT pode ser uma das seguintes formas:</span><span class="sxs-lookup"><span data-stu-id="ec5d1-106">The ADsPath string for the ADSI WinNT provider can be one of the following forms:</span></span>


```C++
WinNT:
WinNT://<domain name>
WinNT://<domain name>/<server>
WinNT://<domain name>/<path>
WinNT://<domain name>/<object name>
WinNT://<domain name>/<object name>,<object class>
WinNT://<server>
WinNT://<server>/<object name>
WinNT://<server>/<object name>,<object class>
```



<span data-ttu-id="ec5d1-107">O nome de domínio pode ser um nome NETBIOS ou um nome DNS.</span><span class="sxs-lookup"><span data-stu-id="ec5d1-107">The domain name can be either a NETBIOS name or a DNS name.</span></span>

<span data-ttu-id="ec5d1-108">O servidor é o nome de um servidor específico dentro do domínio.</span><span class="sxs-lookup"><span data-stu-id="ec5d1-108">The server is the name of a specific server within the domain.</span></span>

<span data-ttu-id="ec5d1-109">O caminho é o caminho de no objeto, como "diserver1/printer2".</span><span class="sxs-lookup"><span data-stu-id="ec5d1-109">The path is the path of on object, such as "printserver1/printer2".</span></span>

<span data-ttu-id="ec5d1-110">O nome do objeto é o nome de um objeto específico.</span><span class="sxs-lookup"><span data-stu-id="ec5d1-110">The object name is the name of a specific object.</span></span>

<span data-ttu-id="ec5d1-111">A classe de objeto é o nome de classe do objeto nomeado.</span><span class="sxs-lookup"><span data-stu-id="ec5d1-111">The object class is the class name of the named object.</span></span> <span data-ttu-id="ec5d1-112">Um exemplo desse uso seria "WinNT://MyServer/JeffSmith,user".</span><span class="sxs-lookup"><span data-stu-id="ec5d1-112">One example of this usage would be "WinNT://MyServer/JeffSmith,user".</span></span> <span data-ttu-id="ec5d1-113">A especificação de um nome de classe pode melhorar o desempenho da operação de associação.</span><span class="sxs-lookup"><span data-stu-id="ec5d1-113">Specifying a class name can improve the performance of the bind operation.</span></span>

 

 




