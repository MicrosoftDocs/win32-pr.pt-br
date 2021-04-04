---
description: A versão de depuração do mecanismo XAudio2 valida parâmetros e fornece avisos detalhados e mensagens de erro.
ms.assetid: a7aaebf9-98d4-e96c-993d-b0d0b7074788
title: Instalações de depuração XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc50e710f30969e024078eeaf2660545e1da45c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647377"
---
# <a name="xaudio2-debugging-facilities"></a><span data-ttu-id="52c00-103">Instalações de depuração XAudio2</span><span class="sxs-lookup"><span data-stu-id="52c00-103">XAudio2 Debugging Facilities</span></span>

<span data-ttu-id="52c00-104">A versão de depuração do mecanismo XAudio2 valida parâmetros e fornece avisos detalhados e mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="52c00-104">The debug version of the XAudio2 engine validates parameters, and provides detailed warning and error messages.</span></span>

## <a name="setting-the-debug-logging-level-at-run-time"></a><span data-ttu-id="52c00-105">Configurando o nível de log de depuração em tempo de execução</span><span class="sxs-lookup"><span data-stu-id="52c00-105">Setting the Debug Logging Level at Run Time</span></span>

<span data-ttu-id="52c00-106">Você pode definir o nível de informações de depuração mostradas por XAudio2 a qualquer momento preenchendo uma estrutura de [**\_ \_ configuração de depuração XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration) com os sinalizadores para o nível de log desejado e, em seguida, passando a estrutura para o método [**IXAudio2:: SetDebugConfiguration**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-setdebugconfiguration) .</span><span class="sxs-lookup"><span data-stu-id="52c00-106">You can set the level of debugging information shown by XAudio2 at any time by filling out an [**XAUDIO2\_DEBUG\_CONFIGURATION**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration) structure with the flags for the desired logging level, and then pass the structure to the [**IXAudio2::SetDebugConfiguration**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-setdebugconfiguration) method.</span></span> <span data-ttu-id="52c00-107">Os valores passados para o método **IXAudio2:: SetDebugConfiguration** sempre substituem todos os valores padrão que foram definidos no registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="52c00-107">Values passed to the **IXAudio2::SetDebugConfiguration** method always override any default values that were set in the Windows registry.</span></span>

## <a name="debug-support"></a><span data-ttu-id="52c00-108">Suporte de depuração</span><span class="sxs-lookup"><span data-stu-id="52c00-108">Debug Support</span></span>

<span data-ttu-id="52c00-109">Os recursos de depuração estão sempre disponíveis para XAUDIO2 no Windows 8.</span><span class="sxs-lookup"><span data-stu-id="52c00-109">The debugging facilities are always available for XAUDIO2 in Windows 8.</span></span>

<span data-ttu-id="52c00-110">Para as versões do SDK do DirectX do XAUDIO2, você deve usar o **\_ \_ mecanismo de depuração do XAudio2** ao criar o objeto XAudio2 com o [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) e o sistema deve ter o tempo de execução do desenvolvedor do SDK do DirectX instalado para que a depuração tenha suporte.</span><span class="sxs-lookup"><span data-stu-id="52c00-110">For the DirectX SDK versions of XAUDIO2, you must use **XAUDIO2\_DEBUG\_ENGINE** when creating the XAUDIO2 object with [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) and the system must have the DirectX SDK Developer Runtime installed for debugging to be supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52c00-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="52c00-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52c00-112">Depuração de instalações</span><span class="sxs-lookup"><span data-stu-id="52c00-112">Debugging Facilities</span></span>](debugging-facilities.md)
</dt> <dt>

[<span data-ttu-id="52c00-113">Referência de programação em XAudio2</span><span class="sxs-lookup"><span data-stu-id="52c00-113">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 
