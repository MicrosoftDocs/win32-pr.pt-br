---
title: Propriedade IVMGuestOS SuiteMask (VPCCOMInterfaces. h)
description: Recupera o SuiteMask do sistema operacional convidado em execução na máquina virtual.
ms.assetid: 11d065c1-9d46-4c81-b843-776db3507a04
keywords:
- Propriedade SuiteMask Virtual PC
- Propriedade SuiteMask Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, Propriedade SuiteMask
topic_type:
- apiref
api_name:
- IVMGuestOS.SuiteMask
- IVMGuestOS.get_SuiteMask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 348384dd729c5c7e63a45fcb8b3f05d0189a7fec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645172"
---
# <a name="ivmguestossuitemask-property"></a><span data-ttu-id="cf691-106">Propriedade IVMGuestOS:: SuiteMask</span><span class="sxs-lookup"><span data-stu-id="cf691-106">IVMGuestOS::SuiteMask property</span></span>

<span data-ttu-id="cf691-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cf691-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cf691-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cf691-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cf691-109">Recupera o SuiteMask do sistema operacional convidado em execução na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cf691-109">Retrieves the SuiteMask of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="cf691-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="cf691-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf691-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cf691-111">Syntax</span></span>


```C++
HRESULT get_SuiteMask(
  [out, retval] BSTR *suiteMask
);
```



## <a name="property-value"></a><span data-ttu-id="cf691-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="cf691-112">Property value</span></span>

<span data-ttu-id="cf691-113">A máscara do pacote.</span><span class="sxs-lookup"><span data-stu-id="cf691-113">The suite mask.</span></span> <span data-ttu-id="cf691-114">Há suporte para os valores de cadeia de caracteres a seguir.</span><span class="sxs-lookup"><span data-stu-id="cf691-114">The following string values are supported.</span></span>



| <span data-ttu-id="cf691-115">Valor</span><span class="sxs-lookup"><span data-stu-id="cf691-115">Value</span></span>                                                                                   | <span data-ttu-id="cf691-116">Significado</span><span class="sxs-lookup"><span data-stu-id="cf691-116">Meaning</span></span>                                                                                                                                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cf691-117"><dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="cf691-117"><dt>"0x00000004"</dt></span></span> </dl> | <span data-ttu-id="cf691-118">Os componentes do Microsoft BackOffice são instalados.</span><span class="sxs-lookup"><span data-stu-id="cf691-118">Microsoft BackOffice components are installed.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="cf691-119"><dt>"0x00000400"</dt></span><span class="sxs-lookup"><span data-stu-id="cf691-119"><dt>"0x00000400"</dt></span></span> </dl> | <span data-ttu-id="cf691-120">O Windows Server 2003, Web Edition está instalado.</span><span class="sxs-lookup"><span data-stu-id="cf691-120">Windows Server 2003, Web Edition is installed.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="cf691-121"><dt>"0x00004000"</dt></span><span class="sxs-lookup"><span data-stu-id="cf691-121"><dt>"0x00004000"</dt></span></span> </dl> | <span data-ttu-id="cf691-122">O Windows Server 2003, Compute Cluster Edition, está instalado.</span><span class="sxs-lookup"><span data-stu-id="cf691-122">Windows Server 2003, Compute Cluster Edition is installed.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="cf691-123"><dt>"0x00000080"</dt></span><span class="sxs-lookup"><span data-stu-id="cf691-123"><dt>"0x00000080"</dt></span></span> </dl> | <span data-ttu-id="cf691-124">O Windows Server 2008 R2 Datacenter, o Windows Server 2008 Datacenter, o Windows Server 2003, o Datacenter Edition ou o Windows 2000 Datacenter Server está instalado.</span><span class="sxs-lookup"><span data-stu-id="cf691-124">Windows Server 2008 R2 Datacenter, Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition, or Windows 2000 Datacenter Server is installed.</span></span><br/> |
| <dl> <span data-ttu-id="cf691-125"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="cf691-125"><dt>"0x00000002"</dt></span></span> </dl> | <span data-ttu-id="cf691-126">O Windows Server 2008 R2 Enterprise, o Windows Server 2008 Enterprise, o Windows Server 2003, Enterprise Edition ou o Windows 2000 Advanced Server está instalado.</span><span class="sxs-lookup"><span data-stu-id="cf691-126">Windows Server 2008 R2 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition, or Windows 2000 Advanced Server is installed.</span></span><br/>   |
| <dl> <span data-ttu-id="cf691-127"><dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="cf691-127"><dt>"0x00000040"</dt></span></span> </dl> | <span data-ttu-id="cf691-128">O Windows XP Embedded está instalado.</span><span class="sxs-lookup"><span data-stu-id="cf691-128">Windows XP Embedded is installed.</span></span><br/>                                                                                                                           |
| <dl> <span data-ttu-id="cf691-129"><dt>"0x00000200"</dt></span><span class="sxs-lookup"><span data-stu-id="cf691-129"><dt>"0x00000200"</dt></span></span> </dl> | <span data-ttu-id="cf691-130">O Windows Vista Home Premium, o Windows Vista Home Basic ou o Windows XP Home Edition está instalado.</span><span class="sxs-lookup"><span data-stu-id="cf691-130">Windows Vista Home Premium, Windows Vista Home Basic, or Windows XP Home Edition is installed.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="cf691-131"><dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="cf691-131"><dt>"0x00000100"</dt></span></span> </dl> | <span data-ttu-id="cf691-132">Há suporte para Área de Trabalho Remota, mas há suporte para apenas uma sessão interativa.</span><span class="sxs-lookup"><span data-stu-id="cf691-132">Remote Desktop is supported, but only one interactive session is supported.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="cf691-133"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="cf691-133"><dt>"0x00000001"</dt></span></span> </dl> | <span data-ttu-id="cf691-134">O Microsoft Small Business Server já foi instalado no sistema, mas pode ter sido atualizado para outra versão do Windows.</span><span class="sxs-lookup"><span data-stu-id="cf691-134">Microsoft Small Business Server was once installed on the system, but may have been upgraded to another version of Windows.</span></span><br/>                                 |
| <dl> <span data-ttu-id="cf691-135"><dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="cf691-135"><dt>"0x00000020"</dt></span></span> </dl> | <span data-ttu-id="cf691-136">O Microsoft Small Business Server é instalado com a licença de cliente restritiva em vigor.</span><span class="sxs-lookup"><span data-stu-id="cf691-136">Microsoft Small Business Server is installed with the restrictive client license in force.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="cf691-137"><dt>0x00002000</dt></span><span class="sxs-lookup"><span data-stu-id="cf691-137"><dt>"0x00002000"</dt></span></span> </dl> | <span data-ttu-id="cf691-138">O Windows Storage Server 2003 R2 ou o Windows Storage Server 2003 está instalado.</span><span class="sxs-lookup"><span data-stu-id="cf691-138">Windows Storage Server 2003 R2 or Windows Storage Server 2003 is installed.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="cf691-139"><dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="cf691-139"><dt>"0x00000010"</dt></span></span> </dl> | <span data-ttu-id="cf691-140">O Serviços de Área de Trabalho Remota está instalado.</span><span class="sxs-lookup"><span data-stu-id="cf691-140">Remote Desktop Services is installed.</span></span> <span data-ttu-id="cf691-141">Esse valor é sempre definido.</span><span class="sxs-lookup"><span data-stu-id="cf691-141">This value is always set.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="cf691-142"><dt>"0x00008000"</dt></span><span class="sxs-lookup"><span data-stu-id="cf691-142"><dt>"0x00008000"</dt></span></span> </dl> | <span data-ttu-id="cf691-143">O Windows Home Server está instalado.</span><span class="sxs-lookup"><span data-stu-id="cf691-143">Windows Home Server is installed.</span></span><br/>                                                                                                                           |



 

## <a name="error-codes"></a><span data-ttu-id="cf691-144">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="cf691-144">Error codes</span></span>



| <span data-ttu-id="cf691-145">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="cf691-145">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="cf691-146">Significado</span><span class="sxs-lookup"><span data-stu-id="cf691-146">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="cf691-147"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cf691-147"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="cf691-148">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="cf691-148">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="cf691-149"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="cf691-149"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="cf691-150">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="cf691-150">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="cf691-151"><dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="cf691-151"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="cf691-152">A VM não está em execução.</span><span class="sxs-lookup"><span data-stu-id="cf691-152">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="cf691-153"><dt>VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP</dt> . <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="cf691-153"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="cf691-154">Os componentes de integração não estão instalados nesta VM.</span><span class="sxs-lookup"><span data-stu-id="cf691-154">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="cf691-155"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="cf691-155"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="cf691-156">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="cf691-156">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="cf691-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf691-157">Requirements</span></span>



| <span data-ttu-id="cf691-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf691-158">Requirement</span></span> | <span data-ttu-id="cf691-159">Valor</span><span class="sxs-lookup"><span data-stu-id="cf691-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf691-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf691-160">Minimum supported client</span></span><br/> | <span data-ttu-id="cf691-161">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cf691-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cf691-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf691-162">Minimum supported server</span></span><br/> | <span data-ttu-id="cf691-163">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="cf691-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cf691-164">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="cf691-164">End of client support</span></span><br/>    | <span data-ttu-id="cf691-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cf691-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cf691-166">Produto</span><span class="sxs-lookup"><span data-stu-id="cf691-166">Product</span></span><br/>                  | <span data-ttu-id="cf691-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cf691-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cf691-168">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cf691-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf691-169"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf691-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cf691-170">IID</span><span class="sxs-lookup"><span data-stu-id="cf691-170">IID</span></span><br/>                      | <span data-ttu-id="cf691-171">IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="cf691-171">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="cf691-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf691-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf691-173">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="cf691-173">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

