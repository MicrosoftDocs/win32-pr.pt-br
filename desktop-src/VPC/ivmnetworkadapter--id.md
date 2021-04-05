---
title: Método de _ID IVMNetworkAdapter (VPCCOMInterfaces. h)
description: Recupera o identificador interno desta interface de rede.
ms.assetid: 3e71c2cd-1a75-44d9-9a6d-04e6344dfec3
keywords:
- _ID o método virtual PC
- _ID método virtual PC, interface IVMNetworkAdapter
- IVMNetworkAdapter interface virtual PC, método de _ID
topic_type:
- apiref
api_name:
- IVMNetworkAdapter._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9df514d24f9826b58964b4c51c9a76a9ba982e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918574"
---
# <a name="ivmnetworkadapter_id-method"></a><span data-ttu-id="7476e-106">Método IVMNetworkAdapter:: \_ ID</span><span class="sxs-lookup"><span data-stu-id="7476e-106">IVMNetworkAdapter::\_ID method</span></span>

<span data-ttu-id="7476e-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7476e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7476e-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7476e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7476e-109">Recupera o identificador interno desta interface de rede.</span><span class="sxs-lookup"><span data-stu-id="7476e-109">Retrieves the internal identifier of this network interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="7476e-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7476e-110">Syntax</span></span>


```C++
HRESULT _ID(
  [out] long *identifier
);
```



## <a name="parameters"></a><span data-ttu-id="7476e-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7476e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7476e-112">*identificador* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="7476e-112">*identifier* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7476e-113">O identificador interno.</span><span class="sxs-lookup"><span data-stu-id="7476e-113">The internal identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7476e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7476e-114">Return value</span></span>

<span data-ttu-id="7476e-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="7476e-115">This method can return one of these values.</span></span>



| <span data-ttu-id="7476e-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7476e-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="7476e-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="7476e-117">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="7476e-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7476e-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="7476e-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7476e-119">The operation was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="7476e-120"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="7476e-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="7476e-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="7476e-121">The parameter is **NULL**.</span></span><br/>           |
| <dl> <span data-ttu-id="7476e-122"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7476e-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="7476e-123">Não é possível encontrar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7476e-123">The virtual machine cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="7476e-124"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="7476e-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="7476e-125">Erro desconhecido na operação.</span><span class="sxs-lookup"><span data-stu-id="7476e-125">The operation had an unknown error.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="7476e-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="7476e-126">Remarks</span></span>

<span data-ttu-id="7476e-127">Esse método não pode ser usado por linguagens de script.</span><span class="sxs-lookup"><span data-stu-id="7476e-127">This method is not usable by scripting languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="7476e-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7476e-128">Requirements</span></span>



| <span data-ttu-id="7476e-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="7476e-129">Requirement</span></span> | <span data-ttu-id="7476e-130">Valor</span><span class="sxs-lookup"><span data-stu-id="7476e-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7476e-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7476e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7476e-132">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7476e-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7476e-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7476e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7476e-134">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7476e-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7476e-135">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="7476e-135">End of client support</span></span><br/>    | <span data-ttu-id="7476e-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7476e-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7476e-137">Produto</span><span class="sxs-lookup"><span data-stu-id="7476e-137">Product</span></span><br/>                  | <span data-ttu-id="7476e-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7476e-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7476e-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7476e-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="7476e-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7476e-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7476e-141">IID</span><span class="sxs-lookup"><span data-stu-id="7476e-141">IID</span></span><br/>                      | <span data-ttu-id="7476e-142">IID \_ IVMNetworkAdapter é definido como e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="7476e-142">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="7476e-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="7476e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7476e-144">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="7476e-144">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

