---
title: Estrutura GUESTOSVERSIONINFOEX (VPCCOMInterfaces. h)
description: Contém informações de versão do sistema operacional para o sistema operacional convidado.
ms.assetid: 9cfd5cac-c8ea-4e09-ba47-3563554bdafa
keywords:
- Virtual PC de estrutura GUESTOSVERSIONINFOEX
topic_type:
- apiref
api_name:
- GUESTOSVERSIONINFOEX
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b633838affb9a9ff1453a0c49de9588428b038fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085755"
---
# <a name="guestosversioninfoex-structure"></a><span data-ttu-id="166f3-104">Estrutura GUESTOSVERSIONINFOEX</span><span class="sxs-lookup"><span data-stu-id="166f3-104">GUESTOSVERSIONINFOEX structure</span></span>

<span data-ttu-id="166f3-105">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="166f3-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="166f3-106">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="166f3-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="166f3-107">Contém informações de versão do sistema operacional para o sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="166f3-107">Contains operating system version information for the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="166f3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="166f3-108">Syntax</span></span>


```C++
typedef struct _GUESTOSVERSIONINFOEX {
  long    dwOSVersionInfoSize;
  long    dwMajorVersion;
  long    dwMinorVersion;
  long    dwBuildNumber;
  long    dwPlatformId;
  wchar_t szCSDVersion[128];
  short   wServicePackMajor;
  short   wServicePackMinor;
  short   wSuiteMask;
  byte    wProductType;
  byte    wReserved;
} GUESTOSVERSIONINFOEX;
```



## <a name="members"></a><span data-ttu-id="166f3-109">Membros</span><span class="sxs-lookup"><span data-stu-id="166f3-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="166f3-110">**dwOSVersionInfoSize**</span><span class="sxs-lookup"><span data-stu-id="166f3-110">**dwOSVersionInfoSize**</span></span>
</dt> <dd>

<span data-ttu-id="166f3-111">O tamanho dessa estrutura de dados, em bytes.</span><span class="sxs-lookup"><span data-stu-id="166f3-111">The size of this data structure, in bytes.</span></span> <span data-ttu-id="166f3-112">Defina este membro como `sizeof(GUESTOSVERSIONINFOEX)` .</span><span class="sxs-lookup"><span data-stu-id="166f3-112">Set this member to `sizeof(GUESTOSVERSIONINFOEX)`.</span></span>

</dd> <dt>

<span data-ttu-id="166f3-113">**dwMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="166f3-113">**dwMajorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="166f3-114">O número da versão principal.</span><span class="sxs-lookup"><span data-stu-id="166f3-114">The major version number.</span></span>

</dd> <dt>

<span data-ttu-id="166f3-115">**dwMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="166f3-115">**dwMinorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="166f3-116">O número da versão secundária.</span><span class="sxs-lookup"><span data-stu-id="166f3-116">The minor version number.</span></span>

</dd> <dt>

<span data-ttu-id="166f3-117">**dwBuildNumber**</span><span class="sxs-lookup"><span data-stu-id="166f3-117">**dwBuildNumber**</span></span>
</dt> <dd>

<span data-ttu-id="166f3-118">O número de build.</span><span class="sxs-lookup"><span data-stu-id="166f3-118">The build number.</span></span>

</dd> <dt>

<span data-ttu-id="166f3-119">**dwPlatformId**</span><span class="sxs-lookup"><span data-stu-id="166f3-119">**dwPlatformId**</span></span>
</dt> <dd>

<span data-ttu-id="166f3-120">A plataforma do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="166f3-120">The operating system platform.</span></span> <span data-ttu-id="166f3-121">Esse membro pode ser **ver a \_ plataforma \_ Win32 \_ NT** (2).</span><span class="sxs-lookup"><span data-stu-id="166f3-121">This member can be **VER\_PLATFORM\_WIN32\_NT** (2).</span></span>

</dd> <dt>

<span data-ttu-id="166f3-122">**szCSDVersion**</span><span class="sxs-lookup"><span data-stu-id="166f3-122">**szCSDVersion**</span></span>
</dt> <dd>

<span data-ttu-id="166f3-123">Uma cadeia de caracteres terminada em nulo, como "Service Pack 3", que indica o Service Pack mais recente instalado no sistema.</span><span class="sxs-lookup"><span data-stu-id="166f3-123">A null-terminated string, such as "Service Pack 3", that indicates the latest Service Pack installed on the system.</span></span> <span data-ttu-id="166f3-124">Se nenhum Service Pack tiver sido instalado, a cadeia de caracteres estará vazia.</span><span class="sxs-lookup"><span data-stu-id="166f3-124">If no Service Pack has been installed, the string is empty.</span></span>

</dd> <dt>

<span data-ttu-id="166f3-125">**wServicePackMajor**</span><span class="sxs-lookup"><span data-stu-id="166f3-125">**wServicePackMajor**</span></span>
</dt> <dd>

<span data-ttu-id="166f3-126">O número de versão principal do Service Pack mais recente instalado.</span><span class="sxs-lookup"><span data-stu-id="166f3-126">The major version number of the latest Service Pack installed.</span></span>

</dd> <dt>

<span data-ttu-id="166f3-127">**wServicePackMinor**</span><span class="sxs-lookup"><span data-stu-id="166f3-127">**wServicePackMinor**</span></span>
</dt> <dd>

<span data-ttu-id="166f3-128">O número de versão secundária do Service Pack mais recente instalado.</span><span class="sxs-lookup"><span data-stu-id="166f3-128">The minor version number of the latest Service Pack installed.</span></span>

</dd> <dt>

<span data-ttu-id="166f3-129">**wSuiteMask**</span><span class="sxs-lookup"><span data-stu-id="166f3-129">**wSuiteMask**</span></span>
</dt> <dd>

<span data-ttu-id="166f3-130">Um bitmask que identifica os pacotes de produtos disponíveis no sistema.</span><span class="sxs-lookup"><span data-stu-id="166f3-130">A bitmask that identifies the product suites available on the system.</span></span> <span data-ttu-id="166f3-131">Esse membro pode ser uma combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="166f3-131">This member can be a combination of the following values.</span></span>



| <span data-ttu-id="166f3-132">Valor</span><span class="sxs-lookup"><span data-stu-id="166f3-132">Value</span></span>                                                                                                                                                                                                                                                                                          | <span data-ttu-id="166f3-133">Significado</span><span class="sxs-lookup"><span data-stu-id="166f3-133">Meaning</span></span>                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_SUITE_BACKOFFICE"></span><span id="ver_suite_backoffice"></span><dl> <span data-ttu-id="166f3-134"><dt>**Ver \_ PACOTE de \_ backoffice**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="166f3-134"><dt>**VER\_SUITE\_BACKOFFICE**</dt> <dt>0x00000004</dt></span></span> </dl>                                            | <span data-ttu-id="166f3-135">Os componentes do Microsoft BackOffice são instalados.</span><span class="sxs-lookup"><span data-stu-id="166f3-135">Microsoft BackOffice components are installed.</span></span><br/>                                                                                                                                                         |
| <span id="VER_SUITE_BLADE"></span><span id="ver_suite_blade"></span><dl> <span data-ttu-id="166f3-136"><dt>**Ver \_ 0x00000400 \_ Blade Suite**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="166f3-136"><dt>**VER\_SUITE\_BLADE**</dt> <dt>0x00000400</dt></span></span> </dl>                                                           | <span data-ttu-id="166f3-137">O Windows Server 2003, Web Edition está instalado.</span><span class="sxs-lookup"><span data-stu-id="166f3-137">Windows Server 2003, Web Edition is installed.</span></span><br/>                                                                                                                                                         |
| <span id="VER_SUITE_COMPUTE_SERVER"></span><span id="ver_suite_compute_server"></span><dl> <span data-ttu-id="166f3-138"><dt>**Ver \_ Pacote de \_ computação \_ do Suite**</dt> <dt>0x00004000</dt></span><span class="sxs-lookup"><span data-stu-id="166f3-138"><dt>**VER\_SUITE\_COMPUTE\_SERVER**</dt> <dt>0x00004000</dt></span></span> </dl>                               | <span data-ttu-id="166f3-139">O Windows Server 2003, Compute Cluster Edition, está instalado.</span><span class="sxs-lookup"><span data-stu-id="166f3-139">Windows Server 2003, Compute Cluster Edition is installed.</span></span><br/>                                                                                                                                             |
| <span id="VER_SUITE_DATACENTER"></span><span id="ver_suite_datacenter"></span><dl> <span data-ttu-id="166f3-140"><dt>**Ver \_ 0x00000080 do \_ DATAcenter do pacote**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="166f3-140"><dt>**VER\_SUITE\_DATACENTER**</dt> <dt>0x00000080</dt></span></span> </dl>                                            | <span data-ttu-id="166f3-141">O Windows Server 2008 Datacenter, o Windows Server 2003, o Datacenter Edition ou o Windows 2000 Datacenter Server está instalado.</span><span class="sxs-lookup"><span data-stu-id="166f3-141">Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition, or Windows 2000 Datacenter Server is installed.</span></span><br/>                                                                               |
| <span id="VER_SUITE_ENTERPRISE"></span><span id="ver_suite_enterprise"></span><dl> <span data-ttu-id="166f3-142"><dt>**Ver \_ SUITE \_ Enterprise**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="166f3-142"><dt>**VER\_SUITE\_ENTERPRISE**</dt> <dt>0x00000002</dt></span></span> </dl>                                            | <span data-ttu-id="166f3-143">O Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition ou Windows 2000 Advanced Server está instalado.</span><span class="sxs-lookup"><span data-stu-id="166f3-143">Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition, or Windows 2000 Advanced Server is installed.</span></span> <span data-ttu-id="166f3-144">Consulte a seção comentários para obter mais informações sobre este sinalizador de bit.</span><span class="sxs-lookup"><span data-stu-id="166f3-144">Refer to the Remarks section for more information about this bit flag.</span></span><br/>          |
| <span id="VER_SUITE_EMBEDDEDNT"></span><span id="ver_suite_embeddednt"></span><dl> <span data-ttu-id="166f3-145"><dt>**Ver \_ SUITE \_ EMBEDDEDNT**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="166f3-145"><dt>**VER\_SUITE\_EMBEDDEDNT**</dt> <dt>0x00000040</dt></span></span> </dl>                                            | <span data-ttu-id="166f3-146">O Windows XP Embedded está instalado.</span><span class="sxs-lookup"><span data-stu-id="166f3-146">Windows XP Embedded is installed.</span></span><br/>                                                                                                                                                                      |
| <span id="VER_SUITE_PERSONAL"></span><span id="ver_suite_personal"></span><dl> <span data-ttu-id="166f3-147"><dt>**Ver \_ 0x00000200 \_ pessoal de Suite**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="166f3-147"><dt>**VER\_SUITE\_PERSONAL**</dt> <dt>0x00000200</dt></span></span> </dl>                                                  | <span data-ttu-id="166f3-148">O Windows Vista Home Premium, o Windows Vista Home Basic ou o Windows XP Home Edition está instalado.</span><span class="sxs-lookup"><span data-stu-id="166f3-148">Windows Vista Home Premium, Windows Vista Home Basic, or Windows XP Home Edition is installed.</span></span><br/>                                                                                                         |
| <span id="VER_SUITE_SINGLEUSERTS"></span><span id="ver_suite_singleuserts"></span><dl> <span data-ttu-id="166f3-149"><dt>**Ver \_ SUITE \_ SINGLEUSERTS**</dt> <dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="166f3-149"><dt>**VER\_SUITE\_SINGLEUSERTS**</dt> <dt>0x00000100</dt></span></span> </dl>                                      | <span data-ttu-id="166f3-150">Há suporte para Área de Trabalho Remota, mas há suporte para apenas uma sessão interativa.</span><span class="sxs-lookup"><span data-stu-id="166f3-150">Remote Desktop is supported, but only one interactive session is supported.</span></span> <span data-ttu-id="166f3-151">Esse valor é definido, a menos que o sistema esteja sendo executado no modo de servidor de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="166f3-151">This value is set unless the system is running in application server mode.</span></span><br/>                                                 |
| <span id="VER_SUITE_SMALLBUSINESS"></span><span id="ver_suite_smallbusiness"></span><dl> <span data-ttu-id="166f3-152"><dt>**Ver \_ PACOTE do \_ SMALLBUSINESS**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="166f3-152"><dt>**VER\_SUITE\_SMALLBUSINESS**</dt> <dt>0x00000001</dt></span></span> </dl>                                   | <span data-ttu-id="166f3-153">O Microsoft Small Business Server já foi instalado no sistema, mas pode ter sido atualizado para outra versão do Windows.</span><span class="sxs-lookup"><span data-stu-id="166f3-153">Microsoft Small Business Server was once installed on the system, but may have been upgraded to another version of Windows.</span></span> <span data-ttu-id="166f3-154">Consulte a seção comentários para obter mais informações sobre este sinalizador de bit.</span><span class="sxs-lookup"><span data-stu-id="166f3-154">Refer to the Remarks section for more information about this bit flag.</span></span><br/>     |
| <span id="VER_SUITE_SMALLBUSINESS_RESTRICTED"></span><span id="ver_suite_smallbusiness_restricted"></span><dl> <span data-ttu-id="166f3-155"><dt>**Ver \_ CONJUNTO de o do \_ SMALLBUSINESS \_ Restricted**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="166f3-155"><dt>**VER\_SUITE\_SMALLBUSINESS\_RESTRICTED**</dt> <dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="166f3-156">O Microsoft Small Business Server é instalado com a licença de cliente restritiva em vigor.</span><span class="sxs-lookup"><span data-stu-id="166f3-156">Microsoft Small Business Server is installed with the restrictive client license in force.</span></span> <span data-ttu-id="166f3-157">Consulte a seção comentários para obter mais informações sobre este sinalizador de bit.</span><span class="sxs-lookup"><span data-stu-id="166f3-157">Refer to the Remarks section for more information about this bit flag.</span></span><br/>                                      |
| <span id="VER_SUITE_STORAGE_SERVER"></span><span id="ver_suite_storage_server"></span><dl> <span data-ttu-id="166f3-158"><dt>**Ver \_ CONJUNTO de 0x00002000 \_ \_ do servidor de armazenamento**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="166f3-158"><dt>**VER\_SUITE\_STORAGE\_SERVER**</dt> <dt>0x00002000</dt></span></span> </dl>                               | <span data-ttu-id="166f3-159">O Windows Storage Server 2003 R2 ou o Windows Storage Server 2003 está instalado.</span><span class="sxs-lookup"><span data-stu-id="166f3-159">Windows Storage Server 2003 R2 or Windows Storage Server 2003is installed.</span></span><br/>                                                                                                                             |
| <span id="VER_SUITE_TERMINAL"></span><span id="ver_suite_terminal"></span><dl> <span data-ttu-id="166f3-160"><dt>**Ver \_ \_Terminal do Suite**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="166f3-160"><dt>**VER\_SUITE\_TERMINAL**</dt> <dt>0x00000010</dt></span></span> </dl>                                                  | <span data-ttu-id="166f3-161">Os serviços de terminal estão instalados.</span><span class="sxs-lookup"><span data-stu-id="166f3-161">Terminal Services is installed.</span></span> <span data-ttu-id="166f3-162">Esse valor é sempre definido.</span><span class="sxs-lookup"><span data-stu-id="166f3-162">This value is always set.</span></span><br/> <span data-ttu-id="166f3-163">Se **o \_ \_ terminal Suite ver** estiver definido, mas o **\_ \_ SINGLEUSERTS Suite** não estiver definido, o sistema estará sendo executado no modo de servidor de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="166f3-163">If **VER\_SUITE\_TERMINAL** is set but **VER\_SUITE\_SINGLEUSERTS** is not set, the system is running in application server mode.</span></span><br/> |
| <span id="VER_SUITE_WH_SERVER"></span><span id="ver_suite_wh_server"></span><dl> <span data-ttu-id="166f3-164"><dt>**Ver \_ 0x00008000 \_ \_ do servidor do Suite**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="166f3-164"><dt>**VER\_SUITE\_WH\_SERVER**</dt> <dt>0x00008000</dt></span></span> </dl>                                              | <span data-ttu-id="166f3-165">O Windows Home Server está instalado.</span><span class="sxs-lookup"><span data-stu-id="166f3-165">Windows Home Server is installed.</span></span><br/>                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="166f3-166">**wProductType**</span><span class="sxs-lookup"><span data-stu-id="166f3-166">**wProductType**</span></span>
</dt> <dd>

<span data-ttu-id="166f3-167">Quaisquer informações adicionais sobre o sistema.</span><span class="sxs-lookup"><span data-stu-id="166f3-167">Any additional information about the system.</span></span> <span data-ttu-id="166f3-168">Esse membro pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="166f3-168">This member can be one of the following values.</span></span>



| <span data-ttu-id="166f3-169">Valor</span><span class="sxs-lookup"><span data-stu-id="166f3-169">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="166f3-170">Significado</span><span class="sxs-lookup"><span data-stu-id="166f3-170">Meaning</span></span>                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_NT_DOMAIN_CONTROLLER"></span><span id="ver_nt_domain_controller"></span><dl> <span data-ttu-id="166f3-171"><dt>**Ver \_ 0x0000002 \_ do \_ controlador de domínio NT**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="166f3-171"><dt>**VER\_NT\_DOMAIN\_CONTROLLER**</dt> <dt>0x0000002</dt></span></span> </dl> | <span data-ttu-id="166f3-172">O sistema é um controlador de domínio e o sistema operacional é o Windows Server 2008 R2, o Windows Server 2008, o Windows Server 2003 R2, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="166f3-172">The system is a domain controller and the operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/>                                                                                                   |
| <span id="VER_NT_SERVER"></span><span id="ver_nt_server"></span><dl> <span data-ttu-id="166f3-173"><dt>**Ver \_ 0x0000003 NT \_ Server**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="166f3-173"><dt>**VER\_NT\_SERVER**</dt> <dt>0x0000003</dt></span></span> </dl>                                   | <span data-ttu-id="166f3-174">O sistema operacional é o Windows Server 2008 R2, o Windows Server 2008, o Windows Server 2003 R2, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="166f3-174">The operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/> <span data-ttu-id="166f3-175">Observe que um servidor que também é um controlador de domínio é relatado **como \_ \_ \_ controlador de domínio do NT**, não ver o **\_ \_ servidor NT**.</span><span class="sxs-lookup"><span data-stu-id="166f3-175">Note that a server that is also a domain controller is reported as **VER\_NT\_DOMAIN\_CONTROLLER**, not **VER\_NT\_SERVER**.</span></span><br/> |
| <span id="VER_NT_WORKSTATION"></span><span id="ver_nt_workstation"></span><dl> <span data-ttu-id="166f3-176"><dt>**Ver \_ NT \_ Workstation**</dt> <dt>0x0000001</dt></span><span class="sxs-lookup"><span data-stu-id="166f3-176"><dt>**VER\_NT\_WORKSTATION**</dt> <dt>0x0000001</dt></span></span> </dl>                    | <span data-ttu-id="166f3-177">O sistema operacional é o Windows 7, o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="166f3-177">The operating system is Windows 7, Windows Vista, Windows XP, or Windows 2000 Professional.</span></span><br/>                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="166f3-178">**wReserved**</span><span class="sxs-lookup"><span data-stu-id="166f3-178">**wReserved**</span></span>
</dt> <dd>

<span data-ttu-id="166f3-179">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="166f3-179">Reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="166f3-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="166f3-180">Requirements</span></span>



| <span data-ttu-id="166f3-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="166f3-181">Requirement</span></span> | <span data-ttu-id="166f3-182">Valor</span><span class="sxs-lookup"><span data-stu-id="166f3-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="166f3-183">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="166f3-183">Minimum supported client</span></span><br/> | <span data-ttu-id="166f3-184">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="166f3-184">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="166f3-185">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="166f3-185">Minimum supported server</span></span><br/> | <span data-ttu-id="166f3-186">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="166f3-186">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="166f3-187">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="166f3-187">End of client support</span></span><br/>    | <span data-ttu-id="166f3-188">Windows 7</span><span class="sxs-lookup"><span data-stu-id="166f3-188">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="166f3-189">Produto</span><span class="sxs-lookup"><span data-stu-id="166f3-189">Product</span></span><br/>                  | <span data-ttu-id="166f3-190">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="166f3-190">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="166f3-191">parâmetro</span><span class="sxs-lookup"><span data-stu-id="166f3-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="166f3-192"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="166f3-192"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="166f3-193">Confira também</span><span class="sxs-lookup"><span data-stu-id="166f3-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="166f3-194">**IVMGuestOS::GetOsVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="166f3-194">**IVMGuestOS::GetOsVersionInfo**</span></span>](ivmguestos-getosversioninfo.md)
</dt> </dl>

 

