---
title: atributo void
description: O tipo de base void indica um procedimento sem argumentos ou um procedimento que não retorna um valor de resultado.
ms.assetid: a3eebfe7-bf43-4bab-b87b-9188a54ab9bf
keywords:
- atributo void MIDL
topic_type:
- apiref
api_name:
- void
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b14a5ae4a2325f840d8a840cb0a1bc5283bb4a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105750831"
---
# <a name="void-attribute"></a><span data-ttu-id="88bb5-104">atributo void</span><span class="sxs-lookup"><span data-stu-id="88bb5-104">void attribute</span></span>

<span data-ttu-id="88bb5-105">O tipo de base **void** indica um procedimento sem argumentos ou um procedimento que não retorna um valor de resultado.</span><span class="sxs-lookup"><span data-stu-id="88bb5-105">The base type **void** indicates a procedure with no arguments or a procedure that does not return a result value.</span></span>

``` syntax
void function-name(parameter-list);

return-type function-name(void);

typedef [context_handle] void * context-handle-type;

return-type function-name(
    [context_handle] void * * context-handle-type
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="88bb5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88bb5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88bb5-107">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="88bb5-107">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="88bb5-108">Especifica o nome do procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="88bb5-108">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="88bb5-109">*parameter-list*</span><span class="sxs-lookup"><span data-stu-id="88bb5-109">*parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="88bb5-110">Especifica a lista de parâmetros passados para a função junto com os tipos de parâmetro associados e atributos de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="88bb5-110">Specifies the list of parameters passed to the function along with the associated parameter types and parameter attributes.</span></span>

</dd> <dt>

<span data-ttu-id="88bb5-111">*tipo de retorno*</span><span class="sxs-lookup"><span data-stu-id="88bb5-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="88bb5-112">Especifica o nome do tipo retornado pela função.</span><span class="sxs-lookup"><span data-stu-id="88bb5-112">Specifies the name of the type returned by the function.</span></span>

</dd> <dt>

<span data-ttu-id="88bb5-113">*tipo de identificador de contexto*</span><span class="sxs-lookup"><span data-stu-id="88bb5-113">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="88bb5-114">Especifica o nome do tipo que usa o atributo de **\[** [**\_ identificador de contexto**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="88bb5-114">Specifies the name of the type that takes the **\[**[**context\_handle**](context-handle.md)**\]** attribute.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88bb5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="88bb5-115">Remarks</span></span>

<span data-ttu-id="88bb5-116">O tipo de **ponteiro \* void**, que em C descreve um ponteiro genérico que pode ser convertido para representar qualquer tipo de ponteiro, é limitado em MIDL para seu uso com a palavra-chave de **\[ \_ manipulador \] de contexto** .</span><span class="sxs-lookup"><span data-stu-id="88bb5-116">The pointer type **void \***, which in C describes a generic pointer that can be cast to represent any pointer type, is limited in MIDL to its use with the **\[context\_handle\]** keyword.</span></span>

## <a name="examples"></a><span data-ttu-id="88bb5-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="88bb5-117">Examples</span></span>

``` syntax
void VoidFunc1(void); 
HRESULT VoidFunc2([in, out] short s1); 
typedef [context_handle] void * MY_CX_HNDL_TYPE; 
HRESULT InitHandle([out] MY_CX_HNDL_TYPE * ppCxHndl);
```

## <a name="see-also"></a><span data-ttu-id="88bb5-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="88bb5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88bb5-119">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="88bb5-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="88bb5-120">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="88bb5-120">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="88bb5-121">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="88bb5-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> </dl>

 

 




