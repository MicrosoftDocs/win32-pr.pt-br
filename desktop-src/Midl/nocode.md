---
title: atributo Nocode
description: O atributo \ Nocode \ é usado em cabeçalhos ACF ou com funções individuais para evitar a geração de código stub de cliente.
ms.assetid: d3b6e4c8-103c-4ea2-8748-11d844fdda97
keywords:
- MIDL de atributo Nocode
topic_type:
- apiref
api_name:
- nocode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64f5138dc1794e9b2714e5f64762c1af17b47fb2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293083"
---
# <a name="nocode-attribute"></a><span data-ttu-id="2318e-104">atributo Nocode</span><span class="sxs-lookup"><span data-stu-id="2318e-104">nocode attribute</span></span>

<span data-ttu-id="2318e-105">O atributo **\[ Nocode \]** é usado em cabeçalhos ACF ou com funções individuais para evitar a geração de código stub de cliente.</span><span class="sxs-lookup"><span data-stu-id="2318e-105">The **\[nocode\]** attribute is used in ACF headers or with individual functions to prevent the generation of client stub code.</span></span>

``` syntax
[ 
    nocode 
    [ , ACF-interface-attributes ] 
] 
interface interface-name
{
  [ include filename-list ; ]
  [ typedef [type-attribute-list] typename; ] 
  [ [ nocode [ , ACF-function-attributes ] ] function-name (
        [ ACF-parameter-attributes ] parameter-name ;
        ...);
  ]
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="2318e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2318e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2318e-107">*ACF-interface-atributos*</span><span class="sxs-lookup"><span data-stu-id="2318e-107">*ACF-interface-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="2318e-108">Especifica uma lista de um ou mais atributos que se aplicam à interface como um todo.</span><span class="sxs-lookup"><span data-stu-id="2318e-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="2318e-109">Os atributos válidos incluem o **\[** [**\_ identificador automático**](auto-handle.md) **\]** ou o **\[** [**\_ identificador implícito**](implicit-handle.md) **\]** e o **\[** [**código**](code.md) **\]** ou **\[ \] Nocode**.</span><span class="sxs-lookup"><span data-stu-id="2318e-109">Valid attributes include either **\[**[**auto\_handle**](auto-handle.md)**\]** or **\[**[**implicit\_handle**](implicit-handle.md)**\]** and either **\[**[**code**](code.md)**\]** or **\[nocode\]**.</span></span> <span data-ttu-id="2318e-110">Quando dois ou mais atributos de interface estão presentes, eles devem ser separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="2318e-110">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="2318e-111">*nome da interface*</span><span class="sxs-lookup"><span data-stu-id="2318e-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="2318e-112">Especifica o nome da interface.</span><span class="sxs-lookup"><span data-stu-id="2318e-112">Specifies the name of the interface.</span></span> <span data-ttu-id="2318e-113">No modo de compatibilidade com DCE, o nome da interface deve corresponder ao nome da interface especificada no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="2318e-113">In DCE-compatibility mode, the interface name must match the name of the interface specified in the IDL file.</span></span> <span data-ttu-id="2318e-114">Quando você usa o switch do compilador MIDL [**/ACF**](-acf.md), o nome da interface no ACF e o nome da interface no arquivo IDL podem ser diferentes.</span><span class="sxs-lookup"><span data-stu-id="2318e-114">When you use the MIDL compiler switch [**/acf**](-acf.md), the interface name in the ACF and the interface name in the IDL file can be different.</span></span>

</dd> <dt>

<span data-ttu-id="2318e-115">*nome do arquivo-lista*</span><span class="sxs-lookup"><span data-stu-id="2318e-115">*filename-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2318e-116">Especifica uma lista de um ou mais nomes de arquivos de cabeçalho de linguagem C, separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="2318e-116">Specifies a list of one or more C-language header file names, separated by commas.</span></span> <span data-ttu-id="2318e-117">O nome completo do arquivo, incluindo a extensão, deve ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="2318e-117">The full file name, including the extension, must be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="2318e-118">*lista de atributos de tipo*</span><span class="sxs-lookup"><span data-stu-id="2318e-118">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2318e-119">Especifica uma lista de um ou mais atributos, separados por vírgulas, que se aplicam ao tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="2318e-119">Specifies a list of one or more attributes, separated by commas, that apply to the specified type.</span></span> <span data-ttu-id="2318e-120">Os atributos de tipo válidos incluem **\[** [**ALLOCATE**](allocate.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="2318e-120">Valid type attributes include **\[**[**allocate**](allocate.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="2318e-121">*TypeName*</span><span class="sxs-lookup"><span data-stu-id="2318e-121">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="2318e-122">Especifica um tipo definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="2318e-122">Specifies a type defined in the IDL file.</span></span> <span data-ttu-id="2318e-123">Os atributos de tipo no ACF só podem ser aplicados a tipos definidos anteriormente no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="2318e-123">Type attributes in the ACF can only be applied to types previously defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="2318e-124">*ACF-função-atributos*</span><span class="sxs-lookup"><span data-stu-id="2318e-124">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="2318e-125">Especifica os atributos que se aplicam à função como um todo, como o **\[** [**\_ status de comunicação**](comm-status.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="2318e-125">Specifies attributes that apply to the function as a whole, such as **\[**[**comm\_status**](comm-status.md)**\]**.</span></span> <span data-ttu-id="2318e-126">Os atributos de função são colocados entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="2318e-126">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="2318e-127">Separe vários atributos de função com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="2318e-127">Separate multiple function attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="2318e-128">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="2318e-128">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="2318e-129">Especifica o nome da função, conforme definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="2318e-129">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="2318e-130">*ACF-parâmetros-atributos*</span><span class="sxs-lookup"><span data-stu-id="2318e-130">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="2318e-131">Especifica atributos de ACF que se aplicam a um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="2318e-131">Specifies ACF attributes that apply to a parameter.</span></span> <span data-ttu-id="2318e-132">Observe que zero ou mais atributos podem ser aplicados ao parâmetro.</span><span class="sxs-lookup"><span data-stu-id="2318e-132">Note that zero or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="2318e-133">Separe vários atributos de parâmetro com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="2318e-133">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="2318e-134">Os atributos de parâmetro de ACF são colocados entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="2318e-134">ACF parameter attributes are enclosed in square brackets.</span></span>

</dd> <dt>

<span data-ttu-id="2318e-135">*nome do parâmetro*</span><span class="sxs-lookup"><span data-stu-id="2318e-135">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="2318e-136">Especifica um parâmetro da função, conforme definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="2318e-136">Specifies a parameter of the function as defined in the IDL file.</span></span> <span data-ttu-id="2318e-137">Cada parâmetro para a função deve ser especificado na mesma sequência e usando o mesmo nome definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="2318e-137">Each parameter for the function must be specified in the same sequence and using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2318e-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="2318e-138">Remarks</span></span>

<span data-ttu-id="2318e-139">O atributo **\[ Nocode \]** pode aparecer no cabeçalho ACF ou pode ser aplicado a uma função individual.</span><span class="sxs-lookup"><span data-stu-id="2318e-139">The **\[nocode\]** attribute can appear in the ACF header, or it can be applied to an individual function.</span></span>

<span data-ttu-id="2318e-140">Quando o atributo **\[ \] Nocode** aparece no cabeçalho ACF, o código stub do cliente não é gerado para nenhuma função remota, a menos que ele tenha o atributo de função de **\[** [**código**](code.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="2318e-140">When the **\[nocode\]** attribute appears in the ACF header, client stub code is not generated for any remote function unless it has the **\[**[**code**](code.md)**\]** function attribute.</span></span> <span data-ttu-id="2318e-141">Você pode substituir o atributo **\[ Nocode \]** no cabeçalho de uma função individual especificando o atributo de **\[ código \]** como um atributo de função.</span><span class="sxs-lookup"><span data-stu-id="2318e-141">You can override the **\[nocode\]** attribute in the header for an individual function by specifying the **\[code\]** attribute as a function attribute.</span></span>

<span data-ttu-id="2318e-142">Quando o atributo **\[ Nocode \]** aparece na lista de atributos da função, nenhum código stub do cliente é gerado para a função.</span><span class="sxs-lookup"><span data-stu-id="2318e-142">When the **\[nocode\]** attribute appears in the function's attribute list, no client stub code is generated for the function.</span></span>

<span data-ttu-id="2318e-143">O código stub do cliente não é gerado quando:</span><span class="sxs-lookup"><span data-stu-id="2318e-143">Client stub code is not generated when:</span></span>

-   <span data-ttu-id="2318e-144">O cabeçalho ACF inclui o atributo **\[ Nocode \]** .</span><span class="sxs-lookup"><span data-stu-id="2318e-144">The ACF header includes the **\[nocode\]** attribute.</span></span>
-   <span data-ttu-id="2318e-145">O atributo **\[ Nocode \]** é aplicado à função.</span><span class="sxs-lookup"><span data-stu-id="2318e-145">The **\[nocode\]** attribute is applied to the function.</span></span>
-   <span data-ttu-id="2318e-146">O **\[** [](local.md) **\]** atributo local se aplica à função no arquivo de interface.</span><span class="sxs-lookup"><span data-stu-id="2318e-146">The **\[**[**local**](local.md)**\]** attribute applies to the function in the interface file.</span></span>

<span data-ttu-id="2318e-147">O **\[** [**código**](code.md) **\]** ou o **\[ Nocode \]** podem aparecer na lista de atributos de uma função e o que você escolher pode aparecer exatamente uma vez.</span><span class="sxs-lookup"><span data-stu-id="2318e-147">Either **\[**[**code**](code.md)**\]** or **\[nocode\]** can appear in a function's attribute list, and the one you choose can appear exactly once.</span></span>

<span data-ttu-id="2318e-148">O atributo **\[ Nocode \]** é ignorado quando stubs de servidor são gerados.</span><span class="sxs-lookup"><span data-stu-id="2318e-148">The **\[nocode\]** attribute is ignored when server stubs are generated.</span></span> <span data-ttu-id="2318e-149">Você não pode aplicá-lo ao gerar stubs de servidor no modo de compatibilidade de DCE.</span><span class="sxs-lookup"><span data-stu-id="2318e-149">You cannot apply it when generating server stubs in DCE-compatibility mode.</span></span>

## <a name="see-also"></a><span data-ttu-id="2318e-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="2318e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2318e-151">Arquivo de configuração de aplicativo (ACF)</span><span class="sxs-lookup"><span data-stu-id="2318e-151">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="2318e-152">**/acf**</span><span class="sxs-lookup"><span data-stu-id="2318e-152">**/acf**</span></span>](-acf.md)
</dt> <dt>

[<span data-ttu-id="2318e-153">**aloca**</span><span class="sxs-lookup"><span data-stu-id="2318e-153">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="2318e-154">**\_identificador automático**</span><span class="sxs-lookup"><span data-stu-id="2318e-154">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="2318e-155">**auto-completar**</span><span class="sxs-lookup"><span data-stu-id="2318e-155">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="2318e-156">**status de comunicação \_**</span><span class="sxs-lookup"><span data-stu-id="2318e-156">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="2318e-157">**\_identificador implícito**</span><span class="sxs-lookup"><span data-stu-id="2318e-157">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> </dl>

 

 




