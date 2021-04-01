---
title: opção/cpp_cmd
description: A \_ opção cmd/cpp especifica o pré-processador que o compilador MIDL usa para pré-processar arquivos de entrada.
ms.assetid: d6261fdd-155d-4327-b254-d0267f0dec69
keywords:
- /cpp_cmd MIDL do comutador
topic_type:
- apiref
api_name:
- /cpp_cmd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ad693f8dbf3ddc7acda6539b89930972ca81a87
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638634"
---
# <a name="cpp_cmd-switch"></a><span data-ttu-id="d5e20-104">\_opção/cpp cmd</span><span class="sxs-lookup"><span data-stu-id="d5e20-104">/cpp\_cmd switch</span></span>

<span data-ttu-id="d5e20-105">A **opção \_ cmd/cpp** especifica o pré-processador que o compilador MIDL usa para pré-processar arquivos de entrada.</span><span class="sxs-lookup"><span data-stu-id="d5e20-105">The **/cpp\_cmd** switch specifies the preprocessor that the MIDL compiler uses to preprocess input files.</span></span>

``` syntax
midl /cpp_cmd "C_preprocessor_binary"
```

## <a name="switch-options"></a><span data-ttu-id="d5e20-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="d5e20-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="d5e20-107">*\_Binário de pré-processador C \_*</span><span class="sxs-lookup"><span data-stu-id="d5e20-107">*C\_preprocessor\_binary*</span></span> 
</dt> <dd>

<span data-ttu-id="d5e20-108">Especifica o comando que invoca o pré-processador.</span><span class="sxs-lookup"><span data-stu-id="d5e20-108">Specifies the command that invokes the preprocessor.</span></span> <span data-ttu-id="d5e20-109">Esse comando permite que os desenvolvedores substituam o pré-processador padrão.</span><span class="sxs-lookup"><span data-stu-id="d5e20-109">This command allows developers to override the default preprocessor.</span></span> <span data-ttu-id="d5e20-110">Por padrão, o MIDL invoca o compilador C/C++ da Microsoft do ambiente de compilação da máquina de compilação.</span><span class="sxs-lookup"><span data-stu-id="d5e20-110">By default, MIDL invokes the Microsoft C/C++ compiler from the build machine's build environment.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d5e20-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5e20-111">Remarks</span></span>

<span data-ttu-id="d5e20-112">O *argumento \_ \_ binário de pré-processador C* para a opção pode especificar o caminho completo; o sufixo exe e as aspas são opcionais.</span><span class="sxs-lookup"><span data-stu-id="d5e20-112">The *C\_preprocessor\_binary* argument to the switch may specify the full path; the exe suffix and quotes are optional.</span></span> <span data-ttu-id="d5e20-113">Normalmente, os desenvolvedores usam a opção para escolher uma versão específica do pré-processador do Microsoft C/C++ ou equivalente no ambiente de compilação.</span><span class="sxs-lookup"><span data-stu-id="d5e20-113">Typically, developers use the switch to choose a particular version of the Microsoft C/C++ preprocessor or equivalent in the build environment.</span></span> <span data-ttu-id="d5e20-114">Nesse caso, não é necessário usar a opção [**/cpp \_ opt**](-cpp-opt.md) com **/cpp \_ cmd**.</span><span class="sxs-lookup"><span data-stu-id="d5e20-114">In this case, it is not necessary to use the [**/cpp\_opt**](-cpp-opt.md) switch with **/cpp\_cmd**.</span></span>

<span data-ttu-id="d5e20-115">Ao usar um pré-processador que não seja da Microsoft, especialmente quando o pré-processador especificado não direciona sua saída para stdout, a opção de compilador C que redireciona a saída para stdout como parte da opção [**/cpp \_ opt**](-cpp-opt.md) do compilador MIDL deve ser especificada.</span><span class="sxs-lookup"><span data-stu-id="d5e20-115">When using a non-Microsoft preprocessor, especially when the specified preprocessor does not direct its output to stdout, the C compiler switch that redirects output to stdout as part of the MIDL compiler [**/cpp\_opt**](-cpp-opt.md) switch must be specified.</span></span> <span data-ttu-id="d5e20-116">Consulte [requisitos do pré-processador do C para MIDL](c-preprocessor-requirements-for-midl.md) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d5e20-116">See [C-Preprocessor Requirements for MIDL](c-preprocessor-requirements-for-midl.md) for details</span></span>

<span data-ttu-id="d5e20-117">O pré-processador é invocado por uma cadeia de caracteres de comando que é formada pelas informações fornecidas ao compilador MIDL **por/cpp \_ cmd**, [**/cpp \_ opt**](-cpp-opt.md), [**/d**](-d.md), [**/i**](-i.md)e [**/u**](-u.md) opções.</span><span class="sxs-lookup"><span data-stu-id="d5e20-117">The preprocessor is invoked by a command string that is formed from the information provided to the MIDL compiler by **/cpp\_cmd**, [**/cpp\_opt**](-cpp-opt.md), [**/D**](-d.md), [**/I**](-i.md), and [**/U**](-u.md) switches.</span></span> <span data-ttu-id="d5e20-118">A tabela a seguir resume como a cadeia de caracteres de comando é construída para cada combinação de **/cpp \_ cmd** e **/cpp \_ opt** switches.</span><span class="sxs-lookup"><span data-stu-id="d5e20-118">The following table summarizes how the command string is constructed for each combination of **/cpp\_cmd** and **/cpp\_opt** switches.</span></span>

<span data-ttu-id="d5e20-119">Quando a opção **/cpp \_ cmd** não é especificada, o compilador MIDL invoca o compilador do Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="d5e20-119">When the **/cpp\_cmd** switch is not specified, the MIDL compiler invokes the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="d5e20-120">MIDL usa um binário Cl.exe encontrado no ambiente de compilação.</span><span class="sxs-lookup"><span data-stu-id="d5e20-120">MIDL uses a Cl.exe binary found in the build environment.</span></span>

<span data-ttu-id="d5e20-121">Quando a opção [**/cpp \_ opt**](-cpp-opt.md) não está presente, o compilador MIDL concatena a cadeia de caracteres especificada pela **opção/cpp \_ cmd** com as informações especificadas pelas opções MIDL [**/i**](-i.md), [**/d**](-d.md) e [**/u**](-u.md) .</span><span class="sxs-lookup"><span data-stu-id="d5e20-121">When the [**/cpp\_opt**](-cpp-opt.md) switch is not present, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the information specified by the MIDL [**/I**](-i.md), [**/D**](-d.md) and [**/U**](-u.md) options.</span></span> <span data-ttu-id="d5e20-122">A cadeia de caracteres/E também é concatenada à cadeia de caracteres de invocação do compilador C para indicar que o compilador C/C++ deve executar o pré-processamento apenas.</span><span class="sxs-lookup"><span data-stu-id="d5e20-122">The string /E is also concatenated to the C-compiler invocation string to indicate that the C/C++ compiler should perform preprocessing only.</span></span> <span data-ttu-id="d5e20-123">A opção [**/nologo**](-nologo.md) é adicionada para suprimir a faixa do compilador C/C++.</span><span class="sxs-lookup"><span data-stu-id="d5e20-123">The [**/nologo**](-nologo.md) switch is added to suppress the C/C++ compiler banner.</span></span> <span data-ttu-id="d5e20-124">O compilador MIDL usa a cadeia de caracteres concatenada para invocar o pré-processador C para IDL de nível superior, bem como arquivos IDL importados, e também para quaisquer arquivos ACF presentes correspondentes.</span><span class="sxs-lookup"><span data-stu-id="d5e20-124">The MIDL compiler uses the concatenated string to invoke the C preprocessor for top-level IDL as well as imported IDL files, and also for any present, corresponding ACF files.</span></span>

<span data-ttu-id="d5e20-125">Quando a opção [**/cpp \_ opt**](-cpp-opt.md) está presente, o que deve ser um caso raro para as plataformas atuais de 32 bits e 64 bits, o compilador MIDL concatena a cadeia de caracteres especificada pela **opção \_ cmd/cpp** com a cadeia de caracteres especificada pela opção **\_ opcional/cpp** .</span><span class="sxs-lookup"><span data-stu-id="d5e20-125">When the [**/cpp\_opt**](-cpp-opt.md) switch is present, which should be a rare case for the current 32-bit and 64-bit platforms, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the string specified by the **/cpp\_opt** switch.</span></span> <span data-ttu-id="d5e20-126">O compilador MIDL usa a cadeia de caracteres concatenada para invocar o binário do pré-processador indicado no lugar do pré-processador padrão.</span><span class="sxs-lookup"><span data-stu-id="d5e20-126">The MIDL compiler uses the concatenated string to invoke the indicated preprocessor binary in place of the default preprocessor.</span></span> <span data-ttu-id="d5e20-127">Quando a **opção/cpp \_ opt** está presente, nem as opções do compilador MIDL especificadas pelas comutações [**/I**](-i.md), [**/d**](-d.md)e [**/u**](-u.md) nem o switch do compilador C/e são concatenados com a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d5e20-127">When the **/cpp\_opt** switch is present, neither the MIDL compiler options specified by the [**/I**](-i.md), [**/D**](-d.md), and [**/U**](-u.md) switches nor the C compiler switch /E is concatenated with the string.</span></span> <span data-ttu-id="d5e20-128">Você deve fornecer a opção/E, ou equivalente, como parte da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d5e20-128">You must supply the /E option, or equivalent, as part of the string.</span></span>



| <span data-ttu-id="d5e20-129">/cpp \_ cmd presente?</span><span class="sxs-lookup"><span data-stu-id="d5e20-129">/cpp\_cmd present?</span></span> | <span data-ttu-id="d5e20-130">a \_ opção/cpp está presente?</span><span class="sxs-lookup"><span data-stu-id="d5e20-130">/cpp\_opt present?</span></span> | <span data-ttu-id="d5e20-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="d5e20-131">Description</span></span>                                                                                                                                                                                                       |
|--------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5e20-132">Não (padrão)</span><span class="sxs-lookup"><span data-stu-id="d5e20-132">No (default)</span></span>       | <span data-ttu-id="d5e20-133">Não (padrão)</span><span class="sxs-lookup"><span data-stu-id="d5e20-133">No (default)</span></span>       | <span data-ttu-id="d5e20-134">Invoca o compilador padrão do Microsoft C/C++ com as configurações obtidas nas opções MIDL [**/i**](-i.md), [**/d**](-d.md) e [**/u**](-u.md) .</span><span class="sxs-lookup"><span data-stu-id="d5e20-134">Invokes the default Microsoft C/C++ compiler with settings obtained from MIDL [**/I**](-i.md), [**/D**](-d.md) and [**/U**](-u.md) switches.</span></span> <span data-ttu-id="d5e20-135">Adiciona os comutadores de pré-processador/E e [**/nologo**](-nologo.md).</span><span class="sxs-lookup"><span data-stu-id="d5e20-135">Adds the preprocessor switches /E and [**/nologo**](-nologo.md).</span></span> |
| <span data-ttu-id="d5e20-136">Sim</span><span class="sxs-lookup"><span data-stu-id="d5e20-136">Yes</span></span>                | <span data-ttu-id="d5e20-137">Não</span><span class="sxs-lookup"><span data-stu-id="d5e20-137">No</span></span>                 | <span data-ttu-id="d5e20-138">Invoca o binário de pré-processador indicado com os mesmos comutadores acima.</span><span class="sxs-lookup"><span data-stu-id="d5e20-138">Invokes the indicated preprocessor binary with the same switches as above.</span></span>                                                                                                                                        |
| <span data-ttu-id="d5e20-139">Não</span><span class="sxs-lookup"><span data-stu-id="d5e20-139">No</span></span>                 | <span data-ttu-id="d5e20-140">Sim</span><span class="sxs-lookup"><span data-stu-id="d5e20-140">Yes</span></span>                | <span data-ttu-id="d5e20-141">Invoca o compilador C da Microsoft com opções especificadas.</span><span class="sxs-lookup"><span data-stu-id="d5e20-141">Invokes the Microsoft C compiler with specified options.</span></span> <span data-ttu-id="d5e20-142">Não usa MIDL [**/i**](-i.md), [**/d**](-d.md), [**/u**](-u.md) opções.</span><span class="sxs-lookup"><span data-stu-id="d5e20-142">Does not use MIDL [**/I**](-i.md), [**/D**](-d.md), [**/U**](-u.md) options.</span></span> <span data-ttu-id="d5e20-143">Você deve fornecer/E como parte da [**/cpp \_ opt**](-cpp-opt.md).</span><span class="sxs-lookup"><span data-stu-id="d5e20-143">You must supply /E as part of [**/cpp\_opt**](-cpp-opt.md).</span></span>             |
| <span data-ttu-id="d5e20-144">Sim</span><span class="sxs-lookup"><span data-stu-id="d5e20-144">Yes</span></span>                | <span data-ttu-id="d5e20-145">Sim</span><span class="sxs-lookup"><span data-stu-id="d5e20-145">Yes</span></span>                | <span data-ttu-id="d5e20-146">Invoca o binário do pré-processador especificado somente com as opções especificadas.</span><span class="sxs-lookup"><span data-stu-id="d5e20-146">Invokes the specified preprocessor binary with specified options only.</span></span> <span data-ttu-id="d5e20-147">Você deve usar aspas.</span><span class="sxs-lookup"><span data-stu-id="d5e20-147">You must use quotes.</span></span>                                                                                                                       |



 

## <a name="examples"></a><span data-ttu-id="d5e20-148">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d5e20-148">Examples</span></span>

<span data-ttu-id="d5e20-149">**MIDL/cpp \_ cmd d: \\ NT \\ Tools \\ IA64 \\cl.exe/DFLAG = true/IC: \\ Inc filename. idl**</span><span class="sxs-lookup"><span data-stu-id="d5e20-149">**midl /cpp\_cmd d:\\nt\\tools\\ia64\\cl.exe /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="d5e20-150">**MIDL/cpp \_ cmd "mycpp"/DFLAG = true/IC: \\ Inc filename. idl**</span><span class="sxs-lookup"><span data-stu-id="d5e20-150">**midl /cpp\_cmd "mycpp" /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="d5e20-151">**MIDL/cpp \_ opt "/E/DFLAG = true/IC: \\ Inc" filename. idl**</span><span class="sxs-lookup"><span data-stu-id="d5e20-151">**midl /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

<span data-ttu-id="d5e20-152">**MIDL/cpp \_ cmd "CL"/cpp \_ opt "/e/DFLAG = true/IC: \\ Inc" filename. idl**</span><span class="sxs-lookup"><span data-stu-id="d5e20-152">**midl /cpp\_cmd "cl" /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="d5e20-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5e20-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5e20-154">**/savePP**</span><span class="sxs-lookup"><span data-stu-id="d5e20-154">**/savePP**</span></span>](-savepp.md)
</dt> <dt>

[<span data-ttu-id="d5e20-155">**/cpp \_ aceitar**</span><span class="sxs-lookup"><span data-stu-id="d5e20-155">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="d5e20-156">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="d5e20-156">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="d5e20-157">**///// \_ cpp**</span><span class="sxs-lookup"><span data-stu-id="d5e20-157">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> <dt>

[<span data-ttu-id="d5e20-158">Requisitos de pré-processador do C para MIDL</span><span class="sxs-lookup"><span data-stu-id="d5e20-158">C-Preprocessor Requirements for MIDL</span></span>](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 




