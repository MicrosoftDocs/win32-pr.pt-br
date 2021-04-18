---
description: Recupera uma máscara de bits que identifica os conjuntos de produtos disponíveis no sistema. Se essa função for chamada em um aplicativo que é executado no contexto de um silo de servidores, a máscara do pacote para o silo do servidor será recuperada.
ms.assetid: 1D6434FD-D7BD-45F9-B7C3-238890AF9928
title: Função RtlGetSuiteMask (Ntddk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetSuiteMask
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: ed8d8906273d18125131251636bc6199d166547b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753077"
---
# <a name="rtlgetsuitemask-function"></a><span data-ttu-id="1d2f2-104">Função RtlGetSuiteMask</span><span class="sxs-lookup"><span data-stu-id="1d2f2-104">RtlGetSuiteMask function</span></span>

<span data-ttu-id="1d2f2-105">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1d2f2-106">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="1d2f2-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1d2f2-107">Recupera uma máscara de bits que identifica os conjuntos de produtos disponíveis no sistema.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-107">Retrieves a bit mask that identifies the product suites available on the system.</span></span> <span data-ttu-id="1d2f2-108">Se essa função for chamada em um aplicativo que é executado no contexto de um silo de servidores, a máscara do pacote para o silo do servidor será recuperada.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-108">If this function is called in an application that runs in the context of a server silo, the suite mask for the server silo is retrieved instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d2f2-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d2f2-109">Syntax</span></span>


```C++
ULONG NTAPI RtlGetSuiteMask(void);
```



## <a name="parameters"></a><span data-ttu-id="1d2f2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d2f2-110">Parameters</span></span>

<span data-ttu-id="1d2f2-111">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-111">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1d2f2-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1d2f2-112">Return value</span></span>

<span data-ttu-id="1d2f2-113">Uma máscara de bits que identifica os conjuntos de produtos disponíveis no sistema.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-113">A bit mask that identifies the product suites available on the system.</span></span> <span data-ttu-id="1d2f2-114">A máscara de bits pode incluir os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-114">The bit mask can include the following values.</span></span>



| <span data-ttu-id="1d2f2-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1d2f2-115">Return value</span></span>                                                                          | <span data-ttu-id="1d2f2-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="1d2f2-116">Description</span></span>                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1d2f2-117"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="1d2f2-117"><dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="1d2f2-118">O Microsoft Small Business Server já foi instalado no sistema, mas pode ter sido atualizado para outra versão do Windows.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-118">Microsoft Small Business Server was once installed on the system, but may have been upgraded to another version of Windows.</span></span> <span data-ttu-id="1d2f2-119">Consulte a seção comentários para obter mais informações sobre este sinalizador de bit.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-119">Refer to the Remarks section for more information about this bit flag.</span></span><br/>                                           |
| <dl> <span data-ttu-id="1d2f2-120"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="1d2f2-120"><dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="1d2f2-121">O Windows 10 Enterprise, Windows 8.1 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition ou Windows 2000 Advanced Server está instalado.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-121">Windows 10 Enterprise, Windows 8.1 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition, or Windows 2000 Advanced Server is installed.</span></span> <span data-ttu-id="1d2f2-122">Consulte a seção comentários para obter mais informações sobre este sinalizador de bit.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-122">Refer to the Remarks section for more information about this bit flag.</span></span><br/> |
| <dl> <span data-ttu-id="1d2f2-123"><dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="1d2f2-123"><dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="1d2f2-124">Os componentes do Microsoft BackOffice são instalados.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-124">Microsoft BackOffice components are installed.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="1d2f2-125"><dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="1d2f2-125"><dt>0x00000008</dt></span></span> </dl> | <span data-ttu-id="1d2f2-126">O Communications Server 2003, o Communications Server 2005, o Communications Server 2007 ou o Communications Server 2007 R2 está instalado.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-126">Communications Server 2003, Communications Server 2005, Communications Server 2007, or Communications Server 2007 R2 is installed.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="1d2f2-127"><dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="1d2f2-127"><dt>0x00000010</dt></span></span> </dl> | <span data-ttu-id="1d2f2-128">Os serviços de terminal estão instalados.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-128">Terminal Services is installed.</span></span> <span data-ttu-id="1d2f2-129">Esse valor é sempre definido.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-129">This value is always set.</span></span><br/> <span data-ttu-id="1d2f2-130">Se **TerminalServer** for definido, mas **SingleUserTS** não estiver definido, o sistema estará sendo executado no modo de servidor de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-130">If **TerminalServer** is set but **SingleUserTS** is not set, the system is running in application server mode.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="1d2f2-131"><dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="1d2f2-131"><dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="1d2f2-132">O Microsoft Small Business Server é instalado com a licença de cliente restritiva em vigor.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-132">Microsoft Small Business Server is installed with the restrictive client license in force.</span></span> <span data-ttu-id="1d2f2-133">Consulte a seção comentários para obter mais informações sobre este sinalizador de bit.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-133">Refer to the Remarks section for more information about this bit flag.</span></span><br/>                                                                            |
| <dl> <span data-ttu-id="1d2f2-134"><dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="1d2f2-134"><dt>0x00000040</dt></span></span> </dl> | <span data-ttu-id="1d2f2-135">O Windows XP Embedded está instalado.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-135">Windows XP Embedded is installed.</span></span><br/>                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="1d2f2-136"><dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="1d2f2-136"><dt>0x00000080</dt></span></span> </dl> | <span data-ttu-id="1d2f2-137">O Windows Server 2008 Datacenter, o Windows Server 2003, o Datacenter Edition ou o Windows 2000 Datacenter Server está instalado.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-137">Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition, or Windows 2000 Datacenter Server is installed.</span></span><br/>                                                                                                                     |
| <dl> <span data-ttu-id="1d2f2-138"><dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="1d2f2-138"><dt>0x00000100</dt></span></span> </dl> | <span data-ttu-id="1d2f2-139">Há suporte para Área de Trabalho Remota, mas há suporte para apenas uma sessão interativa.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-139">Remote Desktop is supported, but only one interactive session is supported.</span></span> <span data-ttu-id="1d2f2-140">Esse valor é definido, a menos que o sistema esteja sendo executado no modo de servidor de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-140">This value is set unless the system is running in application server mode.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="1d2f2-141"><dt>0x00000200</dt></span><span class="sxs-lookup"><span data-stu-id="1d2f2-141"><dt>0x00000200</dt></span></span> </dl> | <span data-ttu-id="1d2f2-142">O Windows Vista Home Premium, o Windows Vista Home Basic ou o Windows XP Home Edition está instalado.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-142">Windows Vista Home Premium, Windows Vista Home Basic, or Windows XP Home Edition is installed.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="1d2f2-143"><dt>0x00000400</dt></span><span class="sxs-lookup"><span data-stu-id="1d2f2-143"><dt>0x00000400</dt></span></span> </dl> | <span data-ttu-id="1d2f2-144">O Windows Server 2003, Web Edition está instalado.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-144">Windows Server 2003, Web Edition is installed.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="1d2f2-145"><dt>0x00002000</dt></span><span class="sxs-lookup"><span data-stu-id="1d2f2-145"><dt>0x00002000</dt></span></span> </dl> | <span data-ttu-id="1d2f2-146">O Windows Storage Server 2003 R2 ou o Windows Storage Server 2003 está instalado.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-146">Windows Storage Server 2003 R2 or Windows Storage Server 2003 is installed.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="1d2f2-147"><dt>0x00004000</dt></span><span class="sxs-lookup"><span data-stu-id="1d2f2-147"><dt>0x00004000</dt></span></span> </dl> | <span data-ttu-id="1d2f2-148">O Windows Server 2003, Compute Cluster Edition, está instalado.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-148">Windows Server 2003, Compute Cluster Edition is installed.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="1d2f2-149"><dt>0x00008000</dt></span><span class="sxs-lookup"><span data-stu-id="1d2f2-149"><dt>0x00008000</dt></span></span> </dl> | <span data-ttu-id="1d2f2-150">O Windows Home Server está instalado.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-150">Windows Home Server is installed.</span></span><br/>                                                                                                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="1d2f2-151">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d2f2-151">Remarks</span></span>

<span data-ttu-id="1d2f2-152">Você não deve confiar apenas no sinalizador 0x00000001 para determinar se o Small Business Server foi instalado no sistema, pois esse sinalizador e o sinalizador 0x00000020 são definidos quando esse pacote de produto é instalado.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-152">You should not rely upon only the 0x00000001 flag to determine whether Small Business Server has been installed on the system, as both this flag and the 0x00000020 flag are set when this product suite is installed.</span></span> <span data-ttu-id="1d2f2-153">Se você atualizar essa instalação para o Windows Server, Standard Edition, o sinalizador 0x00000020 será limpo, no entanto, o sinalizador 0x00000001 permanecerá definido.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-153">If you upgrade this installation to Windows Server, Standard Edition, the 0x00000020 flag will be cleared however, the 0x00000001 flag will remain set.</span></span> <span data-ttu-id="1d2f2-154">Nesse caso, isso indica que o Small Business Server já foi instalado neste sistema.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-154">In this case, this indicates that Small Business Server was once installed on this system.</span></span> <span data-ttu-id="1d2f2-155">Se essa instalação for atualizada ainda mais para o Windows Server, Enterprise Edition, o sinalizador 0x00000001 permanecerá definido.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-155">If this installation is further upgraded to Windows Server, Enterprise Edition, the 0x00000001 flag will remain set.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d2f2-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d2f2-156">Requirements</span></span>



| <span data-ttu-id="1d2f2-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d2f2-157">Requirement</span></span> | <span data-ttu-id="1d2f2-158">Valor</span><span class="sxs-lookup"><span data-stu-id="1d2f2-158">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1d2f2-159">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d2f2-159">Minimum supported client</span></span><br/> | <span data-ttu-id="1d2f2-160">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1d2f2-160">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1d2f2-161">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d2f2-161">Minimum supported server</span></span><br/> | <span data-ttu-id="1d2f2-162">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="1d2f2-162">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1d2f2-163">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1d2f2-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d2f2-164"><dt>Ntddk. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d2f2-164"><dt>Ntddk.h</dt></span></span> </dl>   |
| <span data-ttu-id="1d2f2-165">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1d2f2-165">Library</span></span><br/>                  | <dl> <span data-ttu-id="1d2f2-166"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d2f2-166"><dt>Ntdll.lib</dt></span></span> </dl> |
| <span data-ttu-id="1d2f2-167">DLL</span><span class="sxs-lookup"><span data-stu-id="1d2f2-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d2f2-168"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d2f2-168"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 




