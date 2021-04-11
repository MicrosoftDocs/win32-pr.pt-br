---
description: Contém informações sobre um formulário de impressão localizável.
ms.assetid: 5cc11a77-2b9d-44a4-88de-6ed0b7460bc8
title: Estrutura de FORM_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_2
- _FORM_INFO_2A
- _FORM_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 6e2129f9776706ce331677e75c5d9c81d82393c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169341"
---
# <a name="form_info_2-structure"></a><span data-ttu-id="5e589-103">Estrutura de informações de formulário \_ \_ 2</span><span class="sxs-lookup"><span data-stu-id="5e589-103">FORM\_INFO\_2 structure</span></span>

<span data-ttu-id="5e589-104">Contém informações sobre um formulário de impressão localizável.</span><span class="sxs-lookup"><span data-stu-id="5e589-104">Contains information about a localizable print form.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e589-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e589-105">Syntax</span></span>


```C++
typedef struct _FORM_INFO_2 {
  DWORD   Flags;
  LPTSTR  pName;
  SIZEL   Size;
  RECTL   ImageableArea;
  LPCSTR  pKeyword;
  DWORD   StringType;
  LPCTSTR pMuiDll;
  DWORD   dwResourceId;
  LPCTSTR pDisplayName;
  LANGID  wLangId;
} FORM_INFO_2, *PFORM_INFO_2;
```



## <a name="members"></a><span data-ttu-id="5e589-106">Membros</span><span class="sxs-lookup"><span data-stu-id="5e589-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5e589-107">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="5e589-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="5e589-108">As propriedades do formulário.</span><span class="sxs-lookup"><span data-stu-id="5e589-108">The form properties.</span></span> <span data-ttu-id="5e589-109">Os valores a seguir são definidos, mas apenas um pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="5e589-109">The following values are defined, but only one can be set.</span></span> <span data-ttu-id="5e589-110">Quando o **formulário \_ informações \_ 2** é retornado por [**GetForm**](getform.md) ou [**EnumForms**](enumforms.md), **flags** é definido como o valor atual no banco de dados de formulários.</span><span class="sxs-lookup"><span data-stu-id="5e589-110">When the **FORM\_INFO\_2** is returned by [**GetForm**](getform.md) or [**EnumForms**](enumforms.md), **Flags** is set to the current value in the forms database.</span></span>



| <span data-ttu-id="5e589-111">Valor</span><span class="sxs-lookup"><span data-stu-id="5e589-111">Value</span></span>         | <span data-ttu-id="5e589-112">Significado</span><span class="sxs-lookup"><span data-stu-id="5e589-112">Meaning</span></span>                                                                                                                                                                                                                                                                                  |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e589-113">usuário do formulário \_</span><span class="sxs-lookup"><span data-stu-id="5e589-113">FORM\_USER</span></span>    | <span data-ttu-id="5e589-114">Se esse sinalizador de bit for definido, o formulário terá sido definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="5e589-114">If this bit flag is set, the form has been defined by the user.</span></span> <span data-ttu-id="5e589-115">Formulários com esse sinalizador definido são definidos no registro.</span><span class="sxs-lookup"><span data-stu-id="5e589-115">Forms with this flag set are defined in the registry.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="5e589-116">FORMULÁRIO \_ interno</span><span class="sxs-lookup"><span data-stu-id="5e589-116">FORM\_BUILTIN</span></span> | <span data-ttu-id="5e589-117">Se esse sinalizador de bit estiver definido, o formulário será parte do spooler.</span><span class="sxs-lookup"><span data-stu-id="5e589-117">If this bit-flag is set, the form is part of the spooler.</span></span> <span data-ttu-id="5e589-118">As definições de formulário com este sinalizador definido não aparecem no registro.</span><span class="sxs-lookup"><span data-stu-id="5e589-118">Form definitions with this flag set do not appear in the registry.</span></span> <span data-ttu-id="5e589-119">Os formulários internos não podem ser modificados, portanto, esse sinalizador não deve ser definido quando a estrutura é passada para [**AddForm**](addform.md) ou [**setform**](setform.md).</span><span class="sxs-lookup"><span data-stu-id="5e589-119">Built-in forms cannot be modified, so this flag should not be set when the structure is passed to [**AddForm**](addform.md) or [**SetForm**](setform.md).</span></span> |
| <span data-ttu-id="5e589-120">impressora de formulário \_</span><span class="sxs-lookup"><span data-stu-id="5e589-120">FORM\_PRINTER</span></span> | <span data-ttu-id="5e589-121">Se esse sinalizador de bit for definido, o formulário será associado a uma determinada impressora e sua definição aparecerá no registro.</span><span class="sxs-lookup"><span data-stu-id="5e589-121">If this bit flag is set, the form is associated with a certain printer, and its definition appears in the registry.</span></span>                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="5e589-122">**pName**</span><span class="sxs-lookup"><span data-stu-id="5e589-122">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="5e589-123">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do formulário.</span><span class="sxs-lookup"><span data-stu-id="5e589-123">A pointer to a null-terminated string that specifies the name of the form.</span></span> <span data-ttu-id="5e589-124">O nome do formulário não pode exceder 31 caracteres.</span><span class="sxs-lookup"><span data-stu-id="5e589-124">The form name cannot exceed 31 characters.</span></span>

</dd> <dt>

<span data-ttu-id="5e589-125">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="5e589-125">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="5e589-126">A largura e a altura do formulário em milésimos de milímetros.</span><span class="sxs-lookup"><span data-stu-id="5e589-126">The width and height of the form in thousandths of millimeters.</span></span>

</dd> <dt>

<span data-ttu-id="5e589-127">**ImageableArea**</span><span class="sxs-lookup"><span data-stu-id="5e589-127">**ImageableArea**</span></span>
</dt> <dd>

<span data-ttu-id="5e589-128">A largura e a altura, em milésimos de milímetros, da área da página na qual a impressora pode imprimir.</span><span class="sxs-lookup"><span data-stu-id="5e589-128">The width and height, in thousandths of millimeters, of the area of the page on which the printer can print.</span></span>

</dd> <dt>

<span data-ttu-id="5e589-129">**pKeyword**</span><span class="sxs-lookup"><span data-stu-id="5e589-129">**pKeyword**</span></span>
</dt> <dd>

<span data-ttu-id="5e589-130">Um ponteiro para um identificador de cadeia de caracteres não localizável do formulário.</span><span class="sxs-lookup"><span data-stu-id="5e589-130">A pointer to a non-localizable string identifier of the form.</span></span> <span data-ttu-id="5e589-131">Quando passado para [**AddFormat**](addform.md) ou [**setform**](setform.md), isso fornece ao chamador um meio de identificar o formulário em todas as localidades.</span><span class="sxs-lookup"><span data-stu-id="5e589-131">When passed to [**AddForm**](addform.md) or [**SetForm**](setform.md), this gives the caller a means of identifying the form in all locales.</span></span>

</dd> <dt>

<span data-ttu-id="5e589-132">**StringType**</span><span class="sxs-lookup"><span data-stu-id="5e589-132">**StringType**</span></span>
</dt> <dd>

<span data-ttu-id="5e589-133">Especifica como um nome de exibição localizado para o formulário é obtido em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="5e589-133">Specifies how a localized display name for the form is obtained at runtime.</span></span> <span data-ttu-id="5e589-134">Os valores a seguir são definidos.</span><span class="sxs-lookup"><span data-stu-id="5e589-134">The following values are defined.</span></span> <span data-ttu-id="5e589-135">Apenas um pode ser definido em qualquer chamada fornecida para [**AddForm**](addform.md) ou [**setform**](setform.md).</span><span class="sxs-lookup"><span data-stu-id="5e589-135">Only one can be set in any given call to [**AddForm**](addform.md) or [**SetForm**](setform.md).</span></span> <span data-ttu-id="5e589-136">A cadeia de caracteres \_ MUIDLL e a cadeia de caracteres \_ LANGPAIR podem ser definidas no **formato \_ info \_ 2** (s) retornado por [**GetForm**](getform.md) ou [**EnumForms**](enumforms.md).</span><span class="sxs-lookup"><span data-stu-id="5e589-136">Both STRING\_MUIDLL and STRING\_LANGPAIR can be set in the **FORM\_INFO\_2** (s) returned by [**GetForm**](getform.md) or [**EnumForms**](enumforms.md).</span></span> <span data-ttu-id="5e589-137">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="5e589-137">See Remarks.</span></span>



| <span data-ttu-id="5e589-138">Valor</span><span class="sxs-lookup"><span data-stu-id="5e589-138">Value</span></span>            | <span data-ttu-id="5e589-139">Significado</span><span class="sxs-lookup"><span data-stu-id="5e589-139">Meaning</span></span>                                                                                                                                                                                        |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e589-140">Cadeia de caracteres \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="5e589-140">STRING\_NONE</span></span>     | <span data-ttu-id="5e589-141">Não há nenhum nome de exibição localizado.</span><span class="sxs-lookup"><span data-stu-id="5e589-141">There is no localized display name.</span></span>                                                                                                                                                            |
| <span data-ttu-id="5e589-142">Cadeia de caracteres \_ MUIDLL</span><span class="sxs-lookup"><span data-stu-id="5e589-142">STRING\_MUIDLL</span></span>   | <span data-ttu-id="5e589-143">O nome de exibição é extraído da DLL de recursos localizadas da [interface do usuário multilíngüe](/windows/desktop/Intl/mui-resource-management) especificada em **pMuiDll**.</span><span class="sxs-lookup"><span data-stu-id="5e589-143">The display name is extracted from the [Multilingual User Interface](/windows/desktop/Intl/mui-resource-management) localized resources DLL specified in **pMuiDll**.</span></span> <span data-ttu-id="5e589-144">A ID está no membro **dwResourceId** .</span><span class="sxs-lookup"><span data-stu-id="5e589-144">The ID is in the **dwResourceId** member.</span></span> |
| <span data-ttu-id="5e589-145">Cadeia de caracteres \_ LANGPAIR</span><span class="sxs-lookup"><span data-stu-id="5e589-145">STRING\_LANGPAIR</span></span> | <span data-ttu-id="5e589-146">O nome de exibição e a ID de idioma são fornecidos diretamente pelo **pDisplayName** e o idioma é especificado por **wLangId**.</span><span class="sxs-lookup"><span data-stu-id="5e589-146">The display name and language ID are provided directly by **pDisplayName** and the language is specified by **wLangId**.</span></span>                                                                       |



 

</dd> <dt>

<span data-ttu-id="5e589-147">**pMuiDll**</span><span class="sxs-lookup"><span data-stu-id="5e589-147">**pMuiDll**</span></span>
</dt> <dd>

<span data-ttu-id="5e589-148">A DLL de recurso localizada da [interface de usuário multilíngue](/windows/desktop/Intl/mui-resource-management) que contém o nome de exibição localizado.</span><span class="sxs-lookup"><span data-stu-id="5e589-148">The [Multilingual User Interface](/windows/desktop/Intl/mui-resource-management) localized resource DLL that contains the localized display name.</span></span>

</dd> <dt>

<span data-ttu-id="5e589-149">**dwResourceId**</span><span class="sxs-lookup"><span data-stu-id="5e589-149">**dwResourceId**</span></span>
</dt> <dd>

<span data-ttu-id="5e589-150">A ID de recurso do nome de exibição do formulário em **pMuiDll**.</span><span class="sxs-lookup"><span data-stu-id="5e589-150">The resource ID of the form's display name in **pMuiDll**.</span></span>

</dd> <dt>

<span data-ttu-id="5e589-151">**pDisplayName**</span><span class="sxs-lookup"><span data-stu-id="5e589-151">**pDisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="5e589-152">O nome de exibição do formulário no idioma especificado por **wLangId**.</span><span class="sxs-lookup"><span data-stu-id="5e589-152">The form's display name in the language specified by **wLangId**.</span></span>

</dd> <dt>

<span data-ttu-id="5e589-153">**wLangId**</span><span class="sxs-lookup"><span data-stu-id="5e589-153">**wLangId**</span></span>
</dt> <dd>

<span data-ttu-id="5e589-154">O idioma do **pDisplayName**.</span><span class="sxs-lookup"><span data-stu-id="5e589-154">The language of the **pDisplayName**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e589-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e589-155">Remarks</span></span>

<span data-ttu-id="5e589-156">Em uma chamada para [**AddForm**](addform.md) ou [**setform**](setform.md):</span><span class="sxs-lookup"><span data-stu-id="5e589-156">On a call to [**AddForm**](addform.md) or [**SetForm**](setform.md):</span></span>

-   <span data-ttu-id="5e589-157">Se **StringType** for String \_ None, **pMuiDll** e **PDisplayName** deverão ser **nulos** e **dwResourceId** e **wLangId** deverão ser 0.</span><span class="sxs-lookup"><span data-stu-id="5e589-157">If **StringType** is STRING\_NONE, both **pMuiDll** and **pDisplayName** must be **NULL** and both **dwResourceId** and **wLangId** must be 0.</span></span>
-   <span data-ttu-id="5e589-158">Se **StringType** for cadeia \_ de caracteres MUIDLL, **pDisplayName** deverá ser **nulo** e **wLangId** deverá ser 0.</span><span class="sxs-lookup"><span data-stu-id="5e589-158">If **StringType** is STRING\_MUIDLL, **pDisplayName** must be **NULL** and **wLangId** must be 0.</span></span>
-   <span data-ttu-id="5e589-159">Se **StringType** for cadeia \_ de caracteres LANGPAIR, **pMuiDll** deverá ser **nulo** e **dwResourceId** deverá ser 0.</span><span class="sxs-lookup"><span data-stu-id="5e589-159">If **StringType** is STRING\_LANGPAIR, **pMuiDll** must be **NULL** and **dwResourceId** must be 0.</span></span>

<span data-ttu-id="5e589-160">Para uma **informação de formulário \_ \_ 2** retornada por uma chamada para [**GetForm**](getform.md) ou [**EnumForms**](enumforms.md):</span><span class="sxs-lookup"><span data-stu-id="5e589-160">For a **FORM\_INFO\_2** returned by a call to [**GetForm**](getform.md) or [**EnumForms**](enumforms.md):</span></span>

-   <span data-ttu-id="5e589-161">Se **StringType** for a cadeia \_ de caracteres MUIDLL e a cadeia de caracteres \_ LANGPAIR, **pMuiDll**, **pDisplayName**, **dwResourceId** e **wLangId** terão valores válidos.</span><span class="sxs-lookup"><span data-stu-id="5e589-161">If **StringType** is both STRING\_MUIDLL and STRING\_LANGPAIR, **pMuiDll**, **pDisplayName**, **dwResourceId**, and **wLangId** will all have valid values.</span></span>
-   <span data-ttu-id="5e589-162">Se **StringType** for String \_ MUIDLL somente, **pMuiDll** e **dwResourceId** terão valores válidos.</span><span class="sxs-lookup"><span data-stu-id="5e589-162">If **StringType** is STRING\_MUIDLL only, **pMuiDll** and **dwResourceId** will have valid values.</span></span> <span data-ttu-id="5e589-163">**pDisplayName** será **NULL** e **wLangId** será 0.</span><span class="sxs-lookup"><span data-stu-id="5e589-163">**pDisplayName** will be **NULL** and **wLangId** will be 0.</span></span>
-   <span data-ttu-id="5e589-164">Se **StringType** for String \_ LANGPAIR somente, **pDisplayName** e **wLangId** terão valores válidos.</span><span class="sxs-lookup"><span data-stu-id="5e589-164">If **StringType** is STRING\_LANGPAIR only, **pDisplayName** and **wLangId** will have valid values.</span></span> <span data-ttu-id="5e589-165">**pMuiDll** será **NULL** e **dwResourceId** será 0.</span><span class="sxs-lookup"><span data-stu-id="5e589-165">**pMuiDll** will be **NULL** and **dwResourceId** will be 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e589-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e589-166">Requirements</span></span>



| <span data-ttu-id="5e589-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e589-167">Requirement</span></span> | <span data-ttu-id="5e589-168">Valor</span><span class="sxs-lookup"><span data-stu-id="5e589-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e589-169">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e589-169">Minimum supported client</span></span><br/> | <span data-ttu-id="5e589-170">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e589-170">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="5e589-171">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e589-171">Minimum supported server</span></span><br/> | <span data-ttu-id="5e589-172">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5e589-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5e589-173">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5e589-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e589-174"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e589-174"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5e589-175">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="5e589-175">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5e589-176">Informações de **\_ formulário \_ \_ 2W** (Unicode) e **\_ informações de formulário \_ \_ 2a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5e589-176">**\_FORM\_INFO\_2W** (Unicode) and **\_FORM\_INFO\_2A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="5e589-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e589-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e589-178">Impressão</span><span class="sxs-lookup"><span data-stu-id="5e589-178">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5e589-179">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="5e589-179">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="5e589-180">Interface do Usuário Multilíngue</span><span class="sxs-lookup"><span data-stu-id="5e589-180">Multilingual User Interface</span></span>](/windows/desktop/Intl/mui-resource-management)
</dt> <dt>

[<span data-ttu-id="5e589-181">**AddFormat**</span><span class="sxs-lookup"><span data-stu-id="5e589-181">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="5e589-182">**GetForm**</span><span class="sxs-lookup"><span data-stu-id="5e589-182">**GetForm**</span></span>](getform.md)
</dt> <dt>

[<span data-ttu-id="5e589-183">**EnumForms**</span><span class="sxs-lookup"><span data-stu-id="5e589-183">**EnumForms**</span></span>](enumforms.md)
</dt> <dt>

[<span data-ttu-id="5e589-184">**Formulário**</span><span class="sxs-lookup"><span data-stu-id="5e589-184">**SetForm**</span></span>](setform.md)
</dt> </dl>

 

