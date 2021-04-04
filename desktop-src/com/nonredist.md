---
title: NONREDIST
description: Adiciona nomes à lista de arquivos que não devem ser exportados quando aplicativos COM+ são empacotados para instalação em outros computadores. Observe que essa é uma subchave, não um valor.
ms.assetid: c50e20e4-1a25-4978-ab84-8f7b4b2f6069
keywords:
- COM valor do registro NONREDIST COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d537208ecaf98cec46591966e4ae7d9c205850a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006209"
---
# <a name="nonredist"></a><span data-ttu-id="049ed-105">NONREDIST</span><span class="sxs-lookup"><span data-stu-id="049ed-105">NONREDIST</span></span>

<span data-ttu-id="049ed-106">Adiciona nomes à lista de arquivos que não devem ser exportados quando aplicativos COM+ são empacotados para instalação em outros computadores.</span><span class="sxs-lookup"><span data-stu-id="049ed-106">Adds names to the list of files that should not be exported when COM+ applications are packaged for installation on other computers.</span></span> <span data-ttu-id="049ed-107">Observe que essa é uma subchave, não um valor.</span><span class="sxs-lookup"><span data-stu-id="049ed-107">Note that this is a subkey, not a value.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="049ed-108">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="049ed-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   NONREDIST
      name1
      name2
```

## <a name="remarks"></a><span data-ttu-id="049ed-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="049ed-109">Remarks</span></span>

<span data-ttu-id="049ed-110">Os arquivos que você adiciona à lista são representados por pares de nome/valor armazenados nessa chave.</span><span class="sxs-lookup"><span data-stu-id="049ed-110">The files you add to the list are represented by name/value pairs stored under this key.</span></span> <span data-ttu-id="049ed-111">Em cada par de nome/valor, o nome é o nome do arquivo e o valor é reservado.</span><span class="sxs-lookup"><span data-stu-id="049ed-111">In each name/value pair, the name is the file name and the value is reserved.</span></span>

 

 




