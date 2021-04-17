---
title: comutador/env
description: A opção/env seleciona o ambiente no qual o aplicativo é executado.
ms.assetid: 70a548c8-fdc3-48f3-a865-14ba9b29fb02
keywords:
- MIDL do comutador/env
topic_type:
- apiref
api_name:
- /env
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59da7185900d4b75781916bd6b4a9d70bf39dc85
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365882"
---
# <a name="env-switch"></a><span data-ttu-id="50ead-104">comutador/env</span><span class="sxs-lookup"><span data-stu-id="50ead-104">/env switch</span></span>

<span data-ttu-id="50ead-105">A opção **/env** seleciona o ambiente no qual o aplicativo é executado.</span><span class="sxs-lookup"><span data-stu-id="50ead-105">The **/env** switch selects the environment in which the application runs.</span></span>

``` syntax
midl /env { win32 | ia64 | amd64 | win64 }
```

## <a name="switch-options"></a><span data-ttu-id="50ead-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="50ead-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span data-ttu-id="50ead-107"><span id="win32"></span><span id="WIN32"></span>Win32 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="50ead-107"><span id="win32"></span><span id="WIN32"></span>\*\*\*\*win32\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="50ead-108">Direciona o compilador MIDL para gerar arquivos stub, ou um arquivo de biblioteca de tipos, para um ambiente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="50ead-108">Directs the MIDL compiler to generate stub files, or a type library file, for a 32-bit environment.</span></span>

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span data-ttu-id="50ead-109"><span id="ia64"></span><span id="IA64"></span>IA64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="50ead-109"><span id="ia64"></span><span id="IA64"></span>\*\*\*\*ia64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="50ead-110">Direciona o compilador MIDL para gerar arquivos stub, ou um arquivo de biblioteca de tipos, para um ambiente de arquitetura Intel de 64 bits (IA64).</span><span class="sxs-lookup"><span data-stu-id="50ead-110">Directs the MIDL compiler to generate stub files, or a type library file, for a Intel Architecture 64-bit (IA64) environment.</span></span>

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span data-ttu-id="50ead-111"><span id="amd64"></span><span id="AMD64"></span>AMD64 \* \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="50ead-111"><span id="amd64"></span><span id="AMD64"></span>\*\*\*\*amd64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="50ead-112">Direciona o compilador MIDL para gerar arquivos stub, ou um arquivo de biblioteca de tipos, para um ambiente avançado de micro dispositivos 64 bits (AMD64).</span><span class="sxs-lookup"><span data-stu-id="50ead-112">Directs the MIDL compiler to generate stub files, or a type library file, for an Advanced Micro Devices 64-bit (AMD64) environment.</span></span>

</dd> <dt>

<span id="win64"></span><span id="WIN64"></span>

<span data-ttu-id="50ead-113"><span id="win64"></span><span id="WIN64"></span>Win64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="50ead-113"><span id="win64"></span><span id="WIN64"></span>\*\*\*\*win64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="50ead-114">Mesmo comportamento que *IA64*.</span><span class="sxs-lookup"><span data-stu-id="50ead-114">Same behavior as *ia64*.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50ead-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="50ead-115">Remarks</span></span>

<span data-ttu-id="50ead-116">A opção **/env** afeta principalmente o nível de embalagem usado para estruturas nesse ambiente.</span><span class="sxs-lookup"><span data-stu-id="50ead-116">The **/env** switch primarily affects the packing level used for structures in that environment.</span></span> <span data-ttu-id="50ead-117">Certifique-se de especificar a mesma configuração de nível de embalagem para o compilador de MIDL e o compilador do C.</span><span class="sxs-lookup"><span data-stu-id="50ead-117">Be sure you specify the same packing-level setting for both the MIDL compiler and the C compiler.</span></span>

<span data-ttu-id="50ead-118">A opção **/env** determina o nível de embalagem e outras configurações da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="50ead-118">The **/env** switch determines the packing level and other settings as follows:</span></span>

-   <span data-ttu-id="50ead-119">Quando você especifica o **Win32**, os stubs gerados usam o nível de empacotamento do C-Compiler 8 para todos os tipos envolvidos em operações remotas.</span><span class="sxs-lookup"><span data-stu-id="50ead-119">When you specify **win32**, generated stubs use C-compiler packing-level 8 for all types involved in remote operations.</span></span> <span data-ttu-id="50ead-120">Os tipos de dados [**int**](int.md) são 32 bits.</span><span class="sxs-lookup"><span data-stu-id="50ead-120">The [**int**](int.md) data types are both 32 bits.</span></span> <span data-ttu-id="50ead-121">Os ponteiros são 32 bits.</span><span class="sxs-lookup"><span data-stu-id="50ead-121">Pointers are 32 bits.</span></span>
-   <span data-ttu-id="50ead-122">Quando você especifica **IA64** ou **AMD64**, o compilador MIDL é executado em um modo de compilador cruzado para a plataforma indicada (Intel ou AMD) 64 bits.</span><span class="sxs-lookup"><span data-stu-id="50ead-122">When you specify **ia64** or **amd64**, the MIDL compiler runs in a cross-compiler mode for the indicated (Intel or AMD) 64-bit platform.</span></span> <span data-ttu-id="50ead-123">Os stubs gerados usam o nível de empacotamento do C-Compiler 8 para todos os tipos envolvidos em operações remotas.</span><span class="sxs-lookup"><span data-stu-id="50ead-123">The generated stubs use C-compiler packing-level 8 for all types involved in remote operations.</span></span> <span data-ttu-id="50ead-124">Os tipos de dados [**Long**](long.md) e [**int**](int.md) são 32 bits.</span><span class="sxs-lookup"><span data-stu-id="50ead-124">The [**long**](long.md) and [**int**](int.md) data types are 32 bits.</span></span> <span data-ttu-id="50ead-125">Os ponteiros são 64 bits.</span><span class="sxs-lookup"><span data-stu-id="50ead-125">Pointers are 64 bits.</span></span>

<span data-ttu-id="50ead-126">Os comutadores [**/align**](-align.md), [**/Pack**](-pack.md)e [**/ZP**](-zp.md) têm precedência sobre as configurações de **/env** .</span><span class="sxs-lookup"><span data-stu-id="50ead-126">The [**/align**](-align.md), [**/pack**](-pack.md), and [**/Zp**](-zp.md) switches take precedence over the **/env** settings.</span></span>

<span data-ttu-id="50ead-127">Para obter mais informações sobre o suporte de 64 bits para MIDL e RPC [, consulte Projetando interfaces compatíveis com 64 bits](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces).</span><span class="sxs-lookup"><span data-stu-id="50ead-127">For more information on 64 bit support for MIDL and RPC see [Designing 64-bit-Compatible Interfaces](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces).</span></span>

## <a name="examples"></a><span data-ttu-id="50ead-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="50ead-128">Examples</span></span>

<span data-ttu-id="50ead-129">**MIDL/Env Win32 nomedoarquivo. idl**</span><span class="sxs-lookup"><span data-stu-id="50ead-129">**midl /env win32 filename.idl**</span></span>

<span data-ttu-id="50ead-130">**MIDL/Env IA64 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="50ead-130">**midl /env ia64 filename.idl**</span></span>

<span data-ttu-id="50ead-131">**MIDL/Env AMD64 nomedoarquivo. idl**</span><span class="sxs-lookup"><span data-stu-id="50ead-131">**midl /env amd64 filename.idl**</span></span>

<span data-ttu-id="50ead-132">**MIDL/Env Win64 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="50ead-132">**midl /env win64 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="50ead-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="50ead-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50ead-134">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="50ead-134">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="50ead-135">**/Pack**</span><span class="sxs-lookup"><span data-stu-id="50ead-135">**/pack**</span></span>](-pack.md)
</dt> <dt>

[<span data-ttu-id="50ead-136">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="50ead-136">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 