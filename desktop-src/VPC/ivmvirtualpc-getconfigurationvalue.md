---
title: Método getconfigurationvalue IVMVirtualPC (VPCCOMInterfaces. h)
description: Recupera o valor da definição de configuração especificada.
ms.assetid: 4598b57c-9942-4b40-97b5-41ad9ec74bfa
keywords:
- PC virtual do método getconfigurationvalue
- Método getconfigurationvalue Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método getconfigurationvalue
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11851e2dc2e51c0dc5eed876fc755655ed488554
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086062"
---
# <a name="ivmvirtualpcgetconfigurationvalue-method"></a><span data-ttu-id="a2906-106">Método IVMVirtualPC:: getconfigurationvalue</span><span class="sxs-lookup"><span data-stu-id="a2906-106">IVMVirtualPC::GetConfigurationValue method</span></span>

<span data-ttu-id="a2906-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a2906-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a2906-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a2906-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a2906-109">Recupera o valor da definição de configuração especificada.</span><span class="sxs-lookup"><span data-stu-id="a2906-109">Retrieves the value of the specified configuration setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2906-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2906-110">Syntax</span></span>


```C++
HRESULT GetConfigurationValue(
  [in]          BSTR    preferenceKey,
  [out, retval] VARIANT *preferenceValue
);
```



## <a name="parameters"></a><span data-ttu-id="a2906-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2906-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2906-112">*preferenceKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a2906-112">*preferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2906-113">A chave usada para identificar a preferência, conforme armazenado no arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="a2906-113">The key used to identify the preference, as stored in the configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="a2906-114">*preferência* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a2906-114">*preferenceValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a2906-115">O valor de preferência.</span><span class="sxs-lookup"><span data-stu-id="a2906-115">The preference value.</span></span> <span data-ttu-id="a2906-116">Esse parâmetro pode ser um dos seguintes tipos **variantes** : **VT \_ array** \| **VT \_ UI1** (bytes brutos), **VT \_ BSTR** (String), **VT \_ i4** (Integer) ou **VT \_ bool** (booliano).</span><span class="sxs-lookup"><span data-stu-id="a2906-116">This parameter may be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_I4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2906-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a2906-117">Return value</span></span>

<span data-ttu-id="a2906-118">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="a2906-118">This method can return one of these values.</span></span>



| <span data-ttu-id="a2906-119">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a2906-119">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="a2906-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="a2906-120">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a2906-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a2906-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="a2906-122">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a2906-122">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="a2906-123"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="a2906-123"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="a2906-124">O parâmetro *preferenceKey* ou *preferencevalue* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a2906-124">The *preferenceKey* or *preferenceValue* parameter is **NULL**.</span></span><br/>                      |
| <dl> <span data-ttu-id="a2906-125"><dt>**VM \_ E \_ pref \_ não \_ encontrado**</dt> <dt>0xa0040300</dt></span><span class="sxs-lookup"><span data-stu-id="a2906-125"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xa0040300</dt></span></span> </dl>                   | <span data-ttu-id="a2906-126">A preferência não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2906-126">The preference was not found.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="a2906-127"><dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a2906-127"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="a2906-128">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="a2906-128">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="a2906-129"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="a2906-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="a2906-130">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="a2906-130">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="a2906-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2906-131">Remarks</span></span>

<span data-ttu-id="a2906-132">Esse método fornece acesso de baixo nível a qualquer valor de preferência para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="a2906-132">This method provides low-level access to any preference value for the current user.</span></span> <span data-ttu-id="a2906-133">Ele pode ser usado para recuperar valores de preferência para chaves definidas pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="a2906-133">It can be used to retrieve preference values for customer-defined keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2906-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2906-134">Requirements</span></span>



| <span data-ttu-id="a2906-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2906-135">Requirement</span></span> | <span data-ttu-id="a2906-136">Valor</span><span class="sxs-lookup"><span data-stu-id="a2906-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2906-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2906-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a2906-138">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a2906-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a2906-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2906-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a2906-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a2906-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a2906-141">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a2906-141">End of client support</span></span><br/>    | <span data-ttu-id="a2906-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a2906-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a2906-143">Produto</span><span class="sxs-lookup"><span data-stu-id="a2906-143">Product</span></span><br/>                  | <span data-ttu-id="a2906-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a2906-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a2906-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a2906-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2906-146"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2906-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a2906-147">IID</span><span class="sxs-lookup"><span data-stu-id="a2906-147">IID</span></span><br/>                      | <span data-ttu-id="a2906-148">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="a2906-148">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a2906-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2906-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2906-150">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="a2906-150">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

