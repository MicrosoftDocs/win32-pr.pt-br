---
description: Você está tentando encontrar mais informações sobre objetos do Direct3D durante a depuração? Por exemplo, a captura de tela a seguir mostra o que você normalmente vê quando examina uma interface do Direct3D na janela Watch.
ms.assetid: 365451f8-e93e-4cc4-b688-2e668518c245
title: Habilitando informações de depuração do Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17bb46cf8658d0417d021faa6bdbefd10822d1dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087217"
---
# <a name="enabling-direct3d-debug-information-direct3d-9"></a><span data-ttu-id="2df76-104">Habilitando informações de depuração do Direct3D (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2df76-104">Enabling Direct3D Debug Information (Direct3D 9)</span></span>

<span data-ttu-id="2df76-105">Você está tentando encontrar mais informações sobre objetos do Direct3D durante a depuração?</span><span class="sxs-lookup"><span data-stu-id="2df76-105">Are you trying to find out more information about Direct3D objects during debug?</span></span> <span data-ttu-id="2df76-106">Por exemplo, a captura de tela a seguir mostra o que você normalmente vê quando examina uma interface do Direct3D na janela Watch.</span><span class="sxs-lookup"><span data-stu-id="2df76-106">For instance, the following screen shot shows what you typically see when you look at a Direct3D interface in the watch window.</span></span>

![captura de tela de uma interface do Direct3D na janela Watch](images/d3d-debug-info1.png)

<span data-ttu-id="2df76-108">Você pode habilitar os principais objetos de depuração para que um objeto espelhado que contém todas as propriedades do objeto possa ser exibido na janela Watch.</span><span class="sxs-lookup"><span data-stu-id="2df76-108">You can enable the core debug objects so that a mirrored object which contains all of the properties of the object can be viewed in the watch window.</span></span> <span data-ttu-id="2df76-109">Basta incluir a seguinte \# definição no seu código antes do arquivo d3d9. h:</span><span class="sxs-lookup"><span data-stu-id="2df76-109">Simply include the following \#define in your code before the D3D9.h file:</span></span>


```
#define D3D_DEBUG_INFO
```



<span data-ttu-id="2df76-110">Para habilitar as informações de depuração, a \# definição deve ser criada antes do arquivo d3d9. h (qualquer programa que use DXUT habilitará automaticamente \_ \_ as informações de depuração do D3D quando o programa for compilado para depuração).</span><span class="sxs-lookup"><span data-stu-id="2df76-110">To enable debug information, the \#define must get built before the D3D9.h file (Any program using DXUT will automatically enable D3D\_DEBUG\_INFO when the program is compiled for debug).</span></span> <span data-ttu-id="2df76-111">Se você estiver executando um exemplo de SDK, poderá ver isso em DXStdAfx. h (que afeta todos os exemplos de C++).</span><span class="sxs-lookup"><span data-stu-id="2df76-111">If you are running a SDK sample, you can see this in DXStdAfx.h (which affects all the C++ samples).</span></span> <span data-ttu-id="2df76-112">Você também deve estar executando o tempo de execução de debug Direct3D (que pode ser habilitado no painel de controle, se necessário).</span><span class="sxs-lookup"><span data-stu-id="2df76-112">You must also be running the debug Direct3D runtime (which can be enabled from the Control Panel if necessary).</span></span>

<span data-ttu-id="2df76-113">Aqui está um exemplo usando o [exemplo BasicHLSL](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="2df76-113">Here's an example using the [BasicHLSL Sample](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx).</span></span>

1.  <span data-ttu-id="2df76-114">Adicione o \# definir ao arquivo Dxstdafx. h antes da linha 37.</span><span class="sxs-lookup"><span data-stu-id="2df76-114">Add the \#define to the Dxstdafx.h file before line 37.</span></span>
2.  <span data-ttu-id="2df76-115">Compilar um projeto de depuração.</span><span class="sxs-lookup"><span data-stu-id="2df76-115">Build a debug project.</span></span>
3.  <span data-ttu-id="2df76-116">Definir um ponto de interrupção na linha 307 em BasicHLSL. cpp</span><span class="sxs-lookup"><span data-stu-id="2df76-116">Set a breakpoint at line 307 in BasicHLSL.cpp</span></span>
4.  <span data-ttu-id="2df76-117">Execute o depurador.</span><span class="sxs-lookup"><span data-stu-id="2df76-117">Run the debugger.</span></span>

<span data-ttu-id="2df76-118">A captura de tela a seguir mostra o tipo de informações detalhadas que você pode obter sobre um objeto de textura de Direct3D na janela Watch.</span><span class="sxs-lookup"><span data-stu-id="2df76-118">The following screen shot shows the kind of detailed information you can get about a Direct3D texture object from the watch window.</span></span>

![captura de tela de um objeto de textura de Direct3D na janela Watch](images/d3d-debug-info2.png)

> [!Note]
>
> <span data-ttu-id="2df76-120">Os nomes de propriedade de objeto são visíveis e os valores só são corretos quando o tempo de execução de depuração está habilitado.</span><span class="sxs-lookup"><span data-stu-id="2df76-120">The object property names are visible and the values are correct only when the debug runtime is enabled.</span></span> <span data-ttu-id="2df76-121">Ao executar no tempo de execução de varejo, os valores são inválidos.</span><span class="sxs-lookup"><span data-stu-id="2df76-121">When running against the retail runtime, the values are invalid.</span></span>

 

## <a name="use-the-call-stack-for-extended-debug"></a><span data-ttu-id="2df76-122">Usar a pilha de chamadas para depuração estendida</span><span class="sxs-lookup"><span data-stu-id="2df76-122">Use the Call Stack for Extended Debug</span></span>

<span data-ttu-id="2df76-123">Com a depuração do Direct3D habilitada, você também pode examinar uma pilha de chamadas cada vez que um objeto é criado.</span><span class="sxs-lookup"><span data-stu-id="2df76-123">With Direct3D debug enabled, you can also look at a call stack each time an object is created.</span></span> <span data-ttu-id="2df76-124">Isso tornará seu aplicativo muito lento, mas poderá ser usado para verificar se há vazamentos de recursos.</span><span class="sxs-lookup"><span data-stu-id="2df76-124">This will make your application very slow, but can be used to check for resource leaks.</span></span> <span data-ttu-id="2df76-125">Para gravar a pilha de chamadas, defina a seguinte chave do registro como 1:</span><span class="sxs-lookup"><span data-stu-id="2df76-125">To write out the call stack, set the following registry key to 1:</span></span>


```
\\HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Direct3D\\
D3D9Debugging\\EnableCreationStack
```



<span data-ttu-id="2df76-126">Criar seu aplicativo com depuração habilitada lhe dará acesso a essa variável adicional:</span><span class="sxs-lookup"><span data-stu-id="2df76-126">Building your application with debug enabled will give you access to this additional variable:</span></span>


```
  LPCWSTR CreationCallStack;
```



<span data-ttu-id="2df76-127">Essa variável armazenará a pilha de chamadas cada vez que um objeto for criado.</span><span class="sxs-lookup"><span data-stu-id="2df76-127">This variable will store the call stack each time that an object is created.</span></span> <span data-ttu-id="2df76-128">Isso tornará seu aplicativo muito lento, mas poderá ser usado para depurar vazamentos de recursos.</span><span class="sxs-lookup"><span data-stu-id="2df76-128">This will make your application very slow, but can be used to debug resource leaks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2df76-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2df76-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2df76-130">Dicas de programação</span><span class="sxs-lookup"><span data-stu-id="2df76-130">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 



