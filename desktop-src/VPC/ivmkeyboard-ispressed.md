---
title: Método ispressioned IVMKeyboard (VPCCOMInterfaces. h)
description: Determina se a chave especificada está inativa.
ms.assetid: 7541d678-762a-4c2e-80cd-686bb56c9cd7
keywords:
- Método ispressioned PC virtual
- Método ispressioned PC virtual, interface IVMKeyboard
- IVMKeyboard interface virtual PC, método isprensaed
topic_type:
- apiref
api_name:
- IVMKeyboard.IsPressed
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a4185fa0310994bc1cffa917348dfca2fdedfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644924"
---
# <a name="ivmkeyboardispressed-method"></a><span data-ttu-id="b606a-106">Método IVMKeyboard:: ispressioned</span><span class="sxs-lookup"><span data-stu-id="b606a-106">IVMKeyboard::IsPressed method</span></span>

<span data-ttu-id="b606a-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b606a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b606a-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b606a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b606a-109">Determina se a chave especificada está inativa.</span><span class="sxs-lookup"><span data-stu-id="b606a-109">Determines whether the specified key is down.</span></span>

## <a name="syntax"></a><span data-ttu-id="b606a-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b606a-110">Syntax</span></span>


```C++
HRESULT IsPressed(
  [in]          BSTR         key,
  [out, retval] VARIANT_BOOL *pressed
);
```



## <a name="parameters"></a><span data-ttu-id="b606a-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b606a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b606a-112">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b606a-112">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b606a-113">O código de chave para a chave cujo estado deve ser consultado.</span><span class="sxs-lookup"><span data-stu-id="b606a-113">The key code for the key whose state is to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="b606a-114">*pressionado* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="b606a-114">*pressed* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b606a-115">**True** se a chave estiver pressionada no momento; caso contrário, **retornará false** .</span><span class="sxs-lookup"><span data-stu-id="b606a-115">**TRUE** if the key is currently pressed down, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b606a-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b606a-116">Return value</span></span>

<span data-ttu-id="b606a-117">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="b606a-117">This method can return one of these values.</span></span>



| <span data-ttu-id="b606a-118">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b606a-118">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="b606a-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="b606a-119">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b606a-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b606a-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="b606a-121">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b606a-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="b606a-122"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="b606a-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="b606a-123">Um parâmetro é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b606a-123">A parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="b606a-124"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="b606a-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="b606a-125">A cadeia de caracteres especificada está vazia ou contém um código de chave inválido.</span><span class="sxs-lookup"><span data-stu-id="b606a-125">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="b606a-126"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="b606a-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="b606a-127">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="b606a-127">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="b606a-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b606a-128">Requirements</span></span>



| <span data-ttu-id="b606a-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b606a-129">Requirement</span></span> | <span data-ttu-id="b606a-130">Valor</span><span class="sxs-lookup"><span data-stu-id="b606a-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b606a-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b606a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b606a-132">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b606a-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b606a-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b606a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b606a-134">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b606a-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b606a-135">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b606a-135">End of client support</span></span><br/>    | <span data-ttu-id="b606a-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b606a-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b606a-137">Produto</span><span class="sxs-lookup"><span data-stu-id="b606a-137">Product</span></span><br/>                  | <span data-ttu-id="b606a-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b606a-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b606a-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b606a-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="b606a-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b606a-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b606a-141">IID</span><span class="sxs-lookup"><span data-stu-id="b606a-141">IID</span></span><br/>                      | <span data-ttu-id="b606a-142">IID \_ IVMKeyboard é definido como 00695f2e-c5ad-4d6e-B1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="b606a-142">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="b606a-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="b606a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b606a-144">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="b606a-144">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

