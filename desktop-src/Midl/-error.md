---
title: comutador/Error
description: A opção/Error determina os tipos de erro de verificação de que os stubs gerados serão executados em tempo de execução.
ms.assetid: abd3616a-2d2c-4a7d-bf3a-c84a43387894
keywords:
- MIDL do comutador/Error
topic_type:
- apiref
api_name:
- /error
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84a56c1ae3d57ab1931ec175aa8dc9010ea6b8a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364950"
---
# <a name="error-switch"></a><span data-ttu-id="cbb4a-104">comutador/Error</span><span class="sxs-lookup"><span data-stu-id="cbb4a-104">/error switch</span></span>

<span data-ttu-id="cbb4a-105">A opção **/Error** determina os tipos de erro de verificação de que os stubs gerados serão executados em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="cbb4a-105">The **/error** switch determines the types of error checking that the generated stubs will perform at run time.</span></span>

> [!Note]  
> <span data-ttu-id="cbb4a-106">Este recurso está obsoleto e não tem mais suporte.</span><span class="sxs-lookup"><span data-stu-id="cbb4a-106">This feature is obsolete and no longer supported.</span></span> <span data-ttu-id="cbb4a-107">O uso da opção [**/robust**](-robust.md) é recomendado.</span><span class="sxs-lookup"><span data-stu-id="cbb4a-107">The use of the [**/robust**](-robust.md) switch is recommended.</span></span>

 

``` syntax
midl /error { allocation | stub_data | ref | bounds_check | none | all }
```

## <a name="switch-options"></a><span data-ttu-id="cbb4a-108">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="cbb4a-108">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="allocation"></span><span id="ALLOCATION"></span>

<span data-ttu-id="cbb4a-109"><span id="allocation"></span><span id="ALLOCATION"></span>alocação \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="cbb4a-109"><span id="allocation"></span><span id="ALLOCATION"></span>\*\*\*\*allocation\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="cbb4a-110">Verifica se [**a \_ \_ alocação de usuário MIDL**](midl-user-allocate-1.md) retorna um valor **nulo** , indicando um erro de memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="cbb4a-110">Checks whether [**midl\_user\_allocate**](midl-user-allocate-1.md) returns a **NULL** value, indicating an out-of-memory error.</span></span>

</dd> <dt>

<span id="stub_data"></span><span id="STUB_DATA"></span>

<span data-ttu-id="cbb4a-111"><span id="stub_data"></span><span id="STUB_DATA"></span>dados de stub \* \* \* \* \_</span><span class="sxs-lookup"><span data-stu-id="cbb4a-111"><span id="stub_data"></span><span id="STUB_DATA"></span>\*\*\*\*stub\_data\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="cbb4a-112">Gera um stub que captura exceções de desempacotamento no lado do servidor e as propaga de volta para o cliente.</span><span class="sxs-lookup"><span data-stu-id="cbb4a-112">Generates a stub that catches unmarshaling exceptions on the server side and propagates them back to the client.</span></span>

</dd> <dt>

<span id="ref"></span><span id="REF"></span>

<span data-ttu-id="cbb4a-113"><span id="ref"></span><span id="REF"></span>Ref \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="cbb4a-113"><span id="ref"></span><span id="REF"></span>\*\*\*\*ref\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="cbb4a-114">Gera um código que executa uma verificação em tempo de execução para garantir que nenhum ponteiro de referência **nulo** esteja sendo passado para os stubs do cliente e gere uma \_ exceção de ponteiro ref de RPC X \_ NULL \_ \_ se encontrar algum.</span><span class="sxs-lookup"><span data-stu-id="cbb4a-114">Generates code that runs a check at run time to ensure that no **NULL** reference pointers are being passed to the client stubs and raises an RPC\_X\_NULL\_REF\_POINTER exception if it finds any.</span></span>

</dd> <dt>

<span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>

<span data-ttu-id="cbb4a-115"><span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>verificação de limites \* \* \* \* \_</span><span class="sxs-lookup"><span data-stu-id="cbb4a-115"><span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>\*\*\*\*bounds\_check\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="cbb4a-116">Verifica o tamanho das matrizes em conformidade e variáveis variáveis em relação à especificação do comprimento da transmissão.</span><span class="sxs-lookup"><span data-stu-id="cbb4a-116">Checks size of conformant-varying and varying arrays against transmission length specification.</span></span>

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span data-ttu-id="cbb4a-117"><span id="none"></span><span id="NONE"></span>nenhum \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="cbb4a-117"><span id="none"></span><span id="NONE"></span>\*\*\*\*none\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="cbb4a-118">Não executa nenhuma verificação de erro.</span><span class="sxs-lookup"><span data-stu-id="cbb4a-118">Performs no error checking.</span></span>

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span data-ttu-id="cbb4a-119"><span id="all"></span><span id="ALL"></span>todos \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="cbb4a-119"><span id="all"></span><span id="ALL"></span>\*\*\*\*all\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="cbb4a-120">Executa todas as verificações de erro.</span><span class="sxs-lookup"><span data-stu-id="cbb4a-120">Performs all error checking.</span></span> <span data-ttu-id="cbb4a-121">Em vigor com o MIDL versão 5,0, essa é uma opção de compilador padrão.</span><span class="sxs-lookup"><span data-stu-id="cbb4a-121">Effective with MIDL version 5.0, this is a default compiler switch.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cbb4a-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbb4a-122">Remarks</span></span>

<span data-ttu-id="cbb4a-123">A opção **/Error** seleciona o número de verificações de erro que serão executadas pelos arquivos stub gerados.</span><span class="sxs-lookup"><span data-stu-id="cbb4a-123">The **/error** switch selects the number of error checks that the generated stub files will perform.</span></span> <span data-ttu-id="cbb4a-124">Em vigor com o MIDL versão 5,0, a configuração padrão é **/Error All**.</span><span class="sxs-lookup"><span data-stu-id="cbb4a-124">Effective with MIDL version 5.0, the default setting is **/error all**.</span></span>

<span data-ttu-id="cbb4a-125">Os erros de enumeração que são verificados (por padrão em todas as versões de MIDL) são erros de truncamento causados durante a conversão entre os tipos de **Enumeração longos** (inteiros de 32 bits) e os tipos de **Enumeração curtos** (a representação de dados de rede de [**enum**](enum.md)) e o número de identificadores em uma enumeração que excedem 32.767.</span><span class="sxs-lookup"><span data-stu-id="cbb4a-125">The enum errors that are checked (by default in all versions of MIDL) are truncation errors caused when converting between **long enum** types (32-bit integers) and **short enum** types (the network-data representation of [**enum**](enum.md)), and the number of identifiers in an enumeration exceeding 32,767.</span></span>

<span data-ttu-id="cbb4a-126">A verificação de erro de acesso à memória (também por padrão em todas as versões de MIDL) é para ponteiros que excedem o final do buffer no código de marshaling e para matrizes compatíveis cujo tamanho é menor que zero.</span><span class="sxs-lookup"><span data-stu-id="cbb4a-126">The memory-access error checking (also by default in all versions of MIDL) is for pointers that exceed the end of the buffer in marshaling code and for conformant arrays whose size is less than zero.</span></span> <span data-ttu-id="cbb4a-127">Use o sinalizador de **\_ verificação de limites de/Error** para verificar outros limites de matriz inválidos.</span><span class="sxs-lookup"><span data-stu-id="cbb4a-127">Use the **/error bounds\_check** flag to check for other invalid array bounds.</span></span>

<span data-ttu-id="cbb4a-128">Quando você especifica a **alocação/Error**, os stubs incluem o código que gera uma exceção quando o [**usuário de MIDL \_ \_ aloca**](midl-user-allocate-1.md) retorna 0.</span><span class="sxs-lookup"><span data-stu-id="cbb4a-128">When you specify **/error allocation**, the stubs include code that raises an exception when [**midl\_user\_allocate**](midl-user-allocate-1.md) returns 0.</span></span>

<span data-ttu-id="cbb4a-129">A opção de **\_ dados stub/Error** impede que os dados do cliente falhem no servidor durante o desempacotamento, fornecendo efetivamente um método mais robusto para lidar com a operação de desempacotamento.</span><span class="sxs-lookup"><span data-stu-id="cbb4a-129">The **/error stub\_data** option prevents client data from crashing the server during unmarshaling, effectively providing a more robust method of handling the unmarshaling operation.</span></span>

<span data-ttu-id="cbb4a-130">Em vigor com o WindowsÂ 2000, o mecanismo de marshaling de NDR de tempo de execução subjacente executa a maioria dessas verificações.</span><span class="sxs-lookup"><span data-stu-id="cbb4a-130">Effective with WindowsÂ 2000, the underlying run-time NDR marshaling engine performs most of these checks.</span></span> <span data-ttu-id="cbb4a-131">Isso significa que, se você estiver usando um dos modos totalmente interpretados ([**/Oi**](-oi.md), **/OIF**) de geração de stub, a escolha de opções de verificação de erros diferentes não terá um efeito marcado no desempenho.</span><span class="sxs-lookup"><span data-stu-id="cbb4a-131">This means that if you are using one of the fully-interpreted modes ([**/Oi**](-oi.md), **/Oif**) of stub generation, choosing different error checking options will not have a marked effect on performance.</span></span>

## <a name="examples"></a><span data-ttu-id="cbb4a-132">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cbb4a-132">Examples</span></span>

<span data-ttu-id="cbb4a-133">**nome de arquivo de alocação/Error de MIDL. idl**</span><span class="sxs-lookup"><span data-stu-id="cbb4a-133">**midl /error allocation filename.idl**</span></span>

<span data-ttu-id="cbb4a-134">**MIDL/Error None filename. idl**</span><span class="sxs-lookup"><span data-stu-id="cbb4a-134">**midl /error none filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="cbb4a-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbb4a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbb4a-136">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="cbb4a-136">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="cbb4a-137">**/robust**</span><span class="sxs-lookup"><span data-stu-id="cbb4a-137">**/robust**</span></span>](-robust.md)
</dt> </dl>

 

 




