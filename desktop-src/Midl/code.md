---
title: atributo de código
description: O atributo \ Code \ ACF faz com que o código stub do cliente seja gerado para funções remotas.
ms.assetid: 735a8c25-29d4-4073-a2db-88bc8615ccc1
keywords:
- código de MIDL do atributo code
topic_type:
- apiref
api_name:
- code
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa041859c0bffca2771695b7055105b8ae846221
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293356"
---
# <a name="code-attribute"></a><span data-ttu-id="f6e27-104">atributo de código</span><span class="sxs-lookup"><span data-stu-id="f6e27-104">code attribute</span></span>

<span data-ttu-id="f6e27-105">O atributo de ACF de **\[ código \]** faz com que o código stub do cliente seja gerado para funções remotas.</span><span class="sxs-lookup"><span data-stu-id="f6e27-105">The **\[code\]** ACF attribute causes client stub code to be generated for remote functions.</span></span>

``` syntax
[
    code [ , ACF-interface-attributes ] 
] 
interface interface-name
{
  [ include filename-list ; ]
  [ typedef [type-attribute-list] typenam; ]
  [ [code [ , ACF-function-attributes ]] function-name (
            [ ACF-parameter-attributes ] parameter-name,
        ...);
  ]
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="f6e27-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6e27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6e27-107">*ACF-interface-atributos*</span><span class="sxs-lookup"><span data-stu-id="f6e27-107">*ACF-interface-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="f6e27-108">Especifica uma lista de um ou mais atributos que se aplicam à interface como um todo.</span><span class="sxs-lookup"><span data-stu-id="f6e27-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="f6e27-109">Os atributos válidos incluem o [**\[ \_ identificador \] automático**](auto-handle.md) ou o [**\[ \_ \] identificador implícito**](implicit-handle.md) e o **\[ código \]**, [**\[ Nocode \]**](nocode.md)ou [**\[ Optimize \]**](optimize.md).</span><span class="sxs-lookup"><span data-stu-id="f6e27-109">Valid attributes include either [**\[auto\_handle\]**](auto-handle.md) or [**\[implicit\_handle\]**](implicit-handle.md) and either **\[code\]**, [**\[nocode\]**](nocode.md), or [**\[optimize\]**](optimize.md).</span></span> <span data-ttu-id="f6e27-110">Quando dois ou mais atributos de interface estão presentes, eles devem ser separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="f6e27-110">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="f6e27-111">*nome da interface*</span><span class="sxs-lookup"><span data-stu-id="f6e27-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f6e27-112">Especifica o nome da interface.</span><span class="sxs-lookup"><span data-stu-id="f6e27-112">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="f6e27-113">*nome do arquivo-lista*</span><span class="sxs-lookup"><span data-stu-id="f6e27-113">*filename-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f6e27-114">Especifica uma lista de um ou mais nomes de arquivo de cabeçalho C, separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="f6e27-114">Specifies a list of one or more C-header file names, separated by commas.</span></span> <span data-ttu-id="f6e27-115">Você deve fornecer o nome completo do arquivo, incluindo a extensão.</span><span class="sxs-lookup"><span data-stu-id="f6e27-115">You must supply the full file name, including the extension.</span></span>

</dd> <dt>

<span data-ttu-id="f6e27-116">*lista de atributos de tipo*</span><span class="sxs-lookup"><span data-stu-id="f6e27-116">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f6e27-117">Especifica uma lista de um ou mais atributos, separados por vírgulas, que se aplicam ao tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="f6e27-117">Specifies a list of one or more attributes, separated by commas, that apply to the specified type.</span></span> <span data-ttu-id="f6e27-118">Atributos de tipo válidos incluem [**\[ \] alocar**](allocate.md) e [**\[ representar \_ como \]**](represent-as.md).</span><span class="sxs-lookup"><span data-stu-id="f6e27-118">Valid type attributes include [**\[allocate\]**](allocate.md) and [**\[represent\_as\]**](represent-as.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6e27-119">*TypeName*</span><span class="sxs-lookup"><span data-stu-id="f6e27-119">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="f6e27-120">Especifica um tipo definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="f6e27-120">Specifies a type defined in the IDL file.</span></span> <span data-ttu-id="f6e27-121">Os atributos de tipo no ACF podem ser aplicados somente aos tipos definidos anteriormente no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="f6e27-121">Type attributes in the ACF can be applied only to types previously defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="f6e27-122">*ACF-função-atributos*</span><span class="sxs-lookup"><span data-stu-id="f6e27-122">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="f6e27-123">Especifica zero ou mais atributos que se aplicam à função como um todo, como o [**\[ \_ status \] de comunicação**](comm-status.md).</span><span class="sxs-lookup"><span data-stu-id="f6e27-123">Specifies zero or more attributes that apply to the function as a whole, such as [**\[comm\_status\]**](comm-status.md).</span></span> <span data-ttu-id="f6e27-124">Os atributos de função são colocados entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="f6e27-124">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="f6e27-125">Separe vários atributos de função com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="f6e27-125">Separate multiple function attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="f6e27-126">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="f6e27-126">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f6e27-127">Especifica o nome da função, conforme definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="f6e27-127">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="f6e27-128">*ACF-parâmetros-atributos*</span><span class="sxs-lookup"><span data-stu-id="f6e27-128">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="f6e27-129">Especifica atributos de ACF que se aplicam a um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f6e27-129">Specifies ACF attributes that apply to a parameter.</span></span> <span data-ttu-id="f6e27-130">Observe que zero, um ou mais atributos podem ser aplicados ao parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f6e27-130">Note that zero, one, or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="f6e27-131">Separe vários atributos de parâmetro com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="f6e27-131">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="f6e27-132">Os atributos de parâmetro de ACF são colocados entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="f6e27-132">ACF parameter attributes are enclosed in square brackets.</span></span>

</dd> <dt>

<span data-ttu-id="f6e27-133">*nome do parâmetro*</span><span class="sxs-lookup"><span data-stu-id="f6e27-133">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f6e27-134">Especifica um parâmetro da função, conforme definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="f6e27-134">Specifies a parameter of the function as defined in the IDL file.</span></span> <span data-ttu-id="f6e27-135">Cada parâmetro para a função deve ser especificado na mesma sequência e com o mesmo nome definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="f6e27-135">Each parameter for the function must be specified in the same sequence and with the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6e27-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6e27-136">Remarks</span></span>

<span data-ttu-id="f6e27-137">O atributo **\[ Code \]** pode aparecer no cabeçalho ACF ou ser aplicado a uma função individual.</span><span class="sxs-lookup"><span data-stu-id="f6e27-137">The **\[code\]** attribute can appear in the ACF header or be applied to an individual function.</span></span>

<span data-ttu-id="f6e27-138">Quando o atributo de **\[ código \]** é exibido no cabeçalho ACF, o código stub do cliente é gerado para todas as funções remotas que não têm o atributo função [**\[ Nocode \]**](nocode.md) .</span><span class="sxs-lookup"><span data-stu-id="f6e27-138">When the **\[code\]** attribute appears in the ACF header, client stub code is generated for all remote functions that do not have the [**\[nocode\]**](nocode.md) function attribute.</span></span> <span data-ttu-id="f6e27-139">Você pode substituir o atributo de **\[ código \]** no cabeçalho de uma função individual especificando o atributo **\[ Nocode \]** como um atributo de função.</span><span class="sxs-lookup"><span data-stu-id="f6e27-139">You can override the **\[code\]** attribute in the header for an individual function by specifying the **\[nocode\]** attribute as a function attribute.</span></span>

<span data-ttu-id="f6e27-140">Quando o atributo de **\[ código \]** é exibido na lista de atributos da função remota, o código stub do cliente é gerado para a função.</span><span class="sxs-lookup"><span data-stu-id="f6e27-140">When the **\[code\]** attribute appears in the remote function's attribute list, client stub code is generated for the function.</span></span> <span data-ttu-id="f6e27-141">O código stub do cliente não é gerado quando:</span><span class="sxs-lookup"><span data-stu-id="f6e27-141">Client stub code is not generated when:</span></span>

-   <span data-ttu-id="f6e27-142">O cabeçalho ACF inclui o atributo [**\[ Nocode \]**](nocode.md) .</span><span class="sxs-lookup"><span data-stu-id="f6e27-142">The ACF header includes the [**\[nocode\]**](nocode.md) attribute.</span></span>
-   <span data-ttu-id="f6e27-143">O atributo [**\[ Nocode \]**](nocode.md) é aplicado à função.</span><span class="sxs-lookup"><span data-stu-id="f6e27-143">The [**\[nocode\]**](nocode.md) attribute is applied to the function.</span></span>
-   <span data-ttu-id="f6e27-144">O atributo [**\[ local \]**](local.md) se aplica à função no arquivo de interface.</span><span class="sxs-lookup"><span data-stu-id="f6e27-144">The [**\[local\]**](local.md) attribute applies to the function in the interface file.</span></span>

<span data-ttu-id="f6e27-145">O **\[ código \]** ou o [**\[ Nocode \]**](nocode.md) podem aparecer na lista de atributos da interface ou da função, mas o que você escolher pode aparecer apenas uma vez na lista.</span><span class="sxs-lookup"><span data-stu-id="f6e27-145">Either **\[code\]** or [**\[nocode\]**](nocode.md) can appear in the interface or function attribute list, but the one you choose can appear only once in the list.</span></span>

## <a name="see-also"></a><span data-ttu-id="f6e27-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6e27-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6e27-147">Arquivo de configuração de aplicativo (ACF)</span><span class="sxs-lookup"><span data-stu-id="f6e27-147">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="f6e27-148">**aloca**</span><span class="sxs-lookup"><span data-stu-id="f6e27-148">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="f6e27-149">**\_identificador automático**</span><span class="sxs-lookup"><span data-stu-id="f6e27-149">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="f6e27-150">**status de comunicação \_**</span><span class="sxs-lookup"><span data-stu-id="f6e27-150">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="f6e27-151">**\_identificador implícito**</span><span class="sxs-lookup"><span data-stu-id="f6e27-151">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="f6e27-152">**local**</span><span class="sxs-lookup"><span data-stu-id="f6e27-152">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="f6e27-153">**Nocode**</span><span class="sxs-lookup"><span data-stu-id="f6e27-153">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="f6e27-154">**formato**</span><span class="sxs-lookup"><span data-stu-id="f6e27-154">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="f6e27-155">**representar \_ como**</span><span class="sxs-lookup"><span data-stu-id="f6e27-155">**represent\_as**</span></span>](represent-as.md)
</dt> </dl>

 

 




