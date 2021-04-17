---
title: Método setdimensions IVMDisplay (VPCCOMInterfaces. h)
description: Define a altura e a largura da exibição da VM, em pixels.
ms.assetid: 8ad5cfc4-59b4-4327-b088-d54adf9c6fda
keywords:
- Método setdimensions Virtual PC
- Método setdimensions Virtual PC, interface IVMDisplay
- IVMDisplay interface virtual PC, método setdimensions
topic_type:
- apiref
api_name:
- IVMDisplay.SetDimensions
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4730d73e06074714c8e6ed31fda992259d5c19ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759588"
---
# <a name="ivmdisplaysetdimensions-method"></a><span data-ttu-id="39bb0-106">Método IVMDisplay:: setdimensions</span><span class="sxs-lookup"><span data-stu-id="39bb0-106">IVMDisplay::SetDimensions method</span></span>

<span data-ttu-id="39bb0-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="39bb0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="39bb0-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="39bb0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="39bb0-109">Define a altura e a largura da exibição da máquina virtual (VM), em pixels.</span><span class="sxs-lookup"><span data-stu-id="39bb0-109">Sets the height and width of the virtual machine's (VM's) display, in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="39bb0-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39bb0-110">Syntax</span></span>


```C++
HRESULT SetDimensions(
  [in] long displayPixelWidth,
  [in] long displayPixelHeight
);
```



## <a name="parameters"></a><span data-ttu-id="39bb0-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39bb0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39bb0-112">*displayPixelWidth* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="39bb0-112">*displayPixelWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39bb0-113">A largura, em pixels.</span><span class="sxs-lookup"><span data-stu-id="39bb0-113">The width, in pixels.</span></span> <span data-ttu-id="39bb0-114">O valor deve estar entre os valores de 640 e 2048.</span><span class="sxs-lookup"><span data-stu-id="39bb0-114">The value must be between the values of 640 and 2048.</span></span> <span data-ttu-id="39bb0-115">Se o valor não for igualmente divisível por 8, ele será reduzido para o próximo múltiplo inferior de 8.</span><span class="sxs-lookup"><span data-stu-id="39bb0-115">If the value is not evenly divisible by 8, then it will be reduced to the next lower multiple of 8.</span></span>

</dd> <dt>

<span data-ttu-id="39bb0-116">*displayPixelHeight* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="39bb0-116">*displayPixelHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39bb0-117">A altura, em pixels.</span><span class="sxs-lookup"><span data-stu-id="39bb0-117">The height, in pixels.</span></span> <span data-ttu-id="39bb0-118">O valor deve estar entre os valores de 480 e 1920.</span><span class="sxs-lookup"><span data-stu-id="39bb0-118">The value must be between the values of 480 and 1920.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39bb0-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="39bb0-119">Return value</span></span>

<span data-ttu-id="39bb0-120">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="39bb0-120">This method can return one of these values.</span></span>



| <span data-ttu-id="39bb0-121">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="39bb0-121">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="39bb0-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="39bb0-122">Description</span></span>                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="39bb0-123"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="39bb0-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="39bb0-124">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="39bb0-124">The operation was successful.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="39bb0-125"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="39bb0-125"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="39bb0-126">O parâmetro *displayPixelWidth* não é divisível por 8, ou o parâmetro *displayPixelWidth* ou *displayPixelHeight* está fora dos valores mínimos permitidos (640x480) ou máximo de 2048x1920).</span><span class="sxs-lookup"><span data-stu-id="39bb0-126">The *displayPixelWidth* parameter is not evenly divisible by 8 or the *displayPixelWidth* or *displayPixelHeight* parameter is outside of the allowed minimum (640x480) or maximum 2048x1920) values.</span></span><br/> |
| <dl> <span data-ttu-id="39bb0-127"><dt>**VM \_ E \_ atingiu o tempo \_ limite**</dt> de <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="39bb0-127"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="39bb0-128">A alteração de resolução não foi concluída em tempo hábil.</span><span class="sxs-lookup"><span data-stu-id="39bb0-128">The resolution change did not finish in a timely manner.</span></span><br/>                                                                                                                                              |
| <dl> <span data-ttu-id="39bb0-129"><dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="39bb0-129"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="39bb0-130">A máquina virtual deve estar em execução para esta operação.</span><span class="sxs-lookup"><span data-stu-id="39bb0-130">The virtual machine must be running for this operation.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="39bb0-131"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="39bb0-131"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                    | <span data-ttu-id="39bb0-132">A máquina virtual não é válida ou não está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="39bb0-132">The virtual machine is not valid or is not currently running.</span></span><br/>                                                                                                                                         |
| <dl> <span data-ttu-id="39bb0-133"><dt>**VM \_ E \_ nenhum \_**</dt> <dt>0xA0040850</dt> de exibição</span><span class="sxs-lookup"><span data-stu-id="39bb0-133"><dt>**VM\_E\_NO\_DISPLAY**</dt> <dt>0xA0040850</dt></span></span> </dl>                    | <span data-ttu-id="39bb0-134">Não é possível localizar uma exibição válida para a VM.</span><span class="sxs-lookup"><span data-stu-id="39bb0-134">Unable to locate a valid display for the VM.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="39bb0-135"><dt>**VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP**</dt> . <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="39bb0-135"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="39bb0-136">A versão dos componentes de integração instalados no sistema operacional convidado não oferece suporte a essa operação.</span><span class="sxs-lookup"><span data-stu-id="39bb0-136">The version of the integration components installed in the guest operating system does not support this operation.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="39bb0-137"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="39bb0-137"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="39bb0-138">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="39bb0-138">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="39bb0-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="39bb0-139">Remarks</span></span>

<span data-ttu-id="39bb0-140">O tamanho mínimo da exibição da máquina virtual é de 640 x 480 pixels.</span><span class="sxs-lookup"><span data-stu-id="39bb0-140">The minimum size of the virtual machine's display is 640 x 480 pixels.</span></span> <span data-ttu-id="39bb0-141">O tamanho máximo é 2048 x 1920.</span><span class="sxs-lookup"><span data-stu-id="39bb0-141">The maximum size is 2048 x 1920.</span></span> <span data-ttu-id="39bb0-142">As tentativas de definir o tamanho de exibição para valores fora desses limites, ou para qualquer largura que não seja divisível por 8, resultarão no retorno de um erro **E \_ INVALIDARG** .</span><span class="sxs-lookup"><span data-stu-id="39bb0-142">Attempts to set the display size to values outside these limits, or to any width not evenly divisible by 8, will result in an **E\_INVALIDARG** error being returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="39bb0-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39bb0-143">Requirements</span></span>



| <span data-ttu-id="39bb0-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="39bb0-144">Requirement</span></span> | <span data-ttu-id="39bb0-145">Valor</span><span class="sxs-lookup"><span data-stu-id="39bb0-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="39bb0-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39bb0-146">Minimum supported client</span></span><br/> | <span data-ttu-id="39bb0-147">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="39bb0-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="39bb0-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39bb0-148">Minimum supported server</span></span><br/> | <span data-ttu-id="39bb0-149">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="39bb0-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="39bb0-150">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="39bb0-150">End of client support</span></span><br/>    | <span data-ttu-id="39bb0-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="39bb0-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="39bb0-152">Produto</span><span class="sxs-lookup"><span data-stu-id="39bb0-152">Product</span></span><br/>                  | <span data-ttu-id="39bb0-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="39bb0-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="39bb0-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="39bb0-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="39bb0-155"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="39bb0-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="39bb0-156">IID</span><span class="sxs-lookup"><span data-stu-id="39bb0-156">IID</span></span><br/>                      | <span data-ttu-id="39bb0-157">IID \_ IVMDisplay é definido como 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="39bb0-157">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="39bb0-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="39bb0-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39bb0-159">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="39bb0-159">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

