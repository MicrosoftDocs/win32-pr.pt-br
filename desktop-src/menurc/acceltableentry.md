---
title: Estrutura ACCELTABLEENTRY
description: Descreve os dados em um recurso de tabela de acelerador individual. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: 510594ae-56ea-49fb-abd3-ec06e51f2e0e
keywords:
- Menus de estrutura ACCELTABLEENTRY e outros recursos
topic_type:
- apiref
api_name:
- ACCELTABLEENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9ff12fe39f2ea54c90530133263bceb157d79dcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455935"
---
# <a name="acceltableentry-structure"></a><span data-ttu-id="f4b73-105">Estrutura ACCELTABLEENTRY</span><span class="sxs-lookup"><span data-stu-id="f4b73-105">ACCELTABLEENTRY structure</span></span>

<span data-ttu-id="f4b73-106">Descreve os dados em um recurso de tabela de acelerador individual.</span><span class="sxs-lookup"><span data-stu-id="f4b73-106">Describes the data in an individual accelerator table resource.</span></span> <span data-ttu-id="f4b73-107">A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.</span><span class="sxs-lookup"><span data-stu-id="f4b73-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4b73-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4b73-108">Syntax</span></span>


```C++
typedef struct {
  WORD fFlags;
  WORD wAnsi;
  WORD wId;
  WORD padding;
} ACCELTABLEENTRY;
```



## <a name="members"></a><span data-ttu-id="f4b73-109">Membros</span><span class="sxs-lookup"><span data-stu-id="f4b73-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="f4b73-110">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="f4b73-110">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="f4b73-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="f4b73-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="f4b73-112">Descreve as características do acelerador de teclado.</span><span class="sxs-lookup"><span data-stu-id="f4b73-112">Describes keyboard accelerator characteristics.</span></span> <span data-ttu-id="f4b73-113">Esse membro pode ter um ou mais dos seguintes valores de WinUser. h.</span><span class="sxs-lookup"><span data-stu-id="f4b73-113">This member can have one or more of the following values from Winuser.h.</span></span>



| <span data-ttu-id="f4b73-114">Valor</span><span class="sxs-lookup"><span data-stu-id="f4b73-114">Value</span></span>                                                                                                                                                                                                      | <span data-ttu-id="f4b73-115">Significado</span><span class="sxs-lookup"><span data-stu-id="f4b73-115">Meaning</span></span>                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVIRTKEY"></span><span id="fvirtkey"></span><dl> <span data-ttu-id="f4b73-116"><dt>**FVIRTKEY**</dt> <dt>true</dt></span><span class="sxs-lookup"><span data-stu-id="f4b73-116"><dt>**FVIRTKEY**</dt> <dt>TRUE</dt></span></span> </dl>    | <span data-ttu-id="f4b73-117">A chave do acelerador é um [código de chave virtual](/windows/desktop/inputdev/virtual-key-codes).</span><span class="sxs-lookup"><span data-stu-id="f4b73-117">The accelerator key is a [virtual-key code](/windows/desktop/inputdev/virtual-key-codes).</span></span> <span data-ttu-id="f4b73-118">Se esse sinalizador não for especificado, a tecla aceleradora será considerada para especificar um código de caractere ASCII.</span><span class="sxs-lookup"><span data-stu-id="f4b73-118">If this flag is not specified, the accelerator key is assumed to specify an ASCII character code.</span></span> <br/>                          |
| <span id="FNOINVERT"></span><span id="fnoinvert"></span><dl> <span data-ttu-id="f4b73-119"><dt>**FNOINVERT**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="f4b73-119"><dt>**FNOINVERT**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="f4b73-120">Um item de menu na barra de menus não é realçado quando um acelerador é usado.</span><span class="sxs-lookup"><span data-stu-id="f4b73-120">A menu item on the menu bar is not highlighted when an accelerator is used.</span></span> <span data-ttu-id="f4b73-121">Este atributo é obsoleto e mantido somente para compatibilidade com versões anteriores com arquivos de recursos projetados para o Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="f4b73-121">This attribute is obsolete and retained only for backward compatibility with resource files designed for 16-bit Windows.</span></span><br/> |
| <span id="FSHIFT"></span><span id="fshift"></span><dl> <span data-ttu-id="f4b73-122"><dt>**FSHIFT**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="f4b73-122"><dt>**FSHIFT**</dt> <dt>0x04</dt></span></span> </dl>          | <span data-ttu-id="f4b73-123">O acelerador será ativado somente se o usuário pressionar a tecla SHIFT.</span><span class="sxs-lookup"><span data-stu-id="f4b73-123">The accelerator is activated only if the user presses the SHIFT key.</span></span> <span data-ttu-id="f4b73-124">Esse sinalizador se aplica somente a chaves virtuais.</span><span class="sxs-lookup"><span data-stu-id="f4b73-124">This flag applies only to virtual keys.</span></span> <br/>                                                                                        |
| <span id="FCONTROL"></span><span id="fcontrol"></span><dl> <span data-ttu-id="f4b73-125"><dt>**FCONTROL**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="f4b73-125"><dt>**FCONTROL**</dt> <dt>0x08</dt></span></span> </dl>    | <span data-ttu-id="f4b73-126">O acelerador será ativado somente se o usuário pressionar a tecla CTRL.</span><span class="sxs-lookup"><span data-stu-id="f4b73-126">The accelerator is activated only if the user presses the CTRL key.</span></span> <span data-ttu-id="f4b73-127">Esse sinalizador se aplica somente a chaves virtuais.</span><span class="sxs-lookup"><span data-stu-id="f4b73-127">This flag applies only to virtual keys.</span></span> <br/>                                                                                         |
| <span id="FALT"></span><span id="falt"></span><dl> <span data-ttu-id="f4b73-128"><dt>**FALT**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="f4b73-128"><dt>**FALT**</dt> <dt>0x10</dt></span></span> </dl>                | <span data-ttu-id="f4b73-129">O acelerador será ativado somente se o usuário pressionar a tecla ALT.</span><span class="sxs-lookup"><span data-stu-id="f4b73-129">The accelerator is activated only if the user presses the ALT key.</span></span> <span data-ttu-id="f4b73-130">Esse sinalizador se aplica somente a chaves virtuais.</span><span class="sxs-lookup"><span data-stu-id="f4b73-130">This flag applies only to virtual keys.</span></span> <br/>                                                                                          |
| <span id="0x80"></span><span id="0X80"></span><dl> <span data-ttu-id="f4b73-131"><dt>**0x80**</dt></span><span class="sxs-lookup"><span data-stu-id="f4b73-131"><dt>**0x80**</dt></span></span> </dl>                                                                          | <span data-ttu-id="f4b73-132">A entrada é a última em uma tabela de acelerador.</span><span class="sxs-lookup"><span data-stu-id="f4b73-132">The entry is last in an accelerator table.</span></span> <br/>                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="f4b73-133">**wAnsi**</span><span class="sxs-lookup"><span data-stu-id="f4b73-133">**wAnsi**</span></span>
</dt> <dd>

<span data-ttu-id="f4b73-134">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="f4b73-134">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="f4b73-135">Um valor de caractere ANSI ou um código de chave virtual que identifica a chave do acelerador.</span><span class="sxs-lookup"><span data-stu-id="f4b73-135">An ANSI character value or a virtual-key code that identifies the accelerator key.</span></span>

</dd> <dt>

<span data-ttu-id="f4b73-136">**wId**</span><span class="sxs-lookup"><span data-stu-id="f4b73-136">**wId**</span></span>
</dt> <dd>

<span data-ttu-id="f4b73-137">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="f4b73-137">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="f4b73-138">Um identificador para o acelerador de teclado.</span><span class="sxs-lookup"><span data-stu-id="f4b73-138">An identifier for the keyboard accelerator.</span></span> <span data-ttu-id="f4b73-139">Esse é o valor passado para o procedimento de janela quando o usuário pressiona a tecla especificada.</span><span class="sxs-lookup"><span data-stu-id="f4b73-139">This is the value passed to the window procedure when the user presses the specified key.</span></span>

</dd> <dt>

<span data-ttu-id="f4b73-140">**padding**</span><span class="sxs-lookup"><span data-stu-id="f4b73-140">**padding**</span></span>
</dt> <dd>

<span data-ttu-id="f4b73-141">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="f4b73-141">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="f4b73-142">O número de bytes inseridos para garantir que a estrutura seja alinhada em um limite **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="f4b73-142">The number of bytes inserted to ensure that the structure is aligned on a **DWORD** boundary.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4b73-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4b73-143">Remarks</span></span>

<span data-ttu-id="f4b73-144">A estrutura **ACCELTABLEENTRY** é repetida para todas as entradas de tabela de acelerador no recurso.</span><span class="sxs-lookup"><span data-stu-id="f4b73-144">The **ACCELTABLEENTRY** structure is repeated for all accelerator table entries in the resource.</span></span> <span data-ttu-id="f4b73-145">A última entrada na tabela é sinalizada com o valor 0x0080.</span><span class="sxs-lookup"><span data-stu-id="f4b73-145">The last entry in the table is flagged with the value 0x0080.</span></span>

<span data-ttu-id="f4b73-146">Você pode calcular o número de elementos na tabela se dividir o comprimento do recurso em oito.</span><span class="sxs-lookup"><span data-stu-id="f4b73-146">You can compute the number of elements in the table if you divide the length of the resource by eight.</span></span> <span data-ttu-id="f4b73-147">Em seguida, seu aplicativo pode acessar aleatoriamente as entradas individuais de comprimento fixo.</span><span class="sxs-lookup"><span data-stu-id="f4b73-147">Then your application can randomly access the individual fixed-length entries.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4b73-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4b73-148">Requirements</span></span>



| <span data-ttu-id="f4b73-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4b73-149">Requirement</span></span> | <span data-ttu-id="f4b73-150">Valor</span><span class="sxs-lookup"><span data-stu-id="f4b73-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f4b73-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4b73-151">Minimum supported client</span></span><br/> | <span data-ttu-id="f4b73-152">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f4b73-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f4b73-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4b73-153">Minimum supported server</span></span><br/> | <span data-ttu-id="f4b73-154">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f4b73-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f4b73-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4b73-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="f4b73-156">**Referência**</span><span class="sxs-lookup"><span data-stu-id="f4b73-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f4b73-157">**CreateAcceleratorTable**</span><span class="sxs-lookup"><span data-stu-id="f4b73-157">**CreateAcceleratorTable**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)
</dt> <dt>

<span data-ttu-id="f4b73-158">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="f4b73-158">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f4b73-159">Recursos</span><span class="sxs-lookup"><span data-stu-id="f4b73-159">Resources</span></span>](resources.md)
</dt> </dl>

 

