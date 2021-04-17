---
title: Referência de Command-Line de MIDL
description: Esta seção contém informações de referência para cada opção de linha de comando e opções de comutador reconhecidas pelo compilador Microsoft RPC MIDL.
ms.assetid: a0e5efb0-a704-4dc5-bd7e-6c98466a2874
keywords:
- MIDL linguagem IDL da Microsoft, referência
- MIDL de referência de linha de comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1569e29daf8a2976379576a5f1671f5117e7990c
ms.sourcegitcommit: 9cf1ed65dfbea1ba118b63d0656f30c3685d8520
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105768491"
---
# <a name="midl-command-line-reference"></a><span data-ttu-id="740f9-105">Referência de Command-Line de MIDL</span><span class="sxs-lookup"><span data-stu-id="740f9-105">MIDL Command-Line Reference</span></span>

<span data-ttu-id="740f9-106">Esta seção contém informações de referência para cada opção de linha de comando e opções de comutador reconhecidas pelo compilador Microsoft RPC MIDL.</span><span class="sxs-lookup"><span data-stu-id="740f9-106">This section contains reference information for each command-line switch and switch option recognized by the Microsoft RPC MIDL compiler.</span></span> <span data-ttu-id="740f9-107">As entradas de comutador são organizadas em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="740f9-107">Switch entries are arranged in alphabetical order.</span></span> <span data-ttu-id="740f9-108">A [sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md) descreve a sintaxe de linha de comando geral.</span><span class="sxs-lookup"><span data-stu-id="740f9-108">[General MIDL Command-line Syntax](general-midl-command-line-syntax.md) describes the general command-line syntax.</span></span>

<dl>

[<span data-ttu-id="740f9-109">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="740f9-109">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)  
[<span data-ttu-id="740f9-110">O comando arquivo de resposta</span><span class="sxs-lookup"><span data-stu-id="740f9-110">The Response File Command</span></span>](the-response-file-command.md)  
[<span data-ttu-id="740f9-111">**/acf**</span><span class="sxs-lookup"><span data-stu-id="740f9-111">**/acf**</span></span>](-acf.md)  
[<span data-ttu-id="740f9-112">**/align**</span><span class="sxs-lookup"><span data-stu-id="740f9-112">**/align**</span></span>](-align.md)  
[<span data-ttu-id="740f9-113">**/amd64**</span><span class="sxs-lookup"><span data-stu-id="740f9-113">**/amd64**</span></span>](-amd64.md)  
[<span data-ttu-id="740f9-114">**configuração do/App \_**</span><span class="sxs-lookup"><span data-stu-id="740f9-114">**/app\_config**</span></span>](-app-config.md)  
[<span data-ttu-id="740f9-115">compatível com/Backward \_</span><span class="sxs-lookup"><span data-stu-id="740f9-115">/backward\_compat</span></span>](-backward-compat.md)  
[<span data-ttu-id="740f9-116">**/c \_ ext**</span><span class="sxs-lookup"><span data-stu-id="740f9-116">**/c\_ext**</span></span>](-c-ext.md)  
[<span data-ttu-id="740f9-117">**/caux**</span><span class="sxs-lookup"><span data-stu-id="740f9-117">**/caux**</span></span>](-caux.md)  
[<span data-ttu-id="740f9-118">**/Char**</span><span class="sxs-lookup"><span data-stu-id="740f9-118">**/char**</span></span>](-char.md)  
[<span data-ttu-id="740f9-119">**/Client**</span><span class="sxs-lookup"><span data-stu-id="740f9-119">**/client**</span></span>](-client.md)  
[<span data-ttu-id="740f9-120">**/confirm**</span><span class="sxs-lookup"><span data-stu-id="740f9-120">**/confirm**</span></span>](-confirm.md)  
[<span data-ttu-id="740f9-121">**/cpp \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="740f9-121">**/cpp\_cmd**</span></span>](-cpp-cmd.md)  
[<span data-ttu-id="740f9-122">**/cpp \_ aceitar**</span><span class="sxs-lookup"><span data-stu-id="740f9-122">**/cpp\_opt**</span></span>](-cpp-opt.md)  
<span data-ttu-id="740f9-123">[**/cstruct_out**](-cstruct-out.md) 
 [ **/cstub**](-cstub.md)</span><span class="sxs-lookup"><span data-stu-id="740f9-123">[**/cstruct_out**](-cstruct-out.md)
[**/cstub**](-cstub.md)</span></span>  
[<span data-ttu-id="740f9-124">**/D**</span><span class="sxs-lookup"><span data-stu-id="740f9-124">**/D**</span></span>](-d.md)  
[<span data-ttu-id="740f9-125">**/dlldata nomedearquivo**</span><span class="sxs-lookup"><span data-stu-id="740f9-125">**/dlldata**</span></span>](-dlldata.md)  
[<span data-ttu-id="740f9-126">**/env**</span><span class="sxs-lookup"><span data-stu-id="740f9-126">**/env**</span></span>](-env.md)  
[<span data-ttu-id="740f9-127">**/Error**</span><span class="sxs-lookup"><span data-stu-id="740f9-127">**/error**</span></span>](-error.md)  
[<span data-ttu-id="740f9-128">**/Error**</span><span class="sxs-lookup"><span data-stu-id="740f9-128">**/error**</span></span>](-error.md)  
[<span data-ttu-id="740f9-129">**/h**</span><span class="sxs-lookup"><span data-stu-id="740f9-129">**/h**</span></span>](-h.md)  
[<span data-ttu-id="740f9-130">**/header**</span><span class="sxs-lookup"><span data-stu-id="740f9-130">**/header**</span></span>](-header.md)  
[<span data-ttu-id="740f9-131">**/Help (/?)**</span><span class="sxs-lookup"><span data-stu-id="740f9-131">**/help (/?)**</span></span>](-help-.md)  
[<span data-ttu-id="740f9-132">**/ia64**</span><span class="sxs-lookup"><span data-stu-id="740f9-132">**/ia64**</span></span>](-ia64.md)  
[<span data-ttu-id="740f9-133">**/I**</span><span class="sxs-lookup"><span data-stu-id="740f9-133">**/I**</span></span>](-i.md)  
[<span data-ttu-id="740f9-134">**/IID nomedearquivo**</span><span class="sxs-lookup"><span data-stu-id="740f9-134">**/iid**</span></span>](-iid.md)  
[<span data-ttu-id="740f9-135">**/Import**</span><span class="sxs-lookup"><span data-stu-id="740f9-135">**/import**</span></span>](-import.md)  
[<span data-ttu-id="740f9-136">**/LCID**</span><span class="sxs-lookup"><span data-stu-id="740f9-136">**/lcid**</span></span>](-lcid.md)  
[<span data-ttu-id="740f9-137">**/mktyplib203**</span><span class="sxs-lookup"><span data-stu-id="740f9-137">**/mktyplib203**</span></span>](-mktyplib203.md)  
[<span data-ttu-id="740f9-138">**/MS \_ ext**</span><span class="sxs-lookup"><span data-stu-id="740f9-138">**/ms\_ext**</span></span>](-ms-ext.md)  
[<span data-ttu-id="740f9-139">**/MS \_ Union**</span><span class="sxs-lookup"><span data-stu-id="740f9-139">**/ms\_union**</span></span>](-ms-union.md)  
[<span data-ttu-id="740f9-140">**/MSC \_ Ver**</span><span class="sxs-lookup"><span data-stu-id="740f9-140">**/msc\_ver**</span></span>](-msc-ver.md)  
[<span data-ttu-id="740f9-141">**/new**</span><span class="sxs-lookup"><span data-stu-id="740f9-141">**/new**</span></span>](-new.md)  
[<span data-ttu-id="740f9-142">**/newtlb**</span><span class="sxs-lookup"><span data-stu-id="740f9-142">**/newtlb**</span></span>](-newtlb.md)  
[<span data-ttu-id="740f9-143">**/// \_ /nocpp**</span><span class="sxs-lookup"><span data-stu-id="740f9-143">**/no\_cpp, /nocpp**</span></span>](-no-cpp-nocpp.md)  
[<span data-ttu-id="740f9-144">**/ \_ \_ EPV padrão**</span><span class="sxs-lookup"><span data-stu-id="740f9-144">**/no\_default\_epv**</span></span>](-no-default-epv.md)  
[<span data-ttu-id="740f9-145">**/. de \_ \_ Idir def**</span><span class="sxs-lookup"><span data-stu-id="740f9-145">**/no\_def\_idir**</span></span>](-no-def-idir.md)  
[<span data-ttu-id="740f9-146">**\_opção de formato de/// \_**</span><span class="sxs-lookup"><span data-stu-id="740f9-146">**/no\_format\_opt**</span></span>](-no-format-opt.md)  
[<span data-ttu-id="740f9-147">**// \_ avançado**</span><span class="sxs-lookup"><span data-stu-id="740f9-147">**/no\_robust**</span></span>](-no-robust.md)  
[<span data-ttu-id="740f9-148">**// \_ avisar**</span><span class="sxs-lookup"><span data-stu-id="740f9-148">**/no\_warn**</span></span>](-no-warn.md)  
[<span data-ttu-id="740f9-149">**/nologo**</span><span class="sxs-lookup"><span data-stu-id="740f9-149">**/nologo**</span></span>](-nologo.md)  
[<span data-ttu-id="740f9-150">**/notlb**</span><span class="sxs-lookup"><span data-stu-id="740f9-150">**/notlb**</span></span>](-notlb.md)  
[<span data-ttu-id="740f9-151">**/o**</span><span class="sxs-lookup"><span data-stu-id="740f9-151">**/o**</span></span>](-o.md)  
[<span data-ttu-id="740f9-152">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="740f9-152">**/Oi**</span></span>](-oi.md)  
[<span data-ttu-id="740f9-153">**/old**</span><span class="sxs-lookup"><span data-stu-id="740f9-153">**/old**</span></span>](-old.md)  
[<span data-ttu-id="740f9-154">**/oldtlb**</span><span class="sxs-lookup"><span data-stu-id="740f9-154">**/oldtlb**</span></span>](-oldtlb.md)  
[<span data-ttu-id="740f9-155">**/oldnames**</span><span class="sxs-lookup"><span data-stu-id="740f9-155">**/oldnames**</span></span>](-oldnames.md)  
[<span data-ttu-id="740f9-156">**/Os**</span><span class="sxs-lookup"><span data-stu-id="740f9-156">**/Os**</span></span>](-os.md)  
[<span data-ttu-id="740f9-157">**/osf**</span><span class="sxs-lookup"><span data-stu-id="740f9-157">**/osf**</span></span>](-osf.md)  
[<span data-ttu-id="740f9-158">**/out**</span><span class="sxs-lookup"><span data-stu-id="740f9-158">**/out**</span></span>](-out.md)  
[<span data-ttu-id="740f9-159">**/Pack**</span><span class="sxs-lookup"><span data-stu-id="740f9-159">**/pack**</span></span>](-pack.md)  
[<span data-ttu-id="740f9-160">**/prefix**</span><span class="sxs-lookup"><span data-stu-id="740f9-160">**/prefix**</span></span>](-prefix.md)  
[<span data-ttu-id="740f9-161">**/protocol**</span><span class="sxs-lookup"><span data-stu-id="740f9-161">**/protocol**</span></span>](-protocol.md)  
[<span data-ttu-id="740f9-162">**/proxy nomedearquivo**</span><span class="sxs-lookup"><span data-stu-id="740f9-162">**/proxy**</span></span>](-proxy.md)  
[<span data-ttu-id="740f9-163">**/robust**</span><span class="sxs-lookup"><span data-stu-id="740f9-163">**/robust**</span></span>](-robust.md)  
[<span data-ttu-id="740f9-164">**/rpcss**</span><span class="sxs-lookup"><span data-stu-id="740f9-164">**/rpcss**</span></span>](-rpcss.md)  
[<span data-ttu-id="740f9-165">**/sal**</span><span class="sxs-lookup"><span data-stu-id="740f9-165">**/sal**</span></span>](-sal.md)  
[<span data-ttu-id="740f9-166">**/sal \_ local**</span><span class="sxs-lookup"><span data-stu-id="740f9-166">**/sal\_local**</span></span>](-sal-local.md)  
[<span data-ttu-id="740f9-167">**/saux**</span><span class="sxs-lookup"><span data-stu-id="740f9-167">**/saux**</span></span>](-saux.md)  
[<span data-ttu-id="740f9-168">**/savePP**</span><span class="sxs-lookup"><span data-stu-id="740f9-168">**/savePP**</span></span>](-savepp.md)  
[<span data-ttu-id="740f9-169">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="740f9-169">**/sstub**</span></span>](-sstub.md)  
[<span data-ttu-id="740f9-170">**verificação de/Syntax \_**</span><span class="sxs-lookup"><span data-stu-id="740f9-170">**/syntax\_check**</span></span>](-syntax-check.md)  
[**/<system>**](-system-.md)  
[<span data-ttu-id="740f9-171">**/debug**</span><span class="sxs-lookup"><span data-stu-id="740f9-171">**/target**</span></span>](-target.md)  
[<span data-ttu-id="740f9-172">**/tlb**</span><span class="sxs-lookup"><span data-stu-id="740f9-172">**/tlb**</span></span>](-tlb.md)  
[<span data-ttu-id="740f9-173">**/U**</span><span class="sxs-lookup"><span data-stu-id="740f9-173">**/U**</span></span>](-u.md)  
[<span data-ttu-id="740f9-174">**/Use \_ EPV**</span><span class="sxs-lookup"><span data-stu-id="740f9-174">**/use\_epv**</span></span>](-use-epv.md)  
[<span data-ttu-id="740f9-175">**/Version \_ carimbo**</span><span class="sxs-lookup"><span data-stu-id="740f9-175">**/version\_stamp**</span></span>](-version-stamp.md)  
[<span data-ttu-id="740f9-176">**/W**</span><span class="sxs-lookup"><span data-stu-id="740f9-176">**/W**</span></span>](-w.md)  
[<span data-ttu-id="740f9-177">**/Warn**</span><span class="sxs-lookup"><span data-stu-id="740f9-177">**/warn**</span></span>](-warn.md)  
[<span data-ttu-id="740f9-178">**/win32**</span><span class="sxs-lookup"><span data-stu-id="740f9-178">**/win32**</span></span>](-win32.md)  
[<span data-ttu-id="740f9-179">**/win64**</span><span class="sxs-lookup"><span data-stu-id="740f9-179">**/win64**</span></span>](-win64.md)  
[<span data-ttu-id="740f9-180">**/WX**</span><span class="sxs-lookup"><span data-stu-id="740f9-180">**/WX**</span></span>](-wx.md)  
[<span data-ttu-id="740f9-181">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="740f9-181">**/Zp**</span></span>](-zp.md)  
[<span data-ttu-id="740f9-182">**/ZS**</span><span class="sxs-lookup"><span data-stu-id="740f9-182">**/Zs**</span></span>](-zs.md)  
</dl>

<span data-ttu-id="740f9-183">O compilador MIDL pode gerar código para diferentes plataformas e versões do sistema.</span><span class="sxs-lookup"><span data-stu-id="740f9-183">The MIDL compiler can generate code for different platforms and system releases.</span></span> <span data-ttu-id="740f9-184">Consulte a opção [**/target**](-target.md) para saber mais sobre as opções sugeridas e como gerar código otimizado para uma determinada versão.</span><span class="sxs-lookup"><span data-stu-id="740f9-184">Consult the [**/target**](-target.md) switch to learn more about suggested switches and how to generate code optimized for a given release.</span></span>

<span data-ttu-id="740f9-185">Observe que o sinal de subtração (–) pode ser substituído pela barra (/) em todas as opções de linha de comando MIDL que começam com uma barra (/).</span><span class="sxs-lookup"><span data-stu-id="740f9-185">Note that the minus sign (–) may be substituted for the slash (/) in all MIDL command-line switches that begin with a slash (/).</span></span> <span data-ttu-id="740f9-186">O exemplo a seguir demonstra sua equivalência ao invocar o compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="740f9-186">The following example demonstrates their equivalence when invoking the MIDL compiler.</span></span>

## <a name="examples"></a><span data-ttu-id="740f9-187">Exemplos</span><span class="sxs-lookup"><span data-stu-id="740f9-187">Examples</span></span>

<span data-ttu-id="740f9-188">**MIDL/ACF meu nome de arquivo \_ ACF. ACF** \*\* \* *. idl*\*</span><span class="sxs-lookup"><span data-stu-id="740f9-188">**midl /acf my\_acf.acf** *filename\*\*\*.idl*\*</span></span>

<span data-ttu-id="740f9-189">**MIDL-ACF My \_ ACF. ACF** *filename \* \* *. idl**</span><span class="sxs-lookup"><span data-stu-id="740f9-189">**midl -acf my\_acf.acf** *filename\*\*\*.idl*\*</span></span>

 

 




