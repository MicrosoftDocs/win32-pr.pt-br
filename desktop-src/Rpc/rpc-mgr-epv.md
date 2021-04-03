---
title: RPC_MGR_EPV (rpcdce. h)
description: O tipo de dados Gerenciador de RPC \_ \_ EPV define um vetor de ponto de entrada de Gerenciador.
ms.assetid: 396e76de-065f-471e-ade9-34770b16a958
keywords:
- RPC_MGR_EPV RPC
topic_type:
- apiref
api_name:
- RPC_MGR_EPV
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 549ca4b5245b12bda07b46407041a01175955693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644328"
---
# <a name="rpc_mgr_epv"></a><span data-ttu-id="dea10-104">Gerenciador de RPC \_ \_ EPV</span><span class="sxs-lookup"><span data-stu-id="dea10-104">RPC\_MGR\_EPV</span></span>

<span data-ttu-id="dea10-105">O tipo de dados Gerenciador de **RPC \_ \_ EPV** define um vetor de ponto de entrada de Gerenciador.</span><span class="sxs-lookup"><span data-stu-id="dea10-105">The data type **RPC\_MGR\_EPV** defines a manager entry-point vector.</span></span>

``` syntax
typedef void RPC_MGR_EPV;
typedef _if-name_SERVER-EPV {
  return-type (* Functionname)  (param-list);
...  //one entry for each function in IDL file
} if-name_SERVER_EPV:
```

## <a name="members"></a><span data-ttu-id="dea10-106">Membros</span><span class="sxs-lookup"><span data-stu-id="dea10-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="dea10-107"><span id="if-name"></span><span id="IF-NAME"></span>**If-name**</span><span class="sxs-lookup"><span data-stu-id="dea10-107"><span id="if-name"></span><span id="IF-NAME"></span>**if-name**</span></span>
</dt> <dd>

<span data-ttu-id="dea10-108">Especifica o nome da interface</span><span class="sxs-lookup"><span data-stu-id="dea10-108">Specifies the name of the interface</span></span>

</dd> <dt>

<span data-ttu-id="dea10-109"><span id="return-type"></span><span id="RETURN-TYPE"></span>**tipo de retorno**</span><span class="sxs-lookup"><span data-stu-id="dea10-109"><span id="return-type"></span><span id="RETURN-TYPE"></span>**return-type**</span></span>
</dt> <dd>

<span data-ttu-id="dea10-110">Especifica o tipo retornado pela função **FunctionName** indicada no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="dea10-110">Specifies the type returned by the function **Functionname** indicated in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="dea10-111"><span id="Functionname"></span><span id="functionname"></span><span id="FUNCTIONNAME"></span>**FunctionName**</span><span class="sxs-lookup"><span data-stu-id="dea10-111"><span id="Functionname"></span><span id="functionname"></span><span id="FUNCTIONNAME"></span>**Functionname**</span></span>
</dt> <dd>

<span data-ttu-id="dea10-112">Especifica o nome da função indicada no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="dea10-112">Specifies the name of the function indicated in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="dea10-113"><span id="param-list"></span><span id="PARAM-LIST"></span>**parâmetro-lista**</span><span class="sxs-lookup"><span data-stu-id="dea10-113"><span id="param-list"></span><span id="PARAM-LIST"></span>**param-list**</span></span>
</dt> <dd>

<span data-ttu-id="dea10-114">Especifica os parâmetros indicados para a função **FunctionName** no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="dea10-114">Specifies the parameters indicated for the function **Functionname** in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dea10-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="dea10-115">Remarks</span></span>

<span data-ttu-id="dea10-116">O vetor de ponto de entrada do Gerenciador (EPV) é uma matriz de ponteiros de função.</span><span class="sxs-lookup"><span data-stu-id="dea10-116">The manager entry-point vector (EPV) is an array of function pointers.</span></span> <span data-ttu-id="dea10-117">A matriz contém ponteiros para as implementações das funções especificadas no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="dea10-117">The array contains pointers to the implementations of the functions specified in the IDL file.</span></span> <span data-ttu-id="dea10-118">O número de elementos na matriz é definido como o número de funções especificadas no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="dea10-118">The number of elements in the array is set to the number of functions specified in the IDL file.</span></span> <span data-ttu-id="dea10-119">Um aplicativo também pode ter vários EPVs, representando várias implementações das funções especificadas na interface.</span><span class="sxs-lookup"><span data-stu-id="dea10-119">An application can also have multiple EPVs, representing multiple implementations of the functions specified in the interface.</span></span>

<span data-ttu-id="dea10-120">O compilador MIDL gera um tipo de dados **EPV** padrão chamado \* If-name \***\_ Server \_ EPV**, em que *If-name* especifica o identificador de interface no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="dea10-120">The MIDL compiler generates a default **EPV** data type named \*if-name\***\_SERVER\_EPV**, where *if-name* specifies the interface identifier in the IDL file.</span></span> <span data-ttu-id="dea10-121">O compilador MIDL inicializa esse **EPV** padrão para conter ponteiros de função para cada um dos procedimentos especificados no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="dea10-121">The MIDL compiler initializes this default **EPV** to contain function pointers for each of the procedures specified in the IDL file.</span></span>

<span data-ttu-id="dea10-122">Quando o servidor oferece várias implementações da mesma interface, o aplicativo de servidor deve declarar e inicializar uma variável do tipo *If-name \* \* \* \_ Server \_ EPV*\* para cada implementação da interface.</span><span class="sxs-lookup"><span data-stu-id="dea10-122">When the server offers multiple implementations of the same interface, the server application must declare and initialize one variable of type *if-name\*\*\*\_SERVER\_EPV*\* for each implementation of the interface.</span></span> <span data-ttu-id="dea10-123">Cada **EPV** deve conter um ponto de entrada (ponteiro de função) para cada procedimento definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="dea10-123">Each **EPV** must contain one entry point (function pointer) for each procedure defined in the IDL file.</span></span>

## <a name="requirements"></a><span data-ttu-id="dea10-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dea10-124">Requirements</span></span>



| <span data-ttu-id="dea10-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="dea10-125">Requirement</span></span> | <span data-ttu-id="dea10-126">Valor</span><span class="sxs-lookup"><span data-stu-id="dea10-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dea10-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dea10-127">Minimum supported client</span></span><br/> | <span data-ttu-id="dea10-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dea10-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="dea10-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dea10-129">Minimum supported server</span></span><br/> | <span data-ttu-id="dea10-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dea10-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dea10-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dea10-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="dea10-132"><dt>Rpcdce. h (incluir RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dea10-132"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dea10-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="dea10-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dea10-134">**RpcServerRegisterIf**</span><span class="sxs-lookup"><span data-stu-id="dea10-134">**RpcServerRegisterIf**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> <dt>

[<span data-ttu-id="dea10-135">**RpcServerRegisterIf2**</span><span class="sxs-lookup"><span data-stu-id="dea10-135">**RpcServerRegisterIf2**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)
</dt> <dt>

[<span data-ttu-id="dea10-136">**RpcServerRegisterIfEx**</span><span class="sxs-lookup"><span data-stu-id="dea10-136">**RpcServerRegisterIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)
</dt> <dt>

[<span data-ttu-id="dea10-137">**RpcServerUnregisterIf**</span><span class="sxs-lookup"><span data-stu-id="dea10-137">**RpcServerUnregisterIf**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)
</dt> <dt>

[<span data-ttu-id="dea10-138">**RpcServerUnregisterIfEx**</span><span class="sxs-lookup"><span data-stu-id="dea10-138">**RpcServerUnregisterIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex)
</dt> </dl>

 

 





