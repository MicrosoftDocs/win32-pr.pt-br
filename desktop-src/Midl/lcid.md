---
title: atributo LCID
description: O atributo \ LCID \ especifica um identificador de localidade e habilita o suporte a compilador de MIDL específico de localidade.
ms.assetid: 40457a1a-251c-41cd-bfa6-9d506601ff5e
keywords:
- atributo LCID MIDL
topic_type:
- apiref
api_name:
- lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa22b231c63583c6d16e6a50f3e9987c5b61128
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640548"
---
# <a name="lcid-attribute"></a><span data-ttu-id="0c336-104">atributo LCID</span><span class="sxs-lookup"><span data-stu-id="0c336-104">lcid attribute</span></span>

<span data-ttu-id="0c336-105">O atributo **\[ LCID \]** especifica um identificador de localidade e habilita o suporte a compilador de MIDL específico de localidade.</span><span class="sxs-lookup"><span data-stu-id="0c336-105">The **\[lcid\]** attribute specifies a locale identifier and enables locale-specific MIDL compiler support.</span></span>

``` syntax
[
    uuid(uuid-number), 
    lcid(localeID)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}

function-name([parameter-attribute-list, lcid] long  parameter-name,. . .);
```

## <a name="parameters"></a><span data-ttu-id="0c336-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c336-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c336-107">*UUID-número*</span><span class="sxs-lookup"><span data-stu-id="0c336-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="0c336-108">Especifica um número de identificação universalmente exclusivo para a [**biblioteca**](library.md).</span><span class="sxs-lookup"><span data-stu-id="0c336-108">Specifies a universally unique identification number for the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c336-109">*localeID*</span><span class="sxs-lookup"><span data-stu-id="0c336-109">*localeID*</span></span> 
</dt> <dd>

<span data-ttu-id="0c336-110">Especifica o identificador de localidade de 32 bits usado no suporte ao idioma nacional do Windows.</span><span class="sxs-lookup"><span data-stu-id="0c336-110">Specifies the 32-bit locale identifier used in Windows National Language Support.</span></span> <span data-ttu-id="0c336-111">Normalmente, o identificador de localidade é fornecido em hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="0c336-111">Typically the locale identifier is given in hexadecimal.</span></span>

</dd> <dt>

<span data-ttu-id="0c336-112">*lista de atributos opcionais*</span><span class="sxs-lookup"><span data-stu-id="0c336-112">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0c336-113">Zero ou mais atributos a serem aplicados à [**biblioteca**](library.md).</span><span class="sxs-lookup"><span data-stu-id="0c336-113">Zero or more attributes to apply to the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c336-114">*nome da biblioteca*</span><span class="sxs-lookup"><span data-stu-id="0c336-114">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="0c336-115">O nome pelo qual os componentes de software se referem à [**biblioteca**](library.md).</span><span class="sxs-lookup"><span data-stu-id="0c336-115">The name by which software components refer to the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c336-116">*bibliotecas-definição-instruções*</span><span class="sxs-lookup"><span data-stu-id="0c336-116">*library-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="0c336-117">Uma ou mais instruções MIDL que definem o conteúdo da [**biblioteca**](library.md).</span><span class="sxs-lookup"><span data-stu-id="0c336-117">One or more MIDL statements which define the contents of the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c336-118">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="0c336-118">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="0c336-119">Especifica o nome da função no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="0c336-119">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="0c336-120">*lista de atributos de parâmetro*</span><span class="sxs-lookup"><span data-stu-id="0c336-120">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0c336-121">Zero ou mais atributos MIDL que serão aplicados ao parâmetro de função.</span><span class="sxs-lookup"><span data-stu-id="0c336-121">Zero or more MIDL attributes that will be applied to the function parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0c336-122">*nome do parâmetro*</span><span class="sxs-lookup"><span data-stu-id="0c336-122">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="0c336-123">Especifica o nome do parâmetro no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="0c336-123">Specifies the name of the parameter in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c336-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c336-124">Remarks</span></span>

<span data-ttu-id="0c336-125">A sintaxe **\[ \] LCID** tem duas formas diferentes; o efeito do atributo depende da sintaxe usada – ou da sintaxe da instrução de [**biblioteca**](library.md) ou da sintaxe do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0c336-125">The **\[lcid\]** syntax has two different forms; the effect of the attribute depends on which syntax you use — either the [**library**](library.md) statement syntax or the parameter syntax.</span></span>

<span data-ttu-id="0c336-126">Quando aplicado à instrução de [**biblioteca**](library.md) , juntamente com um argumento LocaleID, como mostrado no primeiro exemplo, o atributo **\[ LCID \]** identifica a localidade para uma biblioteca de tipos ou para um argumento de função e permite que você use caracteres internacionais dentro do bloco de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="0c336-126">When applied to the [**library**](library.md) statement, along with a localeID argument, as shown in the first example, the **\[lcid\]** attribute identifies the locale for a type library or for a function argument and lets you use international characters inside the library block.</span></span>

<span data-ttu-id="0c336-127">Em vigor com a versão 3.01.75 do compilador MIDL, o identificador de localidade fornecido por esse atributo não apenas decora a biblioteca de tipos resultante, mas, na verdade, altera o comportamento do compilador.</span><span class="sxs-lookup"><span data-stu-id="0c336-127">Effective with version 3.01.75 of the MIDL compiler, the locale identifier supplied by this attribute not only decorates the resulting type library, but actually changes the behavior of the compiler.</span></span> <span data-ttu-id="0c336-128">Dentro de uma instrução de [**biblioteca**](library.md) , do ponto em que o atributo **\[ LCID \]** é usado, MIDL aceitará a entrada localizada de acordo com a localidade especificada.</span><span class="sxs-lookup"><span data-stu-id="0c336-128">Within a [**library**](library.md) statement, from the point where the **\[lcid\]** attribute is used, MIDL will accept input localized according to the specified locale.</span></span> <span data-ttu-id="0c336-129">Em particular, o suporte completo para idiomas asiáticos, como japonês, chinês e coreano (suporte completo a DBCS) está disponível.</span><span class="sxs-lookup"><span data-stu-id="0c336-129">In particular, full support for Asian languages such as Japanese, Chinese and Korean (full DBCS support) is available.</span></span> <span data-ttu-id="0c336-130">Os recursos com suporte da localização são: comentários, cadeias de caracteres, HelpStrings e identificadores.</span><span class="sxs-lookup"><span data-stu-id="0c336-130">Features supported by the localization are: comments, strings, helpstrings and identifiers.</span></span>

<span data-ttu-id="0c336-131">Use a opção de compilador [**/LCID**](-lcid.md) para ter esse suporte de localização disponível para todo o arquivo de entrada, incluindo o nome do arquivo e o caminho do diretório, em vez de apenas dentro do bloco de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="0c336-131">Use the [**/lcid**](-lcid.md) compiler switch to have this localization support available to the entire input file, including file name and directory path, rather than just inside the library block.</span></span>

<span data-ttu-id="0c336-132">Quando aplicado a um parâmetro, o atributo **\[ LCID \]** permite passar um identificador de localidade para uma função, conforme mostrado no segundo exemplo.</span><span class="sxs-lookup"><span data-stu-id="0c336-132">When applied to a parameter, the **\[lcid\]** attribute lets you pass a locale identifier to a function, as shown in the second example.</span></span> <span data-ttu-id="0c336-133">As seguintes restrições se aplicam aos parâmetros **\[ LCID \]** :</span><span class="sxs-lookup"><span data-stu-id="0c336-133">The following restrictions apply to **\[lcid\]** parameters:</span></span>

-   <span data-ttu-id="0c336-134">Uma função pode ter no máximo um parâmetro **\[ LCID \]** .</span><span class="sxs-lookup"><span data-stu-id="0c336-134">A function can have at most one **\[lcid\]** parameter.</span></span>
-   <span data-ttu-id="0c336-135">O tipo de dados do parâmetro deve ser [**longo**](long.md).</span><span class="sxs-lookup"><span data-stu-id="0c336-135">The data type of the parameter must be [**long**](long.md).</span></span>
-   <span data-ttu-id="0c336-136">A direção do parâmetro deve estar **\[** [**em**](in.md) **\]** apenas.</span><span class="sxs-lookup"><span data-stu-id="0c336-136">The direction of the parameter must be **\[**[**in**](in.md)**\]** only.</span></span>
-   <span data-ttu-id="0c336-137">O parâmetro **\[ LCID \]** deve seguir quaisquer outros parâmetros, exceto um **\[** parâmetro [**retval**](retval.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="0c336-137">The **\[lcid\]** parameter must follow any other parameters, except a **\[**[**retval**](retval.md)**\]** parameter.</span></span>
-   <span data-ttu-id="0c336-138">Você não pode aplicar o atributo **\[ LCID \]** a um parâmetro [**dispinterface**](dispinterface.md) ou [**coclass**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="0c336-138">You cannot apply the **\[lcid\]** attribute to a [**dispinterface**](dispinterface.md) or [**coclass**](coclass.md) parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="0c336-139">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0c336-139">Examples</span></span>

``` syntax
[  
    uuid(12345678-1234-1234-1234-123456789ABC),
    lcid(0x09),
    version(1.0)
] 
library MyLibrary
{
    /* Library definition statements */
};

interface IMyFace : IDispatch
{
    [propget] HRESULT MyFunc([in, lcid] long LocaleID,
                          [out, retval] BSTR * ReturnVal);
    // Other interface definition statements
}
```

## <a name="see-also"></a><span data-ttu-id="0c336-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c336-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c336-141">**coclass**</span><span class="sxs-lookup"><span data-stu-id="0c336-141">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="0c336-142">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="0c336-142">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="0c336-143">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="0c336-143">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="0c336-144">**/LCID**</span><span class="sxs-lookup"><span data-stu-id="0c336-144">**/lcid**</span></span>](-lcid.md)
</dt> <dt>

[<span data-ttu-id="0c336-145">**biblioteca**</span><span class="sxs-lookup"><span data-stu-id="0c336-145">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="0c336-146">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="0c336-146">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="0c336-147">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="0c336-147">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="0c336-148">**retval**</span><span class="sxs-lookup"><span data-stu-id="0c336-148">**retval**</span></span>](retval.md)
</dt> </dl>

 

 