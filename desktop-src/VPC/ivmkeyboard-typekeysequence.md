---
title: Método IVMKeyboard TypeKeySequence (VPCCOMInterfaces. h)
description: Simula uma lista delimitada por vírgulas de chaves que estão sendo digitadas.
ms.assetid: ba4d4e43-cb2e-49ae-940d-2e81286d3473
keywords:
- TypeKeySequence do método virtual PC
- Método TypeKeySequence Virtual PC, interface IVMKeyboard
- IVMKeyboard interface virtual PC, método TypeKeySequence
topic_type:
- apiref
api_name:
- IVMKeyboard.TypeKeySequence
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c34bd96077c1d28aad196ee0d6b11de122725d68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919103"
---
# <a name="ivmkeyboardtypekeysequence-method"></a><span data-ttu-id="0b665-106">Método IVMKeyboard:: TypeKeySequence</span><span class="sxs-lookup"><span data-stu-id="0b665-106">IVMKeyboard::TypeKeySequence method</span></span>

<span data-ttu-id="0b665-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0b665-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0b665-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0b665-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0b665-109">Simula uma lista delimitada por vírgulas de chaves que estão sendo digitadas.</span><span class="sxs-lookup"><span data-stu-id="0b665-109">Simulates a comma-delimited list of keys being typed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b665-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b665-110">Syntax</span></span>


```C++
HRESULT TypeKeySequence(
  [in] BSTR keySequence
);
```



## <a name="parameters"></a><span data-ttu-id="0b665-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b665-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b665-112">*KeySequence* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0b665-112">*keySequence* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b665-113">A sequência delimitada por vírgulas de códigos de chave a serem digitados.</span><span class="sxs-lookup"><span data-stu-id="0b665-113">The comma-delimited sequence of key codes to be typed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b665-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0b665-114">Return value</span></span>

<span data-ttu-id="0b665-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="0b665-115">This method can return one of these values.</span></span>



| <span data-ttu-id="0b665-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0b665-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="0b665-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b665-117">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0b665-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0b665-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="0b665-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0b665-119">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="0b665-120"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="0b665-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="0b665-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0b665-121">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="0b665-122"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="0b665-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="0b665-123">A cadeia de caracteres especificada está vazia ou contém um código de chave inválido.</span><span class="sxs-lookup"><span data-stu-id="0b665-123">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="0b665-124"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="0b665-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="0b665-125">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="0b665-125">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="0b665-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b665-126">Remarks</span></span>

<span data-ttu-id="0b665-127">Uma cadeia de caracteres de sequência de chave é um conjunto delimitado por vírgulas de identificadores de chave que são usados para simular o pressionamento de tecla e a sequência de versão de um teclado em estilo padrão dos EUA 101.</span><span class="sxs-lookup"><span data-stu-id="0b665-127">A key sequence string is a comma-delimited set of key identifiers which are used to simulate the key press and release sequence of a standard U.S. 101-key AT-style keyboard.</span></span>

<span data-ttu-id="0b665-128">Se um identificador de chave aparecer na cadeia de caracteres sem um modificador anterior, um código com pressionamento de tecla será enviado para a sessão da máquina virtual, seguido imediatamente pelo código de lançamento de chave correspondente.</span><span class="sxs-lookup"><span data-stu-id="0b665-128">If a key identifier appears in the string without a preceding modifier, a key-pressed code is sent to the virtual machine session, followed immediately by its corresponding key-released code.</span></span> <span data-ttu-id="0b665-129">Os modificadores de chave podem ser usados para alterar esse comportamento.</span><span class="sxs-lookup"><span data-stu-id="0b665-129">Key modifiers can be used to change this behavior.</span></span>

<span data-ttu-id="0b665-130">Por exemplo, o modificador DOWN enviará o código de chave pressionada para o identificador de chave a seguir sem enviar o código de lançamento de chave.</span><span class="sxs-lookup"><span data-stu-id="0b665-130">For example, the DOWN modifier will send the key-pressed code for the following key identifier without sending the key-released code.</span></span> <span data-ttu-id="0b665-131">Isso é útil para simular as teclas CTRL, ALT e Shift quando elas são mantidas enquanto outras chaves estão sendo enviadas.</span><span class="sxs-lookup"><span data-stu-id="0b665-131">This is useful for simulating Ctrl, Alt, and Shift keys when they are held down while other keys are being sent.</span></span> <span data-ttu-id="0b665-132">Para liberar a chave, ela deve ser incluída na cadeia de caracteres de chave novamente junto com um modificador UP anterior.</span><span class="sxs-lookup"><span data-stu-id="0b665-132">To release the key, it must be included in the key string again along with a preceding UP modifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b665-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b665-133">Requirements</span></span>



| <span data-ttu-id="0b665-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b665-134">Requirement</span></span> | <span data-ttu-id="0b665-135">Valor</span><span class="sxs-lookup"><span data-stu-id="0b665-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b665-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b665-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0b665-137">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0b665-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0b665-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b665-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0b665-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0b665-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0b665-140">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="0b665-140">End of client support</span></span><br/>    | <span data-ttu-id="0b665-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0b665-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0b665-142">Produto</span><span class="sxs-lookup"><span data-stu-id="0b665-142">Product</span></span><br/>                  | <span data-ttu-id="0b665-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0b665-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0b665-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0b665-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b665-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b665-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0b665-146">IID</span><span class="sxs-lookup"><span data-stu-id="0b665-146">IID</span></span><br/>                      | <span data-ttu-id="0b665-147">IID \_ IVMKeyboard é definido como 00695f2e-c5ad-4d6e-B1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="0b665-147">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="0b665-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b665-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b665-149">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="0b665-149">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> <dt>

[<span data-ttu-id="0b665-150">Sequências de chave</span><span class="sxs-lookup"><span data-stu-id="0b665-150">Key Sequences</span></span>](key-sequences.md)
</dt> </dl>

 

