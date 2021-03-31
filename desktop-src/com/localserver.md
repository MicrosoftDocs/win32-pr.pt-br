---
title: LocalServer
description: Especifica o caminho completo para um aplicativo de servidor local de 16 bits.
ms.assetid: 6eadadd5-f4d3-4e0d-9491-2ea366861aa7
keywords:
- COM da chave do registro LocalServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7413f9d7c4d17e9498e80d19b70192fbb21911b6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005862"
---
# <a name="localserver"></a><span data-ttu-id="492a2-104">LocalServer</span><span class="sxs-lookup"><span data-stu-id="492a2-104">LocalServer</span></span>

<span data-ttu-id="492a2-105">Especifica o caminho completo para um aplicativo de servidor local de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="492a2-105">Specifies the full path to a 16-bit local server application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="492a2-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="492a2-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      LocalServer = path
```

## <a name="remarks"></a><span data-ttu-id="492a2-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="492a2-107">Remarks</span></span>

<span data-ttu-id="492a2-108">Esse é um valor de **\_ sz de reg** que especifica o caminho completo e pode incluir qualquer argumento de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="492a2-108">This is a **REG\_SZ** value that specifies the full path and can include any command-line arguments.</span></span>

<span data-ttu-id="492a2-109">COM anexa o sinalizador "-incorporando" à cadeia de caracteres, portanto, o aplicativo que usa sinalizadores deve analisar toda a cadeia de caracteres e verificar o sinalizador de incorporação.</span><span class="sxs-lookup"><span data-stu-id="492a2-109">COM appends the "-Embedding" flag to the string, so the application that uses flags must parse the whole string and check for the -Embedding flag.</span></span>

<span data-ttu-id="492a2-110">Para executar um servidor de objetos COM em um espaço de memória separado, altere o valor de **LocalServer** da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="492a2-110">To run a COM object server in a separate memory space, change the value of **LocalServer** as follows:</span></span>

<span data-ttu-id="492a2-111">**cmd/c iniciar** *caminho do/separate \* \* *. exe**</span><span class="sxs-lookup"><span data-stu-id="492a2-111">**cmd /c start /separate** *path\*\*\*.exe*\*</span></span>

## <a name="related-topics"></a><span data-ttu-id="492a2-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="492a2-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="492a2-113">**LocalServer32**</span><span class="sxs-lookup"><span data-stu-id="492a2-113">**LocalServer32**</span></span>](localserver32.md)
</dt> </dl>

 

 




