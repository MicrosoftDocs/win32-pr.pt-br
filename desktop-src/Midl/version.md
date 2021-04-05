---
title: atributo version
description: O atributo \ version \ interface identifica uma versão específica entre várias versões de uma interface RPC. Com o atributo Version, você garante que apenas as versões compatíveis do software cliente e do servidor tenham permissão para ligar.
ms.assetid: 66ac5cf3-2230-44fd-aaf6-8013e4a4ae81
keywords:
- MIDL do atributo de versão
topic_type:
- apiref
api_name:
- version
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bacbf7478ebfb745e5fc9b5e50959d0f1587dedf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006570"
---
# <a name="version-attribute"></a><span data-ttu-id="87e5c-105">atributo version</span><span class="sxs-lookup"><span data-stu-id="87e5c-105">version attribute</span></span>

<span data-ttu-id="87e5c-106">O atributo de interface da **\[ versão \]** identifica uma versão específica entre várias versões de uma interface RPC.</span><span class="sxs-lookup"><span data-stu-id="87e5c-106">The **\[version\]** interface attribute identifies a particular version among multiple versions of an RPC interface.</span></span> <span data-ttu-id="87e5c-107">Com o atributo Version, você garante que apenas as versões compatíveis do software cliente e do servidor tenham permissão para ligar.</span><span class="sxs-lookup"><span data-stu-id="87e5c-107">With the version attribute, you ensure that only compatible versions of client and server software are allowed to bind.</span></span>

``` syntax
version ( major-value[[. minor-value]] )
```

## <a name="parameters"></a><span data-ttu-id="87e5c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87e5c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87e5c-109">*valor principal*</span><span class="sxs-lookup"><span data-stu-id="87e5c-109">*major-value*</span></span> 
</dt> <dd>

<span data-ttu-id="87e5c-110">Especifica um inteiro não assinado curto entre zero e 65.535, inclusive, que representa o número de versão principal.</span><span class="sxs-lookup"><span data-stu-id="87e5c-110">Specifies a short unsigned integer between zero and 65,535, inclusive, that represents the major version number.</span></span>

</dd> <dt>

<span data-ttu-id="87e5c-111">*valor secundário*</span><span class="sxs-lookup"><span data-stu-id="87e5c-111">*minor-value*</span></span> 
</dt> <dd>

<span data-ttu-id="87e5c-112">Especifica um inteiro não assinado curto entre zero e 65.535, inclusive, que representa o número de versão secundária.</span><span class="sxs-lookup"><span data-stu-id="87e5c-112">Specifies a short unsigned integer between zero and 65,535, inclusive, that represents the minor version number.</span></span> <span data-ttu-id="87e5c-113">O valor da versão secundária é opcional.</span><span class="sxs-lookup"><span data-stu-id="87e5c-113">The minor version value is optional.</span></span> <span data-ttu-id="87e5c-114">Se estiver presente, o valor da versão secundária será separado do número de versão principal por um caractere de ponto (.).</span><span class="sxs-lookup"><span data-stu-id="87e5c-114">If present, the minor version value is separated from the major version number by a period character (.).</span></span> <span data-ttu-id="87e5c-115">Se não for especificado, o valor da versão secundária será zero.</span><span class="sxs-lookup"><span data-stu-id="87e5c-115">If not specified, the minor version value is zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87e5c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="87e5c-116">Remarks</span></span>

<span data-ttu-id="87e5c-117">O compilador MIDL não oferece suporte a várias versões de uma interface COM.</span><span class="sxs-lookup"><span data-stu-id="87e5c-117">The MIDL compiler does not support multiple versions of a COM interface.</span></span> <span data-ttu-id="87e5c-118">Como resultado, uma lista de atributos de interface que inclui o **\[** [](object.md) **\]** atributo Object não pode incluir o atributo **\[ version \]** .</span><span class="sxs-lookup"><span data-stu-id="87e5c-118">As a result, an interface attribute list that includes the **\[**[**object**](object.md)**\]** attribute cannot include the **\[version\]** attribute.</span></span> <span data-ttu-id="87e5c-119">Para criar uma nova versão de uma interface COM existente, use a herança de interface.</span><span class="sxs-lookup"><span data-stu-id="87e5c-119">To create a new version of an existing COM interface, use interface inheritance.</span></span> <span data-ttu-id="87e5c-120">Uma interface COM derivada tem um UUID diferente, mas herda as funções de membro de interface, os códigos de status e os atributos de interface da interface base.</span><span class="sxs-lookup"><span data-stu-id="87e5c-120">A derived COM interface has a different UUID but inherits the interface member functions, status codes, and interface attributes of the base interface.</span></span>

<span data-ttu-id="87e5c-121">Em combinação com o **\[** valor do [**UUID**](uuid.md) **\]** , o valor da **\[ versão \]** identifica exclusivamente a interface.</span><span class="sxs-lookup"><span data-stu-id="87e5c-121">In combination with the **\[**[**uuid**](uuid.md)**\]** value, the **\[version\]** value uniquely identifies the interface.</span></span> <span data-ttu-id="87e5c-122">A biblioteca de tempo de execução passa os valores de **\[ versão \]** e **\[ UUID \]** para o servidor quando o cliente chama uma função remota.</span><span class="sxs-lookup"><span data-stu-id="87e5c-122">The run-time library passes the **\[version\]** and **\[uuid\]** values to the server when the client calls a remote function.</span></span> <span data-ttu-id="87e5c-123">Um cliente pode se associar a um servidor para uma determinada interface se:</span><span class="sxs-lookup"><span data-stu-id="87e5c-123">A client can bind to a server for a given interface if:</span></span>

-   <span data-ttu-id="87e5c-124">O valor do **\[ UUID \]** é o mesmo.</span><span class="sxs-lookup"><span data-stu-id="87e5c-124">The **\[uuid\]** value is the same.</span></span>
-   <span data-ttu-id="87e5c-125">O número de versão principal é o mesmo.</span><span class="sxs-lookup"><span data-stu-id="87e5c-125">The major version number is the same.</span></span>
-   <span data-ttu-id="87e5c-126">O número de versão secundária do cliente é menor ou igual ao número de versão secundário do servidor.</span><span class="sxs-lookup"><span data-stu-id="87e5c-126">The client's minor version number is less than or equal to the server's minor version number.</span></span>

<span data-ttu-id="87e5c-127">É para seu benefício e os benefícios dos seus usuários para manter a compatibilidade com o versionsÂ, ou seja, modificar a interface para que apenas o número da versão secundária seja alterado.</span><span class="sxs-lookup"><span data-stu-id="87e5c-127">It is to your benefit and your users' benefit to retain upward compatibility among versionsÂ that is, to modify the interface so that only the minor version number changes.</span></span> <span data-ttu-id="87e5c-128">Você pode manter a compatibilidade com o sentido atual quando adiciona novos tipos de dados que não são usados por funções existentes e quando adiciona novas funções sem alterar a especificação da interface para funções existentes.</span><span class="sxs-lookup"><span data-stu-id="87e5c-128">You can retain upward compatibility when you add new data types that are not used by existing functions and when you add new functions without changing the interface specification for existing functions.</span></span>

<span data-ttu-id="87e5c-129">Altere o número de versão principal se qualquer uma das seguintes condições se aplicar:</span><span class="sxs-lookup"><span data-stu-id="87e5c-129">Change the major version number if any one of the following conditions apply:</span></span>

-   <span data-ttu-id="87e5c-130">Se você alterar um tipo de dados que é usado por uma função existente.</span><span class="sxs-lookup"><span data-stu-id="87e5c-130">If you change a data type that is used by an existing function.</span></span>
-   <span data-ttu-id="87e5c-131">Se você alterar a especificação de interface para uma função existente (como adicionar ou remover um parâmetro).</span><span class="sxs-lookup"><span data-stu-id="87e5c-131">If you change the interface specification for an existing function (such as adding or removing a parameter).</span></span>
-   <span data-ttu-id="87e5c-132">Se você Adicionar retornos de chamada que são chamados por funções existentes.</span><span class="sxs-lookup"><span data-stu-id="87e5c-132">If you add callbacks that are called by existing functions.</span></span>

<span data-ttu-id="87e5c-133">Altere o número de versão secundária se todas as condições a seguir se aplicarem:</span><span class="sxs-lookup"><span data-stu-id="87e5c-133">Change the minor version number if all of the following conditions apply:</span></span>

-   <span data-ttu-id="87e5c-134">Se você adicionar definições de tipo ou constantes que não são usadas por nenhuma função ou retornos de chamada existentes.</span><span class="sxs-lookup"><span data-stu-id="87e5c-134">If you add type definitions or constants that are not used by any existing functions or callbacks.</span></span>
-   <span data-ttu-id="87e5c-135">Se você não alterar nenhuma função existente e adicionar novas funções à interface.</span><span class="sxs-lookup"><span data-stu-id="87e5c-135">If you do not change any existing functions and you add new functions to the interface.</span></span>
-   <span data-ttu-id="87e5c-136">Se você Adicionar retornos de chamada que não são chamados por nenhuma função existente e os novos retornos de chamada seguirem quaisquer funções existentes.</span><span class="sxs-lookup"><span data-stu-id="87e5c-136">If you add callbacks that are not called by any existing functions and the new callbacks follow any existing functions.</span></span>

<span data-ttu-id="87e5c-137">Se suas modificações estiverem qualificadas como uma alteração compatível com o sentido da interface, use o procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="87e5c-137">If your modifications qualify as an upward-compatible change to the interface, use the following procedure.</span></span>

<span data-ttu-id="87e5c-138">**Para modificar o arquivo de interface (IDL)**</span><span class="sxs-lookup"><span data-stu-id="87e5c-138">**To modify the interface (IDL) file**</span></span>

1.  <span data-ttu-id="87e5c-139">Adicione novas definições de constantes e tipos ao arquivo de interface.</span><span class="sxs-lookup"><span data-stu-id="87e5c-139">Add new constant and type definitions to the interface file.</span></span>
2.  <span data-ttu-id="87e5c-140">Adicione funções de retorno de chamada ao final do arquivo de interface.</span><span class="sxs-lookup"><span data-stu-id="87e5c-140">Add callback functions to the end of the interface file.</span></span>
3.  <span data-ttu-id="87e5c-141">Adicione novas funções ao final do arquivo de interface.</span><span class="sxs-lookup"><span data-stu-id="87e5c-141">Add new functions to the end of the interface file.</span></span>

<span data-ttu-id="87e5c-142">O atributo **\[ version \]** pode ocorrer no máximo uma vez no cabeçalho da interface.</span><span class="sxs-lookup"><span data-stu-id="87e5c-142">The **\[version\]** attribute can occur at most once in the interface header.</span></span>

<span data-ttu-id="87e5c-143">Quando o atributo Version não estiver presente, a interface terá uma versão padrão de 0,0.</span><span class="sxs-lookup"><span data-stu-id="87e5c-143">When the version attribute is not present, the interface has a default version of 0.0.</span></span>

<span data-ttu-id="87e5c-144">O caractere de período entre os números principal e secundário é um delimitador e não representa um ponto decimal.</span><span class="sxs-lookup"><span data-stu-id="87e5c-144">The period character between the major and minor numbers is a delimiter and does not represent a decimal point.</span></span> <span data-ttu-id="87e5c-145">O número secundário é tratado como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="87e5c-145">The minor number is treated as an integer.</span></span> <span data-ttu-id="87e5c-146">Os zeros à esquerda não são significativos.</span><span class="sxs-lookup"><span data-stu-id="87e5c-146">Leading zeroes are not significant.</span></span> <span data-ttu-id="87e5c-147">Os zeros à direita são significativos.</span><span class="sxs-lookup"><span data-stu-id="87e5c-147">Trailing zeroes are significant.</span></span>

<span data-ttu-id="87e5c-148">Por exemplo, a configuração de versão 1,11 representa um valor principal de um e um valor secundário de onze.</span><span class="sxs-lookup"><span data-stu-id="87e5c-148">For example, the version setting 1.11 represents a major value of one and a minor value of eleven.</span></span> <span data-ttu-id="87e5c-149">A versão 1,11 não representa um valor entre 1,1 e 1,2.</span><span class="sxs-lookup"><span data-stu-id="87e5c-149">Version 1.11 does not represent a value between 1.1 and 1.2.</span></span>

## <a name="see-also"></a><span data-ttu-id="87e5c-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="87e5c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87e5c-151">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="87e5c-151">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="87e5c-152">**interface**</span><span class="sxs-lookup"><span data-stu-id="87e5c-152">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="87e5c-153">**objeto**</span><span class="sxs-lookup"><span data-stu-id="87e5c-153">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="87e5c-154">**personalizado**</span><span class="sxs-lookup"><span data-stu-id="87e5c-154">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 




