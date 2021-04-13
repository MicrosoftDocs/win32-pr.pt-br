---
title: Método IVMVirtualPC FindVirtualNetwork (VPCCOMInterfaces. h)
description: Recupera um objeto de rede virtual que corresponde ao nome solicitado.
ms.assetid: 84526fa4-fe88-4466-866d-c432ed3125aa
keywords:
- FindVirtualNetwork do método virtual PC
- Método FindVirtualNetwork Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método FindVirtualNetwork
topic_type:
- apiref
api_name:
- IVMVirtualPC.FindVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c59306d2e2022c1323ab52f1a47bd386347f504e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499605"
---
# <a name="ivmvirtualpcfindvirtualnetwork-method"></a><span data-ttu-id="b67ba-106">Método IVMVirtualPC:: FindVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b67ba-106">IVMVirtualPC::FindVirtualNetwork method</span></span>

<span data-ttu-id="b67ba-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b67ba-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b67ba-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b67ba-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b67ba-109">Recupera um objeto de rede virtual que corresponde ao nome solicitado.</span><span class="sxs-lookup"><span data-stu-id="b67ba-109">Retrieves a virtual network object that matches the requested name.</span></span>

## <a name="syntax"></a><span data-ttu-id="b67ba-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b67ba-110">Syntax</span></span>


```C++
HRESULT FindVirtualNetwork(
  [in]          BSTR              virtualNetworkName,
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="parameters"></a><span data-ttu-id="b67ba-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b67ba-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b67ba-112">*virtualNetworkName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b67ba-112">*virtualNetworkName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b67ba-113">O nome da rede virtual a ser localizada.</span><span class="sxs-lookup"><span data-stu-id="b67ba-113">The name of the virtual network to find.</span></span>

</dd> <dt>

<span data-ttu-id="b67ba-114">*virtualNetwork* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="b67ba-114">*virtualNetwork* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b67ba-115">Um ponteiro para um novo objeto [**IVMVirtualNetwork**](ivmvirtualnetwork.md) que representa essa rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b67ba-115">A pointer to a new [**IVMVirtualNetwork**](ivmvirtualnetwork.md) object that represents this virtual network.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b67ba-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b67ba-116">Return value</span></span>

<span data-ttu-id="b67ba-117">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="b67ba-117">This method can return one of these values.</span></span>



| <span data-ttu-id="b67ba-118">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b67ba-118">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="b67ba-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="b67ba-119">Description</span></span>                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b67ba-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b67ba-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="b67ba-121">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b67ba-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="b67ba-122"><dt>**S \_ FALSO**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b67ba-122"><dt>**S\_FALSE**</dt> <dt>1</dt></span></span> </dl>                                               | <span data-ttu-id="b67ba-123">Não foi possível encontrar a rede virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="b67ba-123">The specified virtual network could not be found.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b67ba-124"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="b67ba-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="b67ba-125">O parâmetro *virtualNetwork* é **nulo** ou a rede virtual não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="b67ba-125">The *virtualNetwork* parameter is **NULL** or the virtual network cannot be found.</span></span><br/>   |
| <dl> <span data-ttu-id="b67ba-126"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="b67ba-126"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="b67ba-127">O parâmetro *virtualNetworkName* não é válido ou é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="b67ba-127">The *virtualNetworkName* parameter is not valid or is an empty string.</span></span><br/>               |
| <dl> <span data-ttu-id="b67ba-128"><dt>**HRESULT \_ Do \_ Win32 (arquivo de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="b67ba-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="b67ba-129">Não foi possível encontrar o arquivo de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b67ba-129">The virtual network file could not be found.</span></span><br/>                                         |
| <dl> <span data-ttu-id="b67ba-130"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="b67ba-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="b67ba-131">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="b67ba-131">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="b67ba-132"><dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b67ba-132"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="b67ba-133">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="b67ba-133">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b67ba-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="b67ba-134">Remarks</span></span>

<span data-ttu-id="b67ba-135">Os nomes de rede virtual não diferenciam maiúsculas de minúsculas, por exemplo, "mynetwork" e "mynetwork" referem-se à mesma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b67ba-135">Virtual network names are case-insensitive, for example, "MyNetwork" and "mynetwork" refer to the same virtual network.</span></span>

## <a name="requirements"></a><span data-ttu-id="b67ba-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b67ba-136">Requirements</span></span>



| <span data-ttu-id="b67ba-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="b67ba-137">Requirement</span></span> | <span data-ttu-id="b67ba-138">Valor</span><span class="sxs-lookup"><span data-stu-id="b67ba-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b67ba-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b67ba-139">Minimum supported client</span></span><br/> | <span data-ttu-id="b67ba-140">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b67ba-140">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b67ba-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b67ba-141">Minimum supported server</span></span><br/> | <span data-ttu-id="b67ba-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b67ba-142">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b67ba-143">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b67ba-143">End of client support</span></span><br/>    | <span data-ttu-id="b67ba-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b67ba-144">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b67ba-145">Produto</span><span class="sxs-lookup"><span data-stu-id="b67ba-145">Product</span></span><br/>                  | <span data-ttu-id="b67ba-146">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b67ba-146">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b67ba-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b67ba-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="b67ba-148"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b67ba-148"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b67ba-149">IID</span><span class="sxs-lookup"><span data-stu-id="b67ba-149">IID</span></span><br/>                      | <span data-ttu-id="b67ba-150">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="b67ba-150">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="b67ba-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="b67ba-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b67ba-152">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="b67ba-152">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

