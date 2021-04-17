---
title: Estrutura WMDMRIGHTS
description: A estrutura WMDMRIGHTS descreve os direitos de uso de conteúdo.
ms.assetid: 1be9167b-0d20-4a17-a42b-9696ada2b539
keywords:
- Estrutura WMDMRIGHTS Windows Media Gerenciador de Dispositivos
- Ponteiro de estrutura PWMDMRIGHTS Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDMRIGHTS
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8bc3bcd61efc64d32daa3179b77a9aaa518d4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760905"
---
# <a name="wmdmrights-structure"></a><span data-ttu-id="cf12d-105">Estrutura WMDMRIGHTS</span><span class="sxs-lookup"><span data-stu-id="cf12d-105">WMDMRIGHTS structure</span></span>

<span data-ttu-id="cf12d-106">A estrutura **WMDMRIGHTS** descreve os direitos de uso de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="cf12d-106">The **WMDMRIGHTS** structure describes content-use rights.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf12d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cf12d-107">Syntax</span></span>


```C++
typedef struct __WMDMRIGHTS {
  UINT         cbSize;
  DWORD        dwContentType;
  DWORD        fuFlags;
  DWORD        fuRights;
  DWORD        dwAppSec;
  DWORD        dwPlaybackCount;
  WMDMDATETIME ExpirationDate;
} WMDMRIGHTS, *PWMDMRIGHTS;
```



## <a name="members"></a><span data-ttu-id="cf12d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="cf12d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="cf12d-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="cf12d-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="cf12d-110">Tamanho da estrutura, em bytes.</span><span class="sxs-lookup"><span data-stu-id="cf12d-110">Size of the structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="cf12d-111">**dwContentType**</span><span class="sxs-lookup"><span data-stu-id="cf12d-111">**dwContentType**</span></span>
</dt> <dd>

<span data-ttu-id="cf12d-112">**DWORD** que contém o tipo de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="cf12d-112">**DWORD** containing the type of content.</span></span>

</dd> <dt>

<span data-ttu-id="cf12d-113">**fuFlags**</span><span class="sxs-lookup"><span data-stu-id="cf12d-113">**fuFlags**</span></span>
</dt> <dd>

<span data-ttu-id="cf12d-114">Campo de bits especificando as opções de direitos em uso para o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="cf12d-114">Bit field specifying the rights options in use for the content.</span></span>



| <span data-ttu-id="cf12d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="cf12d-115">Value</span></span>                        | <span data-ttu-id="cf12d-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf12d-116">Description</span></span>                                  |
|------------------------------|----------------------------------------------|
| <span data-ttu-id="cf12d-117">\_PLAYBACKCOUNT de direitos do WMDM \_</span><span class="sxs-lookup"><span data-stu-id="cf12d-117">WMDM\_RIGHTS\_PLAYBACKCOUNT</span></span>  | <span data-ttu-id="cf12d-118">Número de vezes que o arquivo pode ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="cf12d-118">Number of times that the file can be played.</span></span> |
| <span data-ttu-id="cf12d-119">\_EXPIRATIONDATE de direitos do WMDM \_</span><span class="sxs-lookup"><span data-stu-id="cf12d-119">WMDM\_RIGHTS\_EXPIRATIONDATE</span></span> | <span data-ttu-id="cf12d-120">Data de validade do arquivo.</span><span class="sxs-lookup"><span data-stu-id="cf12d-120">Expiration date of the file.</span></span>                 |
| <span data-ttu-id="cf12d-121">\_FREESERIALIDS de direitos do WMDM \_</span><span class="sxs-lookup"><span data-stu-id="cf12d-121">WMDM\_RIGHTS\_FREESERIALIDS</span></span>  | <span data-ttu-id="cf12d-122">Identificador de série livre do arquivo.</span><span class="sxs-lookup"><span data-stu-id="cf12d-122">Free serial identifier of the file.</span></span>          |
| <span data-ttu-id="cf12d-123">\_Grupo GroupId de direitos do WMDM \_</span><span class="sxs-lookup"><span data-stu-id="cf12d-123">WMDM\_RIGHTS\_GROUPID Group</span></span>  | <span data-ttu-id="cf12d-124">Identificador do arquivo.</span><span class="sxs-lookup"><span data-stu-id="cf12d-124">Identifier of the file.</span></span>                      |
| <span data-ttu-id="cf12d-125">\_NAMEDSERIALIDS de direitos do WMDM \_</span><span class="sxs-lookup"><span data-stu-id="cf12d-125">WMDM\_RIGHTS\_NAMEDSERIALIDS</span></span> | <span data-ttu-id="cf12d-126">Identificador de série nomeado do arquivo.</span><span class="sxs-lookup"><span data-stu-id="cf12d-126">Named serial identifier of the file.</span></span>         |



 

</dd> <dt>

<span data-ttu-id="cf12d-127">**fuRights**</span><span class="sxs-lookup"><span data-stu-id="cf12d-127">**fuRights**</span></span>
</dt> <dd>

<span data-ttu-id="cf12d-128">Campo de bits que contém os bits de direitos para o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="cf12d-128">Bit field containing the rights bits for the content.</span></span>



| <span data-ttu-id="cf12d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="cf12d-129">Value</span></span>                                     | <span data-ttu-id="cf12d-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf12d-130">Description</span></span>                                   |
|-------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="cf12d-131">os \_ direitos \_ do WMDM são executados \_ no \_ PC</span><span class="sxs-lookup"><span data-stu-id="cf12d-131">WMDM\_RIGHTS\_PLAY\_ON\_PC</span></span>                | <span data-ttu-id="cf12d-132">O conteúdo pode ser reproduzido em um computador pessoal.</span><span class="sxs-lookup"><span data-stu-id="cf12d-132">Content can be played on a personal computer.</span></span> |
| <span data-ttu-id="cf12d-133">\_ \_ cópia de direitos \_ de WMDM para \_ \_ dispositivo não SDMI \_</span><span class="sxs-lookup"><span data-stu-id="cf12d-133">WMDM\_RIGHTS\_COPY\_TO\_NON\_SDMI\_DEVICE</span></span> | <span data-ttu-id="cf12d-134">O conteúdo pode ser copiado para um dispositivo não SDMI.</span><span class="sxs-lookup"><span data-stu-id="cf12d-134">Content can be copied to a non-SDMI device.</span></span>   |
| <span data-ttu-id="cf12d-135">\_copiar direitos do WMDM \_ para o \_ \_ CD</span><span class="sxs-lookup"><span data-stu-id="cf12d-135">WMDM\_RIGHTS\_COPY\_TO\_CD</span></span>                | <span data-ttu-id="cf12d-136">O conteúdo pode ser copiado para um CD.</span><span class="sxs-lookup"><span data-stu-id="cf12d-136">Content can be copied to a CD.</span></span>                |
| <span data-ttu-id="cf12d-137">\_ \_ cópia de direitos \_ de WMDM para \_ \_ dispositivo SDMI</span><span class="sxs-lookup"><span data-stu-id="cf12d-137">WMDM\_RIGHTS\_COPY\_TO\_SDMI\_DEVICE</span></span>      | <span data-ttu-id="cf12d-138">O conteúdo pode ser copiado para um dispositivo SDMI.</span><span class="sxs-lookup"><span data-stu-id="cf12d-138">Content can be copied to an SDMI device.</span></span>      |



 

</dd> <dt>

<span data-ttu-id="cf12d-139">**dwAppSec**</span><span class="sxs-lookup"><span data-stu-id="cf12d-139">**dwAppSec**</span></span>
</dt> <dd>

<span data-ttu-id="cf12d-140">Matriz de bytes que especifica o nível mínimo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cf12d-140">Byte array that specifies the minimum level of application security.</span></span>

</dd> <dt>

<span data-ttu-id="cf12d-141">**dwPlaybackCount**</span><span class="sxs-lookup"><span data-stu-id="cf12d-141">**dwPlaybackCount**</span></span>
</dt> <dd>

<span data-ttu-id="cf12d-142">**DWORD** que contém o número de horas restantes que o conteúdo pode ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="cf12d-142">**DWORD** containing the number of remaining times that the content can be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="cf12d-143">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="cf12d-143">**ExpirationDate**</span></span>
</dt> <dd>

<span data-ttu-id="cf12d-144">Estrutura [**WMDMDATETIME**](wmdmdatetime.md) que contém a data e a hora de expiração do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="cf12d-144">[**WMDMDATETIME**](wmdmdatetime.md) structure containing the expiration date and time for the content.</span></span> <span data-ttu-id="cf12d-145">Se a licença não tiver uma data de expiração, o membro **Wano** será definido como 0xFFFF e todos os outros membros de **WMDMDATETIME** serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="cf12d-145">If the license has no expiration date, the **wYear** member is set to 0xFFFF, and all other members of **WMDMDATETIME** are ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cf12d-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf12d-146">Requirements</span></span>



| <span data-ttu-id="cf12d-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf12d-147">Requirement</span></span> | <span data-ttu-id="cf12d-148">Valor</span><span class="sxs-lookup"><span data-stu-id="cf12d-148">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cf12d-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cf12d-149">Header</span></span><br/> | <dl> <span data-ttu-id="cf12d-150"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cf12d-150"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf12d-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf12d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf12d-152">**IMDSPStorage:: getrights**</span><span class="sxs-lookup"><span data-stu-id="cf12d-152">**IMDSPStorage::GetRights**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getrights)
</dt> <dt>

[<span data-ttu-id="cf12d-153">**IWMDMStorage:: getrights**</span><span class="sxs-lookup"><span data-stu-id="cf12d-153">**IWMDMStorage::GetRights**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getrights)
</dt> <dt>

[<span data-ttu-id="cf12d-154">**WMDMDATETIME**</span><span class="sxs-lookup"><span data-stu-id="cf12d-154">**WMDMDATETIME**</span></span>](wmdmdatetime.md)
</dt> <dt>

[<span data-ttu-id="cf12d-155">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="cf12d-155">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





