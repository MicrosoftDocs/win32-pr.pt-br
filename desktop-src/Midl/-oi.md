---
title: Comutador/Oi
description: As opções/Oi e/OIC orientam o compilador MIDL a usar um método de marshaling totalmente interpretado. A opção/Oicf fornece aprimoramentos de desempenho adicionais.
ms.assetid: cf597a45-410f-4098-850b-240c6ebce23b
keywords:
- MIDL do comutador/Oi
topic_type:
- apiref
api_name:
- /Oi
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1671b16640d3f3214f10138e50a2ac08b6114674
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104161922"
---
# <a name="oi-switch"></a><span data-ttu-id="68d8c-105">Comutador/Oi</span><span class="sxs-lookup"><span data-stu-id="68d8c-105">/Oi switch</span></span>

<span data-ttu-id="68d8c-106">As opções **/Oi** e **/OIC** orientam o compilador MIDL a usar um método de marshaling totalmente interpretado.</span><span class="sxs-lookup"><span data-stu-id="68d8c-106">The **/Oi** and **/Oic** switches direct the MIDL compiler to use a fully-interpreted marshaling method.</span></span> <span data-ttu-id="68d8c-107">A opção **/Oicf** fornece aprimoramentos de desempenho adicionais.</span><span class="sxs-lookup"><span data-stu-id="68d8c-107">The **/Oicf** switch provides additional performance enhancements.</span></span>

``` syntax
midl /{Oi | Oic | Oif | Oicf}
```

## <a name="switch-options"></a><span data-ttu-id="68d8c-108">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="68d8c-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="68d8c-109">*Oi*</span><span class="sxs-lookup"><span data-stu-id="68d8c-109">*Oi*</span></span> 
</dt> <dd>

<span data-ttu-id="68d8c-110">Especifica o método totalmente interpretado para o empacotamento do código stub passado entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="68d8c-110">Specifies the fully-interpreted method for marshaling stub code passed between client and server.</span></span>

> [!Note]  
> <span data-ttu-id="68d8c-111">Essa opção é obsoleta.</span><span class="sxs-lookup"><span data-stu-id="68d8c-111">This switch is obsolete.</span></span> <span data-ttu-id="68d8c-112">É recomendável que a opção **/Oicf** seja usada em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="68d8c-112">It is recommended that the **/Oicf** switch be used in its place.</span></span>

 

</dd> <dt>

<span data-ttu-id="68d8c-113">*Oic*</span><span class="sxs-lookup"><span data-stu-id="68d8c-113">*Oic*</span></span> 
</dt> <dd>

<span data-ttu-id="68d8c-114">Especifica o método de proxy sem código de marshaling que fornece todos os recursos do **/Oi** e também reduz ainda mais o tamanho do código stub do cliente para interfaces de objeto.</span><span class="sxs-lookup"><span data-stu-id="68d8c-114">Specifies the codeless proxy method of marshaling that provides all the features of **/Oi** and also further reduces the size of the client stub code for object interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="68d8c-115">Essa opção é obsoleta.</span><span class="sxs-lookup"><span data-stu-id="68d8c-115">This switch is obsolete.</span></span> <span data-ttu-id="68d8c-116">É recomendável que a opção **/Oicf** seja usada em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="68d8c-116">It is recommended that the **/Oicf** switch be used in its place.</span></span>

 

</dd> <dt>

<span data-ttu-id="68d8c-117">*OIF ou Oicf*</span><span class="sxs-lookup"><span data-stu-id="68d8c-117">*Oif or Oicf*</span></span> 
</dt> <dd>

<span data-ttu-id="68d8c-118">Especifica o método de proxy sem código de marshaling que inclui todos os recursos fornecidos por **/Oi** e **/OIC** , mas usa um novo interpretador (cadeias de caracteres de formato rápido) que fornece melhor desempenho do que o **/Oi** ou o **/OIC**.</span><span class="sxs-lookup"><span data-stu-id="68d8c-118">Specifies the codeless proxy method of marshaling that includes all the features provided by **/Oi** and **/Oic** but uses a new interpreter (fast format strings) that provides better performance than **/Oi** or **/Oic**.</span></span> <span data-ttu-id="68d8c-119">Essa opção inclui aprimoramentos de RPC recentes e é recomendada para cenários de RPC modernos.</span><span class="sxs-lookup"><span data-stu-id="68d8c-119">This switch includes recent RPC enhancements and is recommended for modern RPC scenarios.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68d8c-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="68d8c-120">Remarks</span></span>

<span data-ttu-id="68d8c-121">Observe as restrições relacionadas às plataformas de suporte.</span><span class="sxs-lookup"><span data-stu-id="68d8c-121">Please note the restrictions related to supporting platforms.</span></span>

<span data-ttu-id="68d8c-122">O compilador MIDL 3,0 fornece dois métodos para empacotamento de código: totalmente interpretado ( **/Oi**, **/OIC** e **/Oicf**) e [**/os**](-os.md)(modo misto).</span><span class="sxs-lookup"><span data-stu-id="68d8c-122">The MIDL 3.0 compiler provides two methods for marshaling code: fully-interpreted ( **/Oi**, **/Oic** and **/Oicf**) and mixed-mode ( [**/Os**](-os.md)).</span></span> <span data-ttu-id="68d8c-123">Começando com o MIDL versão 6.0.359, o compilador MIDL gera stubs **/Oicf** Â  [**/robust**](-robust.md) por padrão.</span><span class="sxs-lookup"><span data-stu-id="68d8c-123">Starting with MIDL version 6.0.359, the MIDL compiler generates **/Oicf** Â  [**/robust**](-robust.md) stubs by default.</span></span> <span data-ttu-id="68d8c-124">Alguns recursos de linguagem não têm suporte em alguns modos.</span><span class="sxs-lookup"><span data-stu-id="68d8c-124">Some language features are not supported in some modes.</span></span> <span data-ttu-id="68d8c-125">Nesse caso, o compilador alterna automaticamente para o modo apropriado e emite um aviso.</span><span class="sxs-lookup"><span data-stu-id="68d8c-125">In this case, the compiler automatically switches to the appropriate mode and issues a warning.</span></span>

<span data-ttu-id="68d8c-126">Se o desempenho for uma preocupação, o método de modo misto ( [**/os**](-os.md)) pode ser a melhor abordagem.</span><span class="sxs-lookup"><span data-stu-id="68d8c-126">If performance is a concern, the mixed-mode ( [**/Os**](-os.md)) method can be the best approach.</span></span> <span data-ttu-id="68d8c-127">Nesse modo, o compilador escolhe realizar marshaling de alguns parâmetros embutidos nos stubs gerados.</span><span class="sxs-lookup"><span data-stu-id="68d8c-127">In this mode, the compiler chooses to marshal some parameters inline in the generated stubs.</span></span> <span data-ttu-id="68d8c-128">Embora isso resulte em um tamanho maior de stub, ele oferece maior desempenho.</span><span class="sxs-lookup"><span data-stu-id="68d8c-128">While this results in larger stub size, it offers increased performance.</span></span>

<span data-ttu-id="68d8c-129">O método totalmente interpretado realiza marshaling de dados completamente offline.</span><span class="sxs-lookup"><span data-stu-id="68d8c-129">The fully-interpreted method marshals data completely offline.</span></span> <span data-ttu-id="68d8c-130">Isso reduz consideravelmente o tamanho do código stub, mas resulta em desempenho reduzido.</span><span class="sxs-lookup"><span data-stu-id="68d8c-130">This considerably reduces the size of the stub code, but results in decreased performance.</span></span> <span data-ttu-id="68d8c-131">Além disso, com o método totalmente interpretado, há um limite de 16 parâmetros para cada procedimento.</span><span class="sxs-lookup"><span data-stu-id="68d8c-131">Also, with the fully-interpreted method, there is a limit of 16 parameters for each procedure.</span></span> <span data-ttu-id="68d8c-132">Qualquer procedimento que contenha mais de 16 parâmetros será automaticamente processado no modo [**/os**](-os.md) .</span><span class="sxs-lookup"><span data-stu-id="68d8c-132">Any procedure containing more than 16 parameters will automatically be processed in [**/Os**](-os.md) mode.</span></span> <span data-ttu-id="68d8c-133">Entre os modos interpretados, o **/Oicf** oferece o melhor desempenho e o **/Oi** oferece a melhor compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="68d8c-133">Among the interpreted modes, **/Oicf** offers the best performance and **/Oi** offers the best backward compatibility.</span></span>

<span data-ttu-id="68d8c-134">Talvez você queira usar a opção **/OIF** se seu aplicativo usar recursos de MIDL que foram introduzidos com MIDL 3,0, como os \[ atributos de [**\_ marshaling de conexão**](wire-marshal.md) \] e de \[ [**\_ marshaling do usuário**](user-marshal.md) \] .</span><span class="sxs-lookup"><span data-stu-id="68d8c-134">You may want to use the **/Oif** option if your application uses MIDL features that were introduced with MIDL 3.0, such as the \[[**wire\_marshal**](wire-marshal.md)\] and \[[**user\_marshal**](user-marshal.md)\] attributes.</span></span> <span data-ttu-id="68d8c-135">Se seu aplicativo usa [pipes](/windows/desktop/Rpc/pipes) , você deve usar a opção **/OIF** ; Se você especificar outro modo, o compilador MIDL será alternado para **/OIF**.</span><span class="sxs-lookup"><span data-stu-id="68d8c-135">If your application uses [pipes](/windows/desktop/Rpc/pipes) you must use the **/Oif** option; if you specify another mode, the MIDL compiler will switch to **/Oif**.</span></span>

<span data-ttu-id="68d8c-136">Para ajustar a maneira como seu código de stub é empacotado, o Microsoft RPC fornece um atributo de ACF \[ [**Optimize**](optimize.md) \] .</span><span class="sxs-lookup"><span data-stu-id="68d8c-136">To fine-tune the way your stub code is marshaled, Microsoft RPC provides an ACF \[[**optimize**](optimize.md)\] attribute.</span></span> <span data-ttu-id="68d8c-137">Esse atributo é usado como um atributo de interface ou atributo de operação para selecionar o modo de marshaling para interfaces individuais ou para operações individuais.</span><span class="sxs-lookup"><span data-stu-id="68d8c-137">This attribute is used as an interface attribute or operation attribute to select the marshaling mode for individual interfaces or for individual operations.</span></span>

### <a name="calling-conventions"></a><span data-ttu-id="68d8c-138">Convenções de chamada</span><span class="sxs-lookup"><span data-stu-id="68d8c-138">Calling Conventions</span></span>

<span data-ttu-id="68d8c-139">Os stubs gerados pelo compilador MIDL no método interpretado usando as opções **/Oi**, **/OIC** ou **/OIF** devem ser compilados como um procedimento stdcall ou cdecl durante a compilação de C.</span><span class="sxs-lookup"><span data-stu-id="68d8c-139">Stubs generated by the MIDL compiler in the interpreted method using the **/Oi**, **/Oic**, or **/Oif** switches must be compiled as either a stdcall or a cdecl procedure during the C compilation.</span></span> <span data-ttu-id="68d8c-140">Uma Convenção de chamada PASCAL ou fastcall não funcionará.</span><span class="sxs-lookup"><span data-stu-id="68d8c-140">A PASCAL or Fastcall calling convention will not work.</span></span> <span data-ttu-id="68d8c-141">Além disso, o stub do servidor deve ser compilado como stdcall.</span><span class="sxs-lookup"><span data-stu-id="68d8c-141">Additionally, the server stub must be compiled as stdcall.</span></span>

## <a name="examples"></a><span data-ttu-id="68d8c-142">Exemplos</span><span class="sxs-lookup"><span data-stu-id="68d8c-142">Examples</span></span>

<span data-ttu-id="68d8c-143">**MIDL/Oi filename. idl**</span><span class="sxs-lookup"><span data-stu-id="68d8c-143">**midl /Oi filename.idl**</span></span>

<span data-ttu-id="68d8c-144">**MIDL/OIC filename. idl**</span><span class="sxs-lookup"><span data-stu-id="68d8c-144">**midl /Oic filename.idl**</span></span>

<span data-ttu-id="68d8c-145">**MIDL/OIF filename. idl**</span><span class="sxs-lookup"><span data-stu-id="68d8c-145">**midl /Oif filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="68d8c-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="68d8c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68d8c-147">**/robust**</span><span class="sxs-lookup"><span data-stu-id="68d8c-147">**/robust**</span></span>](-robust.md)
</dt> <dt>

[<span data-ttu-id="68d8c-148">**// \_ avançado**</span><span class="sxs-lookup"><span data-stu-id="68d8c-148">**/no\_robust**</span></span>](-no-robust.md)
</dt> <dt>

[<span data-ttu-id="68d8c-149">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="68d8c-149">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="68d8c-150">**/Os**</span><span class="sxs-lookup"><span data-stu-id="68d8c-150">**/Os**</span></span>](-os.md)
</dt> <dt>

[<span data-ttu-id="68d8c-151">**formato**</span><span class="sxs-lookup"><span data-stu-id="68d8c-151">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="68d8c-152">**\_opção de formato de/// \_**</span><span class="sxs-lookup"><span data-stu-id="68d8c-152">**/no\_format\_opt**</span></span>](-no-format-opt.md)
</dt> </dl>

 

 