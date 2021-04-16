---
title: Bibliotecas de tipos de extensão ADSI
description: As bibliotecas de tipos para extensões não são mescladas.
ms.assetid: 33cde2fe-9b90-4f63-a215-cf0c8f8defb1
ms.tgt_platform: multiple
keywords:
- ADSI de bibliotecas de tipos de extensão ADSI
- ADSI de extensões, bibliotecas de tipos de extensão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7efc89bd491d5ee244c5a2a64dd7df4c84b61ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498607"
---
# <a name="adsi-extension-type-libraries"></a><span data-ttu-id="7c4fe-105">Bibliotecas de tipos de extensão ADSI</span><span class="sxs-lookup"><span data-stu-id="7c4fe-105">ADSI Extension Type Libraries</span></span>

<span data-ttu-id="7c4fe-106">As bibliotecas de tipos para extensões não são mescladas.</span><span class="sxs-lookup"><span data-stu-id="7c4fe-106">The type libraries for extensions are not merged.</span></span> <span data-ttu-id="7c4fe-107">Os clientes ADSI devem incluir especificamente a biblioteca de tipos para cada extensão.</span><span class="sxs-lookup"><span data-stu-id="7c4fe-107">ADSI clients must specifically include the type library for each extension.</span></span> <span data-ttu-id="7c4fe-108">A biblioteca de tipos é necessária para Visual Basic habilitar as ligações iniciais.</span><span class="sxs-lookup"><span data-stu-id="7c4fe-108">The type library is required for Visual Basic to enable early bindings.</span></span> <span data-ttu-id="7c4fe-109">Os aplicativos cliente escritos em C/C++ podem chamar o método **QueryInterface** nas interfaces de extensão definidas nos arquivos de cabeçalho de extensão.</span><span class="sxs-lookup"><span data-stu-id="7c4fe-109">Client applications written in C/C++ can call the **QueryInterface** method on the extension interfaces defined in the extension header files.</span></span>

 

 




