---
title: implicit_handle atributo
description: O atributo \ \_ identificador \ implícito \ ACF especifica o identificador usado para funções que não incluem um identificador explícito como um parâmetro de procedimento.
ms.assetid: 09c17473-87b5-4fd6-beb9-3d9b7bc82d8c
keywords:
- implicit_handle do atributo MIDL
topic_type:
- apiref
api_name:
- implicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22f410fa048a27e1f7626690e6308de4c1a31c2a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823174"
---
# <a name="implicit_handle-attribute"></a><span data-ttu-id="481f7-104">\_atributo de identificador implícito</span><span class="sxs-lookup"><span data-stu-id="481f7-104">implicit\_handle attribute</span></span>

<span data-ttu-id="481f7-105">O atributo de ACF **\[ \_ identificador \] implícito** especifica o identificador usado para funções que não incluem um identificador explícito como um parâmetro de procedimento.</span><span class="sxs-lookup"><span data-stu-id="481f7-105">The **\[implicit\_handle\]** ACF attribute specifies the handle used for functions that do not include an explicit handle as a procedure parameter.</span></span>

``` syntax
implicit_handle(handle-type handle-name)
```

## <a name="parameters"></a><span data-ttu-id="481f7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="481f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="481f7-107">*tipo de identificador*</span><span class="sxs-lookup"><span data-stu-id="481f7-107">*handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="481f7-108">Especifica o tipo de dados de identificador, como o tipo de base [**Handle \_ t**](handle-t.md) ou um tipo de identificador definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="481f7-108">Specifies the handle data type, such as the base type [**handle\_t**](handle-t.md) or a user-defined handle type.</span></span>

</dd> <dt>

<span data-ttu-id="481f7-109">*nome do identificador*</span><span class="sxs-lookup"><span data-stu-id="481f7-109">*handle-name*</span></span> 
</dt> <dd>

<span data-ttu-id="481f7-110">Especifica o nome do identificador.</span><span class="sxs-lookup"><span data-stu-id="481f7-110">Specifies the name of the handle.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="481f7-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="481f7-111">Remarks</span></span>

<span data-ttu-id="481f7-112">O identificador especificado pelo atributo **\[ \_ identificador \] implícito** é usado de maneiras diferentes, dependendo da natureza do procedimento.</span><span class="sxs-lookup"><span data-stu-id="481f7-112">The handle specified by the **\[implicit\_handle\]** attribute is used in different ways depending on the nature of the procedure.</span></span> <span data-ttu-id="481f7-113">Se o procedimento for remoto, o identificador será usado como o identificador de associação para a chamada remota.</span><span class="sxs-lookup"><span data-stu-id="481f7-113">If the procedure is remote, the handle will be used as the binding handle for the remote call.</span></span> <span data-ttu-id="481f7-114">O identificador implícito também pode ser usado para estabelecer uma associação inicial para uma função que usa um identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="481f7-114">The implicit handle may also be used to establish an initial binding for a function that uses a context handle.</span></span> <span data-ttu-id="481f7-115">Se o procedimento for um procedimento de serialização, o identificador será usado como um identificador de serialização que controla a operação.</span><span class="sxs-lookup"><span data-stu-id="481f7-115">If the procedure is a serializing procedure, the handle is used as a serializing handle controlling the operation.</span></span> <span data-ttu-id="481f7-116">No caso do tipo serialização, o identificador é usado como o identificador de serialização para todos os tipos serializados.</span><span class="sxs-lookup"><span data-stu-id="481f7-116">In the case of type serialization, the handle is used as the serialization handle for all the serialized types.</span></span>

<span data-ttu-id="481f7-117">O atributo **\[ \_ identificador \] implícito** especifica uma variável global que contém um identificador usado por qualquer função que precise de identificadores implícitos.</span><span class="sxs-lookup"><span data-stu-id="481f7-117">The **\[implicit\_handle\]** attribute specifies a global variable that contains a handle used by any function needing implicit handles.</span></span>

<span data-ttu-id="481f7-118">O tipo de identificador de associação implícita deve ser um [**identificador \_ t**](handle-t.md) (ou um tipo com base no **identificador \_ t**) ou um tipo de identificador definido pelo usuário especificado com o atributo [**Handle**](handle.md) .</span><span class="sxs-lookup"><span data-stu-id="481f7-118">The implicit binding handle type must be either [**handle\_t**](handle-t.md) (or a type based on **handle\_t**) or a user-defined handle type specified with the [**handle**](handle.md) attribute.</span></span> <span data-ttu-id="481f7-119">O identificador de serialização implícita deve ser um tipo com base no **identificador \_ t**.</span><span class="sxs-lookup"><span data-stu-id="481f7-119">The implicit serializing handle must be a type based on **handle\_t**.</span></span>

<span data-ttu-id="481f7-120">Se o tipo de identificador implícito não estiver definido no arquivo IDL ou em todos os arquivos incluídos e importados pelo arquivo IDL para o computador MIDL, você deverá fornecer o arquivo que contém a definição de tipo de identificador ao compilar os stubs.</span><span class="sxs-lookup"><span data-stu-id="481f7-120">If the implicit handle type is not defined in the IDL file or in any files included and imported by the IDL file for the MIDL computer, you must supply the file containing the handle-type definition when you compile the stubs.</span></span> <span data-ttu-id="481f7-121">Use a instrução ACF [**include**](include.md) para incluir o arquivo que contém a definição do tipo de identificador.</span><span class="sxs-lookup"><span data-stu-id="481f7-121">Use the ACF [**include**](include.md) statement to include the file containing the handle-type definition.</span></span>

<span data-ttu-id="481f7-122">O atributo de **\[ \_ identificador \] implícito** pode ocorrer uma vez, no máximo.</span><span class="sxs-lookup"><span data-stu-id="481f7-122">The **\[implicit\_handle\]** attribute can occur once, at most.</span></span> <span data-ttu-id="481f7-123">O atributo **\[ \_ identificador \] implícito** só poderá ocorrer [**\[ \_ \]**](auto-handle.md) se os atributos identificador automático e [**\[ \_ identificador \] explícito**](explicit-handle.md) não ocorrerem.</span><span class="sxs-lookup"><span data-stu-id="481f7-123">The **\[implicit\_handle\]** attribute can occur only if the [**\[auto\_handle\]**](auto-handle.md) and [**\[explicit\_handle\]**](explicit-handle.md) attributes do not occur.</span></span>

## <a name="examples"></a><span data-ttu-id="481f7-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="481f7-124">Examples</span></span>

``` syntax
/* ACF file */ 
[
    implicit_handle(handle_t hMyHandle)
] 
interface iface
{ 
    // Attribute configuration statements
}
```

## <a name="see-also"></a><span data-ttu-id="481f7-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="481f7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="481f7-126">Arquivo de configuração de aplicativo (ACF)</span><span class="sxs-lookup"><span data-stu-id="481f7-126">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="481f7-127">**\_identificador automático**</span><span class="sxs-lookup"><span data-stu-id="481f7-127">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="481f7-128">**\_identificador explícito**</span><span class="sxs-lookup"><span data-stu-id="481f7-128">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="481f7-129">**lidar com \_ t**</span><span class="sxs-lookup"><span data-stu-id="481f7-129">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="481f7-130">**incluir**</span><span class="sxs-lookup"><span data-stu-id="481f7-130">**include**</span></span>](include.md)
</dt> </dl>

 

 




