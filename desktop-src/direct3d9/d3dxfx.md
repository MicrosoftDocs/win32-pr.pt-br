---
description: Opções para salvar e criar efeitos.
ms.assetid: df24a132-665e-4eb7-992b-d7a6144257f5
title: D3DXFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9077c8c7e3da479dd8963484bc289b84093ac0
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995073"
---
# <a name="d3dxfx"></a><span data-ttu-id="b96b7-103">D3DXFX</span><span class="sxs-lookup"><span data-stu-id="b96b7-103">D3DXFX</span></span>

<span data-ttu-id="b96b7-104">Opções para salvar e criar efeitos.</span><span class="sxs-lookup"><span data-stu-id="b96b7-104">Options for saving and creating effects.</span></span>

<span data-ttu-id="b96b7-105">As constantes na tabela a seguir são definidas em d3dx9effect. h.</span><span class="sxs-lookup"><span data-stu-id="b96b7-105">The constants in the following table are defined in d3dx9effect.h.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b96b7-106">Sinalizadores de salvamento e restauração de estado do efeito</span><span class="sxs-lookup"><span data-stu-id="b96b7-106">Effect State Save and Restore Flags</span></span></td>
<td><span data-ttu-id="b96b7-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b96b7-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b96b7-108">D3DXFX_DONOTSAVESTATE</span><span class="sxs-lookup"><span data-stu-id="b96b7-108">D3DXFX_DONOTSAVESTATE</span></span></td>
<td><span data-ttu-id="b96b7-109">Nenhum estado é salvo ao chamar <a href="id3dxeffect--begin.md"><strong>begin</strong></a> ou restaurado ao chamar <a href="id3dxeffect--end.md"><strong>end</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b96b7-109">No state is saved when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> or restored when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b96b7-110">D3DXFX_DONOTSAVESAMPLERSTATE</span><span class="sxs-lookup"><span data-stu-id="b96b7-110">D3DXFX_DONOTSAVESAMPLERSTATE</span></span></td>
<td><span data-ttu-id="b96b7-111">Um stateblock salva o estado ao chamar <a href="id3dxeffect--begin.md"><strong>begin</strong></a> e restaura o estado ao chamar <a href="id3dxeffect--end.md"><strong>end</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b96b7-111">A stateblock saves state when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> and restores state when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b96b7-112">D3DXFX_DONOTSAVESHADERSTATE</span><span class="sxs-lookup"><span data-stu-id="b96b7-112">D3DXFX_DONOTSAVESHADERSTATE</span></span></td>
<td><span data-ttu-id="b96b7-113">Um stateblock salva o estado (exceto sombreadores e constantes de sombreador) ao chamar <a href="id3dxeffect--begin.md"><strong>begin</strong></a> e restaura o estado ao chamar <a href="id3dxeffect--end.md"><strong>end</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b96b7-113">A stateblock saves state (except shaders and shader constants) when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> and restores state when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b96b7-114">Sinalizadores de criação de efeito</span><span class="sxs-lookup"><span data-stu-id="b96b7-114">Effect Creation Flags</span></span></td>
<td><span data-ttu-id="b96b7-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="b96b7-115">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b96b7-116">D3DXFX_NOT_CLONEABLE</span><span class="sxs-lookup"><span data-stu-id="b96b7-116">D3DXFX_NOT_CLONEABLE</span></span></td>
<td><span data-ttu-id="b96b7-117">O efeito será não clonável e não conterá dados binários de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b96b7-117">The effect will be non-cloneable and will not contain any shader binary data.</span></span> <span data-ttu-id="b96b7-118"><a href="id3dxbaseeffect--getpassdesc.md"><strong>GetPassDesc</strong></a> não retornará ponteiros de função de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b96b7-118"><a href="id3dxbaseeffect--getpassdesc.md"><strong>GetPassDesc</strong></a> will not return shader function pointers.</span></span> <span data-ttu-id="b96b7-119">Definir esse sinalizador reduz o uso de memória de efeito em cerca de 50%, pois elimina a necessidade do sistema de efeito manter uma cópia dos sombreadores na memória.</span><span class="sxs-lookup"><span data-stu-id="b96b7-119">Setting this flag reduces effect memory usage by about 50% because it eliminates the need for the effect system to keep a copy of the shaders in memory.</span></span> <span data-ttu-id="b96b7-120">Esse sinalizador é usado por <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect</strong></a>, <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>e <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b96b7-120">This flag is used by <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect</strong></a>, <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>, and <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b96b7-121">D3DXFX_LARGEADDRESSAWARE</span><span class="sxs-lookup"><span data-stu-id="b96b7-121">D3DXFX_LARGEADDRESSAWARE</span></span></td>
<td><span data-ttu-id="b96b7-122">Habilita a alocação de um recurso de efeito no espaço de endereço uppder de um computador.</span><span class="sxs-lookup"><span data-stu-id="b96b7-122">Enables the allocation of an effect resource into the uppder address space of a machine.</span></span> <span data-ttu-id="b96b7-123">Uma limitação importante é que você não pode usar cadeias de caracteres e identificadores de forma intercambiável.</span><span class="sxs-lookup"><span data-stu-id="b96b7-123">One important limitation is that you cannot use strings and handles interchangeably.</span></span> <span data-ttu-id="b96b7-124">Por exemplo, o seguinte não funcionaria mais.</span><span class="sxs-lookup"><span data-stu-id="b96b7-124">For example, the following would no longer work.</span></span> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>g_pEffect->SetMatrix( &quot;g_mWorldViewProjection&quot;, &mWorldViewProjection );</code></pre></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b96b7-125">Em vez disso, um método como [<strong>GetParameterByName</strong>](id3dxbaseeffect--getparameterbyname.md) deve ser usado para armazenar o identificador do parâmetro, que é então usado para passar variáveis para o efeito.</span><span class="sxs-lookup"><span data-stu-id="b96b7-125">Instead, a method such as [<strong>GetParameterByName</strong>](id3dxbaseeffect--getparameterbyname.md) must be used to store the handle of the parameter, which is then used to pass variables to the effect.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b96b7-126">As constantes na tabela a seguir não são definidas por padrão e devem ser definidas pelo desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="b96b7-126">The constants in the following table are not defined by default and must be defined by the developer.</span></span>



| <span data-ttu-id="b96b7-127">Vigorar \# definição do pré-processador</span><span class="sxs-lookup"><span data-stu-id="b96b7-127">Effect Preprocessor \#define's</span></span> | <span data-ttu-id="b96b7-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="b96b7-128">Description</span></span>                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b96b7-129">D3DXFX \_ LARGEADDRESS \_ Handle</span><span class="sxs-lookup"><span data-stu-id="b96b7-129">D3DXFX\_LARGEADDRESS\_HANDLE</span></span>   | <span data-ttu-id="b96b7-130">Defina esse valor antes de incluir d3dx9. h para que seu aplicativo não seja compilado ao tentar passar cadeias de caracteres para parâmetros D3DXHANDLE.</span><span class="sxs-lookup"><span data-stu-id="b96b7-130">Define this value before including d3dx9.h so that your application fails to compile when attempting to pass strings into D3DXHANDLE parameters.</span></span> <span data-ttu-id="b96b7-131">Isso ajudará a garantir que as informações válidas sejam passadas para o tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="b96b7-131">This will aid in making sure that valid information is being passed to the runtime.</span></span> |
| <span data-ttu-id="b96b7-132">Sinalizadores do vinculador de efeito</span><span class="sxs-lookup"><span data-stu-id="b96b7-132">Effect Linker Flags</span></span>            | <span data-ttu-id="b96b7-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="b96b7-133">Description</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="b96b7-134">\_reconhecimento de endereço grande \_</span><span class="sxs-lookup"><span data-stu-id="b96b7-134">LARGE\_ADDRESS\_AWARE</span></span>          | <span data-ttu-id="b96b7-135">Definir o sinalizador do vinculador com \_ reconhecimento de endereço grande \_ = 1 permitirá que o aplicativo aloque recursos após o limite de endereços de 2GB, quando necessário.</span><span class="sxs-lookup"><span data-stu-id="b96b7-135">Setting the linker flag LARGE\_ADDRESS\_AWARE = 1 will will allow the application to allocate resources past the 2GB address limit when needed.</span></span>                                                                                      |



 

<span data-ttu-id="b96b7-136">O sistema de efeitos usa blocos de estado para salvar e restaurar o estado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b96b7-136">The effect system uses state blocks to save and restore state automatically.</span></span> <span data-ttu-id="b96b7-137">Para obter mais informações sobre blocos de estado, consulte estado de [salvamento e restauração de blocos de estado (Direct3D 9)](state-blocks-save-and-restore-state.md).</span><span class="sxs-lookup"><span data-stu-id="b96b7-137">For more information about state blocks, see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b96b7-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b96b7-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b96b7-139">Constantes de efeito</span><span class="sxs-lookup"><span data-stu-id="b96b7-139">Effect Constants</span></span>](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 



