---
title: Extensões de Binding-Handle RPC da Microsoft
description: As extensões da Microsoft para a linguagem IDL dão suporte a vários parâmetros de identificador que aparecem em posições diferentes do primeiro, o parâmetro mais à esquerda.
ms.assetid: 084b0d8e-0c8a-43b9-b3ae-4f69cab3a2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a947c10465cb24012be9c3f845fbd874f9de0567
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104008511"
---
# <a name="microsoft-rpc-binding-handle-extensions"></a><span data-ttu-id="de930-103">Extensões de Binding-Handle RPC da Microsoft</span><span class="sxs-lookup"><span data-stu-id="de930-103">Microsoft RPC Binding-Handle Extensions</span></span>

<span data-ttu-id="de930-104">As extensões da Microsoft para a linguagem IDL dão suporte a vários parâmetros de identificador que aparecem em posições diferentes do primeiro, o parâmetro mais à esquerda.</span><span class="sxs-lookup"><span data-stu-id="de930-104">The Microsoft extensions to the IDL language support multiple handle parameters that appear in positions other than the first, leftmost, parameter.</span></span> <span data-ttu-id="de930-105">As etapas a seguir descrevem a sequência que o compilador MIDL passa para resolver o parâmetro de identificador de associação no modo de compatibilidade DCE (/**uso**) e no modo padrão (Microsoft-Extended).</span><span class="sxs-lookup"><span data-stu-id="de930-105">The following steps describe the sequence that the MIDL compiler goes through to resolve the binding-handle parameter in DCE-compatibility mode (/**osf**), and in default (Microsoft-extended) mode.</span></span>

## <a name="dce-compatibility-mode"></a><span data-ttu-id="de930-106">Modo de compatibilidade do DCE</span><span class="sxs-lookup"><span data-stu-id="de930-106">DCE-compatibility mode</span></span>

-   <span data-ttu-id="de930-107">Identificador de associação que aparece na primeira posição.</span><span class="sxs-lookup"><span data-stu-id="de930-107">Binding handle that appears in first position.</span></span>
-   <span data-ttu-id="de930-108">Na extrema esquerda \[ , parâmetro [**de**](/windows/desktop/Midl/in) [**\_ identificador de contexto**](/windows/desktop/Midl/context-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="de930-108">Leftmost \[[**in**](/windows/desktop/Midl/in), [**context\_handle**](/windows/desktop/Midl/context-handle)\] parameter.</span></span>
-   <span data-ttu-id="de930-109">Identificador de associação implícito especificado por \[ [**\_ identificador implícito**](/windows/desktop/Midl/implicit-handle) \] ou \[ [**\_ identificador automático**](/windows/desktop/Midl/auto-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="de930-109">Implicit binding handle specified by \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>
-   <span data-ttu-id="de930-110">Se não houver um ACF presente, o padrão será o uso do \[ **\_ identificador auto** \] .</span><span class="sxs-lookup"><span data-stu-id="de930-110">If no ACF present, default to use of \[**auto\_handle**\].</span></span>

## <a name="default-mode"></a><span data-ttu-id="de930-111">Modo padrão</span><span class="sxs-lookup"><span data-stu-id="de930-111">Default mode</span></span>

-   <span data-ttu-id="de930-112">Identificador de ligação explícita mais à esquerda.</span><span class="sxs-lookup"><span data-stu-id="de930-112">Leftmost explicit binding handle.</span></span>
-   <span data-ttu-id="de930-113">Identificador de associação implícito especificado por \[ [**\_ identificador implícito**](/windows/desktop/Midl/implicit-handle) \] ou \[ [**\_ identificador automático**](/windows/desktop/Midl/auto-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="de930-113">Implicit binding handle specified by \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>
-   <span data-ttu-id="de930-114">Se não houver um ACF presente, o padrão será o uso do \[ [**\_ identificador auto**](/windows/desktop/Midl/auto-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="de930-114">If no ACF present, default to use of \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>

<span data-ttu-id="de930-115">Os compiladores de IDL do DCE procuram um identificador de associação explícito como o primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="de930-115">DCE IDL compilers look for an explicit binding handle as the first parameter.</span></span> <span data-ttu-id="de930-116">Quando o primeiro parâmetro não é um identificador de associação e um ou mais identificadores de contexto são especificados, o identificador de contexto mais à esquerda é usado como o identificador de associação.</span><span class="sxs-lookup"><span data-stu-id="de930-116">When the first parameter is not a binding handle and one or more context handles are specified, the leftmost context handle is used as the binding handle.</span></span> <span data-ttu-id="de930-117">Quando o primeiro parâmetro não é um identificador e não há identificadores de contexto, o procedimento usa a associação implícita usando o \[ [**\_ identificador implícito**](/windows/desktop/Midl/implicit-handle) do atributo de ACF \] ou o \[ [**\_ identificador automático**](/windows/desktop/Midl/auto-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="de930-117">When the first parameter is not a handle and there are no context handles, the procedure uses implicit binding using the ACF attribute \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>

<span data-ttu-id="de930-118">As extensões da Microsoft para a IDL permitem que o identificador de ligação esteja em uma posição diferente do primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="de930-118">The Microsoft extensions to the IDL allow the binding handle to be in a position other than the first parameter.</span></span> <span data-ttu-id="de930-119">A extrema esquerda \[ [**no**](/windows/desktop/Midl/in) \] parâmetro de identificador explícito – se é um primitivo, definido pelo programador ou um identificador de contexto – é o identificador de associação.</span><span class="sxs-lookup"><span data-stu-id="de930-119">The leftmost \[[**in**](/windows/desktop/Midl/in)\] explicit-handle parameter–whether it is a primitive, programmer-defined, or context handle–is the binding handle.</span></span> <span data-ttu-id="de930-120">Quando não há parâmetros de identificador, o procedimento usa associação implícita usando o \[ [**\_ identificador implícito**](/windows/desktop/Midl/implicit-handle) do atributo ACF \] ou o \[ [**\_ identificador auto**](/windows/desktop/Midl/auto-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="de930-120">When there are no handle parameters, the procedure uses implicit binding using the ACF attribute \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>

<span data-ttu-id="de930-121">As regras a seguir se aplicam ao modo de compatibilidade do DCE (/OSF) e ao modo padrão:</span><span class="sxs-lookup"><span data-stu-id="de930-121">The following rules apply to both DCE-compatibility (/osf) mode and default mode:</span></span>

-   <span data-ttu-id="de930-122">A associação de identificador automático é usada quando nenhum ACF está presente.</span><span class="sxs-lookup"><span data-stu-id="de930-122">Auto-handle binding is used when no ACF is present.</span></span>
-   <span data-ttu-id="de930-123">\[ [](/windows/desktop/Midl/in) \] Os identificadores explícitos in ou \[ **in**, [**out**](/windows/desktop/Midl/out-idl) \] para uma função individual imprimem qualquer associação implícita especificada para a interface.</span><span class="sxs-lookup"><span data-stu-id="de930-123">Explicit \[[**in**](/windows/desktop/Midl/in)\] or \[**in**, [**out**](/windows/desktop/Midl/out-idl)\] handles for an individual function preempt any implicit binding specified for the interface.</span></span>
-   <span data-ttu-id="de930-124">\[ [](/windows/desktop/Midl/in) \] \[  \] Não há suporte para vários identificadores primitivos in ou in.</span><span class="sxs-lookup"><span data-stu-id="de930-124">Multiple \[[**in**](/windows/desktop/Midl/in)\] or \[**in**, out\] primitive handles are not supported.</span></span>
-   <span data-ttu-id="de930-125">Vários \[ [](/windows/desktop/Midl/in) \] \[ identificadores de contexto explícitos de entrada ou **de** saída \] são permitidos.</span><span class="sxs-lookup"><span data-stu-id="de930-125">Multiple \[[**in**](/windows/desktop/Midl/in)\] or \[**in**, out\] explicit context handles are allowed.</span></span>
-   <span data-ttu-id="de930-126">Todos os parâmetros de identificador definidos pelo programador, exceto o parâmetro Binding-Handle, são tratados como dados Transmissible.</span><span class="sxs-lookup"><span data-stu-id="de930-126">All programmer-defined handle parameters except the binding-handle parameter are treated as transmissible data.</span></span>

<span data-ttu-id="de930-127">A tabela a seguir contém exemplos e descreve como os identificadores de associação são atribuídos em cada modo de compilador.</span><span class="sxs-lookup"><span data-stu-id="de930-127">The following table contains examples and describes how binding handles are assigned in each compiler mode.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="de930-128">Exemplo</span><span class="sxs-lookup"><span data-stu-id="de930-128">Example</span></span></th>
<th><span data-ttu-id="de930-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="de930-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>void proc1( void );</code></pre></td>
<td><span data-ttu-id="de930-130">Nenhum identificador explícito foi especificado.</span><span class="sxs-lookup"><span data-stu-id="de930-130">No explicit handle is specified.</span></span> <span data-ttu-id="de930-131">O identificador de associação implícito, especificado por [ <a href="/windows/desktop/Midl/implicit-handle">implicit_handle</a>] ou [ <a href="/windows/desktop/Midl/auto-handle">auto_handle</a>], é usado.</span><span class="sxs-lookup"><span data-stu-id="de930-131">The implicit binding handle, specified by [ <a href="/windows/desktop/Midl/implicit-handle">implicit_handle</a>] or [ <a href="/windows/desktop/Midl/auto-handle">auto_handle</a>], is used.</span></span> <span data-ttu-id="de930-132">Quando nenhum ACF estiver presente, um identificador automático será usado.</span><span class="sxs-lookup"><span data-stu-id="de930-132">When no ACF is present, an auto handle is used.</span></span></td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>void proc2([in] handle_t H,
           [in] short s );</code></pre></td>
<td><span data-ttu-id="de930-133">Um identificador explícito do tipo handle_t é especificado.</span><span class="sxs-lookup"><span data-stu-id="de930-133">An explicit handle of type handle_t is specified.</span></span> <span data-ttu-id="de930-134">O parâmetro <em>H</em> é o identificador de associação para o procedimento.</span><span class="sxs-lookup"><span data-stu-id="de930-134">The parameter <em>H</em> is the binding handle for the procedure.</span></span></td>
</tr>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>void proc3([in] short s,
           [in] handle_t H );</code></pre></td>
<td><span data-ttu-id="de930-135">O primeiro parâmetro não é um identificador.</span><span class="sxs-lookup"><span data-stu-id="de930-135">The first parameter is not a handle.</span></span> <span data-ttu-id="de930-136">No modo padrão, o parâmetro de identificador mais à esquerda, <em>H</em>, é o identificador de associação.</span><span class="sxs-lookup"><span data-stu-id="de930-136">In default mode, the leftmost handle parameter, <em>H</em>, is the binding handle.</span></span> <span data-ttu-id="de930-137">No modo/OSF, a associação implícita é usada.</span><span class="sxs-lookup"><span data-stu-id="de930-137">In /osf mode, implicit binding is used.</span></span> <span data-ttu-id="de930-138">Um erro é relatado porque o segundo parâmetro deve ser transmissible e handle_t não pode ser transmitido.</span><span class="sxs-lookup"><span data-stu-id="de930-138">An error is reported because the second parameter is expected to be transmissible, and handle_t cannot be transmitted.</span></span></td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>typedef [handle] short * MY_HDL;

void proc1([in] short s,
           [in] MY_HDL H );</code></pre></td>
<td><span data-ttu-id="de930-139">O primeiro parâmetro não é um identificador.</span><span class="sxs-lookup"><span data-stu-id="de930-139">The first parameter is not a handle.</span></span> <span data-ttu-id="de930-140">No modo padrão, o parâmetro de identificador mais à esquerda, <em>H</em>, é o identificador de associação.</span><span class="sxs-lookup"><span data-stu-id="de930-140">In default mode, the leftmost handle parameter, <em>H</em>, is the binding handle.</span></span> <span data-ttu-id="de930-141">Os stubs chamam as rotinas fornecidas pelo usuário MY_HDL_bind e MY_HDL_unbind.</span><span class="sxs-lookup"><span data-stu-id="de930-141">The stubs call the user-supplied routines MY_HDL_bind and MY_HDL_unbind.</span></span> <span data-ttu-id="de930-142">No modo/uso, a associação implícita é usada.</span><span class="sxs-lookup"><span data-stu-id="de930-142">In/osf mode, implicit binding is used.</span></span> <span data-ttu-id="de930-143">O parâmetro identificador <em>H</em> definido pelo programador é tratado como dados Transmissible.</span><span class="sxs-lookup"><span data-stu-id="de930-143">The programmer-defined handle parameter <em>H</em> is treated as transmissible data.</span></span></td>
</tr>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>Typedef [handle] short * MY_HDL;

void proc1([in] MY_HDL H, 
           [in] MY_HDL p );</code></pre></td>
<td><span data-ttu-id="de930-144">O primeiro parâmetro é um identificador de associação.</span><span class="sxs-lookup"><span data-stu-id="de930-144">The first parameter is a binding handle.</span></span> <span data-ttu-id="de930-145">O parâmetro <em>H</em> é o parâmetro de identificador de associação.</span><span class="sxs-lookup"><span data-stu-id="de930-145">The parameter <em>H</em> is the binding-handle parameter.</span></span> <span data-ttu-id="de930-146">O segundo parâmetro de identificador definido pelo programador é tratado como dados de Transmissible.</span><span class="sxs-lookup"><span data-stu-id="de930-146">The second programmer-defined handle parameter is treated as transmissible data.</span></span></td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>Typedef [context_handle] 
void * CTXT_HDL;

void proc1([in] short s,
           [in] long l,
           [in] CTXT_HDL H ,
           [in] char c);</code></pre></td>
<td><span data-ttu-id="de930-147">O identificador de associação é um identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="de930-147">The binding handle is a context handle.</span></span> <span data-ttu-id="de930-148">O parâmetro <em>H</em> é o identificador de associação.</span><span class="sxs-lookup"><span data-stu-id="de930-148">The parameter <em>H</em> is the binding handle.</span></span></td>
</tr>
</tbody>
</table>



 

 

 