---
title: Método IVMFloppyDrive AttachImage (VPCCOMInterfaces. h)
description: Anexa uma imagem de mídia de disquete no host à unidade de disquete da máquina virtual.
ms.assetid: ee7ea6ac-47ef-4e7b-8df3-28c716a728b0
keywords:
- AttachImage do método virtual PC
- Método AttachImage Virtual PC, interface IVMFloppyDrive
- IVMFloppyDrive interface virtual PC, método AttachImage
topic_type:
- apiref
api_name:
- IVMFloppyDrive.AttachImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f8821a6d9bdae979f45477d1fe2ba666eb6da10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918300"
---
# <a name="ivmfloppydriveattachimage-method"></a><span data-ttu-id="aae61-106">Método IVMFloppyDrive:: AttachImage</span><span class="sxs-lookup"><span data-stu-id="aae61-106">IVMFloppyDrive::AttachImage method</span></span>

<span data-ttu-id="aae61-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="aae61-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="aae61-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="aae61-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="aae61-109">Anexa uma imagem de mídia de disquete no host à unidade de disquete da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="aae61-109">Attaches a floppy media image on the host to the floppy drive of the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="aae61-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aae61-110">Syntax</span></span>


```C++
HRESULT AttachImage(
  [in] BSTR mediaImagePath
);
```



## <a name="parameters"></a><span data-ttu-id="aae61-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aae61-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aae61-112">*mediaImagePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aae61-112">*mediaImagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aae61-113">O caminho completo para a imagem de mídia de disquete a ser anexada.</span><span class="sxs-lookup"><span data-stu-id="aae61-113">The full path to the floppy media image that is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aae61-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aae61-114">Return value</span></span>

<span data-ttu-id="aae61-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="aae61-115">This method can return one of these values.</span></span>



| <span data-ttu-id="aae61-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="aae61-116">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="aae61-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="aae61-117">Description</span></span>                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aae61-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="aae61-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="aae61-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="aae61-119">The operation was successful.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="aae61-120"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="aae61-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="aae61-121">O parâmetro *mediaImagePath* não é válido.</span><span class="sxs-lookup"><span data-stu-id="aae61-121">The *mediaImagePath* parameter is not valid.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="aae61-122"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="aae61-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="aae61-123">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="aae61-123">The parameter is **NULL**.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="aae61-124"><dt>**HRESULT \_ DO \_ Win32 (erro \_ OUTOFMEMORY)**</dt> <dt>0x8007000E</dt></span><span class="sxs-lookup"><span data-stu-id="aae61-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl>      | <span data-ttu-id="aae61-125">Não há memória suficiente disponível para concluir esta solicitação.</span><span class="sxs-lookup"><span data-stu-id="aae61-125">There is not enough memory available to complete this request.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="aae61-126"><dt>**HRESULT \_ Do \_ Win32 (estouro de buffer de erro \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="aae61-126"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="aae61-127">O caminho especificado pelo parâmetro *mediaImagePath* é muito longo.</span><span class="sxs-lookup"><span data-stu-id="aae61-127">The path specified by the *mediaImagePath* parameter is too long.</span></span> <span data-ttu-id="aae61-128">O caminho deve ser menor que **o \_ caminho máximo** (260) caracteres.</span><span class="sxs-lookup"><span data-stu-id="aae61-128">The path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="aae61-129"><dt>**HRESULT \_ DO \_ Win32 ( \_ \_ nome inválido do erro)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="aae61-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="aae61-130">O parâmetro *mediaImagePath* contém um caractere inválido (um de " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="aae61-130">The *mediaImagePath* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                    |
| <dl> <span data-ttu-id="aae61-131"><dt>**HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="aae61-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="aae61-132">O parâmetro *mediaImagePath* especifica um caminho relativo ou vazio.</span><span class="sxs-lookup"><span data-stu-id="aae61-132">The *mediaImagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="aae61-133">Um caminho absoluto é necessário.</span><span class="sxs-lookup"><span data-stu-id="aae61-133">An absolute path is required.</span></span><br/>                            |
| <dl> <span data-ttu-id="aae61-134"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="aae61-134"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="aae61-135">A configuração desta máquina virtual não é válida ou não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="aae61-135">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="aae61-136"><dt>**VM \_ 0xA00400650 \_ de \_ \_ falha de captura de imagem E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="aae61-136"><dt>**VM\_E\_IMAGE\_CAPTURE\_FAIL**</dt> <dt>0xA00400650</dt></span></span> </dl>                  | <span data-ttu-id="aae61-137">Não foi possível capturar o arquivo de imagem especificado.</span><span class="sxs-lookup"><span data-stu-id="aae61-137">The image file specified could not be captured.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="aae61-138"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="aae61-138"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="aae61-139">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="aae61-139">An unexpected error has occurred.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="aae61-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aae61-140">Requirements</span></span>



| <span data-ttu-id="aae61-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="aae61-141">Requirement</span></span> | <span data-ttu-id="aae61-142">Valor</span><span class="sxs-lookup"><span data-stu-id="aae61-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="aae61-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aae61-143">Minimum supported client</span></span><br/> | <span data-ttu-id="aae61-144">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="aae61-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aae61-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aae61-145">Minimum supported server</span></span><br/> | <span data-ttu-id="aae61-146">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="aae61-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="aae61-147">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="aae61-147">End of client support</span></span><br/>    | <span data-ttu-id="aae61-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="aae61-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="aae61-149">Produto</span><span class="sxs-lookup"><span data-stu-id="aae61-149">Product</span></span><br/>                  | <span data-ttu-id="aae61-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="aae61-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="aae61-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aae61-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="aae61-152"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="aae61-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="aae61-153">IID</span><span class="sxs-lookup"><span data-stu-id="aae61-153">IID</span></span><br/>                      | <span data-ttu-id="aae61-154">IID \_ IVMFloppyDrive é definido como 661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="aae61-154">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="aae61-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="aae61-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aae61-156">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="aae61-156">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

