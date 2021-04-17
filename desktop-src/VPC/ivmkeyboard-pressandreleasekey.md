---
title: Método IVMKeyboard PressAndReleaseKey (VPCCOMInterfaces. h)
description: Simula uma tecla que está sendo pressionada e liberada.
ms.assetid: 2a7fc36f-f1bf-4f1d-b8f7-ea5b167c82a7
keywords:
- PressAndReleaseKey do método virtual PC
- Método PressAndReleaseKey Virtual PC, interface IVMKeyboard
- IVMKeyboard interface virtual PC, método PressAndReleaseKey
topic_type:
- apiref
api_name:
- IVMKeyboard.PressAndReleaseKey
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4adbcac2c79c02ce69584bbfdf21a6b08b350a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105813253"
---
# <a name="ivmkeyboardpressandreleasekey-method"></a><span data-ttu-id="9b041-106">IVMKeyboard: método ressAndReleaseKey de:P</span><span class="sxs-lookup"><span data-stu-id="9b041-106">IVMKeyboard::PressAndReleaseKey method</span></span>

<span data-ttu-id="9b041-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9b041-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9b041-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9b041-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9b041-109">Simula uma tecla que está sendo pressionada e liberada.</span><span class="sxs-lookup"><span data-stu-id="9b041-109">Simulates a key being pressed down and then released.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b041-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b041-110">Syntax</span></span>


```C++
HRESULT PressAndReleaseKey(
  [in] BSTR key
);
```



## <a name="parameters"></a><span data-ttu-id="9b041-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b041-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b041-112">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9b041-112">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b041-113">O código de chave da chave a ser pressionada e liberada.</span><span class="sxs-lookup"><span data-stu-id="9b041-113">The key code for the key to be pressed and released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b041-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9b041-114">Return value</span></span>

<span data-ttu-id="9b041-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="9b041-115">This method can return one of these values.</span></span>



| <span data-ttu-id="9b041-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9b041-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="9b041-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b041-117">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9b041-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9b041-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="9b041-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9b041-119">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="9b041-120"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="9b041-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="9b041-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9b041-121">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="9b041-122"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="9b041-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="9b041-123">A cadeia de caracteres especificada está vazia ou contém um código de chave inválido.</span><span class="sxs-lookup"><span data-stu-id="9b041-123">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="9b041-124"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="9b041-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="9b041-125">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="9b041-125">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="9b041-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b041-126">Requirements</span></span>



| <span data-ttu-id="9b041-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b041-127">Requirement</span></span> | <span data-ttu-id="9b041-128">Valor</span><span class="sxs-lookup"><span data-stu-id="9b041-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b041-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b041-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9b041-130">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9b041-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9b041-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b041-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9b041-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9b041-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9b041-133">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="9b041-133">End of client support</span></span><br/>    | <span data-ttu-id="9b041-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9b041-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9b041-135">Produto</span><span class="sxs-lookup"><span data-stu-id="9b041-135">Product</span></span><br/>                  | <span data-ttu-id="9b041-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9b041-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9b041-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9b041-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b041-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b041-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9b041-139">IID</span><span class="sxs-lookup"><span data-stu-id="9b041-139">IID</span></span><br/>                      | <span data-ttu-id="9b041-140">IID \_ IVMKeyboard é definido como 00695f2e-c5ad-4d6e-B1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="9b041-140">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="9b041-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b041-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b041-142">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="9b041-142">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

