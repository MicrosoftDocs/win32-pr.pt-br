---
title: Constantes de TF_MOD_ (msctf. h)
description: O TF \_ mod \_ \ Constants especifica os modificadores de chave na \_ estrutura TF PRESERVEDKEY.
ms.assetid: 4642ef17-34bd-4482-a9e9-0fbed7b574b1
topic_type:
- apiref
api_name:
- TF_MOD_ALT
- TF_MOD_CONTROL
- TF_MOD_SHIFT
- TF_MOD_RALT
- TF_MOD_RCONTROL
- TF_MOD_RSHIFT
- TF_MOD_LALT
- TF_MOD_LCONTROL
- TF_MOD_LSHIFT
- TF_MOD_ON_KEYUP
- TF_MOD_IGNORE_ALL_MODIFIER
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e67e081d9a0f8714410861c7c36f9f751bad8d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009329"
---
# <a name="tf_mod_-constants"></a><span data-ttu-id="9aa3b-103">Constantes de TF \_ mod \_ \*</span><span class="sxs-lookup"><span data-stu-id="9aa3b-103">TF\_MOD\_\* Constants</span></span>

<span data-ttu-id="9aa3b-104">As \_ constantes TF mod \_ \* especificam modificadores de chave na estrutura [TF \_ PRESERVEDKEY](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey) .</span><span class="sxs-lookup"><span data-stu-id="9aa3b-104">The TF\_MOD\_\* constants specify key modifiers in the [TF\_PRESERVEDKEY](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey) structure.</span></span>



| <span data-ttu-id="9aa3b-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="9aa3b-105">Constant/value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="9aa3b-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="9aa3b-106">Description</span></span>                                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_MOD_ALT"></span><span id="tf_mod_alt"></span><dl> <span data-ttu-id="9aa3b-107"><dt>**TF \_ MOD \_ ALT**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="9aa3b-107"><dt>**TF\_MOD\_ALT**</dt> <dt>0x0001</dt></span></span> </dl>                                                   | <span data-ttu-id="9aa3b-108">Uma das teclas ALT é pressionada</span><span class="sxs-lookup"><span data-stu-id="9aa3b-108">Either of the ALT keys is pressed</span></span><br/>                                                                                                                                         |
| <span id="TF_MOD_CONTROL"></span><span id="tf_mod_control"></span><dl> <span data-ttu-id="9aa3b-109"><dt>**TF \_ 0x0002 de \_ controle mod**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9aa3b-109"><dt>**TF\_MOD\_CONTROL**</dt> <dt>0x0002</dt></span></span> </dl>                                       | <span data-ttu-id="9aa3b-110">Uma das teclas CTRL é pressionada</span><span class="sxs-lookup"><span data-stu-id="9aa3b-110">Either of the CTRL keys is pressed</span></span><br/>                                                                                                                                        |
| <span id="TF_MOD_SHIFT"></span><span id="tf_mod_shift"></span><dl> <span data-ttu-id="9aa3b-111"><dt>**TF \_ MOD \_ Shift**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="9aa3b-111"><dt>**TF\_MOD\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>                                             | <span data-ttu-id="9aa3b-112">Uma das teclas SHIFT é pressionada</span><span class="sxs-lookup"><span data-stu-id="9aa3b-112">Either of the SHIFT keys is pressed</span></span><br/>                                                                                                                                       |
| <span id="TF_MOD_RALT"></span><span id="tf_mod_ralt"></span><dl> <span data-ttu-id="9aa3b-113"><dt>**TF \_ MOD \_ Ralt**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="9aa3b-113"><dt>**TF\_MOD\_RALT**</dt> <dt>0x0008</dt></span></span> </dl>                                                | <span data-ttu-id="9aa3b-114">A tecla ALT direita é pressionada</span><span class="sxs-lookup"><span data-stu-id="9aa3b-114">The right ALT key is pressed</span></span><br/>                                                                                                                                              |
| <span id="TF_MOD_RCONTROL"></span><span id="tf_mod_rcontrol"></span><dl> <span data-ttu-id="9aa3b-115"><dt>**TF \_ MOD \_ RCONTROL**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="9aa3b-115"><dt>**TF\_MOD\_RCONTROL**</dt> <dt>0x0010</dt></span></span> </dl>                                    | <span data-ttu-id="9aa3b-116">A tecla CTRL direita é pressionada</span><span class="sxs-lookup"><span data-stu-id="9aa3b-116">The right CTRL key is pressed</span></span><br/>                                                                                                                                             |
| <span id="TF_MOD_RSHIFT"></span><span id="tf_mod_rshift"></span><dl> <span data-ttu-id="9aa3b-117"><dt>**TF \_ MOD \_ RSHIFT**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="9aa3b-117"><dt>**TF\_MOD\_RSHIFT**</dt> <dt>0x0020</dt></span></span> </dl>                                          | <span data-ttu-id="9aa3b-118">A tecla SHIFT direita é pressionada</span><span class="sxs-lookup"><span data-stu-id="9aa3b-118">The right SHIFT key is pressed</span></span><br/>                                                                                                                                            |
| <span id="TF_MOD_LALT"></span><span id="tf_mod_lalt"></span><dl> <span data-ttu-id="9aa3b-119"><dt>**TF \_ MOD \_ LALT**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="9aa3b-119"><dt>**TF\_MOD\_LALT**</dt> <dt>0x0040</dt></span></span> </dl>                                                | <span data-ttu-id="9aa3b-120">A tecla ALT esquerda é pressionada</span><span class="sxs-lookup"><span data-stu-id="9aa3b-120">The left ALT key is pressed</span></span><br/>                                                                                                                                               |
| <span id="TF_MOD_LCONTROL"></span><span id="tf_mod_lcontrol"></span><dl> <span data-ttu-id="9aa3b-121"><dt>**TF \_ MOD \_ LCONTROL**</dt> <dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="9aa3b-121"><dt>**TF\_MOD\_LCONTROL**</dt> <dt>0x0080</dt></span></span> </dl>                                    | <span data-ttu-id="9aa3b-122">A tecla CTRL esquerda é pressionada</span><span class="sxs-lookup"><span data-stu-id="9aa3b-122">The left CTRL key is pressed</span></span><br/>                                                                                                                                              |
| <span id="TF_MOD_LSHIFT"></span><span id="tf_mod_lshift"></span><dl> <span data-ttu-id="9aa3b-123"><dt>**TF \_ MOD \_ LSHIFT**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="9aa3b-123"><dt>**TF\_MOD\_LSHIFT**</dt> <dt>0x0100</dt></span></span> </dl>                                          | <span data-ttu-id="9aa3b-124">A tecla SHIFT esquerda é pressionada</span><span class="sxs-lookup"><span data-stu-id="9aa3b-124">The left SHIFT key is pressed</span></span><br/>                                                                                                                                             |
| <span id="TF_MOD_ON_KEYUP"></span><span id="tf_mod_on_keyup"></span><dl> <span data-ttu-id="9aa3b-125"><dt>**TF \_ MOD \_ em \_**</dt> <dt>0x0200</dt> KEYUP</span><span class="sxs-lookup"><span data-stu-id="9aa3b-125"><dt>**TF\_MOD\_ON\_KEYUP**</dt> <dt>0x0200</dt></span></span> </dl>                                   | <span data-ttu-id="9aa3b-126">O evento será acionado quando a chave for liberada.</span><span class="sxs-lookup"><span data-stu-id="9aa3b-126">The event will be fired when the key is released.</span></span> <span data-ttu-id="9aa3b-127">Sem esse sinalizador, o evento é acionado quando a tecla é pressionada.</span><span class="sxs-lookup"><span data-stu-id="9aa3b-127">Without this flag, the event is fired when the key is pressed.</span></span><br/>                                                          |
| <span id="TF_MOD_IGNORE_ALL_MODIFIER"></span><span id="tf_mod_ignore_all_modifier"></span><dl> <span data-ttu-id="9aa3b-128"><dt>**TF \_ MOD \_ ignorar \_ todos os 0x0400 \_ modificadores**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9aa3b-128"><dt>**TF\_MOD\_IGNORE\_ALL\_MODIFIER**</dt> <dt>0x0400</dt></span></span> </dl> | <span data-ttu-id="9aa3b-129">O estado das teclas ALT, CTRL e SHIFT é ignorado.</span><span class="sxs-lookup"><span data-stu-id="9aa3b-129">The state of the ALT, CTRL, and SHIFT keys is ignored.</span></span> <span data-ttu-id="9aa3b-130">Isso significa que o evento será acionado quando a tecla virtual for pressionada, independentemente de quais teclas modificadoras forem pressionadas.</span><span class="sxs-lookup"><span data-stu-id="9aa3b-130">This means the event will be fired when the virtual key is pressed, regardless of which modifier keys are pressed.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="9aa3b-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9aa3b-131">Requirements</span></span>



| <span data-ttu-id="9aa3b-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="9aa3b-132">Requirement</span></span> | <span data-ttu-id="9aa3b-133">Valor</span><span class="sxs-lookup"><span data-stu-id="9aa3b-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9aa3b-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9aa3b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9aa3b-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9aa3b-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9aa3b-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9aa3b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9aa3b-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9aa3b-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9aa3b-138">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="9aa3b-138">Redistributable</span></span><br/>          | <span data-ttu-id="9aa3b-139">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9aa3b-139">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="9aa3b-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9aa3b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="9aa3b-141"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="9aa3b-141"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="9aa3b-142">INSERI</span><span class="sxs-lookup"><span data-stu-id="9aa3b-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9aa3b-143"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9aa3b-143"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9aa3b-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="9aa3b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aa3b-145">TF \_ PRESERVEDKEY</span><span class="sxs-lookup"><span data-stu-id="9aa3b-145">TF\_PRESERVEDKEY</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey)
</dt> </dl>

 

 





