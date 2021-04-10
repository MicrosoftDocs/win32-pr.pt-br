---
title: RPC_IF_HANDLE (rpcdce. h)
description: O RPC \_ se o \_ tipo de dados de identificador declara um identificador de interface.
ms.assetid: a85f3a44-7cdf-421f-a1e4-c67a9dd0c54d
keywords:
- RPC_IF_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9590973d5ae1e82d89d6151e224b771d9f55ecc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918913"
---
# <a name="rpc_if_handle"></a><span data-ttu-id="d2b7c-104">RPC \_ se o \_ identificador</span><span class="sxs-lookup"><span data-stu-id="d2b7c-104">RPC\_IF\_HANDLE</span></span>

<span data-ttu-id="d2b7c-105">O **RPC \_ se \_** o tipo de dados de identificador declara um identificador de interface.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-105">The **RPC\_IF\_HANDLE** data type declares an interface handle.</span></span>


```C++
typedef void __RPC_FAR* RPC_IF_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="d2b7c-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2b7c-106">Remarks</span></span>

<span data-ttu-id="d2b7c-107">A biblioteca de tempo de execução RPC usa identificadores de interface para acessar a estrutura de dados de especificação de interface.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-107">The RPC run-time library uses interface handles to access the interface-specification data structure.</span></span> <span data-ttu-id="d2b7c-108">O compilador MIDL cria automaticamente uma estrutura de dados de especificação de interface de cada arquivo IDL e cria uma variável global do tipo RPC \_ se \_ o identificador da especificação da interface.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-108">The MIDL compiler automatically creates an interface-specification data structure from each IDL file and creates a global variable of type RPC\_IF\_HANDLE for the interface specification.</span></span>

<span data-ttu-id="d2b7c-109">O compilador MIDL inclui um identificador de interface em cada arquivo de cabeçalho gerado para a interface.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-109">The MIDL compiler includes an interface handle in each header file generated for the interface.</span></span> <span data-ttu-id="d2b7c-110">As funções que exigem a especificação da interface como um parâmetro mostram um tipo de dados de **RPC, \_ se houver \_ identificador**.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-110">Functions requiring the interface specification as a parameter show a data type of **RPC\_IF\_HANDLE**.</span></span> <span data-ttu-id="d2b7c-111">A forma de cada nome de identificador de interface é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="d2b7c-111">The form of each interface handle name is as follows:</span></span>

-   <span data-ttu-id="d2b7c-112">*If-name* \_ ClientIfHandle (para o cliente)</span><span class="sxs-lookup"><span data-stu-id="d2b7c-112">*if-name*\_ClientIfHandle (for the client)</span></span>
-   <span data-ttu-id="d2b7c-113">*If-name* \_ ServerIfHandle (para o servidor)</span><span class="sxs-lookup"><span data-stu-id="d2b7c-113">*if-name*\_ServerIfHandle (for the server)</span></span>

<span data-ttu-id="d2b7c-114">A parte *If-name* especifica o identificador de interface no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-114">The *if-name* part specifies the interface identifier in the IDL file.</span></span>

<span data-ttu-id="d2b7c-115">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d2b7c-115">For example:</span></span>

<span data-ttu-id="d2b7c-116">Olá \_ ClientIfHandle</span><span class="sxs-lookup"><span data-stu-id="d2b7c-116">hello\_ClientIfHandle</span></span>

<span data-ttu-id="d2b7c-117">Olá \_ ServerIfHandle</span><span class="sxs-lookup"><span data-stu-id="d2b7c-117">hello\_ServerIfHandle</span></span>

> [!Note]  
> <span data-ttu-id="d2b7c-118">O comprimento máximo do nome do identificador de interface é 31 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-118">The maximum length of the interface handle name is 31 characters.</span></span>

 

<span data-ttu-id="d2b7c-119">Como as \_ partes "ClientIfHandle" e " \_ ServerIfHandle" dos nomes exigem 15 caracteres, o elemento *If-name* não pode ter mais de 16 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-119">Because the "\_ClientIfHandle" and "\_ServerIfHandle" parts of the names require 15 characters, the *if-name* element can be no more than 16 characters long.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2b7c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2b7c-120">Requirements</span></span>



| <span data-ttu-id="d2b7c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2b7c-121">Requirement</span></span> | <span data-ttu-id="d2b7c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d2b7c-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2b7c-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2b7c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d2b7c-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d2b7c-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d2b7c-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2b7c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d2b7c-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d2b7c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d2b7c-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d2b7c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2b7c-128"><dt>Rpcdce. h (incluir RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d2b7c-128"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



 

 





