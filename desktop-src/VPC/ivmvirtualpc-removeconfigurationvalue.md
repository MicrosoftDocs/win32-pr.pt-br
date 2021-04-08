---
title: Método IVMVirtualPC RemoveConfigurationValue (VPCCOMInterfaces. h)
description: Remove o valor da definição de configuração especificada.
ms.assetid: 07bafa5e-bf62-45bf-af4e-a66050f5afad
keywords:
- RemoveConfigurationValue do método virtual PC
- Método RemoveConfigurationValue Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método RemoveConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualPC.RemoveConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73821657ed7983e2d92fc379c3222f343763b3ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824648"
---
# <a name="ivmvirtualpcremoveconfigurationvalue-method"></a><span data-ttu-id="56b07-106">Método IVMVirtualPC:: RemoveConfigurationValue</span><span class="sxs-lookup"><span data-stu-id="56b07-106">IVMVirtualPC::RemoveConfigurationValue method</span></span>

<span data-ttu-id="56b07-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="56b07-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="56b07-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="56b07-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="56b07-109">Remove o valor da definição de configuração especificada.</span><span class="sxs-lookup"><span data-stu-id="56b07-109">Removes the value of the specified configuration setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="56b07-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56b07-110">Syntax</span></span>


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR preferenceKey
);
```



## <a name="parameters"></a><span data-ttu-id="56b07-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56b07-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56b07-112">*preferenceKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="56b07-112">*preferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56b07-113">A chave usada para identificar a preferência, conforme armazenado no arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="56b07-113">The key used to identify the preference, as stored in the configuration file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56b07-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="56b07-114">Return value</span></span>

<span data-ttu-id="56b07-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="56b07-115">This method can return one of these values.</span></span>



| <span data-ttu-id="56b07-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="56b07-116">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="56b07-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="56b07-117">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="56b07-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="56b07-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="56b07-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="56b07-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="56b07-120"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="56b07-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="56b07-121">O parâmetro *preferenceKey* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="56b07-121">The *preferenceKey* parameter is **NULL**.</span></span><br/>                                           |
| <dl> <span data-ttu-id="56b07-122"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="56b07-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="56b07-123">O parâmetro *preferenceKey* não é válido ou é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="56b07-123">The *preferenceKey* parameter is not valid or is an empty string.</span></span><br/>                    |
| <dl> <span data-ttu-id="56b07-124"><dt>**VM \_ E \_ pref \_ não \_ encontrado**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="56b07-124"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl>                   | <span data-ttu-id="56b07-125">A preferência não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="56b07-125">The preference was not found.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="56b07-126"><dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="56b07-126"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="56b07-127">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="56b07-127">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="56b07-128"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="56b07-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="56b07-129">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="56b07-129">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="56b07-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="56b07-130">Remarks</span></span>

<span data-ttu-id="56b07-131">Esse método fornece acesso de baixo nível a qualquer valor de preferência para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="56b07-131">This method provides low-level access to any preference value for the current user.</span></span> <span data-ttu-id="56b07-132">Ele pode ser usado para remover valores de preferência para chaves definidas pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="56b07-132">It can be used to remove preference values for customer-defined keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="56b07-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56b07-133">Requirements</span></span>



| <span data-ttu-id="56b07-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="56b07-134">Requirement</span></span> | <span data-ttu-id="56b07-135">Valor</span><span class="sxs-lookup"><span data-stu-id="56b07-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="56b07-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56b07-136">Minimum supported client</span></span><br/> | <span data-ttu-id="56b07-137">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="56b07-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="56b07-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56b07-138">Minimum supported server</span></span><br/> | <span data-ttu-id="56b07-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="56b07-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="56b07-140">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="56b07-140">End of client support</span></span><br/>    | <span data-ttu-id="56b07-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="56b07-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="56b07-142">Produto</span><span class="sxs-lookup"><span data-stu-id="56b07-142">Product</span></span><br/>                  | <span data-ttu-id="56b07-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="56b07-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="56b07-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="56b07-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="56b07-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="56b07-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="56b07-146">IID</span><span class="sxs-lookup"><span data-stu-id="56b07-146">IID</span></span><br/>                      | <span data-ttu-id="56b07-147">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="56b07-147">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="56b07-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="56b07-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56b07-149">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="56b07-149">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

