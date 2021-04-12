---
description: Estados de estágio de textura definem operações de textura de vários misturadores.
ms.assetid: 87a5a1bb-e748-4c72-8320-ea82250dcc0e
title: Enumeração D3DTEXTURESTAGESTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURESTAGESTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0530f428c9ebf89607fa89509c65ddd336fee293
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172967"
---
# <a name="d3dtexturestagestatetype-enumeration"></a><span data-ttu-id="e0786-103">Enumeração D3DTEXTURESTAGESTATETYPE</span><span class="sxs-lookup"><span data-stu-id="e0786-103">D3DTEXTURESTAGESTATETYPE enumeration</span></span>

<span data-ttu-id="e0786-104">Estados de estágio de textura definem operações de textura de vários misturadores.</span><span class="sxs-lookup"><span data-stu-id="e0786-104">Texture stage states define multi-blender texture operations.</span></span> <span data-ttu-id="e0786-105">Alguns Estados de amostra configuram o processamento de vértice e alguns configuram o processamento de pixel.</span><span class="sxs-lookup"><span data-stu-id="e0786-105">Some sampler states set up vertex processing, and some set up pixel processing.</span></span> <span data-ttu-id="e0786-106">Os Estados de estágio de textura podem ser salvos e restaurados usando stateblocks (consulte [estado de salvamento e restauração de blocos de estado (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="e0786-106">Texture stage states can be saved and restored using stateblocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="e0786-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0786-107">Syntax</span></span>


```C++
typedef enum D3DTEXTURESTAGESTATETYPE { 
  D3DTSS_COLOROP                = 1,
  D3DTSS_COLORARG1              = 2,
  D3DTSS_COLORARG2              = 3,
  D3DTSS_ALPHAOP                = 4,
  D3DTSS_ALPHAARG1              = 5,
  D3DTSS_ALPHAARG2              = 6,
  D3DTSS_BUMPENVMAT00           = 7,
  D3DTSS_BUMPENVMAT01           = 8,
  D3DTSS_BUMPENVMAT10           = 9,
  D3DTSS_BUMPENVMAT11           = 10,
  D3DTSS_TEXCOORDINDEX          = 11,
  D3DTSS_BUMPENVLSCALE          = 22,
  D3DTSS_BUMPENVLOFFSET         = 23,
  D3DTSS_TEXTURETRANSFORMFLAGS  = 24,
  D3DTSS_COLORARG0              = 26,
  D3DTSS_ALPHAARG0              = 27,
  D3DTSS_RESULTARG              = 28,
  D3DTSS_CONSTANT               = 32,
  D3DTSS_FORCE_DWORD            = 0x7fffffff
} D3DTEXTURESTAGESTATETYPE, *LPD3DTEXTURESTAGESTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="e0786-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="e0786-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e0786-109"><span id="D3DTSS_COLOROP"></span><span id="d3dtss_colorop"></span>**D3DTSS \_ COLOROP**</span><span class="sxs-lookup"><span data-stu-id="e0786-109"><span id="D3DTSS_COLOROP"></span><span id="d3dtss_colorop"></span>**D3DTSS\_COLOROP**</span></span>
</dt> <dd>

<span data-ttu-id="e0786-110">O estado de estágio de textura é uma operação de mesclagem de cor de textura identificada por um membro do tipo enumerado [**D3DTEXTUREOP**](./d3dtextureop.md) .</span><span class="sxs-lookup"><span data-stu-id="e0786-110">Texture-stage state is a texture color blending operation identified by one member of the [**D3DTEXTUREOP**](./d3dtextureop.md) enumerated type.</span></span> <span data-ttu-id="e0786-111">O valor padrão para o primeiro estágio de textura (estágio 0) é D3DTOP \_ modular; para todos os outros estágios, o padrão é D3DTOP \_ Disable.</span><span class="sxs-lookup"><span data-stu-id="e0786-111">The default value for the first texture stage (stage 0) is D3DTOP\_MODULATE; for all other stages the default is D3DTOP\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="e0786-112"><span id="D3DTSS_COLORARG1"></span><span id="d3dtss_colorarg1"></span>**D3DTSS \_ COLORARG1**</span><span class="sxs-lookup"><span data-stu-id="e0786-112"><span id="D3DTSS_COLORARG1"></span><span id="d3dtss_colorarg1"></span>**D3DTSS\_COLORARG1**</span></span>
</dt> <dd>

<span data-ttu-id="e0786-113">O estado de estágio de textura é o primeiro argumento de cor para o estágio, identificado por um dos [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="e0786-113">Texture-stage state is the first color argument for the stage, identified by one of the [D3DTA](d3dta.md).</span></span> <span data-ttu-id="e0786-114">O argumento padrão é D3DTA \_ Texture.</span><span class="sxs-lookup"><span data-stu-id="e0786-114">The default argument is D3DTA\_TEXTURE.</span></span>

<span data-ttu-id="e0786-115">Especifique D3DTA \_ Temp para selecionar uma cor de registro temporária para leitura ou gravação.</span><span class="sxs-lookup"><span data-stu-id="e0786-115">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="e0786-116">\_O D3DTA Temp terá suporte se a \_ funcionalidade do dispositivo D3DPMISCCAPS TSSARGTEMP estiver presente.</span><span class="sxs-lookup"><span data-stu-id="e0786-116">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="e0786-117">O valor padrão para o registro é (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="e0786-117">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="e0786-118"><span id="D3DTSS_COLORARG2"></span><span id="d3dtss_colorarg2"></span>**D3DTSS \_ COLORARG2**</span><span class="sxs-lookup"><span data-stu-id="e0786-118"><span id="D3DTSS_COLORARG2"></span><span id="d3dtss_colorarg2"></span>**D3DTSS\_COLORARG2**</span></span>
</dt> <dd>

<span data-ttu-id="e0786-119">O estado de estágio de textura é o segundo argumento de cor para o estágio, identificado por [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="e0786-119">Texture-stage state is the second color argument for the stage, identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="e0786-120">O argumento padrão é D3DTA \_ Current.</span><span class="sxs-lookup"><span data-stu-id="e0786-120">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="e0786-121">Especifique D3DTA \_ Temp para selecionar uma cor de registro temporária para leitura ou gravação.</span><span class="sxs-lookup"><span data-stu-id="e0786-121">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="e0786-122">\_O D3DTA Temp terá suporte se a \_ funcionalidade do dispositivo D3DPMISCCAPS TSSARGTEMP estiver presente.</span><span class="sxs-lookup"><span data-stu-id="e0786-122">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="e0786-123">O valor padrão para o registro é (0,0, 0,0, 0,0, 0,0)</span><span class="sxs-lookup"><span data-stu-id="e0786-123">The default value for the register is (0.0, 0.0, 0.0, 0.0)</span></span>

</dd> <dt>

<span data-ttu-id="e0786-124"><span id="D3DTSS_ALPHAOP"></span><span id="d3dtss_alphaop"></span>**D3DTSS \_ ALPHAOP**</span><span class="sxs-lookup"><span data-stu-id="e0786-124"><span id="D3DTSS_ALPHAOP"></span><span id="d3dtss_alphaop"></span>**D3DTSS\_ALPHAOP**</span></span>
</dt> <dd>

<span data-ttu-id="e0786-125">O estado de estágio de textura é uma operação de mesclagem alfa de textura identificada por um membro do tipo enumerado [**D3DTEXTUREOP**](./d3dtextureop.md) .</span><span class="sxs-lookup"><span data-stu-id="e0786-125">Texture-stage state is a texture alpha blending operation identified by one member of the [**D3DTEXTUREOP**](./d3dtextureop.md) enumerated type.</span></span> <span data-ttu-id="e0786-126">O valor padrão para o primeiro estágio de textura (estágio 0) é D3DTOP \_ SELECTARG1 e, para todos os outros estágios, o padrão é D3DTOP \_ Disable.</span><span class="sxs-lookup"><span data-stu-id="e0786-126">The default value for the first texture stage (stage 0) is D3DTOP\_SELECTARG1, and for all other stages the default is D3DTOP\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="e0786-127"><span id="D3DTSS_ALPHAARG1"></span><span id="d3dtss_alphaarg1"></span>**D3DTSS \_ ALPHAARG1**</span><span class="sxs-lookup"><span data-stu-id="e0786-127"><span id="D3DTSS_ALPHAARG1"></span><span id="d3dtss_alphaarg1"></span>**D3DTSS\_ALPHAARG1**</span></span>
</dt> <dd>

<span data-ttu-id="e0786-128">O estado de estágio de textura é o primeiro argumento alfa para o estágio, identificado por [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="e0786-128">Texture-stage state is the first alpha argument for the stage, identified by by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="e0786-129">O argumento padrão é D3DTA \_ Texture.</span><span class="sxs-lookup"><span data-stu-id="e0786-129">The default argument is D3DTA\_TEXTURE.</span></span> <span data-ttu-id="e0786-130">Se nenhuma textura for definida para esse estágio, o argumento padrão será D3DTA \_ difuso.</span><span class="sxs-lookup"><span data-stu-id="e0786-130">If no texture is set for this stage, the default argument is D3DTA\_DIFFUSE.</span></span> <span data-ttu-id="e0786-131">Especifique D3DTA \_ Temp para selecionar uma cor de registro temporária para leitura ou gravação.</span><span class="sxs-lookup"><span data-stu-id="e0786-131">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="e0786-132">\_O D3DTA Temp terá suporte se a \_ funcionalidade do dispositivo D3DPMISCCAPS TSSARGTEMP estiver presente.</span><span class="sxs-lookup"><span data-stu-id="e0786-132">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="e0786-133">O valor padrão para o registro é (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="e0786-133">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="e0786-134"><span id="D3DTSS_ALPHAARG2"></span><span id="d3dtss_alphaarg2"></span>**D3DTSS \_ ALPHAARG2**</span><span class="sxs-lookup"><span data-stu-id="e0786-134"><span id="D3DTSS_ALPHAARG2"></span><span id="d3dtss_alphaarg2"></span>**D3DTSS\_ALPHAARG2**</span></span>
</dt> <dd>

<span data-ttu-id="e0786-135">O estado de estágio de textura é o segundo argumento alfa para o estágio, identificado por [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="e0786-135">Texture-stage state is the second alpha argument for the stage, identified by by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="e0786-136">O argumento padrão é D3DTA \_ Current.</span><span class="sxs-lookup"><span data-stu-id="e0786-136">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="e0786-137">Especifique D3DTA \_ Temp para selecionar uma cor de registro temporária para leitura ou gravação.</span><span class="sxs-lookup"><span data-stu-id="e0786-137">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="e0786-138">\_O D3DTA Temp terá suporte se a \_ funcionalidade do dispositivo D3DPMISCCAPS TSSARGTEMP estiver presente.</span><span class="sxs-lookup"><span data-stu-id="e0786-138">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="e0786-139">O valor padrão para o registro é (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="e0786-139">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="e0786-140"><span id="D3DTSS_BUMPENVMAT00"></span><span id="d3dtss_bumpenvmat00"></span>**D3DTSS \_ BUMPENVMAT00**</span><span class="sxs-lookup"><span data-stu-id="e0786-140"><span id="D3DTSS_BUMPENVMAT00"></span><span id="d3dtss_bumpenvmat00"></span>**D3DTSS\_BUMPENVMAT00**</span></span>
</dt> <dd>

<span data-ttu-id="e0786-141">O estado de estágio de textura é um valor de ponto flutuante para o \[ coeficiente de 0 \] \[ 0 \] em uma matriz de mapeamento de relevo.</span><span class="sxs-lookup"><span data-stu-id="e0786-141">Texture-stage state is a floating-point value for the \[0\]\[0\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="e0786-142">O valor padrão é 0,0.</span><span class="sxs-lookup"><span data-stu-id="e0786-142">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="e0786-143"><span id="D3DTSS_BUMPENVMAT01"></span><span id="d3dtss_bumpenvmat01"></span>**D3DTSS \_ BUMPENVMAT01**</span><span class="sxs-lookup"><span data-stu-id="e0786-143"><span id="D3DTSS_BUMPENVMAT01"></span><span id="d3dtss_bumpenvmat01"></span>**D3DTSS\_BUMPENVMAT01**</span></span>
</dt> <dd>

<span data-ttu-id="e0786-144">O estado de estágio de textura é um valor de ponto flutuante para o \[ coeficiente de 0 \] \[ 1 \] em uma matriz de mapeamento de relevo.</span><span class="sxs-lookup"><span data-stu-id="e0786-144">Texture-stage state is a floating-point value for the \[0\]\[1\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="e0786-145">O valor padrão é 0,0.</span><span class="sxs-lookup"><span data-stu-id="e0786-145">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="e0786-146"><span id="D3DTSS_BUMPENVMAT10"></span><span id="d3dtss_bumpenvmat10"></span>**D3DTSS \_ BUMPENVMAT10**</span><span class="sxs-lookup"><span data-stu-id="e0786-146"><span id="D3DTSS_BUMPENVMAT10"></span><span id="d3dtss_bumpenvmat10"></span>**D3DTSS\_BUMPENVMAT10**</span></span>
</dt> <dd>

<span data-ttu-id="e0786-147">O estado de estágio de textura é um valor de ponto flutuante para o \[ coeficiente de 1 \] \[ 0 \] em uma matriz de mapeamento de relevo.</span><span class="sxs-lookup"><span data-stu-id="e0786-147">Texture-stage state is a floating-point value for the \[1\]\[0\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="e0786-148">O valor padrão é 0,0.</span><span class="sxs-lookup"><span data-stu-id="e0786-148">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="e0786-149"><span id="D3DTSS_BUMPENVMAT11"></span><span id="d3dtss_bumpenvmat11"></span>**D3DTSS \_ BUMPENVMAT11**</span><span class="sxs-lookup"><span data-stu-id="e0786-149"><span id="D3DTSS_BUMPENVMAT11"></span><span id="d3dtss_bumpenvmat11"></span>**D3DTSS\_BUMPENVMAT11**</span></span>
</dt> <dd>

<span data-ttu-id="e0786-150">O estado de estágio de textura é um valor de ponto flutuante para o \[ \] \[ coeficiente 1 1 \] em uma matriz de mapeamento de relevo.</span><span class="sxs-lookup"><span data-stu-id="e0786-150">Texture-stage state is a floating-point value for the \[1\]\[1\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="e0786-151">O valor padrão é 0,0.</span><span class="sxs-lookup"><span data-stu-id="e0786-151">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="e0786-152"><span id="D3DTSS_TEXCOORDINDEX"></span><span id="d3dtss_texcoordindex"></span>**D3DTSS \_ TEXCOORDINDEX**</span><span class="sxs-lookup"><span data-stu-id="e0786-152"><span id="D3DTSS_TEXCOORDINDEX"></span><span id="d3dtss_texcoordindex"></span>**D3DTSS\_TEXCOORDINDEX**</span></span>
</dt> <dd>

<span data-ttu-id="e0786-153">Índice do conjunto de coordenadas de textura a ser usado com este estágio de textura.</span><span class="sxs-lookup"><span data-stu-id="e0786-153">Index of the texture coordinate set to use with this texture stage.</span></span> <span data-ttu-id="e0786-154">Você pode especificar até oito conjuntos de coordenadas de textura por vértice.</span><span class="sxs-lookup"><span data-stu-id="e0786-154">You can specify up to eight sets of texture coordinates per vertex.</span></span> <span data-ttu-id="e0786-155">Se um vértice não incluir um conjunto de coordenadas de textura no índice especificado, o sistema usa como padrão as coordenadas você e v (0, 0).</span><span class="sxs-lookup"><span data-stu-id="e0786-155">If a vertex does not include a set of texture coordinates at the specified index, the system defaults to the u and v coordinates (0,0).</span></span>

<span data-ttu-id="e0786-156">Ao renderizar usando sombreadores de vértice, o índice de coordenadas de textura de cada estágio deve ser definido como seu valor padrão.</span><span class="sxs-lookup"><span data-stu-id="e0786-156">When rendering using vertex shaders, each stage's texture coordinate index must be set to its default value.</span></span> <span data-ttu-id="e0786-157">O índice padrão para cada estágio é igual ao índice de estágio.</span><span class="sxs-lookup"><span data-stu-id="e0786-157">The default index for each stage is equal to the stage index.</span></span> <span data-ttu-id="e0786-158">Defina esse estado como o índice de base zero do conjunto de coordenadas para cada vértice usado por esse estágio de textura.</span><span class="sxs-lookup"><span data-stu-id="e0786-158">Set this state to the zero-based index of the coordinate set for each vertex that this texture stage uses.</span></span>

<span data-ttu-id="e0786-159">Além disso, os aplicativos podem incluir, como lógico ou com o índice que está sendo definido, uma das constantes para solicitar que o Direct3D gere automaticamente as coordenadas de textura de entrada para uma transformação de textura.</span><span class="sxs-lookup"><span data-stu-id="e0786-159">Additionally, applications can include, as logical OR with the index being set, one of the constants to request that Direct3D automatically generate the input texture coordinates for a texture transformation.</span></span> <span data-ttu-id="e0786-160">Para obter uma lista de todas as constantes, consulte [D3DTSS \_ TCI](d3dtss-tci.md).</span><span class="sxs-lookup"><span data-stu-id="e0786-160">For a list of all the constants, see [D3DTSS\_TCI](d3dtss-tci.md).</span></span>

<span data-ttu-id="e0786-161">Com exceção de D3DTSS \_ TCI \_ PassThru, que é resolvida como zero, se qualquer um dos valores a seguir estiver incluído no índice que está sendo definido, o sistema usará o índice estritamente para determinar o modo de disposição da textura.</span><span class="sxs-lookup"><span data-stu-id="e0786-161">With the exception of D3DTSS\_TCI\_PASSTHRU, which resolves to zero, if any of the following values is included with the index being set, the system uses the index strictly to determine texture wrapping mode.</span></span> <span data-ttu-id="e0786-162">Esses sinalizadores são mais úteis ao executar o mapeamento de ambiente.</span><span class="sxs-lookup"><span data-stu-id="e0786-162">These flags are most useful when performing environment mapping.</span></span>

</dd> <dt>

<span data-ttu-id="e0786-163"><span id="D3DTSS_BUMPENVLSCALE"></span><span id="d3dtss_bumpenvlscale"></span>**D3DTSS \_ BUMPENVLSCALE**</span><span class="sxs-lookup"><span data-stu-id="e0786-163"><span id="D3DTSS_BUMPENVLSCALE"></span><span id="d3dtss_bumpenvlscale"></span>**D3DTSS\_BUMPENVLSCALE**</span></span>
</dt> <dd>

<span data-ttu-id="e0786-164">Valor de escala de ponto flutuante para luminância de mapa de relevo.</span><span class="sxs-lookup"><span data-stu-id="e0786-164">Floating-point scale value for bump-map luminance.</span></span> <span data-ttu-id="e0786-165">O valor padrão é 0,0.</span><span class="sxs-lookup"><span data-stu-id="e0786-165">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="e0786-166"><span id="D3DTSS_BUMPENVLOFFSET"></span><span id="d3dtss_bumpenvloffset"></span>**D3DTSS \_ BUMPENVLOFFSET**</span><span class="sxs-lookup"><span data-stu-id="e0786-166"><span id="D3DTSS_BUMPENVLOFFSET"></span><span id="d3dtss_bumpenvloffset"></span>**D3DTSS\_BUMPENVLOFFSET**</span></span>
</dt> <dd>

<span data-ttu-id="e0786-167">Valor de deslocamento de ponto flutuante para luminância de mapa de relevo.</span><span class="sxs-lookup"><span data-stu-id="e0786-167">Floating-point offset value for bump-map luminance.</span></span> <span data-ttu-id="e0786-168">O valor padrão é 0,0.</span><span class="sxs-lookup"><span data-stu-id="e0786-168">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="e0786-169"><span id="D3DTSS_TEXTURETRANSFORMFLAGS"></span><span id="d3dtss_texturetransformflags"></span>**D3DTSS \_ TEXTURETRANSFORMFLAGS**</span><span class="sxs-lookup"><span data-stu-id="e0786-169"><span id="D3DTSS_TEXTURETRANSFORMFLAGS"></span><span id="d3dtss_texturetransformflags"></span>**D3DTSS\_TEXTURETRANSFORMFLAGS**</span></span>
</dt> <dd>

<span data-ttu-id="e0786-170">Membro do tipo enumerado [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) que controla a transformação de coordenadas de textura para este estágio de textura.</span><span class="sxs-lookup"><span data-stu-id="e0786-170">Member of the [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) enumerated type that controls the transformation of texture coordinates for this texture stage.</span></span> <span data-ttu-id="e0786-171">O valor padrão é D3DTTFF \_ Disable.</span><span class="sxs-lookup"><span data-stu-id="e0786-171">The default value is D3DTTFF\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="e0786-172"><span id="D3DTSS_COLORARG0"></span><span id="d3dtss_colorarg0"></span>**D3DTSS \_ COLORARG0**</span><span class="sxs-lookup"><span data-stu-id="e0786-172"><span id="D3DTSS_COLORARG0"></span><span id="d3dtss_colorarg0"></span>**D3DTSS\_COLORARG0**</span></span>
</dt> <dd>

<span data-ttu-id="e0786-173">Configurações para o terceiro operando de cor para operações triadic (multiplicar, adicionar e interpolar linearmente), identificados por [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="e0786-173">Settings for the third color operand for triadic operations (multiply, add, and linearly interpolate), identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="e0786-174">Essa configuração terá suporte se os \_ recursos do dispositivo D3DTEXOPCAPS MULTIPLYADD ou D3DTEXOPCAPS \_ LERP estiverem presentes.</span><span class="sxs-lookup"><span data-stu-id="e0786-174">This setting is supported if the D3DTEXOPCAPS\_MULTIPLYADD or D3DTEXOPCAPS\_LERP device capabilities are present.</span></span> <span data-ttu-id="e0786-175">O argumento padrão é D3DTA \_ Current.</span><span class="sxs-lookup"><span data-stu-id="e0786-175">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="e0786-176">Especifique D3DTA \_ Temp para selecionar uma cor de registro temporária para leitura ou gravação.</span><span class="sxs-lookup"><span data-stu-id="e0786-176">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="e0786-177">\_O D3DTA Temp terá suporte se a \_ funcionalidade do dispositivo D3DPMISCCAPS TSSARGTEMP estiver presente.</span><span class="sxs-lookup"><span data-stu-id="e0786-177">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="e0786-178">O valor padrão para o registro é (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="e0786-178">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="e0786-179"><span id="D3DTSS_ALPHAARG0"></span><span id="d3dtss_alphaarg0"></span>**D3DTSS \_ ALPHAARG0**</span><span class="sxs-lookup"><span data-stu-id="e0786-179"><span id="D3DTSS_ALPHAARG0"></span><span id="d3dtss_alphaarg0"></span>**D3DTSS\_ALPHAARG0**</span></span>
</dt> <dd>

<span data-ttu-id="e0786-180">Configurações para o operando do seletor de canal alfa para operações triadic (multiplicar, adicionar e interpolar linearmente), identificados por [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="e0786-180">Settings for the alpha channel selector operand for triadic operations (multiply, add, and linearly interpolate), identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="e0786-181">Essa configuração terá suporte se os \_ recursos do dispositivo D3DTEXOPCAPS MULTIPLYADD ou D3DTEXOPCAPS \_ LERP estiverem presentes.</span><span class="sxs-lookup"><span data-stu-id="e0786-181">This setting is supported if the D3DTEXOPCAPS\_MULTIPLYADD or D3DTEXOPCAPS\_LERP device capabilities are present.</span></span> <span data-ttu-id="e0786-182">O argumento padrão é D3DTA \_ Current.</span><span class="sxs-lookup"><span data-stu-id="e0786-182">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="e0786-183">Especifique D3DTA \_ Temp para selecionar uma cor de registro temporária para leitura ou gravação.</span><span class="sxs-lookup"><span data-stu-id="e0786-183">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="e0786-184">\_O D3DTA Temp terá suporte se a \_ funcionalidade do dispositivo D3DPMISCCAPS TSSARGTEMP estiver presente.</span><span class="sxs-lookup"><span data-stu-id="e0786-184">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="e0786-185">O argumento padrão é (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="e0786-185">The default argument is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="e0786-186"><span id="D3DTSS_RESULTARG"></span><span id="d3dtss_resultarg"></span>**D3DTSS \_ RESULTARG**</span><span class="sxs-lookup"><span data-stu-id="e0786-186"><span id="D3DTSS_RESULTARG"></span><span id="d3dtss_resultarg"></span>**D3DTSS\_RESULTARG**</span></span>
</dt> <dd>

<span data-ttu-id="e0786-187">Configuração para selecionar registro de destino para o resultado deste estágio, identificado por [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="e0786-187">Setting to select destination register for the result of this stage, identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="e0786-188">Esse valor pode ser definido como D3DTA \_ Current (o valor padrão) ou D3DTA \_ temp, que é um único registro temporário que pode ser lido em estágios subsequentes como um argumento de entrada.</span><span class="sxs-lookup"><span data-stu-id="e0786-188">This value can be set to D3DTA\_CURRENT (the default value) or to D3DTA\_TEMP, which is a single temporary register that can be read into subsequent stages as an input argument.</span></span> <span data-ttu-id="e0786-189">A cor final passada para o misturador de neblina e o buffer de quadro é retirada do D3DTA \_ atual, portanto, o último estado de estágio de textura ativo deve ser definido como gravar no atual.</span><span class="sxs-lookup"><span data-stu-id="e0786-189">The final color passed to the fog blender and frame buffer is taken from D3DTA\_CURRENT, so the last active texture stage state must be set to write to current.</span></span> <span data-ttu-id="e0786-190">Essa configuração terá suporte se a \_ funcionalidade de dispositivo D3DPMISCCAPS TSSARGTEMP estiver presente.</span><span class="sxs-lookup"><span data-stu-id="e0786-190">This setting is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span>

</dd> <dt>

<span data-ttu-id="e0786-191"><span id="D3DTSS_CONSTANT"></span><span id="d3dtss_constant"></span>**\_Constante D3DTSS**</span><span class="sxs-lookup"><span data-stu-id="e0786-191"><span id="D3DTSS_CONSTANT"></span><span id="d3dtss_constant"></span>**D3DTSS\_CONSTANT**</span></span>
</dt> <dd>

<span data-ttu-id="e0786-192">Cor constante por estágio.</span><span class="sxs-lookup"><span data-stu-id="e0786-192">Per-stage constant color.</span></span> <span data-ttu-id="e0786-193">Para ver se um dispositivo dá suporte a uma cor constante por estágio, consulte a \_ constante D3DPMISCCAPS PERSTAGECONSTANT em [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="e0786-193">To see if a device supports a per-stage constant color, see the D3DPMISCCAPS\_PERSTAGECONSTANT constant in [D3DPMISCCAPS](d3dpmisccaps.md).</span></span> <span data-ttu-id="e0786-194">\_A constante D3DTSS é usada pela \_ constante D3DTA.</span><span class="sxs-lookup"><span data-stu-id="e0786-194">D3DTSS\_CONSTANT is used by D3DTA\_CONSTANT.</span></span> <span data-ttu-id="e0786-195">Consulte [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="e0786-195">See [D3DTA](d3dta.md).</span></span>

</dd> <dt>

<span data-ttu-id="e0786-196"><span id="D3DTSS_FORCE_DWORD"></span><span id="d3dtss_force_dword"></span>**D3DTSS \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e0786-196"><span id="D3DTSS_FORCE_DWORD"></span><span id="d3dtss_force_dword"></span>**D3DTSS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="e0786-197">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="e0786-197">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="e0786-198">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e0786-198">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="e0786-199">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="e0786-199">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0786-200">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0786-200">Remarks</span></span>

<span data-ttu-id="e0786-201">Os membros desse tipo enumerado são usados com os métodos [**IDirect3DDevice9:: GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) e [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) para recuperar e definir valores de estado de textura.</span><span class="sxs-lookup"><span data-stu-id="e0786-201">Members of this enumerated type are used with the [**IDirect3DDevice9::GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) and [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) methods to retrieve and set texture state values.</span></span>

<span data-ttu-id="e0786-202">O intervalo válido de valores para os \_ coeficientes de matriz D3DTSS BUMPENVMAT00, D3DTSS \_ BUMPENVMAT01, D3DTSS \_ BUMPENVMAT10 e D3DTSS \_ BUMPENVMAT11 tapa-Mapping é maior ou igual a-8,0 e menor que 8,0.</span><span class="sxs-lookup"><span data-stu-id="e0786-202">The valid range of values for the D3DTSS\_BUMPENVMAT00, D3DTSS\_BUMPENVMAT01, D3DTSS\_BUMPENVMAT10, and D3DTSS\_BUMPENVMAT11 bump-mapping matrix coefficients is greater than or equal to -8.0 and less than 8.0.</span></span> <span data-ttu-id="e0786-203">Esse intervalo, expresso em notação matemática, é (-8.0, 8.0).</span><span class="sxs-lookup"><span data-stu-id="e0786-203">This range, expressed in mathematical notation is (-8.0,8.0).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0786-204">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0786-204">Requirements</span></span>



| <span data-ttu-id="e0786-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0786-205">Requirement</span></span> | <span data-ttu-id="e0786-206">Valor</span><span class="sxs-lookup"><span data-stu-id="e0786-206">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0786-207">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e0786-207">Header</span></span><br/> | <dl> <span data-ttu-id="e0786-208"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0786-208"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0786-209">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0786-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0786-210">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="e0786-210">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="e0786-211">**IDirect3DDevice9::GetTextureStageState**</span><span class="sxs-lookup"><span data-stu-id="e0786-211">**IDirect3DDevice9::GetTextureStageState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate)
</dt> <dt>

[<span data-ttu-id="e0786-212">**IDirect3DDevice9::SetTextureStageState**</span><span class="sxs-lookup"><span data-stu-id="e0786-212">**IDirect3DDevice9::SetTextureStageState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)
</dt> </dl>

 

 
