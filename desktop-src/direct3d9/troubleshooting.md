---
description: Este tópico lista as categorias comuns de problemas que você pode encontrar ao escrever aplicativos de Direct3D e como evitá-los.
ms.assetid: 27b87f0f-7118-4252-b6e8-6ea18a9399e4
title: Solução de problemas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6726e761dd8c15e2da18e6c370472a73e82cef0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105808223"
---
# <a name="troubleshooting-direct3d-9"></a><span data-ttu-id="e77e5-103">Solução de problemas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e77e5-103">Troubleshooting (Direct3D 9)</span></span>

<span data-ttu-id="e77e5-104">Este tópico lista as categorias comuns de problemas que você pode encontrar ao escrever aplicativos de Direct3D e como evitá-los.</span><span class="sxs-lookup"><span data-stu-id="e77e5-104">This topic lists common categories of problems that you might encounter when writing Direct3D applications, and how to prevent them.</span></span>

## <a name="device-creation"></a><span data-ttu-id="e77e5-105">Criação de dispositivo</span><span class="sxs-lookup"><span data-stu-id="e77e5-105">Device Creation</span></span>

<span data-ttu-id="e77e5-106">Se o aplicativo falhar durante a criação do dispositivo, verifique os erros comuns a seguir.</span><span class="sxs-lookup"><span data-stu-id="e77e5-106">If your application fails during device creation, check for the following common errors.</span></span>

-   <span data-ttu-id="e77e5-107">Certifique-se de verificar os recursos do dispositivo, particularmente as profundidades de renderização.</span><span class="sxs-lookup"><span data-stu-id="e77e5-107">Make sure you check the device capabilities, particularly the render depths.</span></span>
-   <span data-ttu-id="e77e5-108">Examine o código de erro.</span><span class="sxs-lookup"><span data-stu-id="e77e5-108">Examine the error code.</span></span> <span data-ttu-id="e77e5-109">D3DERR \_ OUTOFVIDEOMEMORY sempre é possível.</span><span class="sxs-lookup"><span data-stu-id="e77e5-109">D3DERR\_OUTOFVIDEOMEMORY is always possible.</span></span>
-   <span data-ttu-id="e77e5-110">Use a depuração de DLLs (bibliotecas de vínculo dinâmico) do DirectX e examine as mensagens de saída no depurador.</span><span class="sxs-lookup"><span data-stu-id="e77e5-110">Use the debug DirectX dynamic-link libraries (DLLs) and review output messages under the debugger.</span></span>

## <a name="using-lit-vertices"></a><span data-ttu-id="e77e5-111">Usando vértices acesos</span><span class="sxs-lookup"><span data-stu-id="e77e5-111">Using Lit Vertices</span></span>

<span data-ttu-id="e77e5-112">Os aplicativos que usam vértices acesos devem desabilitar o mecanismo de iluminação Direct3D definindo o \_ estado de renderização de iluminação D3DRS como **false**.</span><span class="sxs-lookup"><span data-stu-id="e77e5-112">Applications that use lit vertices should disable the Direct3D lighting engine by setting the D3DRS\_LIGHTING render state to **FALSE**.</span></span> <span data-ttu-id="e77e5-113">Por padrão, quando a iluminação está habilitada, o sistema define a cor de qualquer vértice que não contenha um vetor normal como 0 (preto), mesmo se o vértice de entrada contiver um valor de cor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="e77e5-113">By default, when lighting is enabled, the system sets the color for any vertex that doesn't contain a normal vector to 0 (black), even if the input vertex contained a nonzero color value.</span></span> <span data-ttu-id="e77e5-114">Como os vértices acesos Não, por sua natureza, contêm um vértice normal, todas as informações de cores passadas para o Direct3D serão perdidas durante a renderização se o mecanismo de iluminação estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="e77e5-114">Because lit-vertices don't, by their nature, contain a vertex normal, any color information passed to Direct3D is lost during rendering if the lighting engine is enabled.</span></span>

<span data-ttu-id="e77e5-115">Obviamente, a cor do vértice é importante para qualquer aplicativo que executa sua própria iluminação.</span><span class="sxs-lookup"><span data-stu-id="e77e5-115">Obviously, vertex color is important to any application that performs its own lighting.</span></span> <span data-ttu-id="e77e5-116">Para impedir que o sistema impondo os valores padrão, certifique-se de definir a \_ iluminação D3DRS como **false**.</span><span class="sxs-lookup"><span data-stu-id="e77e5-116">To prevent the system from imposing the default values, make sure you set D3DRS\_LIGHTING to **FALSE**.</span></span>

<span data-ttu-id="e77e5-117">Se o aplicativo for executado, mas nada estiver visível, verifique os erros comuns a seguir.</span><span class="sxs-lookup"><span data-stu-id="e77e5-117">If your application runs but nothing is visible, check for the following common errors.</span></span>

-   <span data-ttu-id="e77e5-118">Verifique se os triângulos não são degenerados.</span><span class="sxs-lookup"><span data-stu-id="e77e5-118">Ensure that your triangles are not degenerate.</span></span>
-   <span data-ttu-id="e77e5-119">Verifique se os triângulos não estão sendo refigurados.</span><span class="sxs-lookup"><span data-stu-id="e77e5-119">Ensure that your triangles are not being culled.</span></span>
-   <span data-ttu-id="e77e5-120">Certifique-se de que suas transformações sejam consistentes internamente.</span><span class="sxs-lookup"><span data-stu-id="e77e5-120">Make sure that your transformations are internally consistent.</span></span>
-   <span data-ttu-id="e77e5-121">Verifique as configurações do visor para ter certeza de que eles permitem que os triângulos sejam vistos.</span><span class="sxs-lookup"><span data-stu-id="e77e5-121">Check the viewport settings to be sure they allow your triangles to be seen.</span></span>

## <a name="debugging"></a><span data-ttu-id="e77e5-122">Depuração</span><span class="sxs-lookup"><span data-stu-id="e77e5-122">Debugging</span></span>

<span data-ttu-id="e77e5-123">A depuração de um aplicativo Direct3D pode ser desafiadora.</span><span class="sxs-lookup"><span data-stu-id="e77e5-123">Debugging a Direct3D application can be challenging.</span></span> <span data-ttu-id="e77e5-124">Experimente as técnicas a seguir, além de verificar todos os valores de retorno, um pedaço especialmente importante de conselhos na programação do Direct3D, que depende de implementações de hardware muito diferentes.</span><span class="sxs-lookup"><span data-stu-id="e77e5-124">Try the following techniques, in addition to checking all the return values - a particularly important piece of advice in Direct3D programming, which is dependent on very different hardware implementations.</span></span>

-   <span data-ttu-id="e77e5-125">Alterne para Debug DLLs.</span><span class="sxs-lookup"><span data-stu-id="e77e5-125">Switch to debug DLLs.</span></span>
-   <span data-ttu-id="e77e5-126">Forçar um dispositivo somente de software, desativando a aceleração de hardware mesmo quando ela estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="e77e5-126">Force a software-only device, turning off hardware acceleration even when it is available.</span></span>
-   <span data-ttu-id="e77e5-127">Forçar superfícies na memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="e77e5-127">Force surfaces into system memory.</span></span>
-   <span data-ttu-id="e77e5-128">Crie uma opção para ser executada em uma janela, para que você possa usar um depurador integrado.</span><span class="sxs-lookup"><span data-stu-id="e77e5-128">Create an option to run in a window, so that you can use an integrated debugger.</span></span>

<span data-ttu-id="e77e5-129">A segunda e terceira opções dessa lista podem ajudá-lo a evitar o bloqueio de Win16 que, de outra forma, pode fazer com que o depurador trave.</span><span class="sxs-lookup"><span data-stu-id="e77e5-129">The second and third options in this list can help you avoid the Win16 lock which can otherwise cause your debugger to hang.</span></span>

<span data-ttu-id="e77e5-130">Além disso, tente adicionar as entradas a seguir a Win.ini.</span><span class="sxs-lookup"><span data-stu-id="e77e5-130">Also, try adding the following entries to Win.ini.</span></span>


```
[Direct3D] 
debug=3 
[DirectDraw] 
debug=3 
```



## <a name="borland-floating-point-initialization"></a><span data-ttu-id="e77e5-131">Inicialização do Borland Floating-Point</span><span class="sxs-lookup"><span data-stu-id="e77e5-131">Borland Floating-Point Initialization</span></span>

<span data-ttu-id="e77e5-132">Compiladores da Borland reportam exceções de ponto flutuante de uma maneira que é incompatível com o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e77e5-132">Compilers from Borland report floating-point exceptions in a manner that is incompatible with Direct3D.</span></span> <span data-ttu-id="e77e5-133">Para resolver esse problema, inclua um \_ manipulador de exceção matherr como o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e77e5-133">To solve this problem, include a \_matherr exception handler like the following:</span></span>


```
// Borland floating point initialization 
#include <math.h>
#include <float.h>

void initfp(void)
{
    // Disable floating point exceptions
    _control87(MCW_EM,MCW_EM);
}

int _matherr(struct _exception  *e)
{
    e;               // Dummy reference to catch the warning
    return 1;        // Error has been handled
}
```



## <a name="parameter-validation"></a><span data-ttu-id="e77e5-134">Validação de parâmetro</span><span class="sxs-lookup"><span data-stu-id="e77e5-134">Parameter Validation</span></span>

<span data-ttu-id="e77e5-135">Por motivos de desempenho, a versão de depuração do tempo de execução do modo do Direct3D Immediate executa mais validação de parâmetro do que a versão comercial, que às vezes não executa nenhuma validação.</span><span class="sxs-lookup"><span data-stu-id="e77e5-135">For performance reasons, the debug version of the Direct3D Immediate Mode run time performs more parameter validation than the retail version, which sometimes performs no validation at all.</span></span> <span data-ttu-id="e77e5-136">Isso permite que os aplicativos executem uma depuração robusta com o componente de tempo de execução de depuração mais lento antes de usar a versão de varejo mais rápida para o ajuste de desempenho e a versão final.</span><span class="sxs-lookup"><span data-stu-id="e77e5-136">This enables applications to perform robust debugging with the slower debug run-time component before using the faster retail version for performance tuning and final release.</span></span>

<span data-ttu-id="e77e5-137">Embora vários métodos de modo do Direct3D Immediate imponham limites nos valores que eles podem aceitar, esses limites geralmente são verificados e aplicados pela versão de depuração do tempo de execução do modo do Direct3D Immediate.</span><span class="sxs-lookup"><span data-stu-id="e77e5-137">Although several Direct3D Immediate Mode methods impose limits on the values that they can accept, these limits are often only checked and enforced by the debug version of the Direct3D Immediate Mode run time.</span></span> <span data-ttu-id="e77e5-138">Os aplicativos devem estar em conformidade com esses limites ou resultados imprevisíveis e indesejáveis podem ocorrer durante a execução na versão comercial do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e77e5-138">Applications must conform to these limits, or unpredictable and undesirable results can occur when running on the retail version of Direct3D.</span></span> <span data-ttu-id="e77e5-139">Por exemplo, o método [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) aceita um parâmetro (primitiveCount) que indica o número de primitivos que o método processará.</span><span class="sxs-lookup"><span data-stu-id="e77e5-139">For example, the [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) method accepts a parameter (PrimitiveCount) that indicates the number of primitives that the method will render.</span></span> <span data-ttu-id="e77e5-140">O método só pode aceitar valores entre 0 e D3DMAXNUMPRIMITIVES.</span><span class="sxs-lookup"><span data-stu-id="e77e5-140">The method can only accept values between 0 and D3DMAXNUMPRIMITIVES.</span></span> <span data-ttu-id="e77e5-141">Na versão de depuração do Direct3D, se você passar mais de D3DMAXNUMPRIMITIVES primitivos, o método falhará normalmente, imprimindo uma mensagem de erro no log de erros e retornando um valor de erro para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e77e5-141">In the debug version of Direct3D, if you pass more than D3DMAXNUMPRIMITIVES primitives, the method fails gracefully, printing an error message to the error log, and returning an error value to your application.</span></span> <span data-ttu-id="e77e5-142">Por outro lado, se o seu aplicativo fizer o mesmo erro quando ele estiver em execução com a versão de varejo do tempo de execução, o comportamento será indefinido.</span><span class="sxs-lookup"><span data-stu-id="e77e5-142">Conversely, if your application makes the same error when it is running with the retail version of the run time, behavior is undefined.</span></span> <span data-ttu-id="e77e5-143">Por motivos de desempenho, o método não valida os parâmetros, resultando em comportamento imprevisível e de situação completamente quando eles não são válidos.</span><span class="sxs-lookup"><span data-stu-id="e77e5-143">For performance reasons, the method does not validate the parameters, resulting in unpredictable and completely situational behavior when they are not valid.</span></span> <span data-ttu-id="e77e5-144">Em alguns casos, a chamada pode funcionar e, em outros casos, pode causar uma falha de memória no Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e77e5-144">In some cases the call might work, and in other cases it might cause a memory fault in Direct3D.</span></span> <span data-ttu-id="e77e5-145">Se uma chamada inválida funciona consistentemente com uma configuração de hardware específica e a versão do DirectX, não há nenhuma garantia de que ela continuará a funcionar em outro hardware ou em versões posteriores do DirectX.</span><span class="sxs-lookup"><span data-stu-id="e77e5-145">If an invalid call consistently works with a particular hardware configuration and DirectX version, there is no guarantee that it will continue to function on other hardware or with later releases of DirectX.</span></span>

<span data-ttu-id="e77e5-146">Se seu aplicativo encontrar falhas não explicadas ao executar com o arquivo de tempo de execução do Direct3D de varejo, teste em relação à versão de depuração e examine de forma mais detalhada os casos em que seu aplicativo passa parâmetros inválidos.</span><span class="sxs-lookup"><span data-stu-id="e77e5-146">If your application encounters unexplained failures when running with the retail Direct3D run-time file, test against the debug version and look closely for cases where your application passes invalid parameters.</span></span> <span data-ttu-id="e77e5-147">Use o miniaplicativo do painel de controle do DirectX, alterne para o tempo de execução de depuração, se necessário, e marque a opção "interromper no D3DError".</span><span class="sxs-lookup"><span data-stu-id="e77e5-147">Use the DirectX control panel applet, switch to the debug runtime if necessary, and check the "Break on D3DError" option.</span></span> <span data-ttu-id="e77e5-148">Essa opção forçará o tempo de execução a usar o método DebugBreak do Windows para forçar o aplicativo a parar quando um bug de aplicativo for detectado.</span><span class="sxs-lookup"><span data-stu-id="e77e5-148">This option will force the runtime to use the Windows DebugBreak method in order to force the application to stop when an application bug is detected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e77e5-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e77e5-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e77e5-150">Dicas de programação</span><span class="sxs-lookup"><span data-stu-id="e77e5-150">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
