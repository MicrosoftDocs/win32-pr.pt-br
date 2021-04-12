---
title: Mensagem de HKM_SETRULES (commctrl. h)
description: Define as combinações inválidas e a combinação de modificador padrão para um controle de tecla de acesso.
ms.assetid: de3dd463-a534-4c7c-ae04-da80a3bff2ab
keywords:
- Controles de HKM_SETRULES de mensagens do Windows
topic_type:
- apiref
api_name:
- HKM_SETRULES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33c0918a7bb44fdac9a1f2c60fdde8e06b5e679
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455339"
---
# <a name="hkm_setrules-message"></a><span data-ttu-id="4ee6f-104">\_Mensagem hkm SETrules</span><span class="sxs-lookup"><span data-stu-id="4ee6f-104">HKM\_SETRULES message</span></span>

<span data-ttu-id="4ee6f-105">Define as combinações inválidas e a combinação de modificador padrão para um controle de tecla de acesso.</span><span class="sxs-lookup"><span data-stu-id="4ee6f-105">Defines the invalid combinations and the default modifier combination for a hot key control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4ee6f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ee6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ee6f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4ee6f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ee6f-108">Uma matriz de sinalizadores que especificam combinações de chaves inválidas.</span><span class="sxs-lookup"><span data-stu-id="4ee6f-108">An array of flags that specify invalid key combinations.</span></span> <span data-ttu-id="4ee6f-109">Esse parâmetro pode ser uma combinação dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="4ee6f-109">This parameter can be a combination of the following values:</span></span>



| <span data-ttu-id="4ee6f-110">Valor</span><span class="sxs-lookup"><span data-stu-id="4ee6f-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="4ee6f-111">Significado</span><span class="sxs-lookup"><span data-stu-id="4ee6f-111">Meaning</span></span>                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span id="HKCOMB_A"></span><span id="hkcomb_a"></span><dl> <span data-ttu-id="4ee6f-112"><dt>**HKCOMB \_ A**</dt></span><span class="sxs-lookup"><span data-stu-id="4ee6f-112"><dt>**HKCOMB\_A**</dt></span></span> </dl>          | <span data-ttu-id="4ee6f-113">ALT</span><span class="sxs-lookup"><span data-stu-id="4ee6f-113">ALT</span></span><br/>             |
| <span id="HKCOMB_C"></span><span id="hkcomb_c"></span><dl> <span data-ttu-id="4ee6f-114"><dt>**HKCOMB \_ C**</dt></span><span class="sxs-lookup"><span data-stu-id="4ee6f-114"><dt>**HKCOMB\_C**</dt></span></span> </dl>          | <span data-ttu-id="4ee6f-115">CTRL</span><span class="sxs-lookup"><span data-stu-id="4ee6f-115">CTRL</span></span><br/>            |
| <span id="HKCOMB_CA"></span><span id="hkcomb_ca"></span><dl> <span data-ttu-id="4ee6f-116"><dt>**\_AC HKCOMB**</dt></span><span class="sxs-lookup"><span data-stu-id="4ee6f-116"><dt>**HKCOMB\_CA**</dt></span></span> </dl>       | <span data-ttu-id="4ee6f-117">CTRL + ALT</span><span class="sxs-lookup"><span data-stu-id="4ee6f-117">CTRL+ALT</span></span><br/>        |
| <span id="HKCOMB_NONE"></span><span id="hkcomb_none"></span><dl> <span data-ttu-id="4ee6f-118"><dt>**HKCOMB \_ nenhum**</dt></span><span class="sxs-lookup"><span data-stu-id="4ee6f-118"><dt>**HKCOMB\_NONE**</dt></span></span> </dl> | <span data-ttu-id="4ee6f-119">Chaves não modificadas</span><span class="sxs-lookup"><span data-stu-id="4ee6f-119">Unmodified keys</span></span><br/> |
| <span id="HKCOMB_S"></span><span id="hkcomb_s"></span><dl> <span data-ttu-id="4ee6f-120"><dt>**HKCOMB \_ S**</dt></span><span class="sxs-lookup"><span data-stu-id="4ee6f-120"><dt>**HKCOMB\_S**</dt></span></span> </dl>          | <span data-ttu-id="4ee6f-121">ALTERNÂNCIA</span><span class="sxs-lookup"><span data-stu-id="4ee6f-121">SHIFT</span></span><br/>           |
| <span id="HKCOMB_SA"></span><span id="hkcomb_sa"></span><dl> <span data-ttu-id="4ee6f-122"><dt>**\_SA HKCOMB**</dt></span><span class="sxs-lookup"><span data-stu-id="4ee6f-122"><dt>**HKCOMB\_SA**</dt></span></span> </dl>       | <span data-ttu-id="4ee6f-123">SHIFT+ALT</span><span class="sxs-lookup"><span data-stu-id="4ee6f-123">SHIFT+ALT</span></span><br/>       |
| <span id="HKCOMB_SC"></span><span id="hkcomb_sc"></span><dl> <span data-ttu-id="4ee6f-124"><dt>**HKCOMB \_ SC**</dt></span><span class="sxs-lookup"><span data-stu-id="4ee6f-124"><dt>**HKCOMB\_SC**</dt></span></span> </dl>       | <span data-ttu-id="4ee6f-125">SHIFT + CTRL</span><span class="sxs-lookup"><span data-stu-id="4ee6f-125">SHIFT+CTRL</span></span><br/>      |
| <span id="HKCOMB_SCA"></span><span id="hkcomb_sca"></span><dl> <span data-ttu-id="4ee6f-126"><dt>**HKCOMB \_ SCA**</dt></span><span class="sxs-lookup"><span data-stu-id="4ee6f-126"><dt>**HKCOMB\_SCA**</dt></span></span> </dl>    | <span data-ttu-id="4ee6f-127">SHIFT + CTRL + ALT</span><span class="sxs-lookup"><span data-stu-id="4ee6f-127">SHIFT+CTRL+ALT</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="4ee6f-128">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4ee6f-128">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ee6f-129">Uma matriz de sinalizadores que especificam a combinação de teclas a ser usada quando o usuário insere uma combinação inválida.</span><span class="sxs-lookup"><span data-stu-id="4ee6f-129">An array of flags that specify the key combination to use when the user enters an invalid combination.</span></span> <span data-ttu-id="4ee6f-130">Para obter uma lista de valores de sinalizador modificadores, consulte a descrição da mensagem [**hkm \_ getteclaize**](hkm-gethotkey.md) .</span><span class="sxs-lookup"><span data-stu-id="4ee6f-130">For a list of modifier flag values, see the description of the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ee6f-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4ee6f-131">Return value</span></span>

<span data-ttu-id="4ee6f-132">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="4ee6f-132">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ee6f-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ee6f-133">Remarks</span></span>

<span data-ttu-id="4ee6f-134">Quando um usuário insere uma combinação de teclas inválida, conforme definido pelos sinalizadores especificados em *wParam*, o sistema usa o operador bit-a-or para combinar as chaves inseridas pelo usuário com os sinalizadores especificados em *lParam*.</span><span class="sxs-lookup"><span data-stu-id="4ee6f-134">When a user enters an invalid key combination, as defined by flags specified in *wParam*, the system uses the bitwise-OR operator to combine the keys entered by the user with the flags specified in *lParam*.</span></span> <span data-ttu-id="4ee6f-135">A combinação de chave resultante é convertida em uma cadeia de caracteres e, em seguida, exibida no controle de tecla de acesso.</span><span class="sxs-lookup"><span data-stu-id="4ee6f-135">The resulting key combination is converted into a string and then displayed in the hot key control.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ee6f-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ee6f-136">Requirements</span></span>



| <span data-ttu-id="4ee6f-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ee6f-137">Requirement</span></span> | <span data-ttu-id="4ee6f-138">Valor</span><span class="sxs-lookup"><span data-stu-id="4ee6f-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4ee6f-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ee6f-139">Minimum supported client</span></span><br/> | <span data-ttu-id="4ee6f-140">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4ee6f-140">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4ee6f-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ee6f-141">Minimum supported server</span></span><br/> | <span data-ttu-id="4ee6f-142">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4ee6f-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4ee6f-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4ee6f-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ee6f-144"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ee6f-144"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





