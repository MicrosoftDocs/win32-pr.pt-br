---
title: Compilação offline
description: A ferramenta de compilador de efeito (fxc.exe) foi projetada para compilação offline de sombreadores HLSL.
ms.assetid: 56806335-a0c7-4247-b40d-ba93486a88ac
keywords:
- FXC, compilação offline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e7c2bf96a24cb586a5d229a395cbf6dc0cb9ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641752"
---
# <a name="offline-compiling"></a><span data-ttu-id="f3f1b-104">Compilação offline</span><span class="sxs-lookup"><span data-stu-id="f3f1b-104">Offline compiling</span></span>

<span data-ttu-id="f3f1b-105">A ferramenta de compilador de efeito (fxc.exe) foi projetada para compilação offline de sombreadores HLSL.</span><span class="sxs-lookup"><span data-stu-id="f3f1b-105">The effect-compiler tool (fxc.exe) is designed for offline compilation of HLSL shaders.</span></span>

## <a name="compiling-with-the-current-compiler"></a><span data-ttu-id="f3f1b-106">Compilando com o compilador atual</span><span class="sxs-lookup"><span data-stu-id="f3f1b-106">Compiling with the current compiler</span></span>

<span data-ttu-id="f3f1b-107">Os modelos de sombreador com suporte do compilador atual são mostrados em [perfis](dx-graphics-tools-fxc-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="f3f1b-107">The shader models supported by the current compiler are shown in [Profiles](dx-graphics-tools-fxc-syntax.md).</span></span> <span data-ttu-id="f3f1b-108">Este exemplo compila um sombreador de pixel para o destino do modelo do sombreador 5,1.</span><span class="sxs-lookup"><span data-stu-id="f3f1b-108">This example compiles a pixel shader for the shader model 5.1 target.</span></span>

```
fxc /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

<span data-ttu-id="f3f1b-109">Neste exemplo:</span><span class="sxs-lookup"><span data-stu-id="f3f1b-109">In this example:</span></span>

-   <span data-ttu-id="f3f1b-110">\_o PS 5 \_ 1 é o perfil de destino.</span><span class="sxs-lookup"><span data-stu-id="f3f1b-110">ps\_5\_1 is the target profile.</span></span>
-   <span data-ttu-id="f3f1b-111">PixelShader1. fxc é o arquivo de objeto de saída que contém o sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="f3f1b-111">PixelShader1.fxc is the output object file containing the compiled shader.</span></span>
-   <span data-ttu-id="f3f1b-112">PixelShader1. HLSL é a origem.</span><span class="sxs-lookup"><span data-stu-id="f3f1b-112">PixelShader1.hlsl is the source.</span></span>

```
fxc /Od /Zi /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

<span data-ttu-id="f3f1b-113">As opções de depuração incluem opções adicionais para desabilitar a OD (otimizações de compilador) e habilitar informações de depuração (Zi), como números de linha e símbolos.</span><span class="sxs-lookup"><span data-stu-id="f3f1b-113">The debug options include additional options to disable compiler optimizations (Od) and enable debug information (Zi) like line numbers and symbols.</span></span>

<span data-ttu-id="f3f1b-114">Para obter uma lista completa das opções de linha de comando, consulte a página [sintaxe](dx-graphics-tools-fxc-syntax.md) .</span><span class="sxs-lookup"><span data-stu-id="f3f1b-114">For a full listing of the command-line options, see the [Syntax](dx-graphics-tools-fxc-syntax.md) page.</span></span>

## <a name="compiling-with-the-legacy-compiler"></a><span data-ttu-id="f3f1b-115">Compilando com o compilador herdado</span><span class="sxs-lookup"><span data-stu-id="f3f1b-115">Compiling with the legacy compiler</span></span>

<span data-ttu-id="f3f1b-116">A partir do Direct3D 10, não há mais suporte para alguns modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="f3f1b-116">Beginning with Direct3D 10, some shader models are no longer supported.</span></span> <span data-ttu-id="f3f1b-117">Isso inclui modelos de sombreador de pixel: PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3 e PS \_ 1 \_ 4 que dão suporte a recursos muito limitados e dependem de hardware.</span><span class="sxs-lookup"><span data-stu-id="f3f1b-117">These include pixel shader models: ps\_1\_1, ps\_1\_2, ps\_1\_3, and ps\_1\_4 which support very limited resources and are dependent on hardware.</span></span> <span data-ttu-id="f3f1b-118">O compilador foi reprojetado com o modelo de sombreador 2 (ou superior), o que permite maior eficiência com a compilação.</span><span class="sxs-lookup"><span data-stu-id="f3f1b-118">The compiler has been redesigned with shader model 2 (or greater) which allows for greater efficiencies with compilation.</span></span> <span data-ttu-id="f3f1b-119">Isso, é claro, exigirá que você esteja executando o hardware que dá suporte a modelos de sombreamento 2 e superior.</span><span class="sxs-lookup"><span data-stu-id="f3f1b-119">This of course will require that you are running on hardware that supports shader models 2 and greater.</span></span>

<span data-ttu-id="f3f1b-120">Observe também que você deve consultar as notas de versão do SDK associadas à sua versão do compilador FXC para o comportamento afetado pela opção/GEC.</span><span class="sxs-lookup"><span data-stu-id="f3f1b-120">Also note that you should consult the SDK release notes associated with your version of the FXC compiler for behavior affected by the /Gec switch.</span></span>

## <a name="using-the-effect-compiler-tool-in-a-subprocess"></a><span data-ttu-id="f3f1b-121">Usando a ferramenta de compilador de efeito em um subprocesso</span><span class="sxs-lookup"><span data-stu-id="f3f1b-121">Using the effect-compiler tool in a subprocess</span></span>

<span data-ttu-id="f3f1b-122">Se fxc.exe for gerado como um subprocesso por um aplicativo, é importante garantir que o aplicativo Verifique e leia os dados na saída ou os pipes de erro passados para a função CreateProcess.</span><span class="sxs-lookup"><span data-stu-id="f3f1b-122">If fxc.exe is spawned as a subprocess by an application it is important to ensure that the application checks for and reads any data in output or error pipes passed to the CreateProcess function.</span></span> <span data-ttu-id="f3f1b-123">Se o aplicativo só aguardar a conclusão do subprocesso e um dos pipes ficar cheio, o subprocesso nunca será concluído.</span><span class="sxs-lookup"><span data-stu-id="f3f1b-123">If the application only waits for the subprocess to finish and one of the pipes becomes full the subprocess will never finish.</span></span>

<span data-ttu-id="f3f1b-124">O código de exemplo a seguir ilustra a espera em um subprocesso e a leitura dos pipes de erro e saída anexados ao subprocesso.</span><span class="sxs-lookup"><span data-stu-id="f3f1b-124">The following example code illustrates waiting on a subprocess and reading the output and error pipes attached to the subprocess.</span></span> <span data-ttu-id="f3f1b-125">O conteúdo da `WaitHandles` matriz corresponde a identificadores para o subprocesso, o pipe para stdout e o pipe para stderr.</span><span class="sxs-lookup"><span data-stu-id="f3f1b-125">The contents of the `WaitHandles` array correspond to handles for the subprocess, the pipe for stdout and the pipe for stderr.</span></span>

```cpp
HANDLE WaitHandles[] = {
  piProcInfo.hProcess, hReadOutPipe, hReadErrorPipe
};

const DWORD BUFSIZE = 4096;
BYTE buff[BUFSIZE];

while (1)
{
    DWORD dwBytesRead, dwBytesAvailable;

    dwWaitResult = WaitForMultipleObjects(3, WaitHandles, FALSE, 60000L);

    // Read from the pipes...
    while (PeekNamedPipe(hReadOutPipe, NULL, 0, NULL, &dwBytesAvailable, NULL) && dwBytesAvailable)
    {
        ReadFile(hReadOutPipe, buff, BUFSIZE - 1, &dwBytesRead, 0);
        streamOut << std::string((char*)buff, (size_t)dwBytesRead);
    }
    while (PeekNamedPipe(hReadErrorPipe, NULL, 0, NULL, &dwBytesAvailable, NULL) && dwBytesAvailable)
    {
        ReadFile(hReadErrorPipe, buff, BUFSIZE - 1, &dwBytesRead, 0);
        streamError << std::string((char*)buff, (size_t)dwBytesRead);
    }

    // Process is done, or we timed out:
    if (dwWaitResult == WAIT_OBJECT_0 || dwWaitResult == WAIT_TIMEOUT)
        break;
}
```

<span data-ttu-id="f3f1b-126">Para obter informações adicionais sobre como gerar um processo, consulte a página de referência de [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span><span class="sxs-lookup"><span data-stu-id="f3f1b-126">For additional information on spawning a process see the reference page for [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3f1b-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f3f1b-127">Related topics</span></span>

* [<span data-ttu-id="f3f1b-128">Efeito-ferramenta do compilador</span><span class="sxs-lookup"><span data-stu-id="f3f1b-128">Effect-Compiler Tool</span></span>](fxc.md)