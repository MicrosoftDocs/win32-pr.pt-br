---
title: Identificadores de associação automática
description: Os identificadores de associação automática são úteis quando o aplicativo não requer um servidor específico e quando não precisa manter nenhuma informação de estado entre o cliente e o servidor.
ms.assetid: ba049369-6c8b-4313-a266-e0364a30056e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fe83d3f9029e0384c87e5e409583ff70f1e91ac
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294386"
---
# <a name="automatic-binding-handles"></a><span data-ttu-id="a75e9-103">Identificadores de associação automática</span><span class="sxs-lookup"><span data-stu-id="a75e9-103">Automatic Binding Handles</span></span>

<span data-ttu-id="a75e9-104">Os identificadores de associação automática são úteis quando o aplicativo não requer um servidor específico e quando não precisa manter nenhuma informação de estado entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="a75e9-104">Automatic binding handles are useful when the application does not require a specific server and when it does not need to maintain any state information between the client and server.</span></span> <span data-ttu-id="a75e9-105">Quando você usa um identificador de ligação automática, não precisa escrever nenhum código de aplicativo cliente para lidar com associações e identificadores — basta especificar o uso do identificador de ligação automática no arquivo de configuração de aplicativo (ACF).</span><span class="sxs-lookup"><span data-stu-id="a75e9-105">When you use an automatic binding handle, you do not have to write any client application code to deal with binding and handles—you simply specify the use of the automatic binding handle in the application configuration file (ACF).</span></span> <span data-ttu-id="a75e9-106">Em seguida, o stub define o identificador e gerencia a associação.</span><span class="sxs-lookup"><span data-stu-id="a75e9-106">The stub then defines the handle and manages the binding.</span></span>

<span data-ttu-id="a75e9-107">Por exemplo, uma operação de carimbo de data/hora pode ser implementada usando um identificador automático.</span><span class="sxs-lookup"><span data-stu-id="a75e9-107">For example, a time-stamp operation can be implemented using an auto handle.</span></span> <span data-ttu-id="a75e9-108">Não faz diferença ao aplicativo cliente que o servidor fornece com o carimbo de data/hora, pois ele pode aceitar o tempo de qualquer servidor disponível.</span><span class="sxs-lookup"><span data-stu-id="a75e9-108">It makes no difference to the client application which server provides it with the time stamp because it can accept the time from any available server.</span></span>

> [!Note]  
> <span data-ttu-id="a75e9-109">Os identificadores automáticos não têm suporte para a plataforma Macintosh.</span><span class="sxs-lookup"><span data-stu-id="a75e9-109">Auto handles are not supported for the Macintosh platform.</span></span>

 

<span data-ttu-id="a75e9-110">Você especifica o uso de identificadores automáticos, incluindo o atributo de \[ [**\_ identificador automático**](/windows/desktop/Midl/auto-handle) \] no ACF.</span><span class="sxs-lookup"><span data-stu-id="a75e9-110">You specify the use of auto handles by including the \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\] attribute in the ACF.</span></span> <span data-ttu-id="a75e9-111">O exemplo de carimbo de data/hora usa o seguinte ACF:</span><span class="sxs-lookup"><span data-stu-id="a75e9-111">The time-stamp example uses the following ACF:</span></span>

``` syntax
/* ACF file */
[
  auto_handle
]
interface autoh
{
}
```

<span data-ttu-id="a75e9-112">Quando o ACF não inclui nenhum outro atributo de identificador e quando os procedimentos remotos não usam identificadores explícitos, o compilador MIDL usa identificadores automáticos por padrão.</span><span class="sxs-lookup"><span data-stu-id="a75e9-112">When the ACF does not include any other handle attribute, and when the remote procedures do not use explicit handles, the MIDL compiler uses automatic handles by default.</span></span> <span data-ttu-id="a75e9-113">Ele também usa identificadores automáticos como padrão quando o ACF não está presente.</span><span class="sxs-lookup"><span data-stu-id="a75e9-113">It also uses automatic handles as the default when the ACF is not present.</span></span>

<span data-ttu-id="a75e9-114">Os procedimentos remotos são especificados no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="a75e9-114">The remote procedures are specified in the IDL file.</span></span> <span data-ttu-id="a75e9-115">O identificador automático não deve aparecer como um argumento para o procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="a75e9-115">The auto handle must not appear as an argument to the remote procedure.</span></span> <span data-ttu-id="a75e9-116">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="a75e9-116">For example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid (6B29FC40-CA47-1067-B31D-00DD010662DA),
  version(1.0),
  pointer_default(unique)
]
interface autoh
{
  void GetTime([out] long * time);
  void Shutdown(void);
}
```

<span data-ttu-id="a75e9-117">O benefício do identificador automático é que o desenvolvedor não precisa escrever nenhum código para gerenciar o identificador; os stubs gerenciam a associação automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a75e9-117">The benefit of the auto handle is that the developer does not have to write any code to manage the handle; the stubs manage the binding automatically.</span></span> <span data-ttu-id="a75e9-118">Isso é significativamente diferente do [exemplo Hello, World](tutorial.md), em que o cliente gerencia o identificador primitivo implícito definido no ACF e deve chamar várias funções de tempo de execução para estabelecer o identificador de associação.</span><span class="sxs-lookup"><span data-stu-id="a75e9-118">This is significantly different from the [Hello, World example](tutorial.md), where the client manages the implicit primitive handle defined in the ACF and must call several run-time functions to establish the binding handle.</span></span>

 

 