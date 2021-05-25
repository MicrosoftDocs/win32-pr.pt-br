---
description: A API do Direct3D 9 opera no XPDM (Windows XP Display Driver Model) ou no WDDM (Windows Vista Display Driver Model), dependendo do sistema operacional instalado.
ms.assetid: b552c822-aa01-4f1d-a0a6-1411ab006e7b
title: XPDM vs. WDDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12c7d811850c953eb53c346b628363a2642dda9
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343531"
---
# <a name="xpdm-vs-wddm"></a><span data-ttu-id="4c657-103">XPDM vs. WDDM</span><span class="sxs-lookup"><span data-stu-id="4c657-103">XPDM vs. WDDM</span></span>

<span data-ttu-id="4c657-104">A API do Direct3D 9 opera no XPDM (Windows XP Display Driver Model) ou no WDDM (Windows Vista Display Driver Model), dependendo do sistema operacional instalado.</span><span class="sxs-lookup"><span data-stu-id="4c657-104">The Direct3D 9 API operates on either the Windows XP display driver model (XPDM) or the Windows Vista display driver model (WDDM), depending on the operating system installed.</span></span> <span data-ttu-id="4c657-105">Há algumas diferenças na maneira como a API do Direct3D se comporta nos dois modelos de driver.</span><span class="sxs-lookup"><span data-stu-id="4c657-105">There are some differences in the way the Direct3D API behaves on the two driver models.</span></span>

-   [<span data-ttu-id="4c657-106">Proteger área de trabalho</span><span class="sxs-lookup"><span data-stu-id="4c657-106">Secure Desktop</span></span>](#secure-desktop)
-   [<span data-ttu-id="4c657-107">Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="4c657-107">Remote Desktop</span></span>](#remote-desktop)
-   [<span data-ttu-id="4c657-108">Serviço Windows</span><span class="sxs-lookup"><span data-stu-id="4c657-108">Windows Service</span></span>](#windows-service)
-   [<span data-ttu-id="4c657-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4c657-109">Related topics</span></span>](#related-topics)

## <a name="secure-desktop"></a><span data-ttu-id="4c657-110">Proteger área de trabalho</span><span class="sxs-lookup"><span data-stu-id="4c657-110">Secure Desktop</span></span>

<span data-ttu-id="4c657-111">A área de trabalho segura está ativa sempre que ocorrer qualquer uma das seguintes ações: o usuário bloqueia sua área de trabalho (Windows + L), a proteção de tela é ativada (quando nenhum usuário está conectado) ou por padrão quando o controle de conta de usuário apresenta um prompt.</span><span class="sxs-lookup"><span data-stu-id="4c657-111">The secure desktop is active whenever any of the following occur: the user locks their desktop (Windows+L), the screen saver activates (when no user is logged in), or by default when User Account Control presents a prompt.</span></span> <span data-ttu-id="4c657-112">Quando a área de trabalho segura estiver ativa, o dispositivo HAL não estará acessível.</span><span class="sxs-lookup"><span data-stu-id="4c657-112">When the secure desktop is active, the HAL device is not accessible.</span></span>

<span data-ttu-id="4c657-113">Diferenças entre XPDM e WDDM:</span><span class="sxs-lookup"><span data-stu-id="4c657-113">Differences between XPDM and WDDM:</span></span>

- <span data-ttu-id="4c657-114">A tentativa de criar um dispositivo de HAL de Direct3D9 falhará (com **D3DERR \_ não \_ disponível**) e qualquer dispositivo Direct3D 9 existente indicará um código de retorno de dispositivo perdido no presente.</span><span class="sxs-lookup"><span data-stu-id="4c657-114">Attempting to create a Direct3D9 HAL device will fail (with **D3DERR\_NOT\_AVAILABLE**), and any existing Direct3D 9 device will indicate a lost device return code on Present.</span></span>

- <span data-ttu-id="4c657-115">As APIs Direct3D9Ex e Direct3D 10 podem criar um dispositivo com êxito enquanto a área de trabalho segura está ativa e todas as chamadas para apresentar ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) ou dxgi) retornarão um código de status indicando que a área de trabalho não está disponível no momento.</span><span class="sxs-lookup"><span data-stu-id="4c657-115">Direct3D9Ex and Direct3D 10 APIs can successfully create a device while the secure desktop is active, and any calls to Present ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) or DXGI) will return a status code indicating the desktop is currently unavailable.</span></span>



 

## <a name="remote-desktop"></a><span data-ttu-id="4c657-116">Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="4c657-116">Remote Desktop</span></span>

<span data-ttu-id="4c657-117">Quando uma área de trabalho remota está ativa, a exibição é tratada pela máquina de exibição com o computador de hospedagem enviando informações pela rede.</span><span class="sxs-lookup"><span data-stu-id="4c657-117">When a remote desktop is active, the display is handled by the viewing machine with the hosting machine sending information via the network.</span></span>

<span data-ttu-id="4c657-118">Diferenças entre XPDM e WDDM:</span><span class="sxs-lookup"><span data-stu-id="4c657-118">Differences between XPDM and WDDM:</span></span>

- <span data-ttu-id="4c657-119">No XPDM, todas as tentativas de criar um dispositivo Direct3D 9 em uma área de trabalho remota falharão.</span><span class="sxs-lookup"><span data-stu-id="4c657-119">On XPDM, all attempts to create a Direct3D 9 device on a remote desktop will fail.</span></span>

- <span data-ttu-id="4c657-120">No WDDM, a área de trabalho remota dá suporte à criação de um dispositivo HAL em uma sessão de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="4c657-120">On WDDM, remote desktop does support creating a HAL device over a remote desktop session.</span></span>



 

## <a name="windows-service"></a><span data-ttu-id="4c657-121">Serviço Windows</span><span class="sxs-lookup"><span data-stu-id="4c657-121">Windows Service</span></span>

<span data-ttu-id="4c657-122">Um serviço do Windows é um processo executado em segundo plano, controlado pelo SCM (Gerenciador de controle de serviço).</span><span class="sxs-lookup"><span data-stu-id="4c657-122">A Windows service is a process that runs in the background, controlled by the service-control manager (SCM).</span></span> <span data-ttu-id="4c657-123">Um serviço é executado independentemente do Active Desktop e, portanto, tem a capacidade limitada de interagir com os usuários.</span><span class="sxs-lookup"><span data-stu-id="4c657-123">A service runs independent of the active desktop and therefore has limited ability to interact with users.</span></span>

<span data-ttu-id="4c657-124">Diferenças entre XPDM e WDDM:</span><span class="sxs-lookup"><span data-stu-id="4c657-124">Differences between XPDM and WDDM:</span></span>

- <span data-ttu-id="4c657-125">No WDDM, o Isolamento da Sessão 0 garante que um serviço não tenha acesso a nenhuma área de trabalho do usuário como uma medida de segurança, portanto, um dispositivo DIRECT3D 9 HAL nunca está disponível em um serviço Windows.</span><span class="sxs-lookup"><span data-stu-id="4c657-125">On WDDM, Session 0 Isolation ensures that a service does not have access to any user desktop as a security measure, therefore, a Direct3D 9 HAL device is never available from a Windows service.</span></span>



 

> [!Note]  
> <span data-ttu-id="4c657-126">Não é possível usar o Direct3D 9 em um serviço Windows.</span><span class="sxs-lookup"><span data-stu-id="4c657-126">You cannot use Direct3D 9 in a Windows service.</span></span> <span data-ttu-id="4c657-127">Para obter mais informações, consulte [o artigo de suporte da Microsoft 978635](https://support.microsoft.com/kb/978635).</span><span class="sxs-lookup"><span data-stu-id="4c657-127">For more information, see [Microsoft support article 978635](https://support.microsoft.com/kb/978635).</span></span>

 


<span data-ttu-id="4c657-128">A tabela a seguir resume as diferenças listadas aqui.</span><span class="sxs-lookup"><span data-stu-id="4c657-128">The following table summarizes the differences listed here.</span></span>



| <span data-ttu-id="4c657-129">Área de Trabalho Segura</span><span class="sxs-lookup"><span data-stu-id="4c657-129">Secure Desktop</span></span> | <span data-ttu-id="4c657-130">Xpdm</span><span class="sxs-lookup"><span data-stu-id="4c657-130">XPDM</span></span> | <span data-ttu-id="4c657-131">WDDM (Direct3D9)</span><span class="sxs-lookup"><span data-stu-id="4c657-131">WDDM (Direct3D9)</span></span> | <span data-ttu-id="4c657-132">WDDM(Direct3D9Ex/Direct3D10)</span><span class="sxs-lookup"><span data-stu-id="4c657-132">WDDM(Direct3D9Ex/Direct3D10)</span></span> |
|-----------------|------|------------------|------------------------------|
| <span data-ttu-id="4c657-133">NULLREF</span><span class="sxs-lookup"><span data-stu-id="4c657-133">NULLREF</span></span>         | <span data-ttu-id="4c657-134">Sim</span><span class="sxs-lookup"><span data-stu-id="4c657-134">Yes</span></span>  | <span data-ttu-id="4c657-135">Sim</span><span class="sxs-lookup"><span data-stu-id="4c657-135">Yes</span></span>              | <span data-ttu-id="4c657-136">Sim</span><span class="sxs-lookup"><span data-stu-id="4c657-136">Yes</span></span>                          |
| <span data-ttu-id="4c657-137">Hal</span><span class="sxs-lookup"><span data-stu-id="4c657-137">HAL</span></span>             | <span data-ttu-id="4c657-138">Não</span><span class="sxs-lookup"><span data-stu-id="4c657-138">No</span></span>   | <span data-ttu-id="4c657-139">Não</span><span class="sxs-lookup"><span data-stu-id="4c657-139">No</span></span>               | <span data-ttu-id="4c657-140">Sim</span><span class="sxs-lookup"><span data-stu-id="4c657-140">Yes</span></span>                          |
| <span data-ttu-id="4c657-141">REF</span><span class="sxs-lookup"><span data-stu-id="4c657-141">REF</span></span>             | <span data-ttu-id="4c657-142">Sim</span><span class="sxs-lookup"><span data-stu-id="4c657-142">Yes</span></span>  | <span data-ttu-id="4c657-143">Sim</span><span class="sxs-lookup"><span data-stu-id="4c657-143">Yes</span></span>              | <span data-ttu-id="4c657-144">Sim</span><span class="sxs-lookup"><span data-stu-id="4c657-144">Yes</span></span>                          |
| <span data-ttu-id="4c657-145">Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="4c657-145">Remote Desktop</span></span>  |      |                  |                              |
| <span data-ttu-id="4c657-146">NULLREF</span><span class="sxs-lookup"><span data-stu-id="4c657-146">NULLREF</span></span>         | <span data-ttu-id="4c657-147">Não</span><span class="sxs-lookup"><span data-stu-id="4c657-147">No</span></span>   | <span data-ttu-id="4c657-148">Sim</span><span class="sxs-lookup"><span data-stu-id="4c657-148">Yes</span></span>              | <span data-ttu-id="4c657-149">Sim</span><span class="sxs-lookup"><span data-stu-id="4c657-149">Yes</span></span>                          |
| <span data-ttu-id="4c657-150">Hal</span><span class="sxs-lookup"><span data-stu-id="4c657-150">HAL</span></span>             | <span data-ttu-id="4c657-151">Não</span><span class="sxs-lookup"><span data-stu-id="4c657-151">No</span></span>   | <span data-ttu-id="4c657-152">Sim</span><span class="sxs-lookup"><span data-stu-id="4c657-152">Yes</span></span>              | <span data-ttu-id="4c657-153">Sim</span><span class="sxs-lookup"><span data-stu-id="4c657-153">Yes</span></span>                          |
| <span data-ttu-id="4c657-154">REF</span><span class="sxs-lookup"><span data-stu-id="4c657-154">REF</span></span>             | <span data-ttu-id="4c657-155">Sim</span><span class="sxs-lookup"><span data-stu-id="4c657-155">Yes</span></span>  | <span data-ttu-id="4c657-156">Sim</span><span class="sxs-lookup"><span data-stu-id="4c657-156">Yes</span></span>              | <span data-ttu-id="4c657-157">Sim</span><span class="sxs-lookup"><span data-stu-id="4c657-157">Yes</span></span>                          |
| <span data-ttu-id="4c657-158">Serviço Windows</span><span class="sxs-lookup"><span data-stu-id="4c657-158">Windows Service</span></span> |      |                  |                              |
| <span data-ttu-id="4c657-159">NULLREF</span><span class="sxs-lookup"><span data-stu-id="4c657-159">NULLREF</span></span>         | <span data-ttu-id="4c657-160">Não</span><span class="sxs-lookup"><span data-stu-id="4c657-160">No</span></span>   | <span data-ttu-id="4c657-161">Não</span><span class="sxs-lookup"><span data-stu-id="4c657-161">No</span></span>               | <span data-ttu-id="4c657-162">Não</span><span class="sxs-lookup"><span data-stu-id="4c657-162">No</span></span>                           |
| <span data-ttu-id="4c657-163">Hal</span><span class="sxs-lookup"><span data-stu-id="4c657-163">HAL</span></span>             | <span data-ttu-id="4c657-164">Não</span><span class="sxs-lookup"><span data-stu-id="4c657-164">No</span></span>   | <span data-ttu-id="4c657-165">Não</span><span class="sxs-lookup"><span data-stu-id="4c657-165">No</span></span>               | <span data-ttu-id="4c657-166">Não</span><span class="sxs-lookup"><span data-stu-id="4c657-166">No</span></span>                           |
| <span data-ttu-id="4c657-167">REF</span><span class="sxs-lookup"><span data-stu-id="4c657-167">REF</span></span>             | <span data-ttu-id="4c657-168">Não</span><span class="sxs-lookup"><span data-stu-id="4c657-168">No</span></span>   | <span data-ttu-id="4c657-169">Não</span><span class="sxs-lookup"><span data-stu-id="4c657-169">No</span></span>               | <span data-ttu-id="4c657-170">Não</span><span class="sxs-lookup"><span data-stu-id="4c657-170">No</span></span>                           |
| <span data-ttu-id="4c657-171">WARP10</span><span class="sxs-lookup"><span data-stu-id="4c657-171">WARP10</span></span>          | <span data-ttu-id="4c657-172">N/D</span><span class="sxs-lookup"><span data-stu-id="4c657-172">N/A</span></span>  | <span data-ttu-id="4c657-173">N/D</span><span class="sxs-lookup"><span data-stu-id="4c657-173">N/A</span></span>              | <span data-ttu-id="4c657-174">Sim</span><span class="sxs-lookup"><span data-stu-id="4c657-174">Yes</span></span>                          |



 

<span data-ttu-id="4c657-175">Para obter mais informações sobre XPDM, WDDM, Direct3D9Ex e Direct3D 10, consulte [APIs gráficas no Windows](../direct3darticles/graphics-apis-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="4c657-175">For more information about XPDM, WDDM, Direct3D9Ex, and Direct3D 10, see [Graphics APIs in Windows](../direct3darticles/graphics-apis-in-windows-vista.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c657-176">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4c657-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c657-177">Dispositivos Direct3D</span><span class="sxs-lookup"><span data-stu-id="4c657-177">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
