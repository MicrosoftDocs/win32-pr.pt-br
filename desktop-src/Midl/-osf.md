---
title: comutador/OSF
description: A opção/OSF força a compatibilidade estrita com o uso DCE.
ms.assetid: d94228fa-24af-43d7-9596-cf3a14690e0b
keywords:
- MIDL do comutador/OSF
topic_type:
- apiref
api_name:
- /osf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2936401d59bb8c2c2bcfdcffce27ba9ed978d506
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007433"
---
# <a name="osf-switch"></a><span data-ttu-id="7c765-104">comutador/OSF</span><span class="sxs-lookup"><span data-stu-id="7c765-104">/osf switch</span></span>

<span data-ttu-id="7c765-105">A opção **/OSF** força a compatibilidade estrita com o uso DCE.</span><span class="sxs-lookup"><span data-stu-id="7c765-105">The **/osf** switch forces strict compatibility with OSF DCE.</span></span>

``` syntax
midl /osf
```

## <a name="switch-options"></a><span data-ttu-id="7c765-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="7c765-106">Switch Options</span></span>

<span data-ttu-id="7c765-107">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7c765-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c765-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c765-108">Remarks</span></span>

<span data-ttu-id="7c765-109">Use essa opção se seu aplicativo exigir compatibilidade estrita com o uso DCE para fins de portabilidade.</span><span class="sxs-lookup"><span data-stu-id="7c765-109">Use this switch if your application requires strict compatibility with OSF DCE for portability reasons.</span></span>

<span data-ttu-id="7c765-110">No modo **/OSF** , o pacote RPCSS é habilitado automaticamente quando você usa ponteiros completos, os argumentos exigem alocação de memória ou quando você usa o atributo [**habilitar \_ alocação**](enable-allocate.md) .</span><span class="sxs-lookup"><span data-stu-id="7c765-110">In **/osf** mode, the RpcSs package is automatically enabled when you use full pointers, the arguments require memory allocation, or when you use the [**enable\_allocate**](enable-allocate.md) attribute.</span></span> <span data-ttu-id="7c765-111">Isso significa que você não precisa fornecer as funções de [**\_ \_ alocação**](/windows/desktop/Rpc/the-midl-user-allocate-function) de usuário de MIDL e de [**\_ \_ usuário MIDL**](/windows/desktop/Rpc/the-midl-user-free-function) em seu aplicativo cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="7c765-111">This means that you do not have to supply the [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function) and [**midl\_user\_free**](/windows/desktop/Rpc/the-midl-user-free-function) functions in your client and server application.</span></span>

<span data-ttu-id="7c765-112">Os seguintes recursos estendidos da Microsoft não estão disponíveis quando você compila com a opção **/OSF** :</span><span class="sxs-lookup"><span data-stu-id="7c765-112">The following Microsoft-extended features are not available when you compile with the **/osf** switch:</span></span>

-   <span data-ttu-id="7c765-113">Os declaradores abstratos (parâmetros sem nome) no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="7c765-113">Abstract declarators (unnamed parameters) in the IDL file.</span></span>
-   <span data-ttu-id="7c765-114">Definições de interface para objetos COM.</span><span class="sxs-lookup"><span data-stu-id="7c765-114">Interface definitions for COM objects.</span></span>
-   <span data-ttu-id="7c765-115">Nomes de interface com mais de 17 caracteres.</span><span class="sxs-lookup"><span data-stu-id="7c765-115">Interface names with more than 17 characters.</span></span>
-   <span data-ttu-id="7c765-116">Atributos somente MIDL, como [**\_ marshaling de conexão**](wire-marshal.md), [**\_ marshaling do usuário**](user-marshal.md)e as extensões de typelib (ODL).</span><span class="sxs-lookup"><span data-stu-id="7c765-116">MIDL-only attributes, such as [**wire\_marshal**](wire-marshal.md), [**user\_marshal**](user-marshal.md), and the typelib (ODL)extensions.</span></span>
-   <span data-ttu-id="7c765-117">Usando palavras-chave ACF em um arquivo IDL (a opção MIDL **/app \_ config** ).</span><span class="sxs-lookup"><span data-stu-id="7c765-117">Using ACF keywords in an IDL file (the MIDL **/app\_config** option).</span></span>
-   <span data-ttu-id="7c765-118">Funções de retorno de chamada estática no cliente.</span><span class="sxs-lookup"><span data-stu-id="7c765-118">Static callback functions on the client.</span></span>
-   <span data-ttu-id="7c765-119">O atributo [**Async**](async.md) .</span><span class="sxs-lookup"><span data-stu-id="7c765-119">The [**async**](async.md) attribute.</span></span>
-   <span data-ttu-id="7c765-120">[**\_ aspas de CPP**](cpp-quote.md) e **\# \_ eco de MIDL de pragma**.</span><span class="sxs-lookup"><span data-stu-id="7c765-120">[**cpp\_quote**](cpp-quote.md) and **\#pragma midl\_echo**.</span></span>
-   <span data-ttu-id="7c765-121">[**WCHAR \_ t**](wchar-t.md) largo-tipos de caractere, constantes e cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7c765-121">[**wchar\_t**](wchar-t.md) wide-character types, constants, and strings.</span></span>
-   <span data-ttu-id="7c765-122">inicialização de [**Enumeração**](enum.md) (enumeradores esparsos).</span><span class="sxs-lookup"><span data-stu-id="7c765-122">[**enum**](enum.md) initialization (sparse enumerators).</span></span>
-   <span data-ttu-id="7c765-123">especificação de tamanho somente [**out**](out-idl.md).</span><span class="sxs-lookup"><span data-stu-id="7c765-123">[**out**](out-idl.md)-only size specification.</span></span>
-   <span data-ttu-id="7c765-124">Tamanhos mistos-ponteiros e matrizes dimensionais.</span><span class="sxs-lookup"><span data-stu-id="7c765-124">Mixed sized-pointers and sized arrays.</span></span>
-   <span data-ttu-id="7c765-125">Expressões usadas para especificadores de tamanho e discriminador.</span><span class="sxs-lookup"><span data-stu-id="7c765-125">Expressions used for size and discriminator specifiers.</span></span>
-   <span data-ttu-id="7c765-126">Parâmetros de identificador explícitos em qualquer posição na lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="7c765-126">Explicit handle parameters in any position in the argument list.</span></span> <span data-ttu-id="7c765-127">No modo **/OSF** , o compilador MIDL procura um identificador de ligação explícito como o primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7c765-127">In **/osf** mode, the MIDL compiler looks for an explicit binding handle as the first parameter.</span></span> <span data-ttu-id="7c765-128">Quando o primeiro parâmetro não é um identificador de associação e um ou mais identificadores de contexto são especificados, o identificador de contexto mais à esquerda é usado como o identificador de associação.</span><span class="sxs-lookup"><span data-stu-id="7c765-128">When the first parameter is not a binding handle and one or more context handles are specified, the leftmost context handle is used as the binding handle.</span></span> <span data-ttu-id="7c765-129">Quando o primeiro parâmetro não é um identificador e não há identificadores de contexto, o procedimento usa a associação implícita usando o [**\_ identificador implícito**](implicit-handle.md) do atributo de ACF ou o [**\_ identificador automático**](auto-handle.md).</span><span class="sxs-lookup"><span data-stu-id="7c765-129">When the first parameter is not a handle and there are no context handles, the procedure uses implicit binding using the ACF attribute [**implicit\_handle**](implicit-handle.md) or [**auto\_handle**](auto-handle.md).</span></span>
-   <span data-ttu-id="7c765-130">Herança de tipo de atributo de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="7c765-130">Pointer-attribute type inheritance.</span></span> <span data-ttu-id="7c765-131">USO o DCE não permite ponteiros sem atributo.</span><span class="sxs-lookup"><span data-stu-id="7c765-131">OSF DCE does not allow unattributed pointers.</span></span> <span data-ttu-id="7c765-132">Portanto, no modo **/OSF** , cada arquivo IDL deve definir atributos para seus ponteiros.</span><span class="sxs-lookup"><span data-stu-id="7c765-132">Therefore, in **/osf** mode each IDL file must define attributes for its pointers.</span></span> <span data-ttu-id="7c765-133">Se qualquer ponteiro não tiver um atributo explícito, o arquivo IDL deverá ter uma especificação de [**ponteiro \_ padrão**](pointer-default.md) para definir o tipo de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="7c765-133">If any pointer does not have an explicit attribute, the IDL file must have a [**pointer\_default**](pointer-default.md) specification to set the pointer type.</span></span>
-   <span data-ttu-id="7c765-134">Várias interfaces em um arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="7c765-134">Multiple interfaces in an IDL file.</span></span>
-   <span data-ttu-id="7c765-135">Definições fora do bloco de interface.</span><span class="sxs-lookup"><span data-stu-id="7c765-135">Definitions outside of the interface block.</span></span>
-   <span data-ttu-id="7c765-136">Qualificadores de tipo, como **far** e **stdcall**.</span><span class="sxs-lookup"><span data-stu-id="7c765-136">Type qualifiers such as **far** and **stdcall**.</span></span>
-   <span data-ttu-id="7c765-137">Omitindo atributos direcionais.</span><span class="sxs-lookup"><span data-stu-id="7c765-137">Omitting directional attributes.</span></span>

<span data-ttu-id="7c765-138">As seguintes extensões de linguagem C/C++ não estão disponíveis quando você compila com a opção **/OSF** :</span><span class="sxs-lookup"><span data-stu-id="7c765-138">The following C/C++ language extensions are not available when you compile with the **/osf** switch:</span></span>

-   <span data-ttu-id="7c765-139">Campos de bits em estruturas e uniões.</span><span class="sxs-lookup"><span data-stu-id="7c765-139">Bit fields in structures and unions.</span></span>
-   <span data-ttu-id="7c765-140">Comentários de linha única delimitados por dois caracteres de barra (//).</span><span class="sxs-lookup"><span data-stu-id="7c765-140">Single line comments delimited with two slash characters (//).</span></span>
-   <span data-ttu-id="7c765-141">Declarações externas.</span><span class="sxs-lookup"><span data-stu-id="7c765-141">External declarations.</span></span>
-   <span data-ttu-id="7c765-142">Procedimentos com reticências na lista de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7c765-142">Procedures with ellipses in the parameter list.</span></span>
-   <span data-ttu-id="7c765-143">Digite [**int**](int.md).</span><span class="sxs-lookup"><span data-stu-id="7c765-143">Type [**int**](int.md).</span></span>
-   <span data-ttu-id="7c765-144">Digite **void \*** (exceto com o atributo de [**\_ identificador de contexto**](context-handle.md) ).</span><span class="sxs-lookup"><span data-stu-id="7c765-144">Type **void \*** (except with the [**context\_handle**](context-handle.md) attribute).</span></span>
-   <span data-ttu-id="7c765-145">Os qualificadores de tipo, incluindo o formulário com o prefixo de conformidade com ANSI, contêm dois caracteres de sublinhado: **\_ \_ cdecl**, **cdecl**, [**const**](const.md), **const**, **\_ \_ Exportar**, **Exportar**, **\_ \_ longe**, **longe**, **\_ \_ LOADDS**, **LOADDS**, **\_ \_ próximo**, **próximo**, **\_ \_ Pascal**, **Pascal**, **\_ \_ stdcall**, **stdcall**, **\_ \_ volátil** e **volátil**.</span><span class="sxs-lookup"><span data-stu-id="7c765-145">Type qualifiers, including the form with the ANSI-conformant prefix, contain two underscore characters: **\_\_cdecl**, **cdecl**, [**const**](const.md), **const**, **\_\_export**, **export**, **\_\_far**, **far**, **\_\_loadds**, **loadds**, **\_\_near**, **near**, **\_\_pascal**, **pascal**, **\_\_stdcall**, **stdcall**, **\_\_volatile**, and **volatile**.</span></span>
-   <span data-ttu-id="7c765-146">Qualquer \# aviso [**pragma**](pragma.md) ou comentário **\# pragma** .</span><span class="sxs-lookup"><span data-stu-id="7c765-146">Any \# [**pragma**](pragma.md) warning or **\#pragma** comment.</span></span>
-   <span data-ttu-id="7c765-147">Serialização de tipo.</span><span class="sxs-lookup"><span data-stu-id="7c765-147">Type serialization.</span></span>
-   <span data-ttu-id="7c765-148">O tipo de dados [**\_ \_ int3264**](--int3264.md) .</span><span class="sxs-lookup"><span data-stu-id="7c765-148">The [**\_\_int3264**](--int3264.md) data type.</span></span>
-   <span data-ttu-id="7c765-149">A opção [**/Protocol**](-protocol.md) e a sintaxe de transferência ndr64.</span><span class="sxs-lookup"><span data-stu-id="7c765-149">The [**/protocol**](-protocol.md) switch, and ndr64 transfer syntax.</span></span>

## <a name="examples"></a><span data-ttu-id="7c765-150">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7c765-150">Examples</span></span>

<span data-ttu-id="7c765-151">**MIDL/OSF filename. idl**</span><span class="sxs-lookup"><span data-stu-id="7c765-151">**midl /osf filename.idl**</span></span>

<span data-ttu-id="7c765-152">**MIDL/OSF/app \_ config filename. idl**</span><span class="sxs-lookup"><span data-stu-id="7c765-152">**midl /osf /app\_config filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="7c765-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c765-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c765-154">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="7c765-154">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="7c765-155">**configuração do/App \_**</span><span class="sxs-lookup"><span data-stu-id="7c765-155">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="7c765-156">**/MS \_ ext**</span><span class="sxs-lookup"><span data-stu-id="7c765-156">**/ms\_ext**</span></span>](-ms-ext.md)
</dt> <dt>

[<span data-ttu-id="7c765-157">Pacote de gerenciamento de memória de RPCSS</span><span class="sxs-lookup"><span data-stu-id="7c765-157">Rpcss Memory Management Package</span></span>](/windows/desktop/Rpc/rpcss-memory-management-package)
</dt> </dl>

 

 