---
title: atributo de identificador
description: O atributo \ Handle \ especifica um definido pelo usuário ou \ 0034; personalizado \ 0034; tipo de identificador.
ms.assetid: db5c6ea6-6081-4cea-9265-5e2f67fd8c14
keywords:
- manipular o atributo MIDL
topic_type:
- apiref
api_name:
- handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d4560de53bf3f24238e9ff96e01c74716729749
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823765"
---
# <a name="handle-attribute"></a><span data-ttu-id="4e1a0-104">atributo de identificador</span><span class="sxs-lookup"><span data-stu-id="4e1a0-104">handle attribute</span></span>

<span data-ttu-id="4e1a0-105">O \[  \] atributo Handle especifica um tipo de identificador definido pelo usuário ou "personalizado".</span><span class="sxs-lookup"><span data-stu-id="4e1a0-105">The \[**handle**\] attribute specifies a user-defined or "customized" handle type.</span></span>

``` syntax
typedef [handle] typename;  
handle_t __RPC_USER typename_bind (typename);
void __RPC_USER typename_unbind (typename, handle_t);
```

## <a name="parameters"></a><span data-ttu-id="4e1a0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e1a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e1a0-107">*TypeName*</span><span class="sxs-lookup"><span data-stu-id="4e1a0-107">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="4e1a0-108">Especifica o nome do tipo de identificador de associação definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="4e1a0-108">Specifies the name of the user-defined binding-handle type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e1a0-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e1a0-109">Remarks</span></span>

<span data-ttu-id="4e1a0-110">Os identificadores definidos pelo usuário permitem que os desenvolvedores criem identificadores que são significativos para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4e1a0-110">User-defined handles permit developers to design handles that are meaningful to the application.</span></span> <span data-ttu-id="4e1a0-111">Um identificador definido pelo usuário só pode ser definido em uma declaração de tipo, não em um Declarador de função.</span><span class="sxs-lookup"><span data-stu-id="4e1a0-111">A user-defined handle can only be defined in a type declaration, not in a function declarator.</span></span>

<span data-ttu-id="4e1a0-112">Um parâmetro de um tipo definido pelo atributo \[ **Handle** \] é usado para determinar a associação para a chamada e é transmitido para o procedimento chamado.</span><span class="sxs-lookup"><span data-stu-id="4e1a0-112">A parameter of a type defined by the \[**handle**\] attribute is used to determine the binding for the call and is transmitted to the called procedure.</span></span>

<span data-ttu-id="4e1a0-113">O usuário deve fornecer associações e desvinculação de rotinas para converter entre tipos de identificador primitivos e definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="4e1a0-113">The user must provide binding and unbinding routines to convert between primitive and user-defined handle types.</span></span> <span data-ttu-id="4e1a0-114">Dado um identificador definido pelo usuário do tipo *TypeName*, o usuário deve fornecer as rotinas *TypeName* \_ **BIND** e *TypeName* \_ **Unbind**.</span><span class="sxs-lookup"><span data-stu-id="4e1a0-114">Given a user-defined handle of type *typename*, the user must supply the routines *typename*\_**bind** and *typename*\_**unbind**.</span></span> <span data-ttu-id="4e1a0-115">Por exemplo, se o tipo de identificador definido pelo usuário for chamado myhandle, as rotinas serão nomeadas como \_ **associar** e mytratar \_ **desassociar**.</span><span class="sxs-lookup"><span data-stu-id="4e1a0-115">For example, if the user-defined handle type is named MYHANDLE, the routines are named MYHANDLE\_**bind** and MYHANDLE\_**unbind**.</span></span>

<span data-ttu-id="4e1a0-116">Se for bem-sucedida, a rotina de \_ **Associação** TypeName deverá retornar um identificador de associação primitivo válido.</span><span class="sxs-lookup"><span data-stu-id="4e1a0-116">If successful, the *typename*\_**bind** routine should return a valid primitive binding handle.</span></span> <span data-ttu-id="4e1a0-117">Se não for bem-sucedida, a rotina deverá retornar um **valor nulo**.</span><span class="sxs-lookup"><span data-stu-id="4e1a0-117">If unsuccessful, the routine should return a **NULL**.</span></span> <span data-ttu-id="4e1a0-118">Se a rotina retornar **NULL**, a  \_ rotina de **desassociar** typeName não será chamada.</span><span class="sxs-lookup"><span data-stu-id="4e1a0-118">If the routine returns **NULL**, the *typename*\_**unbind** routine will not be called.</span></span> <span data-ttu-id="4e1a0-119">Se a rotina de associação retornar um identificador de associação inválido diferente de **NULL**, o comportamento do stub será indefinido.</span><span class="sxs-lookup"><span data-stu-id="4e1a0-119">If the binding routine returns an invalid binding handle different from **NULL**, the stub behavior is undefined.</span></span>

<span data-ttu-id="4e1a0-120">Quando o procedimento remoto tem um identificador definido pelo usuário como um parâmetro ou como um identificador implícito, os stubs do cliente chamam a rotina de associação antes de chamar o procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="4e1a0-120">When the remote procedure has a user-defined handle as a parameter or as an implicit handle, the client stubs call the binding routine before calling the remote procedure.</span></span> <span data-ttu-id="4e1a0-121">Os stubs do cliente chamam a rotina de desvinculação após a chamada remota.</span><span class="sxs-lookup"><span data-stu-id="4e1a0-121">The client stubs call the unbinding routine after the remote call.</span></span>

<span data-ttu-id="4e1a0-122">No DCE IDL, um parâmetro com o \[ atributo **Handle** \] deve aparecer como o primeiro parâmetro na lista de argumentos de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="4e1a0-122">In DCE IDL, a parameter with the \[**handle**\] attribute must appear as the first parameter in the remote procedure argument list.</span></span> <span data-ttu-id="4e1a0-123">Os parâmetros subsequentes, incluindo outros \[  \] atributos de identificador, são tratados como parâmetros comuns.</span><span class="sxs-lookup"><span data-stu-id="4e1a0-123">Subsequent parameters, including other \[**handle**\] attributes, are treated as ordinary parameters.</span></span> <span data-ttu-id="4e1a0-124">A Microsoft dá suporte a uma extensão para o DCE IDL que permite que o parâmetro de identificador definido pelo usuário \[  \] apareça em posições diferentes do primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="4e1a0-124">Microsoft supports an extension to DCE IDL that allows the user-defined \[**handle**\] parameter to appear in positions other than the first parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="4e1a0-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4e1a0-125">Examples</span></span>

``` syntax
typedef [handle] struct 
{ 
    char machine[8]; 
    char nmpipe[256]; 
} h_service; 
 
handle_t __RPC_USER h_service_bind(h_service); 
void __RPC_USER h_service_unbind(h_service, handle_t);
```

## <a name="see-also"></a><span data-ttu-id="4e1a0-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e1a0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e1a0-127">Associação e identificadores</span><span class="sxs-lookup"><span data-stu-id="4e1a0-127">Binding and Handles</span></span>](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[<span data-ttu-id="4e1a0-128">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="4e1a0-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="4e1a0-129">**\_identificador implícito**</span><span class="sxs-lookup"><span data-stu-id="4e1a0-129">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="4e1a0-130">**typedef**</span><span class="sxs-lookup"><span data-stu-id="4e1a0-130">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 