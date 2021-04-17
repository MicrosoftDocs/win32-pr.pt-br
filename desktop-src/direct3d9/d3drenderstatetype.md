---
description: Os Estados de renderização definem Estados de configuração para todos os tipos de processamento de vértice e pixel.
ms.assetid: 2fd56388-f3bd-409f-876c-ae893840b623
title: Enumeração D3DRENDERSTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRENDERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2386762eaa45f1eefbccac97723c3ad71c3a76fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105782540"
---
# <a name="d3drenderstatetype-enumeration"></a><span data-ttu-id="a5f42-103">Enumeração D3DRENDERSTATETYPE</span><span class="sxs-lookup"><span data-stu-id="a5f42-103">D3DRENDERSTATETYPE enumeration</span></span>

<span data-ttu-id="a5f42-104">Os Estados de renderização definem Estados de configuração para todos os tipos de processamento de vértice e pixel.</span><span class="sxs-lookup"><span data-stu-id="a5f42-104">Render states define set-up states for all kinds of vertex and pixel processing.</span></span> <span data-ttu-id="a5f42-105">Alguns Estados de renderização configuram o processamento de vértice e alguns configuram o processamento de pixel (consulte [Estados de renderização (Direct3D 9)](render-states.md)).</span><span class="sxs-lookup"><span data-stu-id="a5f42-105">Some render states set up vertex processing, and some set up pixel processing (see [Render States (Direct3D 9)](render-states.md)).</span></span> <span data-ttu-id="a5f42-106">Os Estados de renderização podem ser salvos e restaurados usando stateblocks (consulte [estado de salvamento e restauração de blocos de estado (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="a5f42-106">Render states can be saved and restored using stateblocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="a5f42-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5f42-107">Syntax</span></span>


```C++
typedef enum D3DRENDERSTATETYPE { 
  D3DRS_ZENABLE                     = 7,
  D3DRS_FILLMODE                    = 8,
  D3DRS_SHADEMODE                   = 9,
  D3DRS_ZWRITEENABLE                = 14,
  D3DRS_ALPHATESTENABLE             = 15,
  D3DRS_LASTPIXEL                   = 16,
  D3DRS_SRCBLEND                    = 19,
  D3DRS_DESTBLEND                   = 20,
  D3DRS_CULLMODE                    = 22,
  D3DRS_ZFUNC                       = 23,
  D3DRS_ALPHAREF                    = 24,
  D3DRS_ALPHAFUNC                   = 25,
  D3DRS_DITHERENABLE                = 26,
  D3DRS_ALPHABLENDENABLE            = 27,
  D3DRS_FOGENABLE                   = 28,
  D3DRS_SPECULARENABLE              = 29,
  D3DRS_FOGCOLOR                    = 34,
  D3DRS_FOGTABLEMODE                = 35,
  D3DRS_FOGSTART                    = 36,
  D3DRS_FOGEND                      = 37,
  D3DRS_FOGDENSITY                  = 38,
  D3DRS_RANGEFOGENABLE              = 48,
  D3DRS_STENCILENABLE               = 52,
  D3DRS_STENCILFAIL                 = 53,
  D3DRS_STENCILZFAIL                = 54,
  D3DRS_STENCILPASS                 = 55,
  D3DRS_STENCILFUNC                 = 56,
  D3DRS_STENCILREF                  = 57,
  D3DRS_STENCILMASK                 = 58,
  D3DRS_STENCILWRITEMASK            = 59,
  D3DRS_TEXTUREFACTOR               = 60,
  D3DRS_WRAP0                       = 128,
  D3DRS_WRAP1                       = 129,
  D3DRS_WRAP2                       = 130,
  D3DRS_WRAP3                       = 131,
  D3DRS_WRAP4                       = 132,
  D3DRS_WRAP5                       = 133,
  D3DRS_WRAP6                       = 134,
  D3DRS_WRAP7                       = 135,
  D3DRS_CLIPPING                    = 136,
  D3DRS_LIGHTING                    = 137,
  D3DRS_AMBIENT                     = 139,
  D3DRS_FOGVERTEXMODE               = 140,
  D3DRS_COLORVERTEX                 = 141,
  D3DRS_LOCALVIEWER                 = 142,
  D3DRS_NORMALIZENORMALS            = 143,
  D3DRS_DIFFUSEMATERIALSOURCE       = 145,
  D3DRS_SPECULARMATERIALSOURCE      = 146,
  D3DRS_AMBIENTMATERIALSOURCE       = 147,
  D3DRS_EMISSIVEMATERIALSOURCE      = 148,
  D3DRS_VERTEXBLEND                 = 151,
  D3DRS_CLIPPLANEENABLE             = 152,
  D3DRS_POINTSIZE                   = 154,
  D3DRS_POINTSIZE_MIN               = 155,
  D3DRS_POINTSPRITEENABLE           = 156,
  D3DRS_POINTSCALEENABLE            = 157,
  D3DRS_POINTSCALE_A                = 158,
  D3DRS_POINTSCALE_B                = 159,
  D3DRS_POINTSCALE_C                = 160,
  D3DRS_MULTISAMPLEANTIALIAS        = 161,
  D3DRS_MULTISAMPLEMASK             = 162,
  D3DRS_PATCHEDGESTYLE              = 163,
  D3DRS_DEBUGMONITORTOKEN           = 165,
  D3DRS_POINTSIZE_MAX               = 166,
  D3DRS_INDEXEDVERTEXBLENDENABLE    = 167,
  D3DRS_COLORWRITEENABLE            = 168,
  D3DRS_TWEENFACTOR                 = 170,
  D3DRS_BLENDOP                     = 171,
  D3DRS_POSITIONDEGREE              = 172,
  D3DRS_NORMALDEGREE                = 173,
  D3DRS_SCISSORTESTENABLE           = 174,
  D3DRS_SLOPESCALEDEPTHBIAS         = 175,
  D3DRS_ANTIALIASEDLINEENABLE       = 176,
  D3DRS_MINTESSELLATIONLEVEL        = 178,
  D3DRS_MAXTESSELLATIONLEVEL        = 179,
  D3DRS_ADAPTIVETESS_X              = 180,
  D3DRS_ADAPTIVETESS_Y              = 181,
  D3DRS_ADAPTIVETESS_Z              = 182,
  D3DRS_ADAPTIVETESS_W              = 183,
  D3DRS_ENABLEADAPTIVETESSELLATION  = 184,
  D3DRS_TWOSIDEDSTENCILMODE         = 185,
  D3DRS_CCW_STENCILFAIL             = 186,
  D3DRS_CCW_STENCILZFAIL            = 187,
  D3DRS_CCW_STENCILPASS             = 188,
  D3DRS_CCW_STENCILFUNC             = 189,
  D3DRS_COLORWRITEENABLE1           = 190,
  D3DRS_COLORWRITEENABLE2           = 191,
  D3DRS_COLORWRITEENABLE3           = 192,
  D3DRS_BLENDFACTOR                 = 193,
  D3DRS_SRGBWRITEENABLE             = 194,
  D3DRS_DEPTHBIAS                   = 195,
  D3DRS_WRAP8                       = 198,
  D3DRS_WRAP9                       = 199,
  D3DRS_WRAP10                      = 200,
  D3DRS_WRAP11                      = 201,
  D3DRS_WRAP12                      = 202,
  D3DRS_WRAP13                      = 203,
  D3DRS_WRAP14                      = 204,
  D3DRS_WRAP15                      = 205,
  D3DRS_SEPARATEALPHABLENDENABLE    = 206,
  D3DRS_SRCBLENDALPHA               = 207,
  D3DRS_DESTBLENDALPHA              = 208,
  D3DRS_BLENDOPALPHA                = 209,
  D3DRS_FORCE_DWORD                 = 0x7fffffff
} D3DRENDERSTATETYPE, *LPD3DRENDERSTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="a5f42-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="a5f42-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a5f42-109"><span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**D3DRS \_ ZENABLE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-109"><span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**D3DRS\_ZENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-110">Estado de buffer de profundidade como um membro do tipo enumerado [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-110">Depth-buffering state as one member of the [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) enumerated type.</span></span> <span data-ttu-id="a5f42-111">Defina esse estado como D3DZB \_ true para habilitar o z-buffer, D3DZB \_ USEW para habilitar o w-buffer ou D3DZB \_ false para desabilitar o buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="a5f42-111">Set this state to D3DZB\_TRUE to enable z-buffering, D3DZB\_USEW to enable w-buffering, or D3DZB\_FALSE to disable depth buffering.</span></span>

<span data-ttu-id="a5f42-112">O valor padrão para esse estado de renderização será D3DZB \_ true se um estêncil de profundidade tiver sido criado junto com a cadeia de permuta definindo o membro EnableAutoDepthStencil da estrutura de [**\_ parâmetros D3DPRESENT**](d3dpresent-parameters.md) como **true** e D3DZB \_ false caso contrário.</span><span class="sxs-lookup"><span data-stu-id="a5f42-112">The default value for this render state is D3DZB\_TRUE if a depth stencil was created along with the swap chain by setting the EnableAutoDepthStencil member of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure to **TRUE**, and D3DZB\_FALSE otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-113"><span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS \_ FillMode**</span><span class="sxs-lookup"><span data-stu-id="a5f42-113"><span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS\_FILLMODE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-114">Um ou mais membros do tipo enumerado [**D3DFILLMODE**](./d3dfillmode.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-114">One or more members of the [**D3DFILLMODE**](./d3dfillmode.md) enumerated type.</span></span> <span data-ttu-id="a5f42-115">O valor padrão é D3DFILL \_ Solid.</span><span class="sxs-lookup"><span data-stu-id="a5f42-115">The default value is D3DFILL\_SOLID.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-116"><span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS \_ shadmode**</span><span class="sxs-lookup"><span data-stu-id="a5f42-116"><span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS\_SHADEMODE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-117">Um ou mais membros do tipo enumerado [**D3DSHADEMODE**](./d3dshademode.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-117">One or more members of the [**D3DSHADEMODE**](./d3dshademode.md) enumerated type.</span></span> <span data-ttu-id="a5f42-118">O valor padrão é D3DSHADE \_ GOURAUD.</span><span class="sxs-lookup"><span data-stu-id="a5f42-118">The default value is D3DSHADE\_GOURAUD.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-119"><span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS \_ ZWRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-119"><span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS\_ZWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-120">**True** para permitir que o aplicativo grave no buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="a5f42-120">**TRUE** to enable the application to write to the depth buffer.</span></span> <span data-ttu-id="a5f42-121">O valor padrão é **true**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-121">The default value is **TRUE**.</span></span> <span data-ttu-id="a5f42-122">Esse membro permite que um aplicativo impeça o sistema de atualizar o buffer de profundidade com novos valores de profundidade.</span><span class="sxs-lookup"><span data-stu-id="a5f42-122">This member enables an application to prevent the system from updating the depth buffer with new depth values.</span></span> <span data-ttu-id="a5f42-123">Se **for false**, as comparações de profundidade ainda serão feitas de acordo com o estado de renderização D3DRS \_ ZFUNC, supondo que o buffer de profundidade esteja ocorrendo, mas os valores de profundidade não são gravados no buffer.</span><span class="sxs-lookup"><span data-stu-id="a5f42-123">If **FALSE**, depth comparisons are still made according to the render state D3DRS\_ZFUNC, assuming that depth buffering is taking place, but depth values are not written to the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-124"><span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS \_ ALPHATESTENABLE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-124"><span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS\_ALPHATESTENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-125">**True** para habilitar testes alfa por pixel.</span><span class="sxs-lookup"><span data-stu-id="a5f42-125">**TRUE** to enable per pixel alpha testing.</span></span> <span data-ttu-id="a5f42-126">Se o teste passar, o pixel será processado pelo buffer de quadros.</span><span class="sxs-lookup"><span data-stu-id="a5f42-126">If the test passes, the pixel is processed by the frame buffer.</span></span> <span data-ttu-id="a5f42-127">Caso contrário, todo o processamento do buffer de quadros será ignorado para o pixel.</span><span class="sxs-lookup"><span data-stu-id="a5f42-127">Otherwise, all frame-buffer processing is skipped for the pixel.</span></span>

<span data-ttu-id="a5f42-128">O teste é feito comparando o valor alfa de entrada com o valor alfa de referência, usando a função de comparação fornecida pelo \_ estado de RENDERIZAÇÃO D3DRS ALPHAFUNC.</span><span class="sxs-lookup"><span data-stu-id="a5f42-128">The test is done by comparing the incoming alpha value with the reference alpha value, using the comparison function provided by the D3DRS\_ALPHAFUNC render state.</span></span> <span data-ttu-id="a5f42-129">O valor alfa de referência é determinado pelo valor definido para D3DRS \_ ALPHAREF.</span><span class="sxs-lookup"><span data-stu-id="a5f42-129">The reference alpha value is determined by the value set for D3DRS\_ALPHAREF.</span></span> <span data-ttu-id="a5f42-130">Para obter mais informações, consulte [Alpha Test State (Direct3D 9)](alpha-testing-state.md).</span><span class="sxs-lookup"><span data-stu-id="a5f42-130">For more information, see [Alpha Testing State (Direct3D 9)](alpha-testing-state.md).</span></span>

<span data-ttu-id="a5f42-131">O valor padrão desse parâmetro é **false**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-131">The default value of this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-132"><span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS \_ LASTPIXEL**</span><span class="sxs-lookup"><span data-stu-id="a5f42-132"><span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS\_LASTPIXEL**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-133">O valor padrão é **true**, que habilita o desenho do último pixel em uma linha.</span><span class="sxs-lookup"><span data-stu-id="a5f42-133">The default value is **TRUE**, which enables drawing of the last pixel in a line.</span></span> <span data-ttu-id="a5f42-134">Para evitar o desenho do último pixel, defina esse valor como **false**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-134">To prevent drawing of the last pixel, set this value to **FALSE**.</span></span> <span data-ttu-id="a5f42-135">Para obter mais informações, consulte [estrutura de tópicos e estado de preenchimento (Direct3D 9)](outline-and-fill-state.md).</span><span class="sxs-lookup"><span data-stu-id="a5f42-135">For more information, see [Outline and Fill State (Direct3D 9)](outline-and-fill-state.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-136"><span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS \_ SRCBLEND**</span><span class="sxs-lookup"><span data-stu-id="a5f42-136"><span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS\_SRCBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-137">Um membro do tipo enumerado [**D3DBLEND**](./d3dblend.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-137">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="a5f42-138">O valor padrão é D3DBLEND \_ One.</span><span class="sxs-lookup"><span data-stu-id="a5f42-138">The default value is D3DBLEND\_ONE.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-139"><span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS \_ DESTBLEND**</span><span class="sxs-lookup"><span data-stu-id="a5f42-139"><span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS\_DESTBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-140">Um membro do tipo enumerado [**D3DBLEND**](./d3dblend.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-140">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="a5f42-141">O valor padrão é D3DBLEND \_ zero.</span><span class="sxs-lookup"><span data-stu-id="a5f42-141">The default value is D3DBLEND\_ZERO.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-142"><span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS de \_ seleção**</span><span class="sxs-lookup"><span data-stu-id="a5f42-142"><span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS\_CULLMODE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-143">Especifica como os triângulos voltados para o verso são examinados, se houver.</span><span class="sxs-lookup"><span data-stu-id="a5f42-143">Specifies how back-facing triangles are culled, if at all.</span></span> <span data-ttu-id="a5f42-144">Isso pode ser definido como um membro do tipo enumerado [**D3DCULL**](./d3dcull.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-144">This can be set to one member of the [**D3DCULL**](./d3dcull.md) enumerated type.</span></span> <span data-ttu-id="a5f42-145">O valor padrão é D3DCULL \_ CCW.</span><span class="sxs-lookup"><span data-stu-id="a5f42-145">The default value is D3DCULL\_CCW.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-146"><span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**D3DRS \_ ZFUNC**</span><span class="sxs-lookup"><span data-stu-id="a5f42-146"><span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**D3DRS\_ZFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-147">Um membro do tipo enumerado [**D3DCMPFUNC**](./d3dcmpfunc.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-147">One member of the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="a5f42-148">O valor padrão é D3DCMP \_ LESSEQUAL.</span><span class="sxs-lookup"><span data-stu-id="a5f42-148">The default value is D3DCMP\_LESSEQUAL.</span></span> <span data-ttu-id="a5f42-149">Esse membro permite que um aplicativo aceite ou rejeite um pixel com base em sua distância da câmera.</span><span class="sxs-lookup"><span data-stu-id="a5f42-149">This member enables an application to accept or reject a pixel, based on its distance from the camera.</span></span>

<span data-ttu-id="a5f42-150">O valor de profundidade do pixel é comparado com o valor do buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="a5f42-150">The depth value of the pixel is compared with the depth-buffer value.</span></span> <span data-ttu-id="a5f42-151">Se o valor de profundidade do pixel passar a função de comparação, o pixel será gravado.</span><span class="sxs-lookup"><span data-stu-id="a5f42-151">If the depth value of the pixel passes the comparison function, the pixel is written.</span></span>

<span data-ttu-id="a5f42-152">O valor de profundidade será gravado no buffer de profundidade somente se o estado de renderização for **true**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-152">The depth value is written to the depth buffer only if the render state is **TRUE**.</span></span>

<span data-ttu-id="a5f42-153">Os rasterizadores de software e muitos aceleradores de hardware funcionam mais rapidamente se o teste de profundidade falhar, porque não há necessidade de filtrar e modular a textura se o pixel não for renderizado.</span><span class="sxs-lookup"><span data-stu-id="a5f42-153">Software rasterizers and many hardware accelerators work faster if the depth test fails, because there is no need to filter and modulate the texture if the pixel is not going to be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-154"><span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**D3DRS \_ ALPHAREF**</span><span class="sxs-lookup"><span data-stu-id="a5f42-154"><span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**D3DRS\_ALPHAREF**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-155">Valor que especifica um valor alfa de referência no qual os pixels são testados quando o teste alfa está habilitado.</span><span class="sxs-lookup"><span data-stu-id="a5f42-155">Value that specifies a reference alpha value against which pixels are tested when alpha testing is enabled.</span></span> <span data-ttu-id="a5f42-156">Esse é um valor de 8 bits colocado nos 8 bits baixos do valor de estado de renderização DWORD.</span><span class="sxs-lookup"><span data-stu-id="a5f42-156">This is an 8-bit value placed in the low 8 bits of the DWORD render-state value.</span></span> <span data-ttu-id="a5f42-157">Os valores podem variar de 0x00000000 a 0x000000FF.</span><span class="sxs-lookup"><span data-stu-id="a5f42-157">Values can range from 0x00000000 through 0x000000FF.</span></span> <span data-ttu-id="a5f42-158">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="a5f42-158">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-159"><span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**D3DRS \_ ALPHAFUNC**</span><span class="sxs-lookup"><span data-stu-id="a5f42-159"><span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**D3DRS\_ALPHAFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-160">Um membro do tipo enumerado [**D3DCMPFUNC**](./d3dcmpfunc.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-160">One member of the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="a5f42-161">O valor padrão é D3DCMP \_ Always.</span><span class="sxs-lookup"><span data-stu-id="a5f42-161">The default value is D3DCMP\_ALWAYS.</span></span> <span data-ttu-id="a5f42-162">Esse membro permite que um aplicativo aceite ou rejeite um pixel com base em seu valor alfa.</span><span class="sxs-lookup"><span data-stu-id="a5f42-162">This member enables an application to accept or reject a pixel, based on its alpha value.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-163"><span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS \_ DITHERENABLE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-163"><span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS\_DITHERENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-164">**True** para habilitar o pontilhamento.</span><span class="sxs-lookup"><span data-stu-id="a5f42-164">**TRUE** to enable dithering.</span></span> <span data-ttu-id="a5f42-165">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-165">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-166"><span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS \_ ALPHABLENDENABLE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-166"><span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS\_ALPHABLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-167">**True** para habilitar a transparência com combinação alfabética.</span><span class="sxs-lookup"><span data-stu-id="a5f42-167">**TRUE** to enable alpha-blended transparency.</span></span> <span data-ttu-id="a5f42-168">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-168">The default value is **FALSE**.</span></span>

<span data-ttu-id="a5f42-169">O tipo de mistura alfa é determinado pelos \_ Estados de RENDERIZAÇÃO D3DRS SRCBLEND e \_ D3DRS DESTBLEND.</span><span class="sxs-lookup"><span data-stu-id="a5f42-169">The type of alpha blending is determined by the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND render states.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-170"><span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS \_ FOGENABLE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-170"><span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS\_FOGENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-171">**True** para habilitar a mesclagem de neblina.</span><span class="sxs-lookup"><span data-stu-id="a5f42-171">**TRUE** to enable fog blending.</span></span> <span data-ttu-id="a5f42-172">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-172">The default value is **FALSE**.</span></span> <span data-ttu-id="a5f42-173">Para obter mais informações sobre como usar a mistura de neblina, consulte [neblina](fog.md).</span><span class="sxs-lookup"><span data-stu-id="a5f42-173">For more information about using fog blending, see [Fog](fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-174"><span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS \_ SPECULARENABLE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-174"><span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS\_SPECULARENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-175">**True** para habilitar os realces especulares.</span><span class="sxs-lookup"><span data-stu-id="a5f42-175">**TRUE** to enable specular highlights.</span></span> <span data-ttu-id="a5f42-176">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-176">The default value is **FALSE**.</span></span>

<span data-ttu-id="a5f42-177">Os realces especulares são calculados como se cada vértice no objeto que está sendo aceso estiver na origem do objeto.</span><span class="sxs-lookup"><span data-stu-id="a5f42-177">Specular highlights are calculated as though every vertex in the object being lit is at the object's origin.</span></span> <span data-ttu-id="a5f42-178">Isso fornece os resultados esperados, desde que o objeto seja modelado em volta da origem e a distância da luz para o objeto seja relativamente grande.</span><span class="sxs-lookup"><span data-stu-id="a5f42-178">This gives the expected results as long as the object is modeled around the origin and the distance from the light to the object is relatively large.</span></span> <span data-ttu-id="a5f42-179">Em outros casos, os resultados são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="a5f42-179">In other cases, the results as undefined.</span></span>

<span data-ttu-id="a5f42-180">Quando esse membro é definido como **true**, a cor especular é adicionada à cor base após a textura em cascata, mas antes da mistura alfa.</span><span class="sxs-lookup"><span data-stu-id="a5f42-180">When this member is set to **TRUE**, the specular color is added to the base color after the texture cascade but before alpha blending.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-181"><span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRS \_ FOGCOLOR**</span><span class="sxs-lookup"><span data-stu-id="a5f42-181"><span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRS\_FOGCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-182">Valor cujo tipo é [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="a5f42-182">Value whose type is [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="a5f42-183">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="a5f42-183">The default value is 0.</span></span> <span data-ttu-id="a5f42-184">Para obter mais informações sobre a cor de neblina, consulte [cor de neblina (Direct3D 9)](fog-color.md).</span><span class="sxs-lookup"><span data-stu-id="a5f42-184">For more information about fog color, see [Fog Color (Direct3D 9)](fog-color.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-185"><span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS \_ FOGTABLEMODE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-185"><span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS\_FOGTABLEMODE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-186">A fórmula de neblina a ser usada para sombra de pixel.</span><span class="sxs-lookup"><span data-stu-id="a5f42-186">The fog formula to be used for pixel fog.</span></span> <span data-ttu-id="a5f42-187">Defina como um dos membros do tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-187">Set to one of the members of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="a5f42-188">O valor padrão é D3DFOG \_ None.</span><span class="sxs-lookup"><span data-stu-id="a5f42-188">The default value is D3DFOG\_NONE.</span></span> <span data-ttu-id="a5f42-189">Para obter mais informações sobre sombra de pixel, consulte [sombra de pixel (Direct3D 9)](pixel-fog.md).</span><span class="sxs-lookup"><span data-stu-id="a5f42-189">For more information about pixel fog, see [Pixel Fog (Direct3D 9)](pixel-fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-190"><span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRS \_ FOGSTART**</span><span class="sxs-lookup"><span data-stu-id="a5f42-190"><span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRS\_FOGSTART**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-191">Profundidade na qual os efeitos de neblina de pixel ou vértice começam para o modo de neblina linear.</span><span class="sxs-lookup"><span data-stu-id="a5f42-191">Depth at which pixel or vertex fog effects begin for linear fog mode.</span></span> <span data-ttu-id="a5f42-192">O valor padrão é 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="a5f42-192">The default value is 0.0f.</span></span> <span data-ttu-id="a5f42-193">A profundidade é especificada no espaço de mundo para a neblina de vértice e espaço \[ de dispositivo 0,0, 1,0 \] ou espaço do mundo para sombra de pixel.</span><span class="sxs-lookup"><span data-stu-id="a5f42-193">Depth is specified in world space for vertex fog and either device space \[0.0, 1.0\] or world space for pixel fog.</span></span> <span data-ttu-id="a5f42-194">Para a neblina de pixel, esses valores estão no espaço do dispositivo quando o sistema usa z para cálculos de neblina e espaço mundial no mundo inteiro quando o sistema está usando uma neblina (neblina) de olho relativo.</span><span class="sxs-lookup"><span data-stu-id="a5f42-194">For pixel fog, these values are in device space when the system uses z for fog calculations and world-world space when the system is using eye-relative fog (w-fog).</span></span> <span data-ttu-id="a5f42-195">Para obter mais informações, consulte [parâmetros de neblina (Direct3D 9)](fog-parameters.md) e [profundidade em relação a Z x](pixel-fog.md).</span><span class="sxs-lookup"><span data-stu-id="a5f42-195">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md) and [Eye-Relative vs. Z-based Depth](pixel-fog.md).</span></span>

<span data-ttu-id="a5f42-196">Os valores para esse estado de renderização são valores de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="a5f42-196">Values for this render state are floating-point values.</span></span> <span data-ttu-id="a5f42-197">Como o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aceita valores DWORD, seu aplicativo deve converter uma variável que contém o valor, conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5f42-197">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
pDevice9->SetRenderState(D3DRS_FOGSTART, 
                         *((DWORD*) (&fFogStart)));
```



</dd> <dt>

<span data-ttu-id="a5f42-198"><span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**D3DRS \_ FOGEND**</span><span class="sxs-lookup"><span data-stu-id="a5f42-198"><span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**D3DRS\_FOGEND**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-199">Profundidade na qual os efeitos de neblina de pixel ou vértice terminam para o modo de neblina linear.</span><span class="sxs-lookup"><span data-stu-id="a5f42-199">Depth at which pixel or vertex fog effects end for linear fog mode.</span></span> <span data-ttu-id="a5f42-200">O valor padrão é 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="a5f42-200">The default value is 1.0f.</span></span> <span data-ttu-id="a5f42-201">A profundidade é especificada no espaço de mundo para a neblina de vértice e espaço \[ de dispositivo 0,0, 1,0 \] ou espaço do mundo para sombra de pixel.</span><span class="sxs-lookup"><span data-stu-id="a5f42-201">Depth is specified in world space for vertex fog and either device space \[0.0, 1.0\] or world space for pixel fog.</span></span> <span data-ttu-id="a5f42-202">Para a neblina de pixel, esses valores estão no espaço do dispositivo quando o sistema usa z para cálculos de neblina e no espaço do mundo quando o sistema está usando uma neblina (neblina) de olho relativo.</span><span class="sxs-lookup"><span data-stu-id="a5f42-202">For pixel fog, these values are in device space when the system uses z for fog calculations and in world space when the system is using eye-relative fog (w-fog).</span></span> <span data-ttu-id="a5f42-203">Para obter mais informações, consulte [parâmetros de neblina (Direct3D 9)](fog-parameters.md) e [profundidade em relação a Z x](pixel-fog.md).</span><span class="sxs-lookup"><span data-stu-id="a5f42-203">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md) and [Eye-Relative vs. Z-based Depth](pixel-fog.md).</span></span>

<span data-ttu-id="a5f42-204">Os valores para esse estado de renderização são valores de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="a5f42-204">Values for this render state are floating-point values.</span></span> <span data-ttu-id="a5f42-205">Como o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aceita valores DWORD, seu aplicativo deve converter uma variável que contém o valor, conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5f42-205">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_FOGEND, *((DWORD*) (&fFogEnd)));
```



</dd> <dt>

<span data-ttu-id="a5f42-206"><span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**D3DRS \_ FOGDENSITY**</span><span class="sxs-lookup"><span data-stu-id="a5f42-206"><span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**D3DRS\_FOGDENSITY**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-207">Densidade de neblina para sombra de pixel ou vértice usada nos modos de neblina exponencial (D3DFOG \_ exp e D3DFOG \_ EXP2).</span><span class="sxs-lookup"><span data-stu-id="a5f42-207">Fog density for pixel or vertex fog used in the exponential fog modes (D3DFOG\_EXP and D3DFOG\_EXP2).</span></span> <span data-ttu-id="a5f42-208">Os valores de densidade válidos variam de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="a5f42-208">Valid density values range from 0.0 through 1.0.</span></span> <span data-ttu-id="a5f42-209">O valor padrão é 1.0.</span><span class="sxs-lookup"><span data-stu-id="a5f42-209">The default value is 1.0.</span></span> <span data-ttu-id="a5f42-210">Para obter mais informações, consulte [parâmetros de neblina (Direct3D 9)](fog-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a5f42-210">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md).</span></span>

<span data-ttu-id="a5f42-211">Os valores para esse estado de renderização são valores de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="a5f42-211">Values for this render state are floating-point values.</span></span> <span data-ttu-id="a5f42-212">Como o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aceita valores DWORD, seu aplicativo deve converter uma variável que contém o valor, conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5f42-212">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
    m_pDevice9->SetRenderState(D3DRS_FOGDENSITY, *((DWORD*) (&fFogDensity)));
```



</dd> <dt>

<span data-ttu-id="a5f42-213"><span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS \_ RANGEFOGENABLE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-213"><span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS\_RANGEFOGENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-214">**True** para habilitar a neblina de vértice com base em intervalos.</span><span class="sxs-lookup"><span data-stu-id="a5f42-214">**TRUE** to enable range-based vertex fog.</span></span> <span data-ttu-id="a5f42-215">O valor padrão é **false**; nesse caso, o sistema usa a neblina baseada em profundidade.</span><span class="sxs-lookup"><span data-stu-id="a5f42-215">The default value is **FALSE**, in which case the system uses depth-based fog.</span></span> <span data-ttu-id="a5f42-216">Na neblina baseada em intervalo, a distância de um objeto do visualizador é usada para computar efeitos de neblina, não a profundidade do objeto (ou seja, a coordenada z) na cena.</span><span class="sxs-lookup"><span data-stu-id="a5f42-216">In range-based fog, the distance of an object from the viewer is used to compute fog effects, not the depth of the object (that is, the z-coordinate) in the scene.</span></span> <span data-ttu-id="a5f42-217">Na neblina baseada em intervalo, todos os métodos de neblina funcionam normalmente, exceto pelo fato de que eles usam o intervalo em vez de profundidade nos cálculos.</span><span class="sxs-lookup"><span data-stu-id="a5f42-217">In range-based fog, all fog methods work as usual, except that they use range instead of depth in the computations.</span></span>

<span data-ttu-id="a5f42-218">Range é o fator correto a ser usado para cálculos de neblina, mas a profundidade geralmente é usada, pois o intervalo é demorado para computar e a profundidade geralmente já está disponível.</span><span class="sxs-lookup"><span data-stu-id="a5f42-218">Range is the correct factor to use for fog computations, but depth is commonly used instead because range is time-consuming to compute and depth is generally already available.</span></span> <span data-ttu-id="a5f42-219">O uso de profundidade para calcular a neblina tem o efeito indesejável de que a fogginess dos objetos periféricos muda à medida que os olhos do visualizador – nesse caso, a profundidade muda e o intervalo permanece constante.</span><span class="sxs-lookup"><span data-stu-id="a5f42-219">Using depth to calculate fog has the undesirable effect of having the fogginess of peripheral objects change as the viewer's eye moves - in this case, the depth changes and the range remains constant.</span></span>

<span data-ttu-id="a5f42-220">Como nenhum hardware dá suporte atualmente a neblina com base em intervalos por pixel, a correção de intervalo é oferecida apenas para a neblina de vértice.</span><span class="sxs-lookup"><span data-stu-id="a5f42-220">Because no hardware currently supports per-pixel range-based fog, range correction is offered only for vertex fog.</span></span>

<span data-ttu-id="a5f42-221">Para obter mais informações, consulte [Vertex neblina (Direct3D 9)](vertex-fog.md).</span><span class="sxs-lookup"><span data-stu-id="a5f42-221">For more information, see [Vertex Fog (Direct3D 9)](vertex-fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-222"><span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**D3DRS \_ STENCILENABLE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-222"><span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**D3DRS\_STENCILENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-223">**True** para habilitar a estêncil, ou **false** para desabilitar o estêncil.</span><span class="sxs-lookup"><span data-stu-id="a5f42-223">**TRUE** to enable stenciling, or **FALSE** to disable stenciling.</span></span> <span data-ttu-id="a5f42-224">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-224">The default value is **FALSE**.</span></span> <span data-ttu-id="a5f42-225">Para obter mais informações, consulte as [técnicas de buffer de estêncil (Direct3D 9)](stencil-buffer-techniques.md).</span><span class="sxs-lookup"><span data-stu-id="a5f42-225">For more information, see [Stencil Buffer Techniques (Direct3D 9)](stencil-buffer-techniques.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-226"><span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS \_ STENCILFAIL**</span><span class="sxs-lookup"><span data-stu-id="a5f42-226"><span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS\_STENCILFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-227">Operação de estêncil a ser executada se o teste de estêncil falhar.</span><span class="sxs-lookup"><span data-stu-id="a5f42-227">Stencil operation to perform if the stencil test fails.</span></span> <span data-ttu-id="a5f42-228">Os valores são do tipo enumerado [**D3DSTENCILOP**](./d3dstencilop.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-228">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="a5f42-229">O valor padrão é D3DSTENCILOP \_ Keep.</span><span class="sxs-lookup"><span data-stu-id="a5f42-229">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-230"><span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS \_ STENCILZFAIL**</span><span class="sxs-lookup"><span data-stu-id="a5f42-230"><span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS\_STENCILZFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-231">Operação de estêncil a ser executada se o teste de estêncil passar e o teste de profundidade (teste de z) falhar.</span><span class="sxs-lookup"><span data-stu-id="a5f42-231">Stencil operation to perform if the stencil test passes and the depth test (z-test) fails.</span></span> <span data-ttu-id="a5f42-232">Os valores são do tipo enumerado [**D3DSTENCILOP**](./d3dstencilop.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-232">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="a5f42-233">O valor padrão é D3DSTENCILOP \_ Keep.</span><span class="sxs-lookup"><span data-stu-id="a5f42-233">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-234"><span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS \_ STENCILPASS**</span><span class="sxs-lookup"><span data-stu-id="a5f42-234"><span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS\_STENCILPASS**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-235">Operação de estêncil a ser executada se os testes de estêncil e de profundidade (z) forem aprovados.</span><span class="sxs-lookup"><span data-stu-id="a5f42-235">Stencil operation to perform if both the stencil and the depth (z) tests pass.</span></span> <span data-ttu-id="a5f42-236">Os valores são do tipo enumerado [**D3DSTENCILOP**](./d3dstencilop.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-236">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="a5f42-237">O valor padrão é D3DSTENCILOP \_ Keep.</span><span class="sxs-lookup"><span data-stu-id="a5f42-237">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-238"><span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS \_ STENCILFUNC**</span><span class="sxs-lookup"><span data-stu-id="a5f42-238"><span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS\_STENCILFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-239">Função de comparação para o teste de estêncil.</span><span class="sxs-lookup"><span data-stu-id="a5f42-239">Comparison function for the stencil test.</span></span> <span data-ttu-id="a5f42-240">Os valores são do tipo enumerado [**D3DCMPFUNC**](./d3dcmpfunc.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-240">Values are from the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="a5f42-241">O valor padrão é D3DCMP \_ Always.</span><span class="sxs-lookup"><span data-stu-id="a5f42-241">The default value is D3DCMP\_ALWAYS.</span></span>

<span data-ttu-id="a5f42-242">A função de comparação é usada para comparar o valor de referência a uma entrada de buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="a5f42-242">The comparison function is used to compare the reference value to a stencil buffer entry.</span></span> <span data-ttu-id="a5f42-243">Essa comparação se aplica somente aos bits no valor de referência e à entrada de buffer de estêncil que são definidos na máscara de estêncil (definida pelo \_ estado de RENDERIZAÇÃO D3DRS STENCILMASK).</span><span class="sxs-lookup"><span data-stu-id="a5f42-243">This comparison applies only to the bits in the reference value and stencil buffer entry that are set in the stencil mask (set by the D3DRS\_STENCILMASK render state).</span></span> <span data-ttu-id="a5f42-244">Se **for true**, o teste de estêncil passará.</span><span class="sxs-lookup"><span data-stu-id="a5f42-244">If **TRUE**, the stencil test passes.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-245"><span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS \_ STENCILREF**</span><span class="sxs-lookup"><span data-stu-id="a5f42-245"><span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS\_STENCILREF**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-246">Um valor de referência int para o teste de estêncil.</span><span class="sxs-lookup"><span data-stu-id="a5f42-246">An int reference value for the stencil test.</span></span> <span data-ttu-id="a5f42-247">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="a5f42-247">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-248"><span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS \_ STENCILMASK**</span><span class="sxs-lookup"><span data-stu-id="a5f42-248"><span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS\_STENCILMASK**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-249">Máscara aplicada ao valor de referência e a cada entrada de buffer de estêncil para determinar os bits significativos para o teste de estêncil.</span><span class="sxs-lookup"><span data-stu-id="a5f42-249">Mask applied to the reference value and each stencil buffer entry to determine the significant bits for the stencil test.</span></span> <span data-ttu-id="a5f42-250">A máscara padrão é 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="a5f42-250">The default mask is 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-251"><span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**D3DRS \_ STENCILWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="a5f42-251"><span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**D3DRS\_STENCILWRITEMASK**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-252">Máscara de gravação aplicada a valores gravados no buffer do estêncil.</span><span class="sxs-lookup"><span data-stu-id="a5f42-252">Write mask applied to values written into the stencil buffer.</span></span> <span data-ttu-id="a5f42-253">A máscara padrão é 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="a5f42-253">The default mask is 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-254"><span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS \_ TEXTUREFACTOR**</span><span class="sxs-lookup"><span data-stu-id="a5f42-254"><span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS\_TEXTUREFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-255">A cor usada para mesclagem de várias texturas com o argumento de mistura de textura D3DTA \_ TFACTOR ou a \_ operação de mesclagem de textura D3DTOP BLENDFACTORALPHA.</span><span class="sxs-lookup"><span data-stu-id="a5f42-255">Color used for multiple-texture blending with the D3DTA\_TFACTOR texture-blending argument or the D3DTOP\_BLENDFACTORALPHA texture-blending operation.</span></span> <span data-ttu-id="a5f42-256">O valor associado é uma variável [**D3DCOLOR**](d3dcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-256">The associated value is a [**D3DCOLOR**](d3dcolor.md) variable.</span></span> <span data-ttu-id="a5f42-257">O valor padrão é opaco branco (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="a5f42-257">The default value is opaque white (0xFFFFFFFF).</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-258"><span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS \_ WRAP0**</span><span class="sxs-lookup"><span data-stu-id="a5f42-258"><span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS\_WRAP0**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-259">Comportamento de disposição de textura para vários conjuntos de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="a5f42-259">Texture-wrapping behavior for multiple sets of texture coordinates.</span></span> <span data-ttu-id="a5f42-260">Os valores válidos para esse estado de renderização podem ser qualquer combinação de D3DWRAPCOORD \_ 0 (ou D3DWRAP \_ U), D3DWRAPCOORD \_ 1 (ou D3DWRAP \_ V), D3DWRAPCOORD \_ 2 (ou D3DWRAP \_ W) e D3DWRAPCOORD \_ 3 flags.</span><span class="sxs-lookup"><span data-stu-id="a5f42-260">Valid values for this render state can be any combination of the D3DWRAPCOORD\_0 (or D3DWRAP\_U), D3DWRAPCOORD\_1 (or D3DWRAP\_V), D3DWRAPCOORD\_2 (or D3DWRAP\_W), and D3DWRAPCOORD\_3 flags.</span></span> <span data-ttu-id="a5f42-261">Isso faz com que o sistema Empacote a direção da primeira, segunda, terceira e quarta dimensões, às vezes chamadas de direções s, t, r e q, para uma determinada textura.</span><span class="sxs-lookup"><span data-stu-id="a5f42-261">These cause the system to wrap in the direction of the first, second, third, and fourth dimensions, sometimes referred to as the s, t, r, and q directions, for a given texture.</span></span> <span data-ttu-id="a5f42-262">O valor padrão para esse estado de renderização é 0 (encapsulamento desabilitado em todas as direções).</span><span class="sxs-lookup"><span data-stu-id="a5f42-262">The default value for this render state is 0 (wrapping disabled in all directions).</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-263"><span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**D3DRS \_ WRAP1**</span><span class="sxs-lookup"><span data-stu-id="a5f42-263"><span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**D3DRS\_WRAP1**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-264">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a5f42-264">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-265"><span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**D3DRS \_ WRAP2**</span><span class="sxs-lookup"><span data-stu-id="a5f42-265"><span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**D3DRS\_WRAP2**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-266">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a5f42-266">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-267"><span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**D3DRS \_ WRAP3**</span><span class="sxs-lookup"><span data-stu-id="a5f42-267"><span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**D3DRS\_WRAP3**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-268">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a5f42-268">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-269"><span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**D3DRS \_ WRAP4**</span><span class="sxs-lookup"><span data-stu-id="a5f42-269"><span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**D3DRS\_WRAP4**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-270">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a5f42-270">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-271"><span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**D3DRS \_ WRAP5**</span><span class="sxs-lookup"><span data-stu-id="a5f42-271"><span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**D3DRS\_WRAP5**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-272">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a5f42-272">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-273"><span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**D3DRS \_ WRAP6**</span><span class="sxs-lookup"><span data-stu-id="a5f42-273"><span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**D3DRS\_WRAP6**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-274">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a5f42-274">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-275"><span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**D3DRS \_ WRAP7**</span><span class="sxs-lookup"><span data-stu-id="a5f42-275"><span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**D3DRS\_WRAP7**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-276">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a5f42-276">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-277"><span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**Recorte de D3DRS \_**</span><span class="sxs-lookup"><span data-stu-id="a5f42-277"><span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**D3DRS\_CLIPPING**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-278">**True** para habilitar o recorte primitivo por Direct3D ou **false** para desabilitá-lo.</span><span class="sxs-lookup"><span data-stu-id="a5f42-278">**TRUE** to enable primitive clipping by Direct3D, or **FALSE** to disable it.</span></span> <span data-ttu-id="a5f42-279">O valor padrão é **true**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-279">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-280"><span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**\_Iluminação D3DRS**</span><span class="sxs-lookup"><span data-stu-id="a5f42-280"><span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**D3DRS\_LIGHTING**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-281">**True** para habilitar a iluminação de Direct3D ou **false** para desabilitá-la.</span><span class="sxs-lookup"><span data-stu-id="a5f42-281">**TRUE** to enable Direct3D lighting, or **FALSE** to disable it.</span></span> <span data-ttu-id="a5f42-282">O valor padrão é **true**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-282">The default value is **TRUE**.</span></span> <span data-ttu-id="a5f42-283">Somente os vértices que incluem um vértice normal estão acesos adequadamente; os vértices que não contêm uma aplicação normal um produto de ponto de 0 em todos os cálculos de iluminação.</span><span class="sxs-lookup"><span data-stu-id="a5f42-283">Only vertices that include a vertex normal are properly lit; vertices that do not contain a normal employ a dot product of 0 in all lighting calculations.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-284"><span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**\_Ambiente D3DRS**</span><span class="sxs-lookup"><span data-stu-id="a5f42-284"><span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**D3DRS\_AMBIENT**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-285">Cor de luz ambiente.</span><span class="sxs-lookup"><span data-stu-id="a5f42-285">Ambient light color.</span></span> <span data-ttu-id="a5f42-286">Esse valor é do tipo [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="a5f42-286">This value is of type [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="a5f42-287">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="a5f42-287">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-288"><span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**D3DRS \_ FOGVERTEXMODE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-288"><span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**D3DRS\_FOGVERTEXMODE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-289">Fórmula de neblina a ser usada para a neblina de vértice.</span><span class="sxs-lookup"><span data-stu-id="a5f42-289">Fog formula to be used for vertex fog.</span></span> <span data-ttu-id="a5f42-290">Defina como um membro do tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-290">Set to one member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="a5f42-291">O valor padrão é D3DFOG \_ None.</span><span class="sxs-lookup"><span data-stu-id="a5f42-291">The default value is D3DFOG\_NONE.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-292"><span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS \_ COLORVERTEX**</span><span class="sxs-lookup"><span data-stu-id="a5f42-292"><span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS\_COLORVERTEX**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-293">**True** para habilitar a cor por vértice ou **false** para desabilitá-la.</span><span class="sxs-lookup"><span data-stu-id="a5f42-293">**TRUE** to enable per-vertex color or **FALSE** to disable it.</span></span> <span data-ttu-id="a5f42-294">O valor padrão é **true**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-294">The default value is **TRUE**.</span></span> <span data-ttu-id="a5f42-295">Habilitar a cor por vértice permite que o sistema inclua a cor definida para vértices individuais em seus cálculos de iluminação.</span><span class="sxs-lookup"><span data-stu-id="a5f42-295">Enabling per-vertex color allows the system to include the color defined for individual vertices in its lighting calculations.</span></span>

<span data-ttu-id="a5f42-296">Para obter mais informações, consulte os seguintes Estados de renderização:</span><span class="sxs-lookup"><span data-stu-id="a5f42-296">For more information, see the following render states:</span></span>

-   <span data-ttu-id="a5f42-297">D3DRS \_ DiffuseMaterialSource</span><span class="sxs-lookup"><span data-stu-id="a5f42-297">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>
-   <span data-ttu-id="a5f42-298">D3DRS \_ SPECULARMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="a5f42-298">D3DRS\_SPECULARMATERIALSOURCE</span></span>
-   <span data-ttu-id="a5f42-299">D3DRS \_ AMBIENTMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="a5f42-299">D3DRS\_AMBIENTMATERIALSOURCE</span></span>
-   <span data-ttu-id="a5f42-300">D3DRS \_ EMISSIVEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="a5f42-300">D3DRS\_EMISSIVEMATERIALSOURCE</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-301"><span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS \_ LOCALVIEWER**</span><span class="sxs-lookup"><span data-stu-id="a5f42-301"><span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS\_LOCALVIEWER**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-302">**True** para habilitar os destaques de especular relativos à câmera ou **false** para usar os destaques ortogonal de especulação.</span><span class="sxs-lookup"><span data-stu-id="a5f42-302">**TRUE** to enable camera-relative specular highlights, or **FALSE** to use orthogonal specular highlights.</span></span> <span data-ttu-id="a5f42-303">O valor padrão é **true**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-303">The default value is **TRUE**.</span></span> <span data-ttu-id="a5f42-304">Os aplicativos que usam projeção ortogonal devem especificar **false**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-304">Applications that use orthogonal projection should specify **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-305"><span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS \_ NORMALIZENORMALS**</span><span class="sxs-lookup"><span data-stu-id="a5f42-305"><span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS\_NORMALIZENORMALS**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-306">**True** para habilitar a normalização automática dos Normals de vértice ou **false** para desabilitá-lo.</span><span class="sxs-lookup"><span data-stu-id="a5f42-306">**TRUE** to enable automatic normalization of vertex normals, or **FALSE** to disable it.</span></span> <span data-ttu-id="a5f42-307">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-307">The default value is **FALSE**.</span></span> <span data-ttu-id="a5f42-308">Habilitar esse recurso faz com que o sistema Normalize os Normals dos vértices depois de transformá-los no espaço da câmera, o que pode ser demorado computacionalmente.</span><span class="sxs-lookup"><span data-stu-id="a5f42-308">Enabling this feature causes the system to normalize the vertex normals for vertices after transforming them to camera space, which can be computationally time-consuming.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-309"><span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS \_ DiffuseMaterialSource**</span><span class="sxs-lookup"><span data-stu-id="a5f42-309"><span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS\_DIFFUSEMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-310">Fonte de cores difusa para cálculos de iluminação.</span><span class="sxs-lookup"><span data-stu-id="a5f42-310">Diffuse color source for lighting calculations.</span></span> <span data-ttu-id="a5f42-311">Os valores válidos são membros do tipo enumerado [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-311">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="a5f42-312">O valor padrão é D3DMCS \_ COLOR1.</span><span class="sxs-lookup"><span data-stu-id="a5f42-312">The default value is D3DMCS\_COLOR1.</span></span> <span data-ttu-id="a5f42-313">O valor para esse estado de renderização será usado somente se o \_ estado de RENDERIZAÇÃO D3DRS COLORVERTEX for definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-313">The value for this render state is used only if the D3DRS\_COLORVERTEX render state is set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-314"><span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS \_ SPECULARMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-314"><span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS\_SPECULARMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-315">Fonte de cor especular para cálculos de iluminação.</span><span class="sxs-lookup"><span data-stu-id="a5f42-315">Specular color source for lighting calculations.</span></span> <span data-ttu-id="a5f42-316">Os valores válidos são membros do tipo enumerado [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-316">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="a5f42-317">O valor padrão é D3DMCS \_ COLOR2.</span><span class="sxs-lookup"><span data-stu-id="a5f42-317">The default value is D3DMCS\_COLOR2.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-318"><span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS \_ AMBIENTMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-318"><span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS\_AMBIENTMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-319">Fonte de cor de ambiente para cálculos de iluminação.</span><span class="sxs-lookup"><span data-stu-id="a5f42-319">Ambient color source for lighting calculations.</span></span> <span data-ttu-id="a5f42-320">Os valores válidos são membros do tipo enumerado [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-320">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="a5f42-321">O valor padrão é \_ material D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="a5f42-321">The default value is D3DMCS\_MATERIAL.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-322"><span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS \_ EMISSIVEMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-322"><span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS\_EMISSIVEMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-323">Fonte de cores emissiva para cálculos de iluminação.</span><span class="sxs-lookup"><span data-stu-id="a5f42-323">Emissive color source for lighting calculations.</span></span> <span data-ttu-id="a5f42-324">Os valores válidos são membros do tipo enumerado [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-324">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="a5f42-325">O valor padrão é \_ material D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="a5f42-325">The default value is D3DMCS\_MATERIAL.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-326"><span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**D3DRS \_ VERTEXBLEND**</span><span class="sxs-lookup"><span data-stu-id="a5f42-326"><span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**D3DRS\_VERTEXBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-327">Número de matrizes a serem usadas para executar a mesclagem de geometria, se houver.</span><span class="sxs-lookup"><span data-stu-id="a5f42-327">Number of matrices to use to perform geometry blending, if any.</span></span> <span data-ttu-id="a5f42-328">Os valores válidos são membros do tipo enumerado [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-328">Valid values are members of the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="a5f42-329">O valor padrão é D3DVBF \_ Disable.</span><span class="sxs-lookup"><span data-stu-id="a5f42-329">The default value is D3DVBF\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-330"><span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**D3DRS \_ CLIPPLANEENABLE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-330"><span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**D3DRS\_CLIPPLANEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-331">Habilita ou desabilita os planos de recorte definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="a5f42-331">Enables or disables user-defined clipping planes.</span></span> <span data-ttu-id="a5f42-332">Os valores válidos são qualquer DWORD em que o status de cada bit (Set ou not set) alterna o estado de ativação de um plano de recorte definido pelo usuário correspondente.</span><span class="sxs-lookup"><span data-stu-id="a5f42-332">Valid values are any DWORD in which the status of each bit (set or not set) toggles the activation state of a corresponding user-defined clipping plane.</span></span> <span data-ttu-id="a5f42-333">O bit menos significativo (bit 0) controla o primeiro plano de recorte no índice 0, e os bits subsequentes controlam a ativação de planos de recorte em índices mais altos.</span><span class="sxs-lookup"><span data-stu-id="a5f42-333">The least significant bit (bit 0) controls the first clipping plane at index 0, and subsequent bits control the activation of clipping planes at higher indexes.</span></span> <span data-ttu-id="a5f42-334">Se um bit for definido, o sistema aplicará o plano de recorte apropriado durante a renderização da cena.</span><span class="sxs-lookup"><span data-stu-id="a5f42-334">If a bit is set, the system applies the appropriate clipping plane during scene rendering.</span></span> <span data-ttu-id="a5f42-335">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="a5f42-335">The default value is 0.</span></span>

<span data-ttu-id="a5f42-336">As macros [**D3DCLIPPLANEn**](d3dclipplanen.md) são definidas para fornecer uma maneira conveniente de habilitar os planos de recorte.</span><span class="sxs-lookup"><span data-stu-id="a5f42-336">The [**D3DCLIPPLANEn**](d3dclipplanen.md) macros are defined to provide a convenient way to enable clipping planes.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-337"><span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**Pontos de D3DRS \_**</span><span class="sxs-lookup"><span data-stu-id="a5f42-337"><span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**D3DRS\_POINTSIZE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-338">Um valor float que especifica o tamanho a ser usado para computação de tamanho de ponto nos casos em que o tamanho do ponto não é especificado para cada vértice.</span><span class="sxs-lookup"><span data-stu-id="a5f42-338">A float value that specifies the size to use for point size computation in cases where point size is not specified for each vertex.</span></span> <span data-ttu-id="a5f42-339">Esse valor não é usado quando o vértice contém o tamanho do ponto.</span><span class="sxs-lookup"><span data-stu-id="a5f42-339">This value is not used when the vertex contains point size.</span></span> <span data-ttu-id="a5f42-340">Esse valor estará em unidades de espaço na tela se D3DRS \_ POINTSCALEENABLE for **false**; caso contrário, esse valor estará em unidades de espaço de mundo.</span><span class="sxs-lookup"><span data-stu-id="a5f42-340">This value is in screen space units if D3DRS\_POINTSCALEENABLE is **FALSE**; otherwise this value is in world space units.</span></span> <span data-ttu-id="a5f42-341">O valor padrão é o valor que um driver retorna.</span><span class="sxs-lookup"><span data-stu-id="a5f42-341">The default value is the value a driver returns.</span></span> <span data-ttu-id="a5f42-342">Se um driver retornar 0 ou 1, o valor padrão será 64, o que permite emulação de tamanho de ponto de software.</span><span class="sxs-lookup"><span data-stu-id="a5f42-342">If a driver returns 0 or 1, the default value is 64, which allows software point size emulation.</span></span> <span data-ttu-id="a5f42-343">Como o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aceita valores DWORD, seu aplicativo deve converter uma variável que contém o valor, conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5f42-343">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE, *((DWORD*)&pointSize));
```



</dd> <dt>

<span data-ttu-id="a5f42-344"><span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS \_ pontos \_ mínimos**</span><span class="sxs-lookup"><span data-stu-id="a5f42-344"><span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS\_POINTSIZE\_MIN**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-345">Um valor float que especifica o tamanho mínimo de primitivos de ponto.</span><span class="sxs-lookup"><span data-stu-id="a5f42-345">A float value that specifies the minimum size of point primitives.</span></span> <span data-ttu-id="a5f42-346">Os primitivos de ponto são clamped a esse tamanho durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="a5f42-346">Point primitives are clamped to this size during rendering.</span></span> <span data-ttu-id="a5f42-347">Definir isso com valores menores que 1,0 resulta em pontos que se esgotam quando o ponto não cobre um centro de pixels e a suavização está desabilitada ou sendo processada com intensidade reduzida quando a suavização está habilitada.</span><span class="sxs-lookup"><span data-stu-id="a5f42-347">Setting this to values smaller than 1.0 results in points dropping out when the point does not cover a pixel center and antialiasing is disabled or being rendered with reduced intensity when antialiasing is enabled.</span></span> <span data-ttu-id="a5f42-348">O valor padrão é 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="a5f42-348">The default value is 1.0f.</span></span> <span data-ttu-id="a5f42-349">O intervalo para esse valor é maior ou igual a 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="a5f42-349">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="a5f42-350">Como o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aceita valores DWORD, seu aplicativo deve converter uma variável que contém o valor, conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5f42-350">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE_MIN, *((DWORD*)&pointSizeMin));
```



</dd> <dt>

<span data-ttu-id="a5f42-351"><span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**D3DRS \_ POINTSPRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-351"><span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**D3DRS\_POINTSPRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-352">valor bool.</span><span class="sxs-lookup"><span data-stu-id="a5f42-352">bool value.</span></span> <span data-ttu-id="a5f42-353">Quando **true**, as coordenadas de textura dos primitivos de ponto são definidas para que as texturas completas sejam mapeadas em cada ponto.</span><span class="sxs-lookup"><span data-stu-id="a5f42-353">When **TRUE**, texture coordinates of point primitives are set so that full textures are mapped on each point.</span></span> <span data-ttu-id="a5f42-354">Quando **for falso**, as coordenadas de textura de vértice serão usadas para todo o ponto.</span><span class="sxs-lookup"><span data-stu-id="a5f42-354">When **FALSE**, the vertex texture coordinates are used for the entire point.</span></span> <span data-ttu-id="a5f42-355">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-355">The default value is **FALSE**.</span></span> <span data-ttu-id="a5f42-356">Você pode obter pontos de pixel único do estilo DirectX 7 definindo D3DRS \_ POINTSCALEENABLE como **false** e D3DRS de \_ pontos para 1,0, que são os valores padrão.</span><span class="sxs-lookup"><span data-stu-id="a5f42-356">You can achieve DirectX 7 style single-pixel points by setting D3DRS\_POINTSCALEENABLE to **FALSE** and D3DRS\_POINTSIZE to 1.0, which are the default values.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-357"><span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS \_ POINTSCALEENABLE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-357"><span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS\_POINTSCALEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-358">valor bool que controla a computação de tamanho para primitivos de ponto.</span><span class="sxs-lookup"><span data-stu-id="a5f42-358">bool value that controls computation of size for point primitives.</span></span> <span data-ttu-id="a5f42-359">Quando **true**, o tamanho do ponto é interpretado como um valor de espaço da câmera e é dimensionado pela função Distance e o frustum para o dimensionamento do eixo y do visor para calcular o tamanho do ponto de espaço da tela final.</span><span class="sxs-lookup"><span data-stu-id="a5f42-359">When **TRUE**, the point size is interpreted as a camera space value and is scaled by the distance function and the frustum to viewport y-axis scaling to compute the final screen-space point size.</span></span> <span data-ttu-id="a5f42-360">Quando **false**, o tamanho do ponto é interpretado como espaço da tela e usado diretamente.</span><span class="sxs-lookup"><span data-stu-id="a5f42-360">When **FALSE**, the point size is interpreted as screen space and used directly.</span></span> <span data-ttu-id="a5f42-361">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-361">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-362"><span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS \_ POINTSCALE \_ A**</span><span class="sxs-lookup"><span data-stu-id="a5f42-362"><span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS\_POINTSCALE\_A**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-363">Um valor float que controla a atenuação de tamanho baseado em distância para primitivos de ponto.</span><span class="sxs-lookup"><span data-stu-id="a5f42-363">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="a5f42-364">Ativo somente quando D3DRS \_ POINTSCALEENABLE for **true**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-364">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="a5f42-365">O valor padrão é 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="a5f42-365">The default value is 1.0f.</span></span> <span data-ttu-id="a5f42-366">O intervalo para esse valor é maior ou igual a 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="a5f42-366">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="a5f42-367">Como o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aceita valores DWORD, seu aplicativo deve converter uma variável que contém o valor, conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5f42-367">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_A, *((DWORD*)&pointScaleA));
```



</dd> <dt>

<span data-ttu-id="a5f42-368"><span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS \_ POINTSCALE \_ B**</span><span class="sxs-lookup"><span data-stu-id="a5f42-368"><span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS\_POINTSCALE\_B**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-369">Um valor float que controla a atenuação de tamanho baseado em distância para primitivos de ponto.</span><span class="sxs-lookup"><span data-stu-id="a5f42-369">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="a5f42-370">Ativo somente quando D3DRS \_ POINTSCALEENABLE for **true**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-370">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="a5f42-371">O valor padrão é 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="a5f42-371">The default value is 0.0f.</span></span> <span data-ttu-id="a5f42-372">O intervalo para esse valor é maior ou igual a 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="a5f42-372">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="a5f42-373">Como o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aceita valores DWORD, seu aplicativo deve converter uma variável que contém o valor, conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5f42-373">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_B, *((DWORD*)&pointScaleB));
```



</dd> <dt>

<span data-ttu-id="a5f42-374"><span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS \_ POINTSCALE \_ C**</span><span class="sxs-lookup"><span data-stu-id="a5f42-374"><span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS\_POINTSCALE\_C**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-375">Um valor float que controla a atenuação de tamanho baseado em distância para primitivos de ponto.</span><span class="sxs-lookup"><span data-stu-id="a5f42-375">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="a5f42-376">Ativo somente quando D3DRS \_ POINTSCALEENABLE for **true**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-376">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="a5f42-377">O valor padrão é 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="a5f42-377">The default value is 0.0f.</span></span> <span data-ttu-id="a5f42-378">O intervalo para esse valor é maior ou igual a 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="a5f42-378">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="a5f42-379">Como o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aceita valores DWORD, seu aplicativo deve converter uma variável que contém o valor, conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5f42-379">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_C, *((DWORD*)&pointScaleC));
```



</dd> <dt>

<span data-ttu-id="a5f42-380"><span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS \_ MULTISAMPLEANTIALIAS**</span><span class="sxs-lookup"><span data-stu-id="a5f42-380"><span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS\_MULTISAMPLEANTIALIAS**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-381">valor bool que determina como as amostras individuais são computadas ao usar um buffer de destino de renderização de multiamostra.</span><span class="sxs-lookup"><span data-stu-id="a5f42-381">bool value that determines how individual samples are computed when using a multisample render-target buffer.</span></span> <span data-ttu-id="a5f42-382">Quando definido como **true**, os vários exemplos são computados para que a suavização da cena completa seja executada por amostragem em diferentes posições de exemplo para cada amostra múltipla.</span><span class="sxs-lookup"><span data-stu-id="a5f42-382">When set to **TRUE**, the multiple samples are computed so that full-scene antialiasing is performed by sampling at different sample positions for each multiple sample.</span></span> <span data-ttu-id="a5f42-383">Quando definido como **false**, os vários exemplos são todos gravados com o mesmo valor de exemplo, amostrados no pixel Center, que permite a renderização sem alias em um buffer de várias amostras.</span><span class="sxs-lookup"><span data-stu-id="a5f42-383">When set to **FALSE**, the multiple samples are all written with the same sample value, sampled at the pixel center, which allows non-antialiased rendering to a multisample buffer.</span></span> <span data-ttu-id="a5f42-384">Esse estado de renderização não tem nenhum efeito ao renderizar para um buffer de exemplo único.</span><span class="sxs-lookup"><span data-stu-id="a5f42-384">This render state has no effect when rendering to a single sample buffer.</span></span> <span data-ttu-id="a5f42-385">O valor padrão é **true**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-385">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-386"><span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS \_ MULTISAMPLEMASK**</span><span class="sxs-lookup"><span data-stu-id="a5f42-386"><span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS\_MULTISAMPLEMASK**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-387">Cada bit nessa máscara, começando pelo bit menos significativo (LSB), controla a modificação de um dos exemplos em um destino de renderização de multiamostrar.</span><span class="sxs-lookup"><span data-stu-id="a5f42-387">Each bit in this mask, starting at the least significant bit (LSB), controls modification of one of the samples in a multisample render target.</span></span> <span data-ttu-id="a5f42-388">Portanto, para um destino de renderização de 8 amostras, o byte baixo contém as oito habilitações de gravação para cada um dos oito exemplos.</span><span class="sxs-lookup"><span data-stu-id="a5f42-388">Thus, for an 8-sample render target, the low byte contains the eight write enables for each of the eight samples.</span></span> <span data-ttu-id="a5f42-389">Esse estado de renderização não tem nenhum efeito ao renderizar para um buffer de exemplo único.</span><span class="sxs-lookup"><span data-stu-id="a5f42-389">This render state has no effect when rendering to a single sample buffer.</span></span> <span data-ttu-id="a5f42-390">O valor padrão é 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="a5f42-390">The default value is 0xFFFFFFFF.</span></span>

<span data-ttu-id="a5f42-391">Esse estado de renderização habilita o uso de um buffer de várias amostras como um buffer de acumulação, fazendo a renderização multipassada de Geometry, em que cada passagem atualiza um subconjunto de amostras.</span><span class="sxs-lookup"><span data-stu-id="a5f42-391">This render state enables use of a multisample buffer as an accumulation buffer, doing multipass rendering of geometry where each pass updates a subset of samples.</span></span>

<span data-ttu-id="a5f42-392">Se houver n amostras habilitadas com várias amostras e k, a intensidade resultante da imagem renderizada deverá ser k/n.</span><span class="sxs-lookup"><span data-stu-id="a5f42-392">If there are n multisamples and k enabled samples, the resulting intensity of the rendered image should be k/n.</span></span> <span data-ttu-id="a5f42-393">Cada componente RGB de cada pixel é fatorado por k/n.</span><span class="sxs-lookup"><span data-stu-id="a5f42-393">Each component RGB of every pixel is factored by k/n.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-394"><span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS \_ PATCHEDGESTYLE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-394"><span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS\_PATCHEDGESTYLE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-395">Define se as bordas do patch usarão o mosaico do estilo flutuante.</span><span class="sxs-lookup"><span data-stu-id="a5f42-395">Sets whether patch edges will use float style tessellation.</span></span> <span data-ttu-id="a5f42-396">Os valores possíveis são definidos pelo tipo enumerado [**D3DPATCHEDGESTYLE**](./d3dpatchedgestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-396">Possible values are defined by the [**D3DPATCHEDGESTYLE**](./d3dpatchedgestyle.md) enumerated type.</span></span> <span data-ttu-id="a5f42-397">O valor padrão é D3DPATCHEDGE \_ discreto.</span><span class="sxs-lookup"><span data-stu-id="a5f42-397">The default value is D3DPATCHEDGE\_DISCRETE.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-398"><span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS \_ DEBUGMONITORTOKEN**</span><span class="sxs-lookup"><span data-stu-id="a5f42-398"><span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS\_DEBUGMONITORTOKEN**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-399">Defina somente para depurar o monitor.</span><span class="sxs-lookup"><span data-stu-id="a5f42-399">Set only for debugging the monitor.</span></span> <span data-ttu-id="a5f42-400">Os valores possíveis são definidos pelo tipo enumerado [**D3DDEBUGMONITORTOKENS**](./d3ddebugmonitortokens.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-400">Possible values are defined by the [**D3DDEBUGMONITORTOKENS**](./d3ddebugmonitortokens.md) enumerated type.</span></span> <span data-ttu-id="a5f42-401">Observe que, se D3DRS \_ DEBUGMONITORTOKEN for definido, a chamada será tratada como passando um token para o monitor de depuração.</span><span class="sxs-lookup"><span data-stu-id="a5f42-401">Note that if D3DRS\_DEBUGMONITORTOKEN is set, the call is treated as passing a token to the debug monitor.</span></span> <span data-ttu-id="a5f42-402">Por exemplo, se-After passing D3DDMT \_ Enable ou D3DDMT \_ Disable to D3DRS \_ DEBUGMONITORTOKEN-outros valores de token forem passados, o estado (Enabled ou Disabled) do monitor de depuração ainda será mantido.</span><span class="sxs-lookup"><span data-stu-id="a5f42-402">For example, if - after passing D3DDMT\_ENABLE or D3DDMT\_DISABLE to D3DRS\_DEBUGMONITORTOKEN - other token values are passed in, the state (enabled or disabled) of the debug monitor will still persist.</span></span>

<span data-ttu-id="a5f42-403">Esse Estado só é útil para compilações de depuração.</span><span class="sxs-lookup"><span data-stu-id="a5f42-403">This state is only useful for debug builds.</span></span> <span data-ttu-id="a5f42-404">O monitor de depuração usa como padrão D3DDMT \_ habilitar.</span><span class="sxs-lookup"><span data-stu-id="a5f42-404">The debug monitor defaults to D3DDMT\_ENABLE.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-405"><span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS \_ pontos \_ máximos**</span><span class="sxs-lookup"><span data-stu-id="a5f42-405"><span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS\_POINTSIZE\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-406">Um valor float que especifica o tamanho máximo para o qual os sprites de ponto serão clampeddos.</span><span class="sxs-lookup"><span data-stu-id="a5f42-406">A float value that specifies the maximum size to which point sprites will be clamped.</span></span> <span data-ttu-id="a5f42-407">O valor deve ser menor ou igual ao membro de MaxPointSize de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) e maior ou igual a D3DRS \_ indica \_ mín.</span><span class="sxs-lookup"><span data-stu-id="a5f42-407">The value must be less than or equal to the MaxPointSize member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) and greater than or equal to D3DRS\_POINTSIZE\_MIN.</span></span> <span data-ttu-id="a5f42-408">O valor padrão é 64,0.</span><span class="sxs-lookup"><span data-stu-id="a5f42-408">The default value is 64.0.</span></span> <span data-ttu-id="a5f42-409">Como o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aceita valores DWORD, seu aplicativo deve converter uma variável que contém o valor, conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5f42-409">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_PONTSIZE_MAX, *((DWORD*)&pointSizeMax));
```



</dd> <dt>

<span data-ttu-id="a5f42-410"><span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS \_ INDEXEDVERTEXBLENDENABLE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-410"><span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS\_INDEXEDVERTEXBLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-411">valor bool que habilita ou desabilita a mistura de vértices indexados.</span><span class="sxs-lookup"><span data-stu-id="a5f42-411">bool value that enables or disables indexed vertex blending.</span></span> <span data-ttu-id="a5f42-412">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-412">The default value is **FALSE**.</span></span> <span data-ttu-id="a5f42-413">Quando definido como **true**, a mesclagem de vértices indexados é habilitada.</span><span class="sxs-lookup"><span data-stu-id="a5f42-413">When set to **TRUE**, indexed vertex blending is enabled.</span></span> <span data-ttu-id="a5f42-414">Quando definido como **false**, a mesclagem de vértices indexados é desabilitada.</span><span class="sxs-lookup"><span data-stu-id="a5f42-414">When set to **FALSE**, indexed vertex blending is disabled.</span></span> <span data-ttu-id="a5f42-415">Se esse estado de renderização estiver habilitado, o usuário deverá passar índices de matriz como um DWORDwith empacotado a cada vértice.</span><span class="sxs-lookup"><span data-stu-id="a5f42-415">If this render state is enabled, the user must pass matrix indices as a packed DWORDwith every vertex.</span></span> <span data-ttu-id="a5f42-416">Quando o estado de renderização é desabilitado e a mesclagem de vértice é habilitada por meio do \_ estado D3DRS VERTEXBLEND, é equivalente a ter os índices de matriz 0, 1, 2, 3 em todos os vértices.</span><span class="sxs-lookup"><span data-stu-id="a5f42-416">When the render state is disabled and vertex blending is enabled through the D3DRS\_VERTEXBLEND state, it is equivalent to having matrix indices 0, 1, 2, 3 in every vertex.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-417"><span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS \_ COLORWRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-417"><span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS\_COLORWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-418">Valor UINT que habilita uma gravação por canal para o buffer de cores de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="a5f42-418">UINT value that enables a per-channel write for the render-target color buffer.</span></span> <span data-ttu-id="a5f42-419">Um bit definido resulta no canal de cores que está sendo atualizado durante a renderização 3D.</span><span class="sxs-lookup"><span data-stu-id="a5f42-419">A set bit results in the color channel being updated during 3D rendering.</span></span> <span data-ttu-id="a5f42-420">Um bit claro faz com que o canal de cor não seja afetado.</span><span class="sxs-lookup"><span data-stu-id="a5f42-420">A clear bit results in the color channel being unaffected.</span></span> <span data-ttu-id="a5f42-421">Essa funcionalidade estará disponível se o \_ bit D3DPMISCCAPS COLORWRITEENABLE Capabilities estiver definido no membro PrimitiveMiscCaps da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5f42-421">This functionality is available if the D3DPMISCCAPS\_COLORWRITEENABLE capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="a5f42-422">Esse estado de renderização não afeta a operação de limpeza.</span><span class="sxs-lookup"><span data-stu-id="a5f42-422">This render state does not affect the clear operation.</span></span> <span data-ttu-id="a5f42-423">O valor padrão é 0x0000000F.</span><span class="sxs-lookup"><span data-stu-id="a5f42-423">The default value is 0x0000000F.</span></span>

<span data-ttu-id="a5f42-424">Os valores válidos para esse estado de renderização podem ser qualquer combinação dos \_ sinalizadores D3DCOLORWRITEENABLE alfa, D3DCOLORWRITEENABLE \_ azul, D3DCOLORWRITEENABLE \_ verde ou D3DCOLORWRITEENABLE \_ vermelho.</span><span class="sxs-lookup"><span data-stu-id="a5f42-424">Valid values for this render state can be any combination of the D3DCOLORWRITEENABLE\_ALPHA, D3DCOLORWRITEENABLE\_BLUE, D3DCOLORWRITEENABLE\_GREEN, or D3DCOLORWRITEENABLE\_RED flags.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-425"><span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS \_ TWEENFACTOR**</span><span class="sxs-lookup"><span data-stu-id="a5f42-425"><span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS\_TWEENFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-426">Um valor float que controla o fator de interpolação.</span><span class="sxs-lookup"><span data-stu-id="a5f42-426">A float value that controls the tween factor.</span></span> <span data-ttu-id="a5f42-427">O valor padrão é 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="a5f42-427">The default value is 0.0f.</span></span> <span data-ttu-id="a5f42-428">Como o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aceita valores DWORD, seu aplicativo deve converter uma variável que contém o valor, conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5f42-428">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_TWEENFACTOR, *((DWORD*)&TweenFactor));
```



</dd> <dt>

<span data-ttu-id="a5f42-429"><span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**D3DRS \_ BLENDOP**</span><span class="sxs-lookup"><span data-stu-id="a5f42-429"><span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**D3DRS\_BLENDOP**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-430">O valor usado para selecionar a operação aritmética aplicada quando o estado de renderização de mistura alfa, D3DRS \_ ALPHABLENDENABLE, é definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-430">Value used to select the arithmetic operation applied when the alpha blending render state, D3DRS\_ALPHABLENDENABLE, is set to **TRUE**.</span></span> <span data-ttu-id="a5f42-431">Os valores válidos são definidos pelo tipo enumerado [**D3DBLENDOP**](./d3dblendop.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-431">Valid values are defined by the [**D3DBLENDOP**](./d3dblendop.md) enumerated type.</span></span> <span data-ttu-id="a5f42-432">O valor padrão é D3DBLENDOP \_ Add.</span><span class="sxs-lookup"><span data-stu-id="a5f42-432">The default value is D3DBLENDOP\_ADD.</span></span>

<span data-ttu-id="a5f42-433">Se o \_ recurso de dispositivo D3DPMISCCAPS BLENDOP não tiver suporte, D3DBLENDOP \_ Adicionar será executado.</span><span class="sxs-lookup"><span data-stu-id="a5f42-433">If the D3DPMISCCAPS\_BLENDOP device capability is not supported, then D3DBLENDOP\_ADD is performed.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-434"><span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS \_ POSITIONDEGREE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-434"><span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS\_POSITIONDEGREE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-435">N-grau de interpolação da posição do patch.</span><span class="sxs-lookup"><span data-stu-id="a5f42-435">N-patch position interpolation degree.</span></span> <span data-ttu-id="a5f42-436">Os valores podem ser D3DDEGREE \_ cúbico (padrão) ou D3DDEGREE \_ linear.</span><span class="sxs-lookup"><span data-stu-id="a5f42-436">The values can be D3DDEGREE\_CUBIC (default) or D3DDEGREE\_LINEAR.</span></span> <span data-ttu-id="a5f42-437">Para obter mais informações, consulte [**D3DDEGREETYPE**](./d3ddegreetype.md).</span><span class="sxs-lookup"><span data-stu-id="a5f42-437">For more information, see [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-438"><span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS \_ NORMALDEGREE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-438"><span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS\_NORMALDEGREE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-439">N-corrigir grau de interpolação normal.</span><span class="sxs-lookup"><span data-stu-id="a5f42-439">N-patch normal interpolation degree.</span></span> <span data-ttu-id="a5f42-440">Os valores podem ser D3DDEGREE \_ lineares (padrão) ou D3DDEGREE \_ quadrática.</span><span class="sxs-lookup"><span data-stu-id="a5f42-440">The values can be D3DDEGREE\_LINEAR (default) or D3DDEGREE\_QUADRATIC.</span></span> <span data-ttu-id="a5f42-441">Para obter mais informações, consulte [**D3DDEGREETYPE**](./d3ddegreetype.md).</span><span class="sxs-lookup"><span data-stu-id="a5f42-441">For more information, see [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-442"><span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS \_ SCISSORTESTENABLE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-442"><span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS\_SCISSORTESTENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-443">**True** para habilitar o teste de recorte e **false** para desabilitá-lo.</span><span class="sxs-lookup"><span data-stu-id="a5f42-443">**TRUE** to enable scissor testing and **FALSE** to disable it.</span></span> <span data-ttu-id="a5f42-444">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-444">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-445"><span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS \_ SLOPESCALEDEPTHBIAS**</span><span class="sxs-lookup"><span data-stu-id="a5f42-445"><span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS\_SLOPESCALEDEPTHBIAS**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-446">Usado para determinar a quantidade de inclinação que pode ser aplicada a primitivos coplanares para reduzir o combate ao z.</span><span class="sxs-lookup"><span data-stu-id="a5f42-446">Used to determine how much bias can be applied to co-planar primitives to reduce z-fighting.</span></span> <span data-ttu-id="a5f42-447">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="a5f42-447">The default value is 0.</span></span>

<span data-ttu-id="a5f42-448">Bias = (Max \* D3DRS \_ SLOPESCALEDEPTHBIAS) + D3DRS \_ DEPTHBIAS.</span><span class="sxs-lookup"><span data-stu-id="a5f42-448">bias = (max \* D3DRS\_SLOPESCALEDEPTHBIAS) + D3DRS\_DEPTHBIAS.</span></span>

<span data-ttu-id="a5f42-449">em que Max é a inclinação de profundidade máxima do triângulo que está sendo renderizado.</span><span class="sxs-lookup"><span data-stu-id="a5f42-449">where max is the maximum depth slope of the triangle being rendered.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-450"><span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS \_ ANTIALIASEDLINEENABLE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-450"><span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS\_ANTIALIASEDLINEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-451">**True** para habilitar a suavização de linha, **false** para desabilitar a suavização de linha.</span><span class="sxs-lookup"><span data-stu-id="a5f42-451">**TRUE** to enable line antialiasing, **FALSE** to disable line antialiasing.</span></span> <span data-ttu-id="a5f42-452">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-452">The default value is **FALSE**.</span></span>

<span data-ttu-id="a5f42-453">Ao renderizar para um destino de renderização multiamostral, D3DRS \_ ANTIALIASEDLINEENABLE é ignorado e todas as linhas são processadas com alias.</span><span class="sxs-lookup"><span data-stu-id="a5f42-453">When rendering to a multisample render target, D3DRS\_ANTIALIASEDLINEENABLE is ignored and all lines are rendered aliased.</span></span> <span data-ttu-id="a5f42-454">Use [**ID3DXLine**](id3dxline.md) para a renderização de linha AntiAlias em um destino de renderização de multiamostra.</span><span class="sxs-lookup"><span data-stu-id="a5f42-454">Use [**ID3DXLine**](id3dxline.md) for antialiased line rendering in a multisample render target.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-455"><span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS \_ MINTESSELLATIONLEVEL**</span><span class="sxs-lookup"><span data-stu-id="a5f42-455"><span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS\_MINTESSELLATIONLEVEL**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-456">Nível de mosaico mínimo.</span><span class="sxs-lookup"><span data-stu-id="a5f42-456">Minimum tessellation level.</span></span> <span data-ttu-id="a5f42-457">O valor padrão é 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="a5f42-457">The default value is 1.0f.</span></span> <span data-ttu-id="a5f42-458">Consulte [mosaico (Direct3D 9)](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="a5f42-458">See [Tessellation (Direct3D 9)](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-459"><span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS \_ MAXTESSELLATIONLEVEL**</span><span class="sxs-lookup"><span data-stu-id="a5f42-459"><span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS\_MAXTESSELLATIONLEVEL**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-460">Nível máximo de mosaico.</span><span class="sxs-lookup"><span data-stu-id="a5f42-460">Maximum tessellation level.</span></span> <span data-ttu-id="a5f42-461">O valor padrão é 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="a5f42-461">The default value is 1.0f.</span></span> <span data-ttu-id="a5f42-462">Consulte [mosaico (Direct3D 9)](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="a5f42-462">See [Tessellation (Direct3D 9)](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-463"><span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS \_ ADAPTIVETESS \_ X**</span><span class="sxs-lookup"><span data-stu-id="a5f42-463"><span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS\_ADAPTIVETESS\_X**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-464">Valor para incluí de forma adaptativa, na direção x.</span><span class="sxs-lookup"><span data-stu-id="a5f42-464">Amount to adaptively tessellate, in the x direction.</span></span> <span data-ttu-id="a5f42-465">O valor padrão é 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="a5f42-465">Default value is 0.0f.</span></span> <span data-ttu-id="a5f42-466">Consulte [mosaico adaptável](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="a5f42-466">See [Adaptive Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-467"><span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS \_ ADAPTIVETESS \_ Y**</span><span class="sxs-lookup"><span data-stu-id="a5f42-467"><span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS\_ADAPTIVETESS\_Y**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-468">Valor para incluí de forma adaptativa, na direção y.</span><span class="sxs-lookup"><span data-stu-id="a5f42-468">Amount to adaptively tessellate, in the y direction.</span></span> <span data-ttu-id="a5f42-469">O valor padrão é 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="a5f42-469">Default value is 0.0f.</span></span> <span data-ttu-id="a5f42-470">Consulte [ \_ mosaico adaptável](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="a5f42-470">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-471"><span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS \_ ADAPTIVETESS \_ Z**</span><span class="sxs-lookup"><span data-stu-id="a5f42-471"><span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS\_ADAPTIVETESS\_Z**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-472">Valor para incluí de forma adaptativa, na direção z.</span><span class="sxs-lookup"><span data-stu-id="a5f42-472">Amount to adaptively tessellate, in the z direction.</span></span> <span data-ttu-id="a5f42-473">O valor padrão é 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="a5f42-473">Default value is 1.0f.</span></span> <span data-ttu-id="a5f42-474">Consulte [ \_ mosaico adaptável](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="a5f42-474">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-475"><span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS \_ ADAPTIVETESS \_ W**</span><span class="sxs-lookup"><span data-stu-id="a5f42-475"><span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS\_ADAPTIVETESS\_W**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-476">Valor para incluí de forma adaptativa, na direção w.</span><span class="sxs-lookup"><span data-stu-id="a5f42-476">Amount to adaptively tessellate, in the w direction.</span></span> <span data-ttu-id="a5f42-477">O valor padrão é 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="a5f42-477">Default value is 0.0f.</span></span> <span data-ttu-id="a5f42-478">Consulte [ \_ mosaico adaptável](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="a5f42-478">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-479"><span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS \_ ENABLEADAPTIVETESSELLATION**</span><span class="sxs-lookup"><span data-stu-id="a5f42-479"><span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS\_ENABLEADAPTIVETESSELLATION**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-480">**True** para habilitar o mosaico adaptável, **false** para desabilitá-lo.</span><span class="sxs-lookup"><span data-stu-id="a5f42-480">**TRUE** to enable adaptive tessellation, **FALSE** to disable it.</span></span> <span data-ttu-id="a5f42-481">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-481">The default value is **FALSE**.</span></span> <span data-ttu-id="a5f42-482">Consulte [ \_ mosaico adaptável](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="a5f42-482">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-483"><span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS \_ TWOSIDEDSTENCILMODE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-483"><span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS\_TWOSIDEDSTENCILMODE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-484">**Verdadeiro** habilita a estêncil em dois lados, **falso** desabilita-o.</span><span class="sxs-lookup"><span data-stu-id="a5f42-484">**TRUE** enables two-sided stenciling, **FALSE** disables it.</span></span> <span data-ttu-id="a5f42-485">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-485">The default value is **FALSE**.</span></span> <span data-ttu-id="a5f42-486">O aplicativo deve definir D3DRS \_ de seleção para D3DCULL \_ nenhum para habilitar o modo de estêncil em dois lados.</span><span class="sxs-lookup"><span data-stu-id="a5f42-486">The application should set D3DRS\_CULLMODE to D3DCULL\_NONE to enable two-sided stencil mode.</span></span> <span data-ttu-id="a5f42-487">Se a ordem de enrolamento de triângulo for no sentido horário, as \_ operações de estêncil D3DRS \* serão usadas.</span><span class="sxs-lookup"><span data-stu-id="a5f42-487">If the triangle winding order is clockwise, the D3DRS\_STENCIL\* operations will be used.</span></span> <span data-ttu-id="a5f42-488">Se a ordem do enrolamento for no sentido anti-horário, as \_ operações do estêncil CCW D3DRS \_ \* serão usadas.</span><span class="sxs-lookup"><span data-stu-id="a5f42-488">If the winding order is counterclockwise, the D3DRS\_CCW\_STENCIL\* operations will be used.</span></span>

<span data-ttu-id="a5f42-489">Para ver se há suporte para o estêncil de dois lados, verifique o membro StencilCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para D3DSTENCILCAPS \_ TWOSIDED.</span><span class="sxs-lookup"><span data-stu-id="a5f42-489">To see if two-sided stencil is supported, check the StencilCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) for D3DSTENCILCAPS\_TWOSIDED.</span></span> <span data-ttu-id="a5f42-490">Consulte também [D3DSTENCILCAPS](d3dstencilcaps.md).</span><span class="sxs-lookup"><span data-stu-id="a5f42-490">See also [D3DSTENCILCAPS](d3dstencilcaps.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-491"><span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**D3DRS \_ CCW \_ STENCILFAIL**</span><span class="sxs-lookup"><span data-stu-id="a5f42-491"><span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**D3DRS\_CCW\_STENCILFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-492">Operação de estêncil a ser executada se o teste de estêncil CCW falhar.</span><span class="sxs-lookup"><span data-stu-id="a5f42-492">Stencil operation to perform if CCW stencil test fails.</span></span> <span data-ttu-id="a5f42-493">Os valores são do tipo enumerado [**D3DSTENCILOP**](./d3dstencilop.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-493">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="a5f42-494">O valor padrão é D3DSTENCILOP \_ Keep.</span><span class="sxs-lookup"><span data-stu-id="a5f42-494">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-495"><span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**D3DRS \_ CCW \_ STENCILZFAIL**</span><span class="sxs-lookup"><span data-stu-id="a5f42-495"><span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**D3DRS\_CCW\_STENCILZFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-496">Operação de estêncil a ser executada se o teste de estêncil do CCW passar e o teste de z falhar.</span><span class="sxs-lookup"><span data-stu-id="a5f42-496">Stencil operation to perform if CCW stencil test passes and z-test fails.</span></span> <span data-ttu-id="a5f42-497">Os valores são do tipo enumerado [**D3DSTENCILOP**](./d3dstencilop.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-497">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="a5f42-498">O valor padrão é D3DSTENCILOP \_ Keep.</span><span class="sxs-lookup"><span data-stu-id="a5f42-498">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-499"><span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS \_ CCW \_ STENCILPASS**</span><span class="sxs-lookup"><span data-stu-id="a5f42-499"><span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS\_CCW\_STENCILPASS**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-500">Operação de estêncil a ser executada se os testes de estêncil do CCW e z forem aprovados.</span><span class="sxs-lookup"><span data-stu-id="a5f42-500">Stencil operation to perform if both CCW stencil and z-tests pass.</span></span> <span data-ttu-id="a5f42-501">Os valores são do tipo enumerado [**D3DSTENCILOP**](./d3dstencilop.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-501">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="a5f42-502">O valor padrão é D3DSTENCILOP \_ Keep.</span><span class="sxs-lookup"><span data-stu-id="a5f42-502">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-503"><span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS \_ CCW \_ STENCILFUNC**</span><span class="sxs-lookup"><span data-stu-id="a5f42-503"><span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS\_CCW\_STENCILFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-504">A função de comparação.</span><span class="sxs-lookup"><span data-stu-id="a5f42-504">The comparison function.</span></span> <span data-ttu-id="a5f42-505">O teste de estêncil do CCW passa se a função de estêncil ((ref & Mask) (estêncil & Mask)) é **verdadeira**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-505">CCW stencil test passes if ((ref & mask) stencil function (stencil & mask)) is **TRUE**.</span></span> <span data-ttu-id="a5f42-506">Os valores são do tipo enumerado [**D3DCMPFUNC**](./d3dcmpfunc.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-506">Values are from the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="a5f42-507">O valor padrão é D3DCMP \_ Always.</span><span class="sxs-lookup"><span data-stu-id="a5f42-507">The default value is D3DCMP\_ALWAYS.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-508"><span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS \_ COLORWRITEENABLE1**</span><span class="sxs-lookup"><span data-stu-id="a5f42-508"><span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS\_COLORWRITEENABLE1**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-509">Valores de ColorWriteEnable adicionais para os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a5f42-509">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="a5f42-510">Consulte D3DRS \_ COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="a5f42-510">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="a5f42-511">Essa funcionalidade estará disponível se o \_ bit D3DPMISCCAPS INDEPENDENTWRITEMASKS Capabilities estiver definido no membro PrimitiveMiscCaps da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5f42-511">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="a5f42-512">O valor padrão é 0x0000000f.</span><span class="sxs-lookup"><span data-stu-id="a5f42-512">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-513"><span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS \_ COLORWRITEENABLE2**</span><span class="sxs-lookup"><span data-stu-id="a5f42-513"><span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS\_COLORWRITEENABLE2**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-514">Valores de ColorWriteEnable adicionais para os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a5f42-514">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="a5f42-515">Consulte D3DRS \_ COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="a5f42-515">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="a5f42-516">Essa funcionalidade estará disponível se o \_ bit D3DPMISCCAPS INDEPENDENTWRITEMASKS Capabilities estiver definido no membro PrimitiveMiscCaps da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5f42-516">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="a5f42-517">O valor padrão é 0x0000000f.</span><span class="sxs-lookup"><span data-stu-id="a5f42-517">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-518"><span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS \_ COLORWRITEENABLE3**</span><span class="sxs-lookup"><span data-stu-id="a5f42-518"><span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS\_COLORWRITEENABLE3**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-519">Valores de ColorWriteEnable adicionais para os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a5f42-519">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="a5f42-520">Consulte D3DRS \_ COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="a5f42-520">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="a5f42-521">Essa funcionalidade estará disponível se o \_ bit D3DPMISCCAPS INDEPENDENTWRITEMASKS Capabilities estiver definido no membro PrimitiveMiscCaps da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5f42-521">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="a5f42-522">O valor padrão é 0x0000000f.</span><span class="sxs-lookup"><span data-stu-id="a5f42-522">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-523"><span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS \_ BLENDFACTOR**</span><span class="sxs-lookup"><span data-stu-id="a5f42-523"><span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS\_BLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-524">[**D3DCOLOR**](d3dcolor.md) usado para um fator de mistura constante durante a mistura alfa.</span><span class="sxs-lookup"><span data-stu-id="a5f42-524">[**D3DCOLOR**](d3dcolor.md) used for a constant blend-factor during alpha blending.</span></span> <span data-ttu-id="a5f42-525">Essa funcionalidade estará disponível se o \_ bit D3DPBLENDCAPS BLENDFACTOR Capabilities estiver definido no membro SrcBlendCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) ou o membro DestBlendCaps de **D3DCAPS9**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-525">This functionality is available if the D3DPBLENDCAPS\_BLENDFACTOR capabilities bit is set in the SrcBlendCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) or the DestBlendCaps member of **D3DCAPS9**.</span></span> <span data-ttu-id="a5f42-526">Consulte [**D3DRENDERSTATETYPE**]().</span><span class="sxs-lookup"><span data-stu-id="a5f42-526">See [**D3DRENDERSTATETYPE**]().</span></span> <span data-ttu-id="a5f42-527">O valor padrão é 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="a5f42-527">The default value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-528"><span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS \_ SRGBWRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-528"><span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS\_SRGBWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-529">Habilite gravações de destino de renderização para que a gama seja corrigida para sRGB.</span><span class="sxs-lookup"><span data-stu-id="a5f42-529">Enable render-target writes to be gamma corrected to sRGB.</span></span> <span data-ttu-id="a5f42-530">O formato deve expor D3DUSAGE \_ SRGBWRITE.</span><span class="sxs-lookup"><span data-stu-id="a5f42-530">The format must expose D3DUSAGE\_SRGBWRITE.</span></span> <span data-ttu-id="a5f42-531">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="a5f42-531">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-532"><span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS \_ DEPTHBIAS**</span><span class="sxs-lookup"><span data-stu-id="a5f42-532"><span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS\_DEPTHBIAS**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-533">Um valor de ponto flutuante que é usado para comparação de valores de profundidade.</span><span class="sxs-lookup"><span data-stu-id="a5f42-533">A floating-point value that is used for comparison of depth values.</span></span> <span data-ttu-id="a5f42-534">Consulte [tendência de profundidade (Direct3D 9)](depth-bias.md).</span><span class="sxs-lookup"><span data-stu-id="a5f42-534">See [Depth Bias (Direct3D 9)](depth-bias.md).</span></span> <span data-ttu-id="a5f42-535">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="a5f42-535">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-536"><span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**D3DRS \_ WRAP8**</span><span class="sxs-lookup"><span data-stu-id="a5f42-536"><span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**D3DRS\_WRAP8**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-537">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a5f42-537">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-538"><span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**D3DRS \_ WRAP9**</span><span class="sxs-lookup"><span data-stu-id="a5f42-538"><span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**D3DRS\_WRAP9**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-539">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a5f42-539">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-540"><span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**D3DRS \_ WRAP10**</span><span class="sxs-lookup"><span data-stu-id="a5f42-540"><span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**D3DRS\_WRAP10**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-541">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a5f42-541">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-542"><span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**D3DRS \_ WRAP11**</span><span class="sxs-lookup"><span data-stu-id="a5f42-542"><span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**D3DRS\_WRAP11**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-543">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a5f42-543">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-544"><span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**D3DRS \_ WRAP12**</span><span class="sxs-lookup"><span data-stu-id="a5f42-544"><span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**D3DRS\_WRAP12**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-545">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a5f42-545">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-546"><span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**D3DRS \_ WRAP13**</span><span class="sxs-lookup"><span data-stu-id="a5f42-546"><span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**D3DRS\_WRAP13**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-547">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a5f42-547">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-548"><span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**D3DRS \_ WRAP14**</span><span class="sxs-lookup"><span data-stu-id="a5f42-548"><span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**D3DRS\_WRAP14**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-549">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a5f42-549">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-550"><span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**D3DRS \_ WRAP15**</span><span class="sxs-lookup"><span data-stu-id="a5f42-550"><span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**D3DRS\_WRAP15**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-551">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a5f42-551">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-552"><span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS \_ SEPARATEALPHABLENDENABLE**</span><span class="sxs-lookup"><span data-stu-id="a5f42-552"><span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS\_SEPARATEALPHABLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-553">**True** habilita o modo de mesclagem separado para o canal alfa.</span><span class="sxs-lookup"><span data-stu-id="a5f42-553">**TRUE** enables the separate blend mode for the alpha channel.</span></span> <span data-ttu-id="a5f42-554">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-554">The default value is **FALSE**.</span></span>

<span data-ttu-id="a5f42-555">Quando definido como **false**, os fatores de mesclagem de destino de renderização e as operações aplicadas a Alfa são forçadas a serem as mesmas que as definidas para a cor.</span><span class="sxs-lookup"><span data-stu-id="a5f42-555">When set to **FALSE**, the render-target blending factors and operations applied to alpha are forced to be the same as those defined for color.</span></span> <span data-ttu-id="a5f42-556">Esse modo é efetivamente fisicamente ligado a **false** nas implementações que não definem a Cap D3DPMISCCAPS \_ SEPARATEALPHABLEND.</span><span class="sxs-lookup"><span data-stu-id="a5f42-556">This mode is effectively hardwired to **FALSE** on implementations that don't set the cap D3DPMISCCAPS\_SEPARATEALPHABLEND.</span></span> <span data-ttu-id="a5f42-557">Consulte [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="a5f42-557">See [D3DPMISCCAPS](d3dpmisccaps.md).</span></span>

<span data-ttu-id="a5f42-558">O tipo de mistura alfa separada é determinado pelos \_ Estados de RENDERIZAÇÃO D3DRS SRCBLENDALPHA e \_ D3DRS DESTBLENDALPHA.</span><span class="sxs-lookup"><span data-stu-id="a5f42-558">The type of separate alpha blending is determined by the D3DRS\_SRCBLENDALPHA and D3DRS\_DESTBLENDALPHA render states.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-559"><span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS \_ SRCBLENDALPHA**</span><span class="sxs-lookup"><span data-stu-id="a5f42-559"><span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS\_SRCBLENDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-560">Um membro do tipo enumerado [**D3DBLEND**](./d3dblend.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-560">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="a5f42-561">Esse valor é ignorado, a menos que D3DRS \_ SEPARATEALPHABLENDENABLE seja **true**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-561">This value is ignored unless D3DRS\_SEPARATEALPHABLENDENABLE is **TRUE**.</span></span> <span data-ttu-id="a5f42-562">O valor padrão é D3DBLEND \_ One.</span><span class="sxs-lookup"><span data-stu-id="a5f42-562">The default value is D3DBLEND\_ONE.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-563"><span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS \_ DESTBLENDALPHA**</span><span class="sxs-lookup"><span data-stu-id="a5f42-563"><span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS\_DESTBLENDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-564">Um membro do tipo enumerado [**D3DBLEND**](./d3dblend.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-564">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="a5f42-565">Esse valor é ignorado, a menos que D3DRS \_ SEPARATEALPHABLENDENABLE seja **true**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-565">This value is ignored unless D3DRS\_SEPARATEALPHABLENDENABLE is **TRUE**.</span></span> <span data-ttu-id="a5f42-566">O valor padrão é D3DBLEND \_ zero.</span><span class="sxs-lookup"><span data-stu-id="a5f42-566">The default value is D3DBLEND\_ZERO.</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-567"><span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS \_ BLENDOPALPHA**</span><span class="sxs-lookup"><span data-stu-id="a5f42-567"><span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS\_BLENDOPALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-568">O valor usado para selecionar a operação aritmética aplicada à mesclagem alfa separada quando o estado de renderização, D3DRS \_ SEPARATEALPHABLENDENABLE, é definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="a5f42-568">Value used to select the arithmetic operation applied to separate alpha blending when the render state, D3DRS\_SEPARATEALPHABLENDENABLE, is set to **TRUE**.</span></span>

<span data-ttu-id="a5f42-569">Os valores válidos são definidos pelo tipo enumerado [**D3DBLENDOP**](./d3dblendop.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f42-569">Valid values are defined by the [**D3DBLENDOP**](./d3dblendop.md) enumerated type.</span></span> <span data-ttu-id="a5f42-570">O valor padrão é D3DBLENDOP \_ Add.</span><span class="sxs-lookup"><span data-stu-id="a5f42-570">The default value is D3DBLENDOP\_ADD.</span></span>

<span data-ttu-id="a5f42-571">Se o \_ recurso de dispositivo D3DPMISCCAPS BLENDOP não tiver suporte, D3DBLENDOP \_ Adicionar será executado.</span><span class="sxs-lookup"><span data-stu-id="a5f42-571">If the D3DPMISCCAPS\_BLENDOP device capability is not supported, then D3DBLENDOP\_ADD is performed.</span></span> <span data-ttu-id="a5f42-572">Consulte [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="a5f42-572">See [D3DPMISCCAPS](d3dpmisccaps.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5f42-573"><span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a5f42-573"><span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="a5f42-574">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="a5f42-574">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="a5f42-575">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a5f42-575">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="a5f42-576">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="a5f42-576">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a5f42-577">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5f42-577">Remarks</span></span>



| <span data-ttu-id="a5f42-578">Processar Estados</span><span class="sxs-lookup"><span data-stu-id="a5f42-578">Render States</span></span>        |                    |
|----------------------|--------------------|
| <span data-ttu-id="a5f42-579">PS \_ 1 \_ 1 para PS \_ 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="a5f42-579">ps\_1\_1 to ps\_1\_3</span></span> | <span data-ttu-id="a5f42-580">4 amostragens de textura</span><span class="sxs-lookup"><span data-stu-id="a5f42-580">4 texture samplers</span></span> |



 

<span data-ttu-id="a5f42-581">O Direct3D define a \_ constante D3DRENDERSTATE WRAPBIAS como uma conveniência para que os aplicativos habilitem ou desabilitem o encapsulamento de textura, com base no inteiro baseado em zero de um conjunto de coordenadas de textura (em vez de usar explicitamente um dos \_ valores de estado n de D3DRS Wrap).</span><span class="sxs-lookup"><span data-stu-id="a5f42-581">Direct3D defines the D3DRENDERSTATE\_WRAPBIAS constant as a convenience for applications to enable or disable texture wrapping, based on the zero-based integer of a texture coordinate set (rather than explicitly using one of the D3DRS\_WRAP n state values).</span></span> <span data-ttu-id="a5f42-582">Adicione o \_ valor WRAPBIAS de D3DRENDERSTATE ao índice de base zero de uma coordenada de textura definida para calcular o \_ valor n do D3DRS Wrap que corresponde a esse índice, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5f42-582">Add the D3DRENDERSTATE\_WRAPBIAS value to the zero-based index of a texture coordinate set to calculate the D3DRS\_WRAP n value that corresponds to that index, as shown in the following example.</span></span>


```
// Enable U/V wrapping for textures that use the texture 
// coordinate set at the index within the dwIndex variable
    
HRESULT hr = pd3dDevice->SetRenderState(
dwIndex + D3DRENDERSTATE_WRAPBIAS,  
D3DWRAPCOORD_0 | D3DWRAPCOORD_1);
     
// If dwIndex is 3, the value that results from 
// the addition equals D3DRS_WRAP3 (131)
```



## <a name="requirements"></a><span data-ttu-id="a5f42-583">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5f42-583">Requirements</span></span>



| <span data-ttu-id="a5f42-584">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5f42-584">Requirement</span></span> | <span data-ttu-id="a5f42-585">Valor</span><span class="sxs-lookup"><span data-stu-id="a5f42-585">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5f42-586">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a5f42-586">Header</span></span><br/> | <dl> <span data-ttu-id="a5f42-587"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5f42-587"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5f42-588">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5f42-588">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5f42-589">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="a5f42-589">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="a5f42-590">**IDirect3DDevice9:: getrenderingstate**</span><span class="sxs-lookup"><span data-stu-id="a5f42-590">**IDirect3DDevice9::GetRenderState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrenderstate)
</dt> <dt>

[<span data-ttu-id="a5f42-591">**IDirect3DDevice9::SetRenderState**</span><span class="sxs-lookup"><span data-stu-id="a5f42-591">**IDirect3DDevice9::SetRenderState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)
</dt> </dl>

 

 
