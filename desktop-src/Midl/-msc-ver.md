---
title: opção/msc_ver
description: A \_ opção/MSC ver é usada para permitir que MIDL gere código que inclui otimizações para versões diferentes de compiladores do Microsoft C/C++.
ms.assetid: cdcb8f3e-e791-44c2-8bea-e77f94cc1682
keywords:
- /msc_ver MIDL do comutador
topic_type:
- apiref
api_name:
- /msc_ver
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3620b3c8ffb1315a4d34eb0b4b2497c1cb3d805
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823332"
---
# <a name="msc_ver-switch"></a><span data-ttu-id="0e470-104">\_opção/MSC ver</span><span class="sxs-lookup"><span data-stu-id="0e470-104">/msc\_ver switch</span></span>

<span data-ttu-id="0e470-105">A opção **/MSC \_ Ver** é usada para permitir que MIDL gere código que inclui otimizações para versões diferentes de compiladores do Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="0e470-105">The **/msc\_ver** switch is used to allow MIDL to generate code that includes optimizations for different versions of Microsoft C/C++ compilers.</span></span>

``` syntax
midl /msc_ver version_number
```

## <a name="switch-options"></a><span data-ttu-id="0e470-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="0e470-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="0e470-107">*número de versão \_*</span><span class="sxs-lookup"><span data-stu-id="0e470-107">*version\_number*</span></span> 
</dt> <dd>

<span data-ttu-id="0e470-108">Especifica um número de versão de inteiro do compilador de Microsoft Visual C++ que será usado para compilar os stubs de cliente e de servidor do aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="0e470-108">Specifies an integer version number of the Microsoft Visual C++ compiler that will be used to compile the client and server stubs of the distributed application.</span></span> <span data-ttu-id="0e470-109">O número de versão padrão é 1100, que corresponde a Visual C++ versão 5,0.</span><span class="sxs-lookup"><span data-stu-id="0e470-109">The default version number is 1100, which corresponds to Visual C++ version 5.0.</span></span> <span data-ttu-id="0e470-110">O número de versão 1200 corresponde a Visual C++ versão 6,0 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="0e470-110">The version number 1200 corresponds to Visual C++ version 6.0, and so on.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e470-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e470-111">Remarks</span></span>

<span data-ttu-id="0e470-112">Em particular, os valores de versão de 1100 ou superior fazem com que o compilador MIDL gere código utilizando a diretiva **\_ \_ declspec (UUID ())** .</span><span class="sxs-lookup"><span data-stu-id="0e470-112">In particular, version values of 1100 or greater cause the MIDL compiler to generate code utilizing the **\_\_declspec(uuid())** directive.</span></span> <span data-ttu-id="0e470-113">Ele também ativa macros que usam as diretivas **\_ \_ declspec (selectany)** e **\_ \_ declspec (novtable)** .</span><span class="sxs-lookup"><span data-stu-id="0e470-113">It also activates macros that use the **\_\_declspec(selectany)** and **\_\_declspec(novtable)** directives.</span></span>

 

 




