---
description: Define os níveis de multiamostragem de cena completa que o dispositivo pode aplicar.
ms.assetid: 1a3c1efe-f5b1-47a1-a5f5-ac49d318f3b8
title: Enumeração de D3DMULTISAMPLE_TYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMULTISAMPLE_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: da8f9c1c8bb3aa74c0ab22a5cc701e7d835898de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298662"
---
# <a name="d3dmultisample_type-enumeration"></a><span data-ttu-id="c0bea-103">\_Enumeração de tipo D3DMULTISAMPLE</span><span class="sxs-lookup"><span data-stu-id="c0bea-103">D3DMULTISAMPLE\_TYPE enumeration</span></span>

<span data-ttu-id="c0bea-104">Define os níveis de multiamostragem de cena completa que o dispositivo pode aplicar.</span><span class="sxs-lookup"><span data-stu-id="c0bea-104">Defines the levels of full-scene multisampling that the device can apply.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0bea-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0bea-105">Syntax</span></span>


```C++
typedef enum D3DMULTISAMPLE_TYPE { 
  D3DMULTISAMPLE_NONE          = 0,
  D3DMULTISAMPLE_NONMASKABLE   = 1,
  D3DMULTISAMPLE_2_SAMPLES     = 2,
  D3DMULTISAMPLE_3_SAMPLES     = 3,
  D3DMULTISAMPLE_4_SAMPLES     = 4,
  D3DMULTISAMPLE_5_SAMPLES     = 5,
  D3DMULTISAMPLE_6_SAMPLES     = 6,
  D3DMULTISAMPLE_7_SAMPLES     = 7,
  D3DMULTISAMPLE_8_SAMPLES     = 8,
  D3DMULTISAMPLE_9_SAMPLES     = 9,
  D3DMULTISAMPLE_10_SAMPLES    = 10,
  D3DMULTISAMPLE_11_SAMPLES    = 11,
  D3DMULTISAMPLE_12_SAMPLES    = 12,
  D3DMULTISAMPLE_13_SAMPLES    = 13,
  D3DMULTISAMPLE_14_SAMPLES    = 14,
  D3DMULTISAMPLE_15_SAMPLES    = 15,
  D3DMULTISAMPLE_16_SAMPLES    = 16,
  D3DMULTISAMPLE_FORCE_DWORD   = 0xffffffff
} D3DMULTISAMPLE_TYPE, *LPD3DMULTISAMPLE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="c0bea-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="c0bea-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c0bea-107"><span id="D3DMULTISAMPLE_NONE"></span><span id="d3dmultisample_none"></span>**D3DMULTISAMPLE \_ nenhum**</span><span class="sxs-lookup"><span data-stu-id="c0bea-107"><span id="D3DMULTISAMPLE_NONE"></span><span id="d3dmultisample_none"></span>**D3DMULTISAMPLE\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="c0bea-108">Nenhum nível de multiamostragem de cena completa está disponível.</span><span class="sxs-lookup"><span data-stu-id="c0bea-108">No level of full-scene multisampling is available.</span></span>

</dd> <dt>

<span data-ttu-id="c0bea-109"><span id="D3DMULTISAMPLE_NONMASKABLE_"></span><span id="d3dmultisample_nonmaskable_"></span>**D3DMULTISAMPLE não \_ mascarable**</span><span class="sxs-lookup"><span data-stu-id="c0bea-109"><span id="D3DMULTISAMPLE_NONMASKABLE_"></span><span id="d3dmultisample_nonmaskable_"></span>**D3DMULTISAMPLE\_NONMASKABLE**</span></span> 
</dt> <dd>

<span data-ttu-id="c0bea-110">Habilita o valor de qualidade de multiamostra.</span><span class="sxs-lookup"><span data-stu-id="c0bea-110">Enables the multisample quality value.</span></span> <span data-ttu-id="c0bea-111">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="c0bea-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c0bea-112"><span id="D3DMULTISAMPLE_2_SAMPLES"></span><span id="d3dmultisample_2_samples"></span>**Exemplos de D3DMULTISAMPLE \_ 2 \_**</span><span class="sxs-lookup"><span data-stu-id="c0bea-112"><span id="D3DMULTISAMPLE_2_SAMPLES"></span><span id="d3dmultisample_2_samples"></span>**D3DMULTISAMPLE\_2\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="c0bea-113">Nível de multiamostragem de cena completa disponível.</span><span class="sxs-lookup"><span data-stu-id="c0bea-113">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="c0bea-114"><span id="D3DMULTISAMPLE_3_SAMPLES"></span><span id="d3dmultisample_3_samples"></span>**Exemplos de D3DMULTISAMPLE \_ 3 \_**</span><span class="sxs-lookup"><span data-stu-id="c0bea-114"><span id="D3DMULTISAMPLE_3_SAMPLES"></span><span id="d3dmultisample_3_samples"></span>**D3DMULTISAMPLE\_3\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="c0bea-115">Nível de multiamostragem de cena completa disponível.</span><span class="sxs-lookup"><span data-stu-id="c0bea-115">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="c0bea-116"><span id="D3DMULTISAMPLE_4_SAMPLES"></span><span id="d3dmultisample_4_samples"></span>**Exemplos de D3DMULTISAMPLE \_ 4 \_**</span><span class="sxs-lookup"><span data-stu-id="c0bea-116"><span id="D3DMULTISAMPLE_4_SAMPLES"></span><span id="d3dmultisample_4_samples"></span>**D3DMULTISAMPLE\_4\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="c0bea-117">Nível de multiamostragem de cena completa disponível.</span><span class="sxs-lookup"><span data-stu-id="c0bea-117">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="c0bea-118"><span id="D3DMULTISAMPLE_5_SAMPLES"></span><span id="d3dmultisample_5_samples"></span>**Exemplos do D3DMULTISAMPLE \_ 5 \_**</span><span class="sxs-lookup"><span data-stu-id="c0bea-118"><span id="D3DMULTISAMPLE_5_SAMPLES"></span><span id="d3dmultisample_5_samples"></span>**D3DMULTISAMPLE\_5\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="c0bea-119">Nível de multiamostragem de cena completa disponível.</span><span class="sxs-lookup"><span data-stu-id="c0bea-119">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="c0bea-120"><span id="D3DMULTISAMPLE_6_SAMPLES"></span><span id="d3dmultisample_6_samples"></span>**Exemplos do D3DMULTISAMPLE \_ 6 \_**</span><span class="sxs-lookup"><span data-stu-id="c0bea-120"><span id="D3DMULTISAMPLE_6_SAMPLES"></span><span id="d3dmultisample_6_samples"></span>**D3DMULTISAMPLE\_6\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="c0bea-121">Nível de multiamostragem de cena completa disponível.</span><span class="sxs-lookup"><span data-stu-id="c0bea-121">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="c0bea-122"><span id="D3DMULTISAMPLE_7_SAMPLES"></span><span id="d3dmultisample_7_samples"></span>**Exemplos do D3DMULTISAMPLE \_ 7 \_**</span><span class="sxs-lookup"><span data-stu-id="c0bea-122"><span id="D3DMULTISAMPLE_7_SAMPLES"></span><span id="d3dmultisample_7_samples"></span>**D3DMULTISAMPLE\_7\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="c0bea-123">Nível de multiamostragem de cena completa disponível.</span><span class="sxs-lookup"><span data-stu-id="c0bea-123">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="c0bea-124"><span id="D3DMULTISAMPLE_8_SAMPLES"></span><span id="d3dmultisample_8_samples"></span>**Exemplos do D3DMULTISAMPLE \_ 8 \_**</span><span class="sxs-lookup"><span data-stu-id="c0bea-124"><span id="D3DMULTISAMPLE_8_SAMPLES"></span><span id="d3dmultisample_8_samples"></span>**D3DMULTISAMPLE\_8\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="c0bea-125">Nível de multiamostragem de cena completa disponível.</span><span class="sxs-lookup"><span data-stu-id="c0bea-125">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="c0bea-126"><span id="D3DMULTISAMPLE_9_SAMPLES"></span><span id="d3dmultisample_9_samples"></span>**Exemplos do D3DMULTISAMPLE \_ 9 \_**</span><span class="sxs-lookup"><span data-stu-id="c0bea-126"><span id="D3DMULTISAMPLE_9_SAMPLES"></span><span id="d3dmultisample_9_samples"></span>**D3DMULTISAMPLE\_9\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="c0bea-127">Nível de multiamostragem de cena completa disponível.</span><span class="sxs-lookup"><span data-stu-id="c0bea-127">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="c0bea-128"><span id="D3DMULTISAMPLE_10_SAMPLES"></span><span id="d3dmultisample_10_samples"></span>**Exemplos de D3DMULTISAMPLE \_ 10 \_**</span><span class="sxs-lookup"><span data-stu-id="c0bea-128"><span id="D3DMULTISAMPLE_10_SAMPLES"></span><span id="d3dmultisample_10_samples"></span>**D3DMULTISAMPLE\_10\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="c0bea-129">Nível de multiamostragem de cena completa disponível.</span><span class="sxs-lookup"><span data-stu-id="c0bea-129">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="c0bea-130"><span id="D3DMULTISAMPLE_11_SAMPLES"></span><span id="d3dmultisample_11_samples"></span>**Exemplos do D3DMULTISAMPLE \_ 11 \_**</span><span class="sxs-lookup"><span data-stu-id="c0bea-130"><span id="D3DMULTISAMPLE_11_SAMPLES"></span><span id="d3dmultisample_11_samples"></span>**D3DMULTISAMPLE\_11\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="c0bea-131">Nível de multiamostragem de cena completa disponível.</span><span class="sxs-lookup"><span data-stu-id="c0bea-131">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="c0bea-132"><span id="D3DMULTISAMPLE_12_SAMPLES"></span><span id="d3dmultisample_12_samples"></span>**Exemplos do D3DMULTISAMPLE \_ 12 \_**</span><span class="sxs-lookup"><span data-stu-id="c0bea-132"><span id="D3DMULTISAMPLE_12_SAMPLES"></span><span id="d3dmultisample_12_samples"></span>**D3DMULTISAMPLE\_12\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="c0bea-133">Nível de multiamostragem de cena completa disponível.</span><span class="sxs-lookup"><span data-stu-id="c0bea-133">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="c0bea-134"><span id="D3DMULTISAMPLE_13_SAMPLES"></span><span id="d3dmultisample_13_samples"></span>**D3DMULTISAMPLE \_ 13 \_ amostras**</span><span class="sxs-lookup"><span data-stu-id="c0bea-134"><span id="D3DMULTISAMPLE_13_SAMPLES"></span><span id="d3dmultisample_13_samples"></span>**D3DMULTISAMPLE\_13\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="c0bea-135">Nível de multiamostragem de cena completa disponível.</span><span class="sxs-lookup"><span data-stu-id="c0bea-135">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="c0bea-136"><span id="D3DMULTISAMPLE_14_SAMPLES"></span><span id="d3dmultisample_14_samples"></span>**\_Amostras de 14 D3DMULTISAMPLE \_**</span><span class="sxs-lookup"><span data-stu-id="c0bea-136"><span id="D3DMULTISAMPLE_14_SAMPLES"></span><span id="d3dmultisample_14_samples"></span>**D3DMULTISAMPLE\_14\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="c0bea-137">Nível de multiamostragem de cena completa disponível.</span><span class="sxs-lookup"><span data-stu-id="c0bea-137">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="c0bea-138"><span id="D3DMULTISAMPLE_15_SAMPLES"></span><span id="d3dmultisample_15_samples"></span>**D3DMULTISAMPLE \_ 15 \_ amostras**</span><span class="sxs-lookup"><span data-stu-id="c0bea-138"><span id="D3DMULTISAMPLE_15_SAMPLES"></span><span id="d3dmultisample_15_samples"></span>**D3DMULTISAMPLE\_15\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="c0bea-139">Nível de multiamostragem de cena completa disponível.</span><span class="sxs-lookup"><span data-stu-id="c0bea-139">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="c0bea-140"><span id="D3DMULTISAMPLE_16_SAMPLES"></span><span id="d3dmultisample_16_samples"></span>**\_Exemplos de 16 D3DMULTISAMPLE \_**</span><span class="sxs-lookup"><span data-stu-id="c0bea-140"><span id="D3DMULTISAMPLE_16_SAMPLES"></span><span id="d3dmultisample_16_samples"></span>**D3DMULTISAMPLE\_16\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="c0bea-141">Nível de multiamostragem de cena completa disponível.</span><span class="sxs-lookup"><span data-stu-id="c0bea-141">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="c0bea-142"><span id="D3DMULTISAMPLE_FORCE_DWORD"></span><span id="d3dmultisample_force_dword"></span>**D3DMULTISAMPLE \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="c0bea-142"><span id="D3DMULTISAMPLE_FORCE_DWORD"></span><span id="d3dmultisample_force_dword"></span>**D3DMULTISAMPLE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="c0bea-143">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="c0bea-143">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="c0bea-144">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c0bea-144">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="c0bea-145">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="c0bea-145">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0bea-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0bea-146">Remarks</span></span>

<span data-ttu-id="c0bea-147">Além de habilitar a multiamostragem de cena completa em [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) time, haverá Estados de renderização que transformam vários aspectos em níveis refinados.</span><span class="sxs-lookup"><span data-stu-id="c0bea-147">In addition to enabling full-scene multisampling at [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) time, there will be render states that turn various aspects on and off at fine-grained levels.</span></span>

<span data-ttu-id="c0bea-148">A multiamostragem é válida somente em uma cadeia de permuta que está sendo criada ou redefinida com o efeito de permuta de descarte de D3DSWAPEFFECT \_ .</span><span class="sxs-lookup"><span data-stu-id="c0bea-148">Multisampling is valid only on a swap chain that is being created or reset with the D3DSWAPEFFECT\_DISCARD swap effect.</span></span>

<span data-ttu-id="c0bea-149">O valor de anti-aliasing multiamostrado pode ser definido com os parâmetros (ou subparâmetros) nos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="c0bea-149">The multisample antialiasing value can be set with the parameters (or sub-parameters) in the following methods.</span></span>



| <span data-ttu-id="c0bea-150">Método</span><span class="sxs-lookup"><span data-stu-id="c0bea-150">Method</span></span>                                                                                             | <span data-ttu-id="c0bea-151">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0bea-151">Parameters</span></span>                         | <span data-ttu-id="c0bea-152">Subparâmetros</span><span class="sxs-lookup"><span data-stu-id="c0bea-152">Sub-parameters</span></span>                     |
|----------------------------------------------------------------------------------------------------|------------------------------------|------------------------------------|
| [<span data-ttu-id="c0bea-153">**IDirect3D9::CheckDeviceMultiSampleType**</span><span class="sxs-lookup"><span data-stu-id="c0bea-153">**IDirect3D9::CheckDeviceMultiSampleType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)           | <span data-ttu-id="c0bea-154">Multiamostratype e pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="c0bea-154">MultiSampleType and pQualityLevels</span></span> |                                    |
| [<span data-ttu-id="c0bea-155">**IDirect3D9:: CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="c0bea-155">**IDirect3D9::CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)                                       | <span data-ttu-id="c0bea-156">pPresentationParameters</span><span class="sxs-lookup"><span data-stu-id="c0bea-156">pPresentationParameters</span></span>            | <span data-ttu-id="c0bea-157">Multiamostratype e pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="c0bea-157">MultiSampleType and pQualityLevels</span></span> |
| [<span data-ttu-id="c0bea-158">**IDirect3DDevice9::CreateAdditionalSwapChain**</span><span class="sxs-lookup"><span data-stu-id="c0bea-158">**IDirect3DDevice9::CreateAdditionalSwapChain**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) | <span data-ttu-id="c0bea-159">pPresentationParameters</span><span class="sxs-lookup"><span data-stu-id="c0bea-159">pPresentationParameters</span></span>            | <span data-ttu-id="c0bea-160">Multiamostratype e pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="c0bea-160">MultiSampleType and pQualityLevels</span></span> |
| [<span data-ttu-id="c0bea-161">**IDirect3DDevice9::CreateDepthStencilSurface**</span><span class="sxs-lookup"><span data-stu-id="c0bea-161">**IDirect3DDevice9::CreateDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) | <span data-ttu-id="c0bea-162">Multiamostratype e pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="c0bea-162">MultiSampleType and pQualityLevels</span></span> |                                    |
| [<span data-ttu-id="c0bea-163">**IDirect3DDevice9::CreateRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="c0bea-163">**IDirect3DDevice9::CreateRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)               | <span data-ttu-id="c0bea-164">Multiamostratype e pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="c0bea-164">MultiSampleType and pQualityLevels</span></span> |                                    |
| [<span data-ttu-id="c0bea-165">**IDirect3DDevice9::Reset**</span><span class="sxs-lookup"><span data-stu-id="c0bea-165">**IDirect3DDevice9::Reset**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)                                         | <span data-ttu-id="c0bea-166">pPresentationParameters</span><span class="sxs-lookup"><span data-stu-id="c0bea-166">pPresentationParameters</span></span>            | <span data-ttu-id="c0bea-167">Multiamostratype e pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="c0bea-167">MultiSampleType and pQualityLevels</span></span> |



 

<span data-ttu-id="c0bea-168">Não é uma boa prática mudar de um tipo multiamostra para outro para aumentar a qualidade da suavização.</span><span class="sxs-lookup"><span data-stu-id="c0bea-168">It is not good practice to switch from one multisample type to another to raise the quality of the antialiasing.</span></span>

<span data-ttu-id="c0bea-169">D3DMULTISAMPLE \_ None permite efeitos de permuta diferentes de descartar, bloquear e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="c0bea-169">D3DMULTISAMPLE\_NONE enables swap effects other than discarding, locking, and so on.</span></span>

<span data-ttu-id="c0bea-170">Se o dispositivo de vídeo dá suporte a várias amostras mascaradas (mais de uma amostra para um formato de destino de renderização de vários exemplos e suporte a AntiAlias) ou apenas multiamostragens não mascaráveis (somente suporte AntiAlias), o driver para o dispositivo fornece o número de níveis de qualidade para o \_ tipo de várias amostras D3DMULTISAMPLE não maskável.</span><span class="sxs-lookup"><span data-stu-id="c0bea-170">Whether the display device supports maskable multisampling (more than one sample for a multiple-sample render-target format plus antialias support) or just non-maskable multisampling (only antialias support), the driver for the device provides the number of quality levels for the D3DMULTISAMPLE\_NONMASKABLE multiple-sample type.</span></span> <span data-ttu-id="c0bea-171">Os aplicativos que usam apenas a multiamostragem para fins de suavização só precisam consultar o número de níveis de qualidade de várias amostras não mascarados que o driver dá suporte.</span><span class="sxs-lookup"><span data-stu-id="c0bea-171">Applications that just use multisampling for antialiasing purposes only need to query for the number of non-maskable multiple-sample quality levels that the driver supports.</span></span>

<span data-ttu-id="c0bea-172">Os níveis de qualidade com suporte do dispositivo podem ser obtidos com o parâmetro pQualityLevels de [**IDirect3D9:: CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype).</span><span class="sxs-lookup"><span data-stu-id="c0bea-172">The quality levels supported by the device can be obtained with the pQualityLevels parameter of [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype).</span></span> <span data-ttu-id="c0bea-173">Os níveis de qualidade usados pelo aplicativo são definidos com o parâmetro MultiSampleQuality de [**IDirect3DDevice9:: CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) e [**IDirect3DDevice9:: CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget).</span><span class="sxs-lookup"><span data-stu-id="c0bea-173">Quality levels used by the application are set with the MultiSampleQuality parameter of [**IDirect3DDevice9::CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) and [**IDirect3DDevice9::CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget).</span></span>

<span data-ttu-id="c0bea-174">Consulte D3DRS \_ MULTISAMPLEMASK para discussão sobre multiamostragens mascaráveis.</span><span class="sxs-lookup"><span data-stu-id="c0bea-174">See D3DRS\_MULTISAMPLEMASK for discussion of maskable multisampling.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0bea-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0bea-175">Requirements</span></span>



| <span data-ttu-id="c0bea-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0bea-176">Requirement</span></span> | <span data-ttu-id="c0bea-177">Valor</span><span class="sxs-lookup"><span data-stu-id="c0bea-177">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0bea-178">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c0bea-178">Header</span></span><br/> | <dl> <span data-ttu-id="c0bea-179"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0bea-179"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0bea-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0bea-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0bea-181">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="c0bea-181">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="c0bea-182">**Parâmetros de D3DPRESENT \_**</span><span class="sxs-lookup"><span data-stu-id="c0bea-182">**D3DPRESENT\_PARAMETERS**</span></span>](d3dpresent-parameters.md)
</dt> <dt>

[<span data-ttu-id="c0bea-183">**D3DSURFACE \_ desc**</span><span class="sxs-lookup"><span data-stu-id="c0bea-183">**D3DSURFACE\_DESC**</span></span>](d3dsurface-desc.md)
</dt> </dl>

 

 
