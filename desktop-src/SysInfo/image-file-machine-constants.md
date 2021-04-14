---
description: Descreve possíveis arquiteturas de computador.
ms.assetid: 1E5E4F98-925B-424D-9B3D-BC6716FBF990
title: Constantes de máquina de arquivo de imagem (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c8c43767ce0d86edf2285241772ea060573efc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501966"
---
# <a name="image-file-machine-constants"></a><span data-ttu-id="8904d-103">Constantes de máquina de arquivo de imagem</span><span class="sxs-lookup"><span data-stu-id="8904d-103">Image File Machine Constants</span></span>

<span data-ttu-id="8904d-104">Descreve possíveis arquiteturas de computador.</span><span class="sxs-lookup"><span data-stu-id="8904d-104">Describes possible machine architectures.</span></span> <span data-ttu-id="8904d-105">Usado em [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a), [**IsWow64GuestMachineSupported**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64guestmachinesupported) e [**IsWow64Process2**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process2).</span><span class="sxs-lookup"><span data-stu-id="8904d-105">Used in [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a), [**IsWow64GuestMachineSupported**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64guestmachinesupported) and [**IsWow64Process2**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process2).</span></span>

<dl> <dt>

<span data-ttu-id="8904d-106"><span id="IMAGE_FILE_MACHINE_UNKNOWN"></span><span id="image_file_machine_unknown"></span>**computador de arquivo de imagem \_ \_ \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="8904d-106"><span id="IMAGE_FILE_MACHINE_UNKNOWN"></span><span id="image_file_machine_unknown"></span>**IMAGE\_FILE\_MACHINE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-107">0</span><span class="sxs-lookup"><span data-stu-id="8904d-107">0</span></span>
</dt> <dt>



<span data-ttu-id="8904d-108">Unknown</span><span class="sxs-lookup"><span data-stu-id="8904d-108">Unknown</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-109"><span id="IMAGE_FILE_MACHINE_TARGET_HOST"></span><span id="image_file_machine_target_host"></span>**\_host de \_ destino da máquina do arquivo de imagem \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8904d-109"><span id="IMAGE_FILE_MACHINE_TARGET_HOST"></span><span id="image_file_machine_target_host"></span>**IMAGE\_FILE\_MACHINE\_TARGET\_HOST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-110">0x0001</span><span class="sxs-lookup"><span data-stu-id="8904d-110">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="8904d-111">Interage com o host e não com um convidado do WOW64</span><span class="sxs-lookup"><span data-stu-id="8904d-111">Interacts with the host and not a WOW64 guest</span></span>

> [!Note]  
> <span data-ttu-id="8904d-112">Essa constante está disponível a partir do Windows 10, versão 1607 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="8904d-112">This constant is available starting with Windows 10, version 1607 and Windows Server 2016.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-113"><span id="IMAGE_FILE_MACHINE_I386"></span><span id="image_file_machine_i386"></span>**Arquivo de imagem/ \_ \_ computador \_ i386**</span><span class="sxs-lookup"><span data-stu-id="8904d-113"><span id="IMAGE_FILE_MACHINE_I386"></span><span id="image_file_machine_i386"></span>**IMAGE\_FILE\_MACHINE\_I386**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-114">0x014c</span><span class="sxs-lookup"><span data-stu-id="8904d-114">0x014c</span></span>
</dt> <dt>



<span data-ttu-id="8904d-115">Intel 386</span><span class="sxs-lookup"><span data-stu-id="8904d-115">Intel 386</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-116"><span id="IMAGE_FILE_MACHINE_R3000"></span><span id="image_file_machine_r3000"></span>**\_R3000 da \_ máquina do arquivo de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="8904d-116"><span id="IMAGE_FILE_MACHINE_R3000"></span><span id="image_file_machine_r3000"></span>**IMAGE\_FILE\_MACHINE\_R3000**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-117">0x0162</span><span class="sxs-lookup"><span data-stu-id="8904d-117">0x0162</span></span>
</dt> <dt>



<span data-ttu-id="8904d-118">MIPS little-endian, 0x160 big-endian</span><span class="sxs-lookup"><span data-stu-id="8904d-118">MIPS little-endian, 0x160 big-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-119"><span id="IMAGE_FILE_MACHINE_R4000"></span><span id="image_file_machine_r4000"></span>**\_R4000 da \_ máquina do arquivo de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="8904d-119"><span id="IMAGE_FILE_MACHINE_R4000"></span><span id="image_file_machine_r4000"></span>**IMAGE\_FILE\_MACHINE\_R4000**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-120">0x0166</span><span class="sxs-lookup"><span data-stu-id="8904d-120">0x0166</span></span>
</dt> <dt>



<span data-ttu-id="8904d-121">MIPS little-endian</span><span class="sxs-lookup"><span data-stu-id="8904d-121">MIPS little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-122"><span id="IMAGE_FILE_MACHINE_R10000"></span><span id="image_file_machine_r10000"></span>**\_R10000 da \_ máquina do arquivo de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="8904d-122"><span id="IMAGE_FILE_MACHINE_R10000"></span><span id="image_file_machine_r10000"></span>**IMAGE\_FILE\_MACHINE\_R10000**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-123">0x0168</span><span class="sxs-lookup"><span data-stu-id="8904d-123">0x0168</span></span>
</dt> <dt>



<span data-ttu-id="8904d-124">MIPS little-endian</span><span class="sxs-lookup"><span data-stu-id="8904d-124">MIPS little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-125"><span id="IMAGE_FILE_MACHINE_WCEMIPSV2"></span><span id="image_file_machine_wcemipsv2"></span>**\_WCEMIPSV2 da \_ máquina do arquivo de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="8904d-125"><span id="IMAGE_FILE_MACHINE_WCEMIPSV2"></span><span id="image_file_machine_wcemipsv2"></span>**IMAGE\_FILE\_MACHINE\_WCEMIPSV2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-126">0x0169</span><span class="sxs-lookup"><span data-stu-id="8904d-126">0x0169</span></span>
</dt> <dt>



<span data-ttu-id="8904d-127">MIPS little-endian Stone v2</span><span class="sxs-lookup"><span data-stu-id="8904d-127">MIPS little-endian WCE v2</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-128"><span id="IMAGE_FILE_MACHINE_ALPHA"></span><span id="image_file_machine_alpha"></span>**computador de arquivo de imagem \_ \_ \_ Alpha**</span><span class="sxs-lookup"><span data-stu-id="8904d-128"><span id="IMAGE_FILE_MACHINE_ALPHA"></span><span id="image_file_machine_alpha"></span>**IMAGE\_FILE\_MACHINE\_ALPHA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-129">0x0184</span><span class="sxs-lookup"><span data-stu-id="8904d-129">0x0184</span></span>
</dt> <dt>



<span data-ttu-id="8904d-130">Alpha \_ AXP</span><span class="sxs-lookup"><span data-stu-id="8904d-130">Alpha\_AXP</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-131"><span id="IMAGE_FILE_MACHINE_SH3"></span><span id="image_file_machine_sh3"></span>**\_SH3 da \_ máquina do arquivo de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="8904d-131"><span id="IMAGE_FILE_MACHINE_SH3"></span><span id="image_file_machine_sh3"></span>**IMAGE\_FILE\_MACHINE\_SH3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-132">0x01a2</span><span class="sxs-lookup"><span data-stu-id="8904d-132">0x01a2</span></span>
</dt> <dt>



<span data-ttu-id="8904d-133">SH3 little-endian</span><span class="sxs-lookup"><span data-stu-id="8904d-133">SH3 little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-134"><span id="IMAGE_FILE_MACHINE_SH3DSP"></span><span id="image_file_machine_sh3dsp"></span>**\_SH3DSP da \_ máquina do arquivo de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="8904d-134"><span id="IMAGE_FILE_MACHINE_SH3DSP"></span><span id="image_file_machine_sh3dsp"></span>**IMAGE\_FILE\_MACHINE\_SH3DSP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-135">0x01a3</span><span class="sxs-lookup"><span data-stu-id="8904d-135">0x01a3</span></span>
</dt> <dt>



<span data-ttu-id="8904d-136">SH3DSP</span><span class="sxs-lookup"><span data-stu-id="8904d-136">SH3DSP</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-137"><span id="IMAGE_FILE_MACHINE_SH3E"></span><span id="image_file_machine_sh3e"></span>**\_SH3E da \_ máquina do arquivo de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="8904d-137"><span id="IMAGE_FILE_MACHINE_SH3E"></span><span id="image_file_machine_sh3e"></span>**IMAGE\_FILE\_MACHINE\_SH3E**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-138">0x01a4</span><span class="sxs-lookup"><span data-stu-id="8904d-138">0x01a4</span></span>
</dt> <dt>



<span data-ttu-id="8904d-139">SH3E little-endian</span><span class="sxs-lookup"><span data-stu-id="8904d-139">SH3E little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-140"><span id="IMAGE_FILE_MACHINE_SH4"></span><span id="image_file_machine_sh4"></span>**\_Sh4 da \_ máquina do arquivo de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="8904d-140"><span id="IMAGE_FILE_MACHINE_SH4"></span><span id="image_file_machine_sh4"></span>**IMAGE\_FILE\_MACHINE\_SH4**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-141">0x01a6</span><span class="sxs-lookup"><span data-stu-id="8904d-141">0x01a6</span></span>
</dt> <dt>



<span data-ttu-id="8904d-142">SH4 little-endian</span><span class="sxs-lookup"><span data-stu-id="8904d-142">SH4 little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-143"><span id="IMAGE_FILE_MACHINE_SH5"></span><span id="image_file_machine_sh5"></span>**\_SH5 da \_ máquina do arquivo de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="8904d-143"><span id="IMAGE_FILE_MACHINE_SH5"></span><span id="image_file_machine_sh5"></span>**IMAGE\_FILE\_MACHINE\_SH5**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-144">0x01a8</span><span class="sxs-lookup"><span data-stu-id="8904d-144">0x01a8</span></span>
</dt> <dt>



<span data-ttu-id="8904d-145">SH5</span><span class="sxs-lookup"><span data-stu-id="8904d-145">SH5</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-146"><span id="IMAGE_FILE_MACHINE_ARM"></span><span id="image_file_machine_arm"></span>**\_ARM de \_ máquina de arquivo de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="8904d-146"><span id="IMAGE_FILE_MACHINE_ARM"></span><span id="image_file_machine_arm"></span>**IMAGE\_FILE\_MACHINE\_ARM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-147">0x01c0</span><span class="sxs-lookup"><span data-stu-id="8904d-147">0x01c0</span></span>
</dt> <dt>



<span data-ttu-id="8904d-148">Little-Endian ARM</span><span class="sxs-lookup"><span data-stu-id="8904d-148">ARM Little-Endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-149"><span id="IMAGE_FILE_MACHINE_THUMB"></span><span id="image_file_machine_thumb"></span>**\_miniatura do \_ computador do arquivo de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="8904d-149"><span id="IMAGE_FILE_MACHINE_THUMB"></span><span id="image_file_machine_thumb"></span>**IMAGE\_FILE\_MACHINE\_THUMB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-150">0x01c2</span><span class="sxs-lookup"><span data-stu-id="8904d-150">0x01c2</span></span>
</dt> <dt>



<span data-ttu-id="8904d-151">Little-Endian ARM Thumb/Thumb-2</span><span class="sxs-lookup"><span data-stu-id="8904d-151">ARM Thumb/Thumb-2 Little-Endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-152"><span id="IMAGE_FILE_MACHINE_ARMNT"></span><span id="image_file_machine_armnt"></span>**\_ARMNT da \_ máquina do arquivo de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="8904d-152"><span id="IMAGE_FILE_MACHINE_ARMNT"></span><span id="image_file_machine_armnt"></span>**IMAGE\_FILE\_MACHINE\_ARMNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-153">0x01c4</span><span class="sxs-lookup"><span data-stu-id="8904d-153">0x01c4</span></span>
</dt> <dt>



<span data-ttu-id="8904d-154">ARM Thumb-2 Little-Endian</span><span class="sxs-lookup"><span data-stu-id="8904d-154">ARM Thumb-2 Little-Endian</span></span>

> [!Note]  
> <span data-ttu-id="8904d-155">Essa constante está disponível a partir do Windows 7 e do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="8904d-155">This constant is available starting with Windows 7 and Windows Server 2008 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-156"><span id="IMAGE_FILE_MACHINE_AM33"></span><span id="image_file_machine_am33"></span>**\_AM33 da \_ máquina do arquivo de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="8904d-156"><span id="IMAGE_FILE_MACHINE_AM33"></span><span id="image_file_machine_am33"></span>**IMAGE\_FILE\_MACHINE\_AM33**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-157">0x01d3</span><span class="sxs-lookup"><span data-stu-id="8904d-157">0x01d3</span></span>
</dt> <dt>



<span data-ttu-id="8904d-158">TAM33BD</span><span class="sxs-lookup"><span data-stu-id="8904d-158">TAM33BD</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-159"><span id="IMAGE_FILE_MACHINE_POWERPC"></span><span id="image_file_machine_powerpc"></span>**\_POWERPC de \_ máquina de arquivo de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="8904d-159"><span id="IMAGE_FILE_MACHINE_POWERPC"></span><span id="image_file_machine_powerpc"></span>**IMAGE\_FILE\_MACHINE\_POWERPC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-160">0x01F0</span><span class="sxs-lookup"><span data-stu-id="8904d-160">0x01F0</span></span>
</dt> <dt>



<span data-ttu-id="8904d-161">IBM PowerPC Little-Endian</span><span class="sxs-lookup"><span data-stu-id="8904d-161">IBM PowerPC Little-Endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-162"><span id="IMAGE_FILE_MACHINE_POWERPCFP"></span><span id="image_file_machine_powerpcfp"></span>**\_POWERPCFP da \_ máquina do arquivo de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="8904d-162"><span id="IMAGE_FILE_MACHINE_POWERPCFP"></span><span id="image_file_machine_powerpcfp"></span>**IMAGE\_FILE\_MACHINE\_POWERPCFP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-163">0x01f1</span><span class="sxs-lookup"><span data-stu-id="8904d-163">0x01f1</span></span>
</dt> <dt>



<span data-ttu-id="8904d-164">POWERPCFP</span><span class="sxs-lookup"><span data-stu-id="8904d-164">POWERPCFP</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-165"><span id="IMAGE_FILE_MACHINE_IA64"></span><span id="image_file_machine_ia64"></span>**Computador de arquivo de imagem \_ \_ \_ IA64**</span><span class="sxs-lookup"><span data-stu-id="8904d-165"><span id="IMAGE_FILE_MACHINE_IA64"></span><span id="image_file_machine_ia64"></span>**IMAGE\_FILE\_MACHINE\_IA64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-166">0x0200</span><span class="sxs-lookup"><span data-stu-id="8904d-166">0x0200</span></span>
</dt> <dt>



<span data-ttu-id="8904d-167">Intel 64</span><span class="sxs-lookup"><span data-stu-id="8904d-167">Intel 64</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-168"><span id="IMAGE_FILE_MACHINE_MIPS16"></span><span id="image_file_machine_mips16"></span>**\_MIPS16 da \_ máquina do arquivo de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="8904d-168"><span id="IMAGE_FILE_MACHINE_MIPS16"></span><span id="image_file_machine_mips16"></span>**IMAGE\_FILE\_MACHINE\_MIPS16**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-169">0x0266</span><span class="sxs-lookup"><span data-stu-id="8904d-169">0x0266</span></span>
</dt> <dt>



<span data-ttu-id="8904d-170">MIPS</span><span class="sxs-lookup"><span data-stu-id="8904d-170">MIPS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-171"><span id="IMAGE_FILE_MACHINE_ALPHA64"></span><span id="image_file_machine_alpha64"></span>**\_ALPHA64 da \_ máquina do arquivo de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="8904d-171"><span id="IMAGE_FILE_MACHINE_ALPHA64"></span><span id="image_file_machine_alpha64"></span>**IMAGE\_FILE\_MACHINE\_ALPHA64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-172">0x0284</span><span class="sxs-lookup"><span data-stu-id="8904d-172">0x0284</span></span>
</dt> <dt>



<span data-ttu-id="8904d-173">ALPHA64</span><span class="sxs-lookup"><span data-stu-id="8904d-173">ALPHA64</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-174"><span id="IMAGE_FILE_MACHINE_MIPSFPU"></span><span id="image_file_machine_mipsfpu"></span>**\_MIPSFPU da \_ máquina do arquivo de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="8904d-174"><span id="IMAGE_FILE_MACHINE_MIPSFPU"></span><span id="image_file_machine_mipsfpu"></span>**IMAGE\_FILE\_MACHINE\_MIPSFPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-175">0x0366</span><span class="sxs-lookup"><span data-stu-id="8904d-175">0x0366</span></span>
</dt> <dt>



<span data-ttu-id="8904d-176">MIPS</span><span class="sxs-lookup"><span data-stu-id="8904d-176">MIPS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-177"><span id="IMAGE_FILE_MACHINE_MIPSFPU16"></span><span id="image_file_machine_mipsfpu16"></span>**\_MIPSFPU16 da \_ máquina do arquivo de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="8904d-177"><span id="IMAGE_FILE_MACHINE_MIPSFPU16"></span><span id="image_file_machine_mipsfpu16"></span>**IMAGE\_FILE\_MACHINE\_MIPSFPU16**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-178">0x0466</span><span class="sxs-lookup"><span data-stu-id="8904d-178">0x0466</span></span>
</dt> <dt>



<span data-ttu-id="8904d-179">MIPS</span><span class="sxs-lookup"><span data-stu-id="8904d-179">MIPS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-180"><span id="IMAGE_FILE_MACHINE_AXP64"></span><span id="image_file_machine_axp64"></span>**\_AXP64 da \_ máquina do arquivo de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="8904d-180"><span id="IMAGE_FILE_MACHINE_AXP64"></span><span id="image_file_machine_axp64"></span>**IMAGE\_FILE\_MACHINE\_AXP64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-181">0x0284</span><span class="sxs-lookup"><span data-stu-id="8904d-181">0x0284</span></span>
</dt> <dt>



<span data-ttu-id="8904d-182">AXP64</span><span class="sxs-lookup"><span data-stu-id="8904d-182">AXP64</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-183"><span id="IMAGE_FILE_MACHINE_TRICORE"></span><span id="image_file_machine_tricore"></span>**computador de arquivo de imagem \_ \_ \_ Tricore**</span><span class="sxs-lookup"><span data-stu-id="8904d-183"><span id="IMAGE_FILE_MACHINE_TRICORE"></span><span id="image_file_machine_tricore"></span>**IMAGE\_FILE\_MACHINE\_TRICORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-184">0x0520</span><span class="sxs-lookup"><span data-stu-id="8904d-184">0x0520</span></span>
</dt> <dt>



<span data-ttu-id="8904d-185">Infineon</span><span class="sxs-lookup"><span data-stu-id="8904d-185">Infineon</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-186"><span id="IMAGE_FILE_MACHINE_CEF"></span><span id="image_file_machine_cef"></span>**máquina de arquivo de imagem \_ \_ \_ CEF**</span><span class="sxs-lookup"><span data-stu-id="8904d-186"><span id="IMAGE_FILE_MACHINE_CEF"></span><span id="image_file_machine_cef"></span>**IMAGE\_FILE\_MACHINE\_CEF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-187">0x0CEF</span><span class="sxs-lookup"><span data-stu-id="8904d-187">0x0CEF</span></span>
</dt> <dt>



<span data-ttu-id="8904d-188">CEF</span><span class="sxs-lookup"><span data-stu-id="8904d-188">CEF</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-189"><span id="IMAGE_FILE_MACHINE_EBC"></span><span id="image_file_machine_ebc"></span>**computador de arquivo de imagem \_ \_ \_ EBC**</span><span class="sxs-lookup"><span data-stu-id="8904d-189"><span id="IMAGE_FILE_MACHINE_EBC"></span><span id="image_file_machine_ebc"></span>**IMAGE\_FILE\_MACHINE\_EBC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-190">0x0EBC</span><span class="sxs-lookup"><span data-stu-id="8904d-190">0x0EBC</span></span>
</dt> <dt>



<span data-ttu-id="8904d-191">Código de byte EFI</span><span class="sxs-lookup"><span data-stu-id="8904d-191">EFI Byte Code</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-192"><span id="IMAGE_FILE_MACHINE_AMD64"></span><span id="image_file_machine_amd64"></span>**Máquina de arquivo de imagem \_ \_ \_ AMD64**</span><span class="sxs-lookup"><span data-stu-id="8904d-192"><span id="IMAGE_FILE_MACHINE_AMD64"></span><span id="image_file_machine_amd64"></span>**IMAGE\_FILE\_MACHINE\_AMD64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-193">0x8664</span><span class="sxs-lookup"><span data-stu-id="8904d-193">0x8664</span></span>
</dt> <dt>



<span data-ttu-id="8904d-194">AMD64 (K8)</span><span class="sxs-lookup"><span data-stu-id="8904d-194">AMD64 (K8)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-195"><span id="IMAGE_FILE_MACHINE_M32R"></span><span id="image_file_machine_m32r"></span>**\_M32R da \_ máquina do arquivo de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="8904d-195"><span id="IMAGE_FILE_MACHINE_M32R"></span><span id="image_file_machine_m32r"></span>**IMAGE\_FILE\_MACHINE\_M32R**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-196">0x9041</span><span class="sxs-lookup"><span data-stu-id="8904d-196">0x9041</span></span>
</dt> <dt>



<span data-ttu-id="8904d-197">M32R little-endian</span><span class="sxs-lookup"><span data-stu-id="8904d-197">M32R little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-198"><span id="IMAGE_FILE_MACHINE_ARM64"></span><span id="image_file_machine_arm64"></span>**\_ARM64 da \_ máquina do arquivo de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="8904d-198"><span id="IMAGE_FILE_MACHINE_ARM64"></span><span id="image_file_machine_arm64"></span>**IMAGE\_FILE\_MACHINE\_ARM64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-199">0xAA64</span><span class="sxs-lookup"><span data-stu-id="8904d-199">0xAA64</span></span>
</dt> <dt>



<span data-ttu-id="8904d-200">Little-Endian ARM64</span><span class="sxs-lookup"><span data-stu-id="8904d-200">ARM64 Little-Endian</span></span>

> [!Note]  
> <span data-ttu-id="8904d-201">Essa constante está disponível a partir do Windows 8.1 e do Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="8904d-201">This constant is available starting with Windows 8.1 and Windows Server 2012 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="8904d-202"><span id="IMAGE_FILE_MACHINE_CEE"></span><span id="image_file_machine_cee"></span>**\_CEE da \_ máquina do arquivo de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="8904d-202"><span id="IMAGE_FILE_MACHINE_CEE"></span><span id="image_file_machine_cee"></span>**IMAGE\_FILE\_MACHINE\_CEE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8904d-203">0xC0EE</span><span class="sxs-lookup"><span data-stu-id="8904d-203">0xC0EE</span></span>
</dt> <dt>



<span data-ttu-id="8904d-204">CEE</span><span class="sxs-lookup"><span data-stu-id="8904d-204">CEE</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8904d-205">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8904d-205">Requirements</span></span>



| <span data-ttu-id="8904d-206">Requisito</span><span class="sxs-lookup"><span data-stu-id="8904d-206">Requirement</span></span> | <span data-ttu-id="8904d-207">Valor</span><span class="sxs-lookup"><span data-stu-id="8904d-207">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8904d-208">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8904d-208">Minimum supported client</span></span><br/> | <span data-ttu-id="8904d-209">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8904d-209">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8904d-210">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8904d-210">Minimum supported server</span></span><br/> | <span data-ttu-id="8904d-211">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8904d-211">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8904d-212">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8904d-212">Header</span></span><br/>                   | <dl> <span data-ttu-id="8904d-213"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="8904d-213"><dt>Winnt.h</dt></span></span> </dl> |



 

 




