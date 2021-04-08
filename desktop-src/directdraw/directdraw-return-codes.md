---
title: Códigos de retorno do DirectDraw (ddraw. h)
description: Os erros são representados por valores negativos e não podem ser combinados.
ms.assetid: F713193E-3614-4741-B293-D312C170270A
topic_type:
- apiref
api_name:
- DD_OK
- DDERR_ALREADYINITIALIZED
- DDERR_BLTFASTCANTCLIP
- DDERR_CANNOTATTACHSURFACE
- DDERR_CANNOTDETACHSURFACE
- DDERR_CANTCREATEDC
- DDERR_CANTDUPLICATE
- DDERR_CANTLOCKSURFACE
- DDERR_CANTPAGELOCK
- DDERR_CANTPAGEUNLOCK
- DDERR_CLIPPERISUSINGHWND
- DDERR_COLORKEYNOTSET
- DDERR_CURRENTLYNOTAVAIL
- DDERR_DDSCAPSCOMPLEXREQUIRED
- DDERR_DCALREADYCREATED
- DDERR_DEVICEDOESNTOWNSURFACE
- DDERR_DIRECTDRAWALREADYCREATED
- DDERR_EXCEPTION
- DDERR_EXCLUSIVEMODEALREADYSET
- DDERR_EXPIRED
- DDERR_GENERIC
- DDERR_HEIGHTALIGN
- DDERR_HWNDALREADYSET
- DDERR_HWNDSUBCLASSED
- DDERR_IMPLICITLYCREATED
- DDERR_INCOMPATIBLEPRIMARY
- DDERR_INVALIDCAPS
- DDERR_INVALIDCLIPLIST
- DDERR_INVALIDDIRECTDRAWGUID
- DDERR_INVALIDMODE
- DDERR_INVALIDOBJECT
- DDERR_INVALIDPARAMS
- DDERR_INVALIDPIXELFORMAT
- DDERR_INVALIDPOSITION
- DDERR_INVALIDRECT
- DDERR_INVALIDSTREAM
- DDERR_INVALIDSURFACETYPE
- DDERR_LOCKEDSURFACES
- DDERR_MOREDATA
- DDERR_NEWMODE
- DDERR_NO3D
- DDERR_NOALPHAHW
- DDERR_NOBLTHW
- DDERR_NOCLIPLIST
- DDERR_NOCLIPPERATTACHED
- DDERR_NOCOLORCONVHW
- DDERR_NOCOLORKEY
- DDERR_NOCOLORKEYHW
- DDERR_NOCOOPERATIVELEVELSET
- DDERR_NODC
- DDERR_NODDROPSHW
- DDERR_NODIRECTDRAWHW
- DDERR_NODIRECTDRAWSUPPORT
- DDERR_NODRIVERSUPPORT
- DDERR_NOEMULATION
- DDERR_NOEXCLUSIVEMODE
- DDERR_NOFLIPHW
- DDERR_NOFOCUSWINDOW
- DDERR_NOGDI
- DDERR_NOHWND
- DDERR_NOMIPMAPHW
- DDERR_NOMIRRORHW
- DDERR_NOMONITORINFORMATION
- DDERR_NONONLOCALVIDMEM
- DDERR_NOOPTIMIZEHW
- DDERR_NOOVERLAYDEST
- DDERR_NOOVERLAYHW
- DDERR_NOPALETTEATTACHED
- DDERR_NOPALETTEHW
- DDERR_NORASTEROPHW
- DDERR_NOROTATIONHW
- DDERR_NOSTEREOHARDWARE
- DDERR_NOSTRETCHHW
- DDERR_NOSURFACELEFT
- DDERR_NOT4BITCOLOR
- DDERR_NOT4BITCOLORINDEX
- DDERR_NOT8BITCOLOR
- DDERR_NOTAOVERLAYSURFACE
- DDERR_NOTEXTUREHW
- DDERR_NOTFLIPPABLE
- DDERR_NOTFOUND
- DDERR_NOTINITIALIZED
- DDERR_NOTLOADED
- DDERR_NOTLOCKED
- DDERR_NOTPAGELOCKED
- DDERR_NOTPALETTIZED
- DDERR_NOVSYNCHW
- DDERR_NOZBUFFERHW
- DDERR_NOZOVERLAYHW
- DDERR_OUTOFCAPS
- DDERR_OUTOFMEMORY
- DDERR_OUTOFVIDEOMEMORY
- DDERR_OVERLAPPINGRECTS
- DDERR_OVERLAYCANTCLIP
- DDERR_OVERLAYCOLORKEYONLYONEACTIVE
- DDERR_OVERLAYNOTVISIBLE
- DDERR_PALETTEBUSY
- DDERR_PRIMARYSURFACEALREADYEXISTS
- DDERR_REGIONTOOSMALL
- DDERR_SURFACEALREADYATTACHED
- DDERR_SURFACEALREADYDEPENDENT
- DDERR_SURFACEBUSY
- DDERR_SURFACEISOBSCURED
- DDERR_SURFACELOST
- DDERR_SURFACENOTATTACHED
- DDERR_TESTFINISHED
- DDERR_TOOBIGHEIGHT
- DDERR_TOOBIGSIZE
- DDERR_TOOBIGWIDTH
- DDERR_UNSUPPORTED
- DDERR_UNSUPPORTEDFORMAT
- DDERR_UNSUPPORTEDMASK
- DDERR_UNSUPPORTEDMODE
- DDERR_VERTICALBLANKINPROGRESS
- DDERR_VIDEONOTACTIVE
- DDERR_WASSTILLDRAWING
- DDERR_WRONGMODE
- DDERR_XALIGN
api_location:
- Ddraw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d70ff2003edc382bac2823235f01f58ffea0d91
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837957"
---
# <a name="directdraw-return-codes"></a><span data-ttu-id="5a631-103">Códigos de retorno do DirectDraw</span><span class="sxs-lookup"><span data-stu-id="5a631-103">DirectDraw Return Codes</span></span>

<span data-ttu-id="5a631-104">Os erros são representados por valores negativos e não podem ser combinados.</span><span class="sxs-lookup"><span data-stu-id="5a631-104">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="5a631-105">Esta tabela lista os valores que podem ser retornados por todos os métodos das [funções](directdraw-functions.md)do DirectDraw e das [interfaces do DirectDraw](directdraw-interfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="5a631-105">This table lists the values that can be returned by all methods of the [DirectDraw Interfaces](directdraw-interfaces.md) and [DirectDraw Functions](directdraw-functions.md).</span></span> <span data-ttu-id="5a631-106">Para obter uma lista dos códigos de erro que cada método ou função pode retornar, consulte a descrição do método ou da função.</span><span class="sxs-lookup"><span data-stu-id="5a631-106">For a list of the error codes that each method or function can return, see the method or function description.</span></span>

<dl> <dt>

<span data-ttu-id="5a631-107"><span id="DD_OK"></span><span id="dd_ok"></span>**DD \_ OK**</span><span class="sxs-lookup"><span data-stu-id="5a631-107"><span id="DD_OK"></span><span id="dd_ok"></span>**DD\_OK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-108">A solicitação foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="5a631-108">The request completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-109"><span id="DDERR_ALREADYINITIALIZED"></span><span id="dderr_alreadyinitialized"></span>**DDERR \_ ALREADYINITIALIZED**</span><span class="sxs-lookup"><span data-stu-id="5a631-109"><span id="DDERR_ALREADYINITIALIZED"></span><span id="dderr_alreadyinitialized"></span>**DDERR\_ALREADYINITIALIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-110">O objeto já foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="5a631-110">The object has already been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-111"><span id="DDERR_BLTFASTCANTCLIP"></span><span id="dderr_bltfastcantclip"></span>**DDERR \_ BLTFASTCANTCLIP**</span><span class="sxs-lookup"><span data-stu-id="5a631-111"><span id="DDERR_BLTFASTCANTCLIP"></span><span id="dderr_bltfastcantclip"></span>**DDERR\_BLTFASTCANTCLIP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-112">Um objeto DirectDrawClipper é anexado a uma superfície de origem que passou para uma chamada para o método [**IDirectDrawSurface7:: BltFast**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-bltfast) .</span><span class="sxs-lookup"><span data-stu-id="5a631-112">A DirectDrawClipper object is attached to a source surface that has passed into a call to the [**IDirectDrawSurface7::BltFast**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-bltfast) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-113"><span id="DDERR_CANNOTATTACHSURFACE"></span><span id="dderr_cannotattachsurface"></span>**DDERR \_ CANNOTATTACHSURFACE**</span><span class="sxs-lookup"><span data-stu-id="5a631-113"><span id="DDERR_CANNOTATTACHSURFACE"></span><span id="dderr_cannotattachsurface"></span>**DDERR\_CANNOTATTACHSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-114">Uma superfície não pode ser anexada a outra superfície solicitada.</span><span class="sxs-lookup"><span data-stu-id="5a631-114">A surface cannot be attached to another requested surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-115"><span id="DDERR_CANNOTDETACHSURFACE"></span><span id="dderr_cannotdetachsurface"></span>**DDERR \_ CANNOTDETACHSURFACE**</span><span class="sxs-lookup"><span data-stu-id="5a631-115"><span id="DDERR_CANNOTDETACHSURFACE"></span><span id="dderr_cannotdetachsurface"></span>**DDERR\_CANNOTDETACHSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-116">Uma superfície não pode ser desanexada de outra superfície solicitada.</span><span class="sxs-lookup"><span data-stu-id="5a631-116">A surface cannot be detached from another requested surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-117"><span id="DDERR_CANTCREATEDC"></span><span id="dderr_cantcreatedc"></span>**DDERR \_ CANTCREATEDC**</span><span class="sxs-lookup"><span data-stu-id="5a631-117"><span id="DDERR_CANTCREATEDC"></span><span id="dderr_cantcreatedc"></span>**DDERR\_CANTCREATEDC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-118">O Windows não pode criar mais DCs (contextos de dispositivo) ou um controlador de domínio solicitou uma superfície indexada pela paleta quando a superfície não tinha nenhuma paleta e o modo de exibição não foi indexado pela paleta (nesse caso, o DirectDraw não pode selecionar uma paleta apropriada no controlador de domínio).</span><span class="sxs-lookup"><span data-stu-id="5a631-118">Windows cannot create any more device contexts (DCs), or a DC has requested a palette-indexed surface when the surface had no palette and the display mode was not palette-indexed (in this case, DirectDraw cannot select a proper palette into the DC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-119"><span id="DDERR_CANTDUPLICATE"></span><span id="dderr_cantduplicate"></span>**DDERR \_ CANTDUPLICATE**</span><span class="sxs-lookup"><span data-stu-id="5a631-119"><span id="DDERR_CANTDUPLICATE"></span><span id="dderr_cantduplicate"></span>**DDERR\_CANTDUPLICATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-120">As superfícies primária e 3D, ou superfícies criadas implicitamente, não podem ser duplicadas.</span><span class="sxs-lookup"><span data-stu-id="5a631-120">Primary and 3-D surfaces, or surfaces that are implicitly created, cannot be duplicated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-121"><span id="DDERR_CANTLOCKSURFACE"></span><span id="dderr_cantlocksurface"></span>**DDERR \_ CANTLOCKSURFACE**</span><span class="sxs-lookup"><span data-stu-id="5a631-121"><span id="DDERR_CANTLOCKSURFACE"></span><span id="dderr_cantlocksurface"></span>**DDERR\_CANTLOCKSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-122">O acesso a essa superfície é recusado porque foi feita uma tentativa de bloquear a superfície primária sem suporte ao DCI (display Control interface).</span><span class="sxs-lookup"><span data-stu-id="5a631-122">Access to this surface is refused because an attempt was made to lock the primary surface without Display Control Interface (DCI) support.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-123"><span id="DDERR_CANTPAGELOCK"></span><span id="dderr_cantpagelock"></span>**DDERR \_ CANTPAGELOCK**</span><span class="sxs-lookup"><span data-stu-id="5a631-123"><span id="DDERR_CANTPAGELOCK"></span><span id="dderr_cantpagelock"></span>**DDERR\_CANTPAGELOCK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-124">Falha ao tentar bloquear paginação de página.</span><span class="sxs-lookup"><span data-stu-id="5a631-124">An attempt to page-lock a surface failed.</span></span> <span data-ttu-id="5a631-125">O bloqueio de página não funciona em uma superfície de memória de exibição ou em uma superfície primária emulada.</span><span class="sxs-lookup"><span data-stu-id="5a631-125">Page lock does not work on a display-memory surface or an emulated primary surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-126"><span id="DDERR_CANTPAGEUNLOCK"></span><span id="dderr_cantpageunlock"></span>**DDERR \_ CANTPAGEUNLOCK**</span><span class="sxs-lookup"><span data-stu-id="5a631-126"><span id="DDERR_CANTPAGEUNLOCK"></span><span id="dderr_cantpageunlock"></span>**DDERR\_CANTPAGEUNLOCK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-127">Falha ao tentar destravar uma superfície na página.</span><span class="sxs-lookup"><span data-stu-id="5a631-127">An attempt to page-unlock a surface failed.</span></span> <span data-ttu-id="5a631-128">O desbloqueio de página não funciona em uma superfície de memória de exibição ou em uma superfície primária emulada.</span><span class="sxs-lookup"><span data-stu-id="5a631-128">Page unlock does not work on a display-memory surface or an emulated primary surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-129"><span id="DDERR_CLIPPERISUSINGHWND"></span><span id="dderr_clipperisusinghwnd"></span>**DDERR \_ CLIPPERISUSINGHWND**</span><span class="sxs-lookup"><span data-stu-id="5a631-129"><span id="DDERR_CLIPPERISUSINGHWND"></span><span id="dderr_clipperisusinghwnd"></span>**DDERR\_CLIPPERISUSINGHWND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-130">Foi feita uma tentativa de definir uma lista de clipes para um objeto DirectDrawClipper que já está monitorando um identificador de janela.</span><span class="sxs-lookup"><span data-stu-id="5a631-130">An attempt was made to set a clip list for a DirectDrawClipper object that is already monitoring a window handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-131"><span id="DDERR_COLORKEYNOTSET"></span><span id="dderr_colorkeynotset"></span>**DDERR \_ COLORKEYNOTSET**</span><span class="sxs-lookup"><span data-stu-id="5a631-131"><span id="DDERR_COLORKEYNOTSET"></span><span id="dderr_colorkeynotset"></span>**DDERR\_COLORKEYNOTSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-132">Nenhuma chave de cor de origem foi especificada para esta operação.</span><span class="sxs-lookup"><span data-stu-id="5a631-132">No source color key is specified for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-133"><span id="DDERR_CURRENTLYNOTAVAIL"></span><span id="dderr_currentlynotavail"></span>**DDERR \_ CURRENTLYNOTAVAIL**</span><span class="sxs-lookup"><span data-stu-id="5a631-133"><span id="DDERR_CURRENTLYNOTAVAIL"></span><span id="dderr_currentlynotavail"></span>**DDERR\_CURRENTLYNOTAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-134">Não há suporte disponível no momento.</span><span class="sxs-lookup"><span data-stu-id="5a631-134">No support is currently available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-135"><span id="DDERR_DDSCAPSCOMPLEXREQUIRED"></span><span id="dderr_ddscapscomplexrequired"></span>**DDERR \_ DDSCAPSCOMPLEXREQUIRED**</span><span class="sxs-lookup"><span data-stu-id="5a631-135"><span id="DDERR_DDSCAPSCOMPLEXREQUIRED"></span><span id="dderr_ddscapscomplexrequired"></span>**DDERR\_DDSCAPSCOMPLEXREQUIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-136">Novo no DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="5a631-136">New for DirectX 7.0.</span></span> <span data-ttu-id="5a631-137">A superfície requer o \_ sinalizador complexo DDSCAPS.</span><span class="sxs-lookup"><span data-stu-id="5a631-137">The surface requires the DDSCAPS\_COMPLEX flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-138"><span id="DDERR_DCALREADYCREATED"></span><span id="dderr_dcalreadycreated"></span>**DDERR \_ DCALREADYCREATED**</span><span class="sxs-lookup"><span data-stu-id="5a631-138"><span id="DDERR_DCALREADYCREATED"></span><span id="dderr_dcalreadycreated"></span>**DDERR\_DCALREADYCREATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-139">Um DC (contexto de dispositivo) já foi retornado para esta superfície.</span><span class="sxs-lookup"><span data-stu-id="5a631-139">A device context (DC) has already been returned for this surface.</span></span> <span data-ttu-id="5a631-140">Somente um controlador de domínio pode ser recuperado para cada superfície.</span><span class="sxs-lookup"><span data-stu-id="5a631-140">Only one DC can be retrieved for each surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-141"><span id="_DDERR_DEVICEDOESNTOWNSURFACE"></span><span id="_dderr_devicedoesntownsurface"></span>**>DDERR \_ DEVICEDOESNTOWNSURFACE**</span><span class="sxs-lookup"><span data-stu-id="5a631-141"><span id="_DDERR_DEVICEDOESNTOWNSURFACE"></span><span id="_dderr_devicedoesntownsurface"></span>**>DDERR\_DEVICEDOESNTOWNSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-142">As superfícies criadas por um dispositivo DirectDraw não podem ser usadas diretamente por outro dispositivo DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="5a631-142">Surfaces created by one DirectDraw device cannot be used directly by another DirectDraw device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-143"><span id="_DDERR_DIRECTDRAWALREADYCREATED"></span><span id="_dderr_directdrawalreadycreated"></span>**>DDERR \_ DIRECTDRAWALREADYCREATED**</span><span class="sxs-lookup"><span data-stu-id="5a631-143"><span id="_DDERR_DIRECTDRAWALREADYCREATED"></span><span id="_dderr_directdrawalreadycreated"></span>**>DDERR\_DIRECTDRAWALREADYCREATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-144">Um objeto do DirectDraw que representa este driver já foi criado para esse processo.</span><span class="sxs-lookup"><span data-stu-id="5a631-144">A DirectDraw object representing this driver has already been created for this process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-145"><span id="DDERR_EXCEPTION"></span><span id="dderr_exception"></span>**\_exceção DDERR**</span><span class="sxs-lookup"><span data-stu-id="5a631-145"><span id="DDERR_EXCEPTION"></span><span id="dderr_exception"></span>**DDERR\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-146">Exceção encontrada ao executar a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="5a631-146">An exception was encountered while performing the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-147"><span id="DDERR_EXCLUSIVEMODEALREADYSET"></span><span id="dderr_exclusivemodealreadyset"></span>**DDERR \_ EXCLUSIVEMODEALREADYSET**</span><span class="sxs-lookup"><span data-stu-id="5a631-147"><span id="DDERR_EXCLUSIVEMODEALREADYSET"></span><span id="dderr_exclusivemodealreadyset"></span>**DDERR\_EXCLUSIVEMODEALREADYSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-148">Foi feita uma tentativa de definir o nível de cooperação quando ele já estava definido como exclusivo.</span><span class="sxs-lookup"><span data-stu-id="5a631-148">An attempt was made to set the cooperative level when it was already set to exclusive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-149"><span id="DDERR_EXPIRED"></span><span id="dderr_expired"></span>**DDERR \_ expirou**</span><span class="sxs-lookup"><span data-stu-id="5a631-149"><span id="DDERR_EXPIRED"></span><span id="dderr_expired"></span>**DDERR\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-150">Os dados expiraram e, portanto, não são mais válidos.</span><span class="sxs-lookup"><span data-stu-id="5a631-150">The data has expired and is therefore no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-151"><span id="DDERR_GENERIC"></span><span id="dderr_generic"></span>**DDERR \_ genérico**</span><span class="sxs-lookup"><span data-stu-id="5a631-151"><span id="DDERR_GENERIC"></span><span id="dderr_generic"></span>**DDERR\_GENERIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-152">Há uma condição de erro indefinida.</span><span class="sxs-lookup"><span data-stu-id="5a631-152">There is an undefined error condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-153"><span id="DDERR_HEIGHTALIGN"></span><span id="dderr_heightalign"></span>**DDERR \_ HEIGHTALIGN**</span><span class="sxs-lookup"><span data-stu-id="5a631-153"><span id="DDERR_HEIGHTALIGN"></span><span id="dderr_heightalign"></span>**DDERR\_HEIGHTALIGN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-154">A altura do retângulo fornecido não é um múltiplo do alinhamento necessário.</span><span class="sxs-lookup"><span data-stu-id="5a631-154">The height of the provided rectangle is not a multiple of the required alignment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-155"><span id="DDERR_HWNDALREADYSET"></span><span id="dderr_hwndalreadyset"></span>**DDERR \_ HWNDALREADYSET**</span><span class="sxs-lookup"><span data-stu-id="5a631-155"><span id="DDERR_HWNDALREADYSET"></span><span id="dderr_hwndalreadyset"></span>**DDERR\_HWNDALREADYSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-156">O identificador de janela de nível cooperativo do DirectDraw já foi definido.</span><span class="sxs-lookup"><span data-stu-id="5a631-156">The DirectDraw cooperative-level window handle has already been set.</span></span> <span data-ttu-id="5a631-157">Ele não pode ser redefinido enquanto o processo tem superfícies ou paletas criadas.</span><span class="sxs-lookup"><span data-stu-id="5a631-157">It cannot be reset while the process has surfaces or palettes created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-158"><span id="DDERR_HWNDSUBCLASSED"></span><span id="dderr_hwndsubclassed"></span>**DDERR \_ HWNDSUBCLASSED**</span><span class="sxs-lookup"><span data-stu-id="5a631-158"><span id="DDERR_HWNDSUBCLASSED"></span><span id="dderr_hwndsubclassed"></span>**DDERR\_HWNDSUBCLASSED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-159">O DirectDraw é impedido de restaurar o estado porque o identificador de janela de nível cooperativo do DirectDraw foi subclasse.</span><span class="sxs-lookup"><span data-stu-id="5a631-159">DirectDraw is prevented from restoring state because the DirectDraw cooperative-level window handle has been subclassed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-160"><span id="DDERR_IMPLICITLYCREATED"></span><span id="dderr_implicitlycreated"></span>**DDERR \_ IMPLICITLYCREATED**</span><span class="sxs-lookup"><span data-stu-id="5a631-160"><span id="DDERR_IMPLICITLYCREATED"></span><span id="dderr_implicitlycreated"></span>**DDERR\_IMPLICITLYCREATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-161">A superfície não pode ser restaurada porque é uma superfície criada implicitamente.</span><span class="sxs-lookup"><span data-stu-id="5a631-161">The surface cannot be restored because it is an implicitly created surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-162"><span id="DDERR_INCOMPATIBLEPRIMARY"></span><span id="dderr_incompatibleprimary"></span>**DDERR \_ INCOMPATIBLEPRIMARY**</span><span class="sxs-lookup"><span data-stu-id="5a631-162"><span id="DDERR_INCOMPATIBLEPRIMARY"></span><span id="dderr_incompatibleprimary"></span>**DDERR\_INCOMPATIBLEPRIMARY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-163">A solicitação de criação de superfície primária não corresponde à superfície primária existente.</span><span class="sxs-lookup"><span data-stu-id="5a631-163">The primary surface creation request does not match the existing primary surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-164"><span id="DDERR_INVALIDCAPS"></span><span id="dderr_invalidcaps"></span>**DDERR \_ INVALIDCAPS**</span><span class="sxs-lookup"><span data-stu-id="5a631-164"><span id="DDERR_INVALIDCAPS"></span><span id="dderr_invalidcaps"></span>**DDERR\_INVALIDCAPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-165">Um ou mais dos bits de funcionalidade passados para a função de retorno de chamada estão incorretos.</span><span class="sxs-lookup"><span data-stu-id="5a631-165">One or more of the capability bits passed to the callback function are incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-166"><span id="DDERR_INVALIDCLIPLIST"></span><span id="dderr_invalidcliplist"></span>**DDERR \_ INVALIDCLIPLIST**</span><span class="sxs-lookup"><span data-stu-id="5a631-166"><span id="DDERR_INVALIDCLIPLIST"></span><span id="dderr_invalidcliplist"></span>**DDERR\_INVALIDCLIPLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-167">O DirectDraw não oferece suporte à lista de clipes fornecida.</span><span class="sxs-lookup"><span data-stu-id="5a631-167">DirectDraw does not support the provided clip list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-168"><span id="DDERR_INVALIDDIRECTDRAWGUID"></span><span id="dderr_invaliddirectdrawguid"></span>**DDERR \_ INVALIDDIRECTDRAWGUID**</span><span class="sxs-lookup"><span data-stu-id="5a631-168"><span id="DDERR_INVALIDDIRECTDRAWGUID"></span><span id="dderr_invaliddirectdrawguid"></span>**DDERR\_INVALIDDIRECTDRAWGUID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-169">O GUID (identificador global exclusivo) passado para a função [**DirectDrawCreate**](/windows/desktop/api/Ddraw/nf-ddraw-directdrawcreate) não é um identificador de driver DirectDraw válido.</span><span class="sxs-lookup"><span data-stu-id="5a631-169">The globally unique identifier (GUID) passed to the [**DirectDrawCreate**](/windows/desktop/api/Ddraw/nf-ddraw-directdrawcreate) function is not a valid DirectDraw driver identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-170"><span id="DDERR_INVALIDMODE"></span><span id="dderr_invalidmode"></span>**DDERR \_ INválidamode**</span><span class="sxs-lookup"><span data-stu-id="5a631-170"><span id="DDERR_INVALIDMODE"></span><span id="dderr_invalidmode"></span>**DDERR\_INVALIDMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-171">O DirectDraw não oferece suporte ao modo solicitado.</span><span class="sxs-lookup"><span data-stu-id="5a631-171">DirectDraw does not support the requested mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-172"><span id="DDERR_INVALIDOBJECT"></span><span id="dderr_invalidobject"></span>**DDERR \_ INvalidaobject**</span><span class="sxs-lookup"><span data-stu-id="5a631-172"><span id="DDERR_INVALIDOBJECT"></span><span id="dderr_invalidobject"></span>**DDERR\_INVALIDOBJECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-173">O DirectDraw recebeu um ponteiro que era um objeto DirectDraw inválido.</span><span class="sxs-lookup"><span data-stu-id="5a631-173">DirectDraw received a pointer that was an invalid DirectDraw object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-174"><span id="DDERR_INVALIDPARAMS"></span><span id="dderr_invalidparams"></span>**DDERR \_ INVALIDPARAMS**</span><span class="sxs-lookup"><span data-stu-id="5a631-174"><span id="DDERR_INVALIDPARAMS"></span><span id="dderr_invalidparams"></span>**DDERR\_INVALIDPARAMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-175">Um ou mais dos parâmetros passados para o método estão incorretos.</span><span class="sxs-lookup"><span data-stu-id="5a631-175">One or more of the parameters passed to the method are incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-176"><span id="DDERR_INVALIDPIXELFORMAT"></span><span id="dderr_invalidpixelformat"></span>**DDERR \_ INVALIDPIXELFORMAT**</span><span class="sxs-lookup"><span data-stu-id="5a631-176"><span id="DDERR_INVALIDPIXELFORMAT"></span><span id="dderr_invalidpixelformat"></span>**DDERR\_INVALIDPIXELFORMAT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-177">O formato de pixel era inválido conforme especificado.</span><span class="sxs-lookup"><span data-stu-id="5a631-177">The pixel format was invalid as specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-178"><span id="DDERR_INVALIDPOSITION"></span><span id="dderr_invalidposition"></span>**DDERR \_ INVALIDPOSITION**</span><span class="sxs-lookup"><span data-stu-id="5a631-178"><span id="DDERR_INVALIDPOSITION"></span><span id="dderr_invalidposition"></span>**DDERR\_INVALIDPOSITION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-179">A posição da sobreposição no destino não é mais válida.</span><span class="sxs-lookup"><span data-stu-id="5a631-179">The position of the overlay on the destination is no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-180"><span id="DDERR_INVALIDRECT"></span><span id="dderr_invalidrect"></span>**DDERR \_ INVALIDRECT**</span><span class="sxs-lookup"><span data-stu-id="5a631-180"><span id="DDERR_INVALIDRECT"></span><span id="dderr_invalidrect"></span>**DDERR\_INVALIDRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-181">O retângulo fornecido era inválido.</span><span class="sxs-lookup"><span data-stu-id="5a631-181">The provided rectangle was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-182"><span id="DDERR_INVALIDSTREAM"></span><span id="dderr_invalidstream"></span>**DDERR \_ INVALIDSTREAM**</span><span class="sxs-lookup"><span data-stu-id="5a631-182"><span id="DDERR_INVALIDSTREAM"></span><span id="dderr_invalidstream"></span>**DDERR\_INVALIDSTREAM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-183">O fluxo especificado contém dados inválidos.</span><span class="sxs-lookup"><span data-stu-id="5a631-183">The specified stream contains invalid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-184"><span id="DDERR_INVALIDSURFACETYPE"></span><span id="dderr_invalidsurfacetype"></span>**DDERR \_ INVALIDSURFACETYPE**</span><span class="sxs-lookup"><span data-stu-id="5a631-184"><span id="DDERR_INVALIDSURFACETYPE"></span><span id="dderr_invalidsurfacetype"></span>**DDERR\_INVALIDSURFACETYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-185">A superfície era do tipo incorreto.</span><span class="sxs-lookup"><span data-stu-id="5a631-185">The surface was of the wrong type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-186"><span id="DDERR_LOCKEDSURFACES"></span><span id="dderr_lockedsurfaces"></span>**DDERR \_ LOCKEDSURFACES**</span><span class="sxs-lookup"><span data-stu-id="5a631-186"><span id="DDERR_LOCKEDSURFACES"></span><span id="dderr_lockedsurfaces"></span>**DDERR\_LOCKEDSURFACES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-187">Uma ou mais superfícies estão bloqueadas, causando a falha da operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="5a631-187">One or more surfaces are locked, causing the failure of the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-188"><span id="DDERR_MOREDATA"></span><span id="dderr_moredata"></span>**DDERR \_ MOREDATA**</span><span class="sxs-lookup"><span data-stu-id="5a631-188"><span id="DDERR_MOREDATA"></span><span id="dderr_moredata"></span>**DDERR\_MOREDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-189">Há mais dados disponíveis do que o tamanho de buffer especificado pode conter.</span><span class="sxs-lookup"><span data-stu-id="5a631-189">There is more data available than the specified buffer size can hold.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-190"><span id="DDERR_NEWMODE"></span><span id="dderr_newmode"></span>**DDERR \_ NewMode**</span><span class="sxs-lookup"><span data-stu-id="5a631-190"><span id="DDERR_NEWMODE"></span><span id="dderr_newmode"></span>**DDERR\_NEWMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-191">Novo no DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="5a631-191">New for DirectX 7.0.</span></span> <span data-ttu-id="5a631-192">Quando [**IDirectDraw7:: StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) é chamado com o \_ sinalizador DDSMT ISTESTREQUIRED, ele pode retornar esse valor para indicar que algumas ou todas as resoluções podem e devem ser testadas.</span><span class="sxs-lookup"><span data-stu-id="5a631-192">When [**IDirectDraw7::StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) is called with the DDSMT\_ISTESTREQUIRED flag, it might return this value to denote that some or all of the resolutions can and should be tested.</span></span> <span data-ttu-id="5a631-193">[**IDirectDraw7:: evaluatemode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode) retorna esse valor para indicar que o teste mudou para um novo modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="5a631-193">[**IDirectDraw7::EvaluateMode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode) returns this value to indicate that the test has switched to a new display mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-194"><span id="DDERR_NO3D"></span><span id="dderr_no3d"></span>**DDERR \_ NO3D**</span><span class="sxs-lookup"><span data-stu-id="5a631-194"><span id="DDERR_NO3D"></span><span id="dderr_no3d"></span>**DDERR\_NO3D**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-195">Nenhum hardware 3D ou emulação está presente.</span><span class="sxs-lookup"><span data-stu-id="5a631-195">No 3-D hardware or emulation is present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-196"><span id="DDERR_NOALPHAHW"></span><span id="dderr_noalphahw"></span>**DDERR \_ NOALPHAHW**</span><span class="sxs-lookup"><span data-stu-id="5a631-196"><span id="DDERR_NOALPHAHW"></span><span id="dderr_noalphahw"></span>**DDERR\_NOALPHAHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-197">Nenhum hardware de aceleração alfa está presente ou disponível, causando a falha da operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="5a631-197">No alpha-acceleration hardware is present or available, causing the failure of the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-198"><span id="DDERR_NOBLTHW"></span><span id="dderr_noblthw"></span>**DDERR \_ NOBLTHW**</span><span class="sxs-lookup"><span data-stu-id="5a631-198"><span id="DDERR_NOBLTHW"></span><span id="dderr_noblthw"></span>**DDERR\_NOBLTHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-199">Nenhum bloco de bits transferindo o hardware está presente.</span><span class="sxs-lookup"><span data-stu-id="5a631-199">No bit block transferring hardware is present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-200"><span id="DDERR_NOCLIPLIST"></span><span id="dderr_nocliplist"></span>**DDERR \_ NOmedialist**</span><span class="sxs-lookup"><span data-stu-id="5a631-200"><span id="DDERR_NOCLIPLIST"></span><span id="dderr_nocliplist"></span>**DDERR\_NOCLIPLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-201">Nenhuma lista de clipes disponível.</span><span class="sxs-lookup"><span data-stu-id="5a631-201">No clip list is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-202"><span id="DDERR_NOCLIPPERATTACHED"></span><span id="dderr_noclipperattached"></span>**DDERR \_ NOCLIPPERATTACHED**</span><span class="sxs-lookup"><span data-stu-id="5a631-202"><span id="DDERR_NOCLIPPERATTACHED"></span><span id="dderr_noclipperattached"></span>**DDERR\_NOCLIPPERATTACHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-203">Nenhum objeto DirectDrawClipper está anexado ao objeto Surface.</span><span class="sxs-lookup"><span data-stu-id="5a631-203">No DirectDrawClipper object is attached to the surface object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-204"><span id="DDERR_NOCOLORCONVHW"></span><span id="dderr_nocolorconvhw"></span>**DDERR \_ NOCOLORCONVHW**</span><span class="sxs-lookup"><span data-stu-id="5a631-204"><span id="DDERR_NOCOLORCONVHW"></span><span id="dderr_nocolorconvhw"></span>**DDERR\_NOCOLORCONVHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-205">Nenhum hardware de conversão de cor está presente ou disponível.</span><span class="sxs-lookup"><span data-stu-id="5a631-205">No color-conversion hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-206"><span id="DDERR_NOCOLORKEY"></span><span id="dderr_nocolorkey"></span>**DDERR \_ NOCOLORKEY**</span><span class="sxs-lookup"><span data-stu-id="5a631-206"><span id="DDERR_NOCOLORKEY"></span><span id="dderr_nocolorkey"></span>**DDERR\_NOCOLORKEY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-207">A superfície não tem uma chave de cor no momento.</span><span class="sxs-lookup"><span data-stu-id="5a631-207">The surface does not currently have a color key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-208"><span id="DDERR_NOCOLORKEYHW"></span><span id="dderr_nocolorkeyhw"></span>**DDERR \_ NOCOLORKEYHW**</span><span class="sxs-lookup"><span data-stu-id="5a631-208"><span id="DDERR_NOCOLORKEYHW"></span><span id="dderr_nocolorkeyhw"></span>**DDERR\_NOCOLORKEYHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-209">Não há suporte de hardware para a chave de cor de destino.</span><span class="sxs-lookup"><span data-stu-id="5a631-209">There is no hardware support for the destination color key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-210"><span id="DDERR_NOCOOPERATIVELEVELSET"></span><span id="dderr_nocooperativelevelset"></span>**DDERR \_ NOCOOPERATIVELEVELSET**</span><span class="sxs-lookup"><span data-stu-id="5a631-210"><span id="DDERR_NOCOOPERATIVELEVELSET"></span><span id="dderr_nocooperativelevelset"></span>**DDERR\_NOCOOPERATIVELEVELSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-211">Uma função CREATE foi chamada sem o método [**IDirectDraw7:: SetCooperativeLevel**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-setcooperativelevel) .</span><span class="sxs-lookup"><span data-stu-id="5a631-211">A create function was called without the [**IDirectDraw7::SetCooperativeLevel**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-setcooperativelevel) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-212"><span id="DDERR_NODC"></span><span id="dderr_nodc"></span>**DDERR \_ NODC**</span><span class="sxs-lookup"><span data-stu-id="5a631-212"><span id="DDERR_NODC"></span><span id="dderr_nodc"></span>**DDERR\_NODC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-213">Nenhum contexto de dispositivo (DC) já foi criado para esta superfície.</span><span class="sxs-lookup"><span data-stu-id="5a631-213">No device context (DC) has ever been created for this surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-214"><span id="DDERR_NODDROPSHW"></span><span id="dderr_noddropshw"></span>**DDERR \_ NODDROPSHW**</span><span class="sxs-lookup"><span data-stu-id="5a631-214"><span id="DDERR_NODDROPSHW"></span><span id="dderr_noddropshw"></span>**DDERR\_NODDROPSHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-215">Nenhum hardware de operação de varredura (ROP) do DirectDraw está disponível.</span><span class="sxs-lookup"><span data-stu-id="5a631-215">No DirectDraw raster-operation (ROP) hardware is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-216"><span id="DDERR_NODIRECTDRAWHW"></span><span id="dderr_nodirectdrawhw"></span>**DDERR \_ NODIRECTDRAWHW**</span><span class="sxs-lookup"><span data-stu-id="5a631-216"><span id="DDERR_NODIRECTDRAWHW"></span><span id="dderr_nodirectdrawhw"></span>**DDERR\_NODIRECTDRAWHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-217">A criação de objeto DirectDraw somente de hardware não é possível; o driver não oferece suporte a nenhum hardware.</span><span class="sxs-lookup"><span data-stu-id="5a631-217">Hardware-only DirectDraw object creation is not possible; the driver does not support any hardware.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-218"><span id="DDERR_NODIRECTDRAWSUPPORT"></span><span id="dderr_nodirectdrawsupport"></span>**DDERR \_ NODIRECTDRAWSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="5a631-218"><span id="DDERR_NODIRECTDRAWSUPPORT"></span><span id="dderr_nodirectdrawsupport"></span>**DDERR\_NODIRECTDRAWSUPPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-219">O suporte do DirectDraw não é possível com o driver de vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="5a631-219">DirectDraw support is not possible with the current display driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-220"><span id="DDERR_NODRIVERSUPPORT"></span><span id="dderr_nodriversupport"></span>**DDERR \_ NODRIVERSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="5a631-220"><span id="DDERR_NODRIVERSUPPORT"></span><span id="dderr_nodriversupport"></span>**DDERR\_NODRIVERSUPPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-221">Novo no DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="5a631-221">New for DirectX 7.0.</span></span> <span data-ttu-id="5a631-222">O teste não pode continuar porque o driver do adaptador de vídeo não enumera taxas de atualização.</span><span class="sxs-lookup"><span data-stu-id="5a631-222">Testing cannot proceed because the display adapter driver does not enumerate refresh rates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-223"><span id="DDERR_NOEMULATION"></span><span id="dderr_noemulation"></span>**DDERR \_ NOemulação**</span><span class="sxs-lookup"><span data-stu-id="5a631-223"><span id="DDERR_NOEMULATION"></span><span id="dderr_noemulation"></span>**DDERR\_NOEMULATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-224">A emulação de software não está disponível.</span><span class="sxs-lookup"><span data-stu-id="5a631-224">Software emulation is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-225"><span id="DDERR_NOEXCLUSIVEMODE"></span><span id="dderr_noexclusivemode"></span>**DDERR \_ NOexcludemode**</span><span class="sxs-lookup"><span data-stu-id="5a631-225"><span id="DDERR_NOEXCLUSIVEMODE"></span><span id="dderr_noexclusivemode"></span>**DDERR\_NOEXCLUSIVEMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-226">A operação requer que o aplicativo tenha o modo exclusivo, mas o aplicativo não tem modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="5a631-226">The operation requires the application to have exclusive mode, but the application does not have exclusive mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-227"><span id="DDERR_NOFLIPHW"></span><span id="dderr_nofliphw"></span>**DDERR \_ NOFLIPHW**</span><span class="sxs-lookup"><span data-stu-id="5a631-227"><span id="DDERR_NOFLIPHW"></span><span id="dderr_nofliphw"></span>**DDERR\_NOFLIPHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-228">Não há suporte para a inversão de superfícies visíveis.</span><span class="sxs-lookup"><span data-stu-id="5a631-228">Flipping visible surfaces is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-229"><span id="DDERR_NOFOCUSWINDOW"></span><span id="dderr_nofocuswindow"></span>**DDERR \_ NOFOCUSWINDOW**</span><span class="sxs-lookup"><span data-stu-id="5a631-229"><span id="DDERR_NOFOCUSWINDOW"></span><span id="dderr_nofocuswindow"></span>**DDERR\_NOFOCUSWINDOW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-230">Foi feita uma tentativa de criar ou definir uma janela do dispositivo sem primeiro definir a janela de foco.</span><span class="sxs-lookup"><span data-stu-id="5a631-230">An attempt was made to create or set a device window without first setting the focus window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-231"><span id="DDERR_NOGDI"></span><span id="dderr_nogdi"></span>**DDERR \_ NOGDI**</span><span class="sxs-lookup"><span data-stu-id="5a631-231"><span id="DDERR_NOGDI"></span><span id="dderr_nogdi"></span>**DDERR\_NOGDI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-232">Não há GDI presente.</span><span class="sxs-lookup"><span data-stu-id="5a631-232">No GDI is present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-233"><span id="DDERR_NOHWND"></span><span id="dderr_nohwnd"></span>**DDERR \_ NOhwnd**</span><span class="sxs-lookup"><span data-stu-id="5a631-233"><span id="DDERR_NOHWND"></span><span id="dderr_nohwnd"></span>**DDERR\_NOHWND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-234">A notificação do Clipper requer um identificador de janela ou nenhum identificador de janela foi definido anteriormente como o identificador de janela de nível cooperativo.</span><span class="sxs-lookup"><span data-stu-id="5a631-234">Clipper notification requires a window handle, or no window handle has been previously set as the cooperative level window handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-235"><span id="DDERR_NOMIPMAPHW"></span><span id="dderr_nomipmaphw"></span>**DDERR \_ NOMIPMAPHW**</span><span class="sxs-lookup"><span data-stu-id="5a631-235"><span id="DDERR_NOMIPMAPHW"></span><span id="dderr_nomipmaphw"></span>**DDERR\_NOMIPMAPHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-236">Nenhum hardware de mapeamento de textura compatível com mipmap está presente ou disponível.</span><span class="sxs-lookup"><span data-stu-id="5a631-236">No mipmap-capable texture mapping hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-237"><span id="DDERR_NOMIRRORHW"></span><span id="dderr_nomirrorhw"></span>**DDERR \_ NOMIRRORHW**</span><span class="sxs-lookup"><span data-stu-id="5a631-237"><span id="DDERR_NOMIRRORHW"></span><span id="dderr_nomirrorhw"></span>**DDERR\_NOMIRRORHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-238">Nenhum hardware de espelhamento está presente ou disponível.</span><span class="sxs-lookup"><span data-stu-id="5a631-238">No mirroring hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-239"><span id="DDERR_NOMONITORINFORMATION"></span><span id="dderr_nomonitorinformation"></span>**DDERR \_ NOMONITORINFORMATION**</span><span class="sxs-lookup"><span data-stu-id="5a631-239"><span id="DDERR_NOMONITORINFORMATION"></span><span id="dderr_nomonitorinformation"></span>**DDERR\_NOMONITORINFORMATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-240">Novo no DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="5a631-240">New for DirectX 7.0.</span></span> <span data-ttu-id="5a631-241">O teste não pode continuar porque o monitor não tem dados EDID associados.</span><span class="sxs-lookup"><span data-stu-id="5a631-241">Testing cannot proceed because the monitor has no associated EDID data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-242"><span id="DDERR_NONONLOCALVIDMEM"></span><span id="dderr_nononlocalvidmem"></span>**DDERR \_ NONONLOCALVIDMEM**</span><span class="sxs-lookup"><span data-stu-id="5a631-242"><span id="DDERR_NONONLOCALVIDMEM"></span><span id="dderr_nononlocalvidmem"></span>**DDERR\_NONONLOCALVIDMEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-243">Foi feita uma tentativa de alocar memória de vídeo não local de um dispositivo que não dá suporte à memória de vídeo não local.</span><span class="sxs-lookup"><span data-stu-id="5a631-243">An attempt was made to allocate nonlocal video memory from a device that does not support nonlocal video memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-244"><span id="DDERR_NOOPTIMIZEHW"></span><span id="dderr_nooptimizehw"></span>**DDERR \_ NOOPTIMIZEHW**</span><span class="sxs-lookup"><span data-stu-id="5a631-244"><span id="DDERR_NOOPTIMIZEHW"></span><span id="dderr_nooptimizehw"></span>**DDERR\_NOOPTIMIZEHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-245">O dispositivo não dá suporte a superfícies otimizadas.</span><span class="sxs-lookup"><span data-stu-id="5a631-245">The device does not support optimized surfaces.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-246"><span id="DDERR_NOOVERLAYDEST"></span><span id="dderr_nooverlaydest"></span>**DDERR \_ NOOVERLAYDEST**</span><span class="sxs-lookup"><span data-stu-id="5a631-246"><span id="DDERR_NOOVERLAYDEST"></span><span id="dderr_nooverlaydest"></span>**DDERR\_NOOVERLAYDEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-247">O método [**IDirectDrawSurface7:: GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) é chamado em uma sobreposição que o método [**IDirectDrawSurface7:: UpdateOverlay**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay) não foi chamado para estabelecer como destino.</span><span class="sxs-lookup"><span data-stu-id="5a631-247">The [**IDirectDrawSurface7::GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) method is called on an overlay that the [**IDirectDrawSurface7::UpdateOverlay**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay) method has not been called on to establish as a destination.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-248"><span id="DDERR_NOOVERLAYHW"></span><span id="dderr_nooverlayhw"></span>**DDERR \_ NOOVERLAYHW**</span><span class="sxs-lookup"><span data-stu-id="5a631-248"><span id="DDERR_NOOVERLAYHW"></span><span id="dderr_nooverlayhw"></span>**DDERR\_NOOVERLAYHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-249">Nenhum hardware de sobreposição está presente ou disponível.</span><span class="sxs-lookup"><span data-stu-id="5a631-249">No overlay hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-250"><span id="DDERR_NOPALETTEATTACHED"></span><span id="dderr_nopaletteattached"></span>**DDERR \_ NOPALETTEATTACHED**</span><span class="sxs-lookup"><span data-stu-id="5a631-250"><span id="DDERR_NOPALETTEATTACHED"></span><span id="dderr_nopaletteattached"></span>**DDERR\_NOPALETTEATTACHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-251">Nenhum objeto de paleta está anexado a esta superfície.</span><span class="sxs-lookup"><span data-stu-id="5a631-251">No palette object is attached to this surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-252"><span id="DDERR_NOPALETTEHW"></span><span id="dderr_nopalettehw"></span>**DDERR \_ NOPALETTEHW**</span><span class="sxs-lookup"><span data-stu-id="5a631-252"><span id="DDERR_NOPALETTEHW"></span><span id="dderr_nopalettehw"></span>**DDERR\_NOPALETTEHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-253">Não há suporte de hardware para paletas de 16 ou 256 cores.</span><span class="sxs-lookup"><span data-stu-id="5a631-253">There is no hardware support for 16- or 256-color palettes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-254"><span id="DDERR_NORASTEROPHW"></span><span id="dderr_norasterophw"></span>**DDERR \_ NORASTEROPHW**</span><span class="sxs-lookup"><span data-stu-id="5a631-254"><span id="DDERR_NORASTEROPHW"></span><span id="dderr_norasterophw"></span>**DDERR\_NORASTEROPHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-255">Nenhum hardware de operação de varredura apropriado está presente ou disponível.</span><span class="sxs-lookup"><span data-stu-id="5a631-255">No appropriate raster-operation hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-256"><span id="DDERR_NOROTATIONHW"></span><span id="dderr_norotationhw"></span>**DDERR \_ NOROTATIONHW**</span><span class="sxs-lookup"><span data-stu-id="5a631-256"><span id="DDERR_NOROTATIONHW"></span><span id="dderr_norotationhw"></span>**DDERR\_NOROTATIONHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-257">Nenhum hardware de rotação está presente ou disponível.</span><span class="sxs-lookup"><span data-stu-id="5a631-257">No rotation hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-258"><span id="DDERR_NOSTEREOHARDWARE"></span><span id="dderr_nostereohardware"></span>**DDERR \_ NOSTEREOHARDWARE**</span><span class="sxs-lookup"><span data-stu-id="5a631-258"><span id="DDERR_NOSTEREOHARDWARE"></span><span id="dderr_nostereohardware"></span>**DDERR\_NOSTEREOHARDWARE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-259">Não há nenhum hardware estéreo presente ou disponível.</span><span class="sxs-lookup"><span data-stu-id="5a631-259">There is no stereo hardware present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-260"><span id="DDERR_NOSTRETCHHW"></span><span id="dderr_nostretchhw"></span>**DDERR \_ NOSTRETCHHW**</span><span class="sxs-lookup"><span data-stu-id="5a631-260"><span id="DDERR_NOSTRETCHHW"></span><span id="dderr_nostretchhw"></span>**DDERR\_NOSTRETCHHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-261">Não há suporte de hardware para alongamento.</span><span class="sxs-lookup"><span data-stu-id="5a631-261">There is no hardware support for stretching.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-262"><span id="DDERR_NOSURFACELEFT"></span><span id="dderr_nosurfaceleft"></span>**DDERR \_ NOSURFACELEFT**</span><span class="sxs-lookup"><span data-stu-id="5a631-262"><span id="DDERR_NOSURFACELEFT"></span><span id="dderr_nosurfaceleft"></span>**DDERR\_NOSURFACELEFT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-263">Não há nenhum hardware presente que dê suporte a superfícies estéreo.</span><span class="sxs-lookup"><span data-stu-id="5a631-263">There is no hardware present that supports stereo surfaces.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-264"><span id="DDERR_NOT4BITCOLOR"></span><span id="dderr_not4bitcolor"></span>**DDERR \_ NOT4BITCOLOR**</span><span class="sxs-lookup"><span data-stu-id="5a631-264"><span id="DDERR_NOT4BITCOLOR"></span><span id="dderr_not4bitcolor"></span>**DDERR\_NOT4BITCOLOR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-265">O objeto DirectDrawSurface não está usando uma paleta de cores de 4 bits e a operação solicitada requer uma paleta de cores de 4 bits.</span><span class="sxs-lookup"><span data-stu-id="5a631-265">The DirectDrawSurface object is not using a 4-bit color palette, and the requested operation requires a 4-bit color palette.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-266"><span id="DDERR_NOT4BITCOLORINDEX"></span><span id="dderr_not4bitcolorindex"></span>**DDERR \_ NOT4BITCOLORINDEX**</span><span class="sxs-lookup"><span data-stu-id="5a631-266"><span id="DDERR_NOT4BITCOLORINDEX"></span><span id="dderr_not4bitcolorindex"></span>**DDERR\_NOT4BITCOLORINDEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-267">O objeto DirectDrawSurface não está usando uma paleta de índice de cores de 4 bits e a operação solicitada requer uma paleta de índice de cores de 4 bits.</span><span class="sxs-lookup"><span data-stu-id="5a631-267">The DirectDrawSurface object is not using a 4-bit color index palette, and the requested operation requires a 4-bit color index palette.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-268"><span id="DDERR_NOT8BITCOLOR"></span><span id="dderr_not8bitcolor"></span>**DDERR \_ NOT8BITCOLOR**</span><span class="sxs-lookup"><span data-stu-id="5a631-268"><span id="DDERR_NOT8BITCOLOR"></span><span id="dderr_not8bitcolor"></span>**DDERR\_NOT8BITCOLOR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-269">O objeto DirectDrawSurface não está usando uma paleta de cores de 8 bits e a operação solicitada requer uma paleta de cores de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="5a631-269">The DirectDrawSurface object is not using an 8-bit color palette, and the requested operation requires an 8-bit color palette.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-270"><span id="DDERR_NOTAOVERLAYSURFACE"></span><span id="dderr_notaoverlaysurface"></span>**DDERR \_ NOTAOVERLAYSURFACE**</span><span class="sxs-lookup"><span data-stu-id="5a631-270"><span id="DDERR_NOTAOVERLAYSURFACE"></span><span id="dderr_notaoverlaysurface"></span>**DDERR\_NOTAOVERLAYSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-271">Um componente de sobreposição é chamado para uma superfície não sobreposta.</span><span class="sxs-lookup"><span data-stu-id="5a631-271">An overlay component is called for a nonoverlay surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-272"><span id="DDERR_NOTEXTUREHW"></span><span id="dderr_notexturehw"></span>**DDERR \_ NOTEXTUREHW**</span><span class="sxs-lookup"><span data-stu-id="5a631-272"><span id="DDERR_NOTEXTUREHW"></span><span id="dderr_notexturehw"></span>**DDERR\_NOTEXTUREHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-273">A operação não pode ser executada porque nenhum hardware de mapeamento de textura está presente ou disponível.</span><span class="sxs-lookup"><span data-stu-id="5a631-273">The operation cannot be carried out because no texture-mapping hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-274"><span id="DDERR_NOTFLIPPABLE"></span><span id="dderr_notflippable"></span>**DDERR não \_ INverteble**</span><span class="sxs-lookup"><span data-stu-id="5a631-274"><span id="DDERR_NOTFLIPPABLE"></span><span id="dderr_notflippable"></span>**DDERR\_NOTFLIPPABLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-275">Foi feita uma tentativa de virar uma superfície que não pode ser invertida.</span><span class="sxs-lookup"><span data-stu-id="5a631-275">An attempt was made to flip a surface that cannot be flipped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-276"><span id="DDERR_NOTFOUND"></span><span id="dderr_notfound"></span>**DDERR não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="5a631-276"><span id="DDERR_NOTFOUND"></span><span id="dderr_notfound"></span>**DDERR\_NOTFOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-277">O item solicitado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="5a631-277">The requested item was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-278"><span id="DDERR_NOTINITIALIZED"></span><span id="dderr_notinitialized"></span>**DDERR não \_ inicializado**</span><span class="sxs-lookup"><span data-stu-id="5a631-278"><span id="DDERR_NOTINITIALIZED"></span><span id="dderr_notinitialized"></span>**DDERR\_NOTINITIALIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-279">Foi feita uma tentativa de chamar um método de interface de um objeto DirectDraw criado por [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) antes da inicialização do objeto.</span><span class="sxs-lookup"><span data-stu-id="5a631-279">An attempt was made to call an interface method of a DirectDraw object created by [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) before the object was initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-280"><span id="DDERR_NOTLOADED"></span><span id="dderr_notloaded"></span>**DDERR não \_ carregado**</span><span class="sxs-lookup"><span data-stu-id="5a631-280"><span id="DDERR_NOTLOADED"></span><span id="dderr_notloaded"></span>**DDERR\_NOTLOADED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-281">A superfície é uma superfície otimizada, mas ainda não foi alocada nenhuma memória.</span><span class="sxs-lookup"><span data-stu-id="5a631-281">The surface is an optimized surface, but it has not yet been allocated any memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-282"><span id="DDERR_NOTLOCKED"></span><span id="dderr_notlocked"></span>**DDERR não \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="5a631-282"><span id="DDERR_NOTLOCKED"></span><span id="dderr_notlocked"></span>**DDERR\_NOTLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-283">Foi feita uma tentativa de desbloquear uma superfície que não estava bloqueada.</span><span class="sxs-lookup"><span data-stu-id="5a631-283">An attempt was made to unlock a surface that was not locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-284"><span id="DDERR_NOTPAGELOCKED"></span><span id="dderr_notpagelocked"></span>**DDERR \_ NOTPAGELOCKED**</span><span class="sxs-lookup"><span data-stu-id="5a631-284"><span id="DDERR_NOTPAGELOCKED"></span><span id="dderr_notpagelocked"></span>**DDERR\_NOTPAGELOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-285">Foi feita uma tentativa de desbloquear a página em uma superfície sem bloqueios de página pendentes.</span><span class="sxs-lookup"><span data-stu-id="5a631-285">An attempt was made to page-unlock a surface with no outstanding page locks.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-286"><span id="DDERR_NOTPALETTIZED"></span><span id="dderr_notpalettized"></span>**DDERR \_ NOTPALETTIZED**</span><span class="sxs-lookup"><span data-stu-id="5a631-286"><span id="DDERR_NOTPALETTIZED"></span><span id="dderr_notpalettized"></span>**DDERR\_NOTPALETTIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-287">A superfície que está sendo usada não é uma superfície baseada em paleta.</span><span class="sxs-lookup"><span data-stu-id="5a631-287">The surface being used is not a palette-based surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-288"><span id="DDERR_NOVSYNCHW"></span><span id="dderr_novsynchw"></span>**DDERR \_ NOVSYNCHW**</span><span class="sxs-lookup"><span data-stu-id="5a631-288"><span id="DDERR_NOVSYNCHW"></span><span id="dderr_novsynchw"></span>**DDERR\_NOVSYNCHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-289">Não há suporte de hardware para operações verticais em branco sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="5a631-289">There is no hardware support for vertical blank synchronized operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-290"><span id="DDERR_NOZBUFFERHW"></span><span id="dderr_nozbufferhw"></span>**DDERR \_ NOZBUFFERHW**</span><span class="sxs-lookup"><span data-stu-id="5a631-290"><span id="DDERR_NOZBUFFERHW"></span><span id="dderr_nozbufferhw"></span>**DDERR\_NOZBUFFERHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-291">A operação para criar um z-buffer na memória de vídeo ou executar uma transferência de bloco de bits (BitBlt), usando um z-buffer não pode ser executada porque não há suporte de hardware para z-buffers.</span><span class="sxs-lookup"><span data-stu-id="5a631-291">The operation to create a z-buffer in display memory or to perform a bit block transfer (bitblt), using a z-buffer cannot be carried out because there is no hardware support for z-buffers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-292"><span id="DDERR_NOZOVERLAYHW"></span><span id="dderr_nozoverlayhw"></span>**DDERR \_ NOZOVERLAYHW**</span><span class="sxs-lookup"><span data-stu-id="5a631-292"><span id="DDERR_NOZOVERLAYHW"></span><span id="dderr_nozoverlayhw"></span>**DDERR\_NOZOVERLAYHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-293">As superfícies de sobreposição não podem ser em camadas z, com base na ordem z, porque o hardware não dá suporte à ordenação z de sobreposições.</span><span class="sxs-lookup"><span data-stu-id="5a631-293">The overlay surfaces cannot be z-layered, based on the z-order because the hardware does not support z-ordering of overlays.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-294"><span id="DDERR_OUTOFCAPS"></span><span id="dderr_outofcaps"></span>**DDERR \_ OUTOFCAPS**</span><span class="sxs-lookup"><span data-stu-id="5a631-294"><span id="DDERR_OUTOFCAPS"></span><span id="dderr_outofcaps"></span>**DDERR\_OUTOFCAPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-295">O hardware necessário para a operação solicitada já foi alocado.</span><span class="sxs-lookup"><span data-stu-id="5a631-295">The hardware needed for the requested operation has already been allocated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-296"><span id="DDERR_OUTOFMEMORY"></span><span id="dderr_outofmemory"></span>**\_OUTOFMEMORY DDERR**</span><span class="sxs-lookup"><span data-stu-id="5a631-296"><span id="DDERR_OUTOFMEMORY"></span><span id="dderr_outofmemory"></span>**DDERR\_OUTOFMEMORY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-297">O DirectDraw não tem memória suficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="5a631-297">DirectDraw does not have enough memory to perform the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-298"><span id="DDERR_OUTOFVIDEOMEMORY"></span><span id="dderr_outofvideomemory"></span>**DDERR \_ OUTOFVIDEOMEMORY**</span><span class="sxs-lookup"><span data-stu-id="5a631-298"><span id="DDERR_OUTOFVIDEOMEMORY"></span><span id="dderr_outofvideomemory"></span>**DDERR\_OUTOFVIDEOMEMORY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-299">O DirectDraw não tem memória de vídeo suficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="5a631-299">DirectDraw does not have enough display memory to perform the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-300"><span id="DDERR_OVERLAPPINGRECTS"></span><span id="dderr_overlappingrects"></span>**DDERR \_ OVERLAPPINGRECTS**</span><span class="sxs-lookup"><span data-stu-id="5a631-300"><span id="DDERR_OVERLAPPINGRECTS"></span><span id="dderr_overlappingrects"></span>**DDERR\_OVERLAPPINGRECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-301">Os retângulos de origem e de destino estão na mesma superfície e se sobrepõem.</span><span class="sxs-lookup"><span data-stu-id="5a631-301">The source and destination rectangles are on the same surface and overlap each other.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-302"><span id="DDERR_OVERLAYCANTCLIP"></span><span id="dderr_overlaycantclip"></span>**DDERR \_ OVERLAYCANTCLIP**</span><span class="sxs-lookup"><span data-stu-id="5a631-302"><span id="DDERR_OVERLAYCANTCLIP"></span><span id="dderr_overlaycantclip"></span>**DDERR\_OVERLAYCANTCLIP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-303">O hardware não oferece suporte a sobreposições recortadas.</span><span class="sxs-lookup"><span data-stu-id="5a631-303">The hardware does not support clipped overlays.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-304"><span id="DDERR_OVERLAYCOLORKEYONLYONEACTIVE"></span><span id="dderr_overlaycolorkeyonlyoneactive"></span>**DDERR \_ OVERLAYCOLORKEYONLYONEACTIVE**</span><span class="sxs-lookup"><span data-stu-id="5a631-304"><span id="DDERR_OVERLAYCOLORKEYONLYONEACTIVE"></span><span id="dderr_overlaycolorkeyonlyoneactive"></span>**DDERR\_OVERLAYCOLORKEYONLYONEACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-305">Foi feita uma tentativa de ter mais de uma chave de cor ativa em uma sobreposição.</span><span class="sxs-lookup"><span data-stu-id="5a631-305">An attempt was made to have more than one color key active on an overlay.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-306"><span id="DDERR_OVERLAYNOTVISIBLE"></span><span id="dderr_overlaynotvisible"></span>**DDERR \_ OVERLAYNOTVISIBLE**</span><span class="sxs-lookup"><span data-stu-id="5a631-306"><span id="DDERR_OVERLAYNOTVISIBLE"></span><span id="dderr_overlaynotvisible"></span>**DDERR\_OVERLAYNOTVISIBLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-307">O método [**IDirectDrawSurface7:: GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) foi chamado em uma sobreposição oculta.</span><span class="sxs-lookup"><span data-stu-id="5a631-307">The [**IDirectDrawSurface7::GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) method was called on a hidden overlay.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-308"><span id="DDERR_PALETTEBUSY"></span><span id="dderr_palettebusy"></span>**DDERR \_ PALETTEBUSY**</span><span class="sxs-lookup"><span data-stu-id="5a631-308"><span id="DDERR_PALETTEBUSY"></span><span id="dderr_palettebusy"></span>**DDERR\_PALETTEBUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-309">O acesso a esta paleta foi recusado porque a paleta está bloqueada por outro thread.</span><span class="sxs-lookup"><span data-stu-id="5a631-309">Access to this palette is refused because the palette is locked by another thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-310"><span id="DDERR_PRIMARYSURFACEALREADYEXISTS"></span><span id="dderr_primarysurfacealreadyexists"></span>**DDERR \_ PRIMARYSURFACEALREADYEXISTS**</span><span class="sxs-lookup"><span data-stu-id="5a631-310"><span id="DDERR_PRIMARYSURFACEALREADYEXISTS"></span><span id="dderr_primarysurfacealreadyexists"></span>**DDERR\_PRIMARYSURFACEALREADYEXISTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-311">Este processo já criou uma superfície primária.</span><span class="sxs-lookup"><span data-stu-id="5a631-311">This process has already created a primary surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-312"><span id="DDERR_REGIONTOOSMALL"></span><span id="dderr_regiontoosmall"></span>**DDERR \_ REGIONTOOSMALL**</span><span class="sxs-lookup"><span data-stu-id="5a631-312"><span id="DDERR_REGIONTOOSMALL"></span><span id="dderr_regiontoosmall"></span>**DDERR\_REGIONTOOSMALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-313">A região passada para o método [**IDirectDrawClipper:: Getmedialist**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawclipper-getcliplist) é muito pequena.</span><span class="sxs-lookup"><span data-stu-id="5a631-313">The region passed to the [**IDirectDrawClipper::GetClipList**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawclipper-getcliplist) method is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-314"><span id="DDERR_SURFACEALREADYATTACHED"></span><span id="dderr_surfacealreadyattached"></span>**DDERR \_ SURFACEALREADYATTACHED**</span><span class="sxs-lookup"><span data-stu-id="5a631-314"><span id="DDERR_SURFACEALREADYATTACHED"></span><span id="dderr_surfacealreadyattached"></span>**DDERR\_SURFACEALREADYATTACHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-315">Foi feita uma tentativa de anexar uma superfície a outra superfície à qual ela já está anexada.</span><span class="sxs-lookup"><span data-stu-id="5a631-315">An attempt was made to attach a surface to another surface to which it is already attached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-316"><span id="DDERR_SURFACEALREADYDEPENDENT"></span><span id="dderr_surfacealreadydependent"></span>**DDERR \_ SURFACEALREADYDEPENDENT**</span><span class="sxs-lookup"><span data-stu-id="5a631-316"><span id="DDERR_SURFACEALREADYDEPENDENT"></span><span id="dderr_surfacealreadydependent"></span>**DDERR\_SURFACEALREADYDEPENDENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-317">Foi feita uma tentativa de tornar uma superfície uma dependência de outra superfície na qual ela já é dependente.</span><span class="sxs-lookup"><span data-stu-id="5a631-317">An attempt was made to make a surface a dependency of another surface on which it is already dependent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-318"><span id="DDERR_SURFACEBUSY"></span><span id="dderr_surfacebusy"></span>**DDERR \_ SURFACEBUSY**</span><span class="sxs-lookup"><span data-stu-id="5a631-318"><span id="DDERR_SURFACEBUSY"></span><span id="dderr_surfacebusy"></span>**DDERR\_SURFACEBUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-319">O acesso à superfície é recusado porque a superfície está bloqueada por outro thread.</span><span class="sxs-lookup"><span data-stu-id="5a631-319">Access to the surface is refused because the surface is locked by another thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-320"><span id="DDERR_SURFACEISOBSCURED"></span><span id="dderr_surfaceisobscured"></span>**DDERR \_ SURFACEISOBSCURED**</span><span class="sxs-lookup"><span data-stu-id="5a631-320"><span id="DDERR_SURFACEISOBSCURED"></span><span id="dderr_surfaceisobscured"></span>**DDERR\_SURFACEISOBSCURED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-321">O acesso à superfície é recusado porque a superfície está obscurecida.</span><span class="sxs-lookup"><span data-stu-id="5a631-321">Access to the surface is refused because the surface is obscured.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-322"><span id="DDERR_SURFACELOST"></span><span id="dderr_surfacelost"></span>**DDERR \_ SURFACELOST**</span><span class="sxs-lookup"><span data-stu-id="5a631-322"><span id="DDERR_SURFACELOST"></span><span id="dderr_surfacelost"></span>**DDERR\_SURFACELOST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-323">O acesso à superfície é recusado porque a memória da superfície não existe mais.</span><span class="sxs-lookup"><span data-stu-id="5a631-323">Access to the surface is refused because the surface memory is gone.</span></span> <span data-ttu-id="5a631-324">Chame o método [**IDirectDrawSurface7:: Restore**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-restore) nesta superfície para restaurar a memória associada a ele.</span><span class="sxs-lookup"><span data-stu-id="5a631-324">Call the [**IDirectDrawSurface7::Restore**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-restore) method on this surface to restore the memory associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-325"><span id="DDERR_SURFACENOTATTACHED"></span><span id="dderr_surfacenotattached"></span>**DDERR \_ SURFACENOTATTACHED**</span><span class="sxs-lookup"><span data-stu-id="5a631-325"><span id="DDERR_SURFACENOTATTACHED"></span><span id="dderr_surfacenotattached"></span>**DDERR\_SURFACENOTATTACHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-326">A superfície solicitada não está anexada.</span><span class="sxs-lookup"><span data-stu-id="5a631-326">The requested surface is not attached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-327"><span id="DDERR_TESTFINISHED"></span><span id="dderr_testfinished"></span>**DDERR \_ TESTFINISHED**</span><span class="sxs-lookup"><span data-stu-id="5a631-327"><span id="DDERR_TESTFINISHED"></span><span id="dderr_testfinished"></span>**DDERR\_TESTFINISHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-328">Novo no DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="5a631-328">New for DirectX 7.0.</span></span> <span data-ttu-id="5a631-329">Quando retornado pelo método [**IDirectDraw7:: StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) , esse valor significa que nenhum teste pôde ser iniciado porque todas as resoluções escolhidas para teste já têm informações de taxa de atualização no registro.</span><span class="sxs-lookup"><span data-stu-id="5a631-329">When returned by the [**IDirectDraw7::StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) method, this value means that no test could be initiated because all the resolutions chosen for testing already have refresh rate information in the registry.</span></span> <span data-ttu-id="5a631-330">Quando retornado por [**IDirectDraw7:: evaluatemode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode), o valor significa que o DirectDraw concluiu um teste de taxa de atualização.</span><span class="sxs-lookup"><span data-stu-id="5a631-330">When returned by [**IDirectDraw7::EvaluateMode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode), the value means that DirectDraw has completed a refresh rate test.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-331"><span id="DDERR_TOOBIGHEIGHT"></span><span id="dderr_toobigheight"></span>**DDERR \_ TOOBIGHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="5a631-331"><span id="DDERR_TOOBIGHEIGHT"></span><span id="dderr_toobigheight"></span>**DDERR\_TOOBIGHEIGHT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-332">A altura solicitada pelo DirectDraw é muito grande.</span><span class="sxs-lookup"><span data-stu-id="5a631-332">The height requested by DirectDraw is too large.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-333"><span id="DDERR_TOOBIGSIZE"></span><span id="dderr_toobigsize"></span>**DDERR \_ TOOBIGSIZE**</span><span class="sxs-lookup"><span data-stu-id="5a631-333"><span id="DDERR_TOOBIGSIZE"></span><span id="dderr_toobigsize"></span>**DDERR\_TOOBIGSIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-334">O tamanho solicitado pelo DirectDraw é muito grande.</span><span class="sxs-lookup"><span data-stu-id="5a631-334">The size requested by DirectDraw is too large.</span></span> <span data-ttu-id="5a631-335">No entanto, a altura e a largura individuais são tamanhos válidos.</span><span class="sxs-lookup"><span data-stu-id="5a631-335">However, the individual height and width are valid sizes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-336"><span id="DDERR_TOOBIGWIDTH"></span><span id="dderr_toobigwidth"></span>**DDERR \_ TOOBIGWIDTH**</span><span class="sxs-lookup"><span data-stu-id="5a631-336"><span id="DDERR_TOOBIGWIDTH"></span><span id="dderr_toobigwidth"></span>**DDERR\_TOOBIGWIDTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-337">A largura solicitada pelo DirectDraw é muito grande.</span><span class="sxs-lookup"><span data-stu-id="5a631-337">The width requested by DirectDraw is too large.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-338"><span id="DDERR_UNSUPPORTED"></span><span id="dderr_unsupported"></span>**DDERR \_ sem suporte**</span><span class="sxs-lookup"><span data-stu-id="5a631-338"><span id="DDERR_UNSUPPORTED"></span><span id="dderr_unsupported"></span>**DDERR\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-339">A operação não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="5a631-339">The operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-340"><span id="DDERR_UNSUPPORTEDFORMAT"></span><span id="dderr_unsupportedformat"></span>**DDERR \_ UNSUPPORTEDFORMAT**</span><span class="sxs-lookup"><span data-stu-id="5a631-340"><span id="DDERR_UNSUPPORTEDFORMAT"></span><span id="dderr_unsupportedformat"></span>**DDERR\_UNSUPPORTEDFORMAT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-341">Não há suporte para o formato de pixel solicitado pelo DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="5a631-341">The pixel format requested is not supported by DirectDraw.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-342"><span id="DDERR_UNSUPPORTEDMASK"></span><span id="dderr_unsupportedmask"></span>**DDERR \_ UNSUPPORTEDMASK**</span><span class="sxs-lookup"><span data-stu-id="5a631-342"><span id="DDERR_UNSUPPORTEDMASK"></span><span id="dderr_unsupportedmask"></span>**DDERR\_UNSUPPORTEDMASK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-343">O DirectDraw não dá suporte ao bitmask no formato de pixel solicitado.</span><span class="sxs-lookup"><span data-stu-id="5a631-343">The bitmask in the pixel format requested is not supported by DirectDraw.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-344"><span id="DDERR_UNSUPPORTEDMODE"></span><span id="dderr_unsupportedmode"></span>**DDERR \_ sem suporte**</span><span class="sxs-lookup"><span data-stu-id="5a631-344"><span id="DDERR_UNSUPPORTEDMODE"></span><span id="dderr_unsupportedmode"></span>**DDERR\_UNSUPPORTEDMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-345">A exibição está atualmente em um modo sem suporte.</span><span class="sxs-lookup"><span data-stu-id="5a631-345">The display is currently in an unsupported mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-346"><span id="DDERR_VERTICALBLANKINPROGRESS"></span><span id="dderr_verticalblankinprogress"></span>**DDERR \_ VERTICALBLANKINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="5a631-346"><span id="DDERR_VERTICALBLANKINPROGRESS"></span><span id="dderr_verticalblankinprogress"></span>**DDERR\_VERTICALBLANKINPROGRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-347">Uma vertical em branco está em andamento.</span><span class="sxs-lookup"><span data-stu-id="5a631-347">A vertical blank is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-348"><span id="DDERR_VIDEONOTACTIVE"></span><span id="dderr_videonotactive"></span>**DDERR \_ VIDEONOTACTIVE**</span><span class="sxs-lookup"><span data-stu-id="5a631-348"><span id="DDERR_VIDEONOTACTIVE"></span><span id="dderr_videonotactive"></span>**DDERR\_VIDEONOTACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-349">A porta de vídeo não está ativa.</span><span class="sxs-lookup"><span data-stu-id="5a631-349">The video port is not active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-350"><span id="DDERR_WASSTILLDRAWING"></span><span id="dderr_wasstilldrawing"></span>**DDERR \_ WASSTILLDRAWING**</span><span class="sxs-lookup"><span data-stu-id="5a631-350"><span id="DDERR_WASSTILLDRAWING"></span><span id="dderr_wasstilldrawing"></span>**DDERR\_WASSTILLDRAWING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-351">A operação BitBlt anterior que está transferindo informações para ou desta superfície está incompleta.</span><span class="sxs-lookup"><span data-stu-id="5a631-351">The previous bitblt operation that is transferring information to or from this surface is incomplete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-352"><span id="DDERR_WRONGMODE"></span><span id="dderr_wrongmode"></span>**DDERR \_ incorretomode**</span><span class="sxs-lookup"><span data-stu-id="5a631-352"><span id="DDERR_WRONGMODE"></span><span id="dderr_wrongmode"></span>**DDERR\_WRONGMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-353">Esta superfície não pode ser restaurada porque foi criada em um modo diferente.</span><span class="sxs-lookup"><span data-stu-id="5a631-353">This surface cannot be restored because it was created in a different mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a631-354"><span id="DDERR_XALIGN"></span><span id="dderr_xalign"></span>**DDERR \_ XALIGN**</span><span class="sxs-lookup"><span data-stu-id="5a631-354"><span id="DDERR_XALIGN"></span><span id="dderr_xalign"></span>**DDERR\_XALIGN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a631-355">O retângulo fornecido não estava alinhado horizontalmente em um limite necessário.</span><span class="sxs-lookup"><span data-stu-id="5a631-355">The provided rectangle was not horizontally aligned on a required boundary.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5a631-356">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a631-356">Requirements</span></span>



| <span data-ttu-id="5a631-357">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a631-357">Requirement</span></span> | <span data-ttu-id="5a631-358">Valor</span><span class="sxs-lookup"><span data-stu-id="5a631-358">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5a631-359">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5a631-359">Header</span></span><br/> | <dl> <span data-ttu-id="5a631-360"><dt>Ddraw. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a631-360"><dt>Ddraw.h</dt></span></span> </dl> |



 

