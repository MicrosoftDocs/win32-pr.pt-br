---
title: enable_allocate atributo
description: O atributo \ Enable \_ ALLOCATE \ ACF especifica que o código stub do servidor deve habilitar o ambiente de gerenciamento de memória de stub.
ms.assetid: 3a232a82-f114-4d8c-8b71-cf8860c77db3
keywords:
- enable_allocate do atributo MIDL
topic_type:
- apiref
api_name:
- enable_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f43e8c10592fcf99ea294327c400c579ce45bf6b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084476"
---
# <a name="enable_allocate-attribute"></a><span data-ttu-id="950ec-104">Habilitar \_ atributo de alocação</span><span class="sxs-lookup"><span data-stu-id="950ec-104">enable\_allocate attribute</span></span>

<span data-ttu-id="950ec-105">O atributo **\[ habilitar \_ alocação \]** ACF especifica que o código stub do servidor deve habilitar o ambiente de gerenciamento de memória de stub.</span><span class="sxs-lookup"><span data-stu-id="950ec-105">The **\[enable\_allocate\]** ACF attribute specifies that the server stub code should enable the stub memory management environment.</span></span>

> [!Note]  
> <span data-ttu-id="950ec-106">O atributo **\[ habilitar \_ alocação \]** é obsoleto e não tem mais suporte.</span><span class="sxs-lookup"><span data-stu-id="950ec-106">The **\[enable\_allocate\]** attribute is obsolete and is no longer supported.</span></span>

 

``` syntax
[
    enable_allocate
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a><span data-ttu-id="950ec-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="950ec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="950ec-108">*lista de atributos opcionais*</span><span class="sxs-lookup"><span data-stu-id="950ec-108">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="950ec-109">Especifica uma lista de zero ou mais atributos MIDL adicionais.</span><span class="sxs-lookup"><span data-stu-id="950ec-109">Specifies a list of zero or more additional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="950ec-110">*nome da interface*</span><span class="sxs-lookup"><span data-stu-id="950ec-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="950ec-111">O nome da interface à qual o atributo de **\[ habilitação de \_ \] imrevestimento** será aplicado.</span><span class="sxs-lookup"><span data-stu-id="950ec-111">The name of the interface to which the **\[enable\_allcoate\]** attribute will be applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="950ec-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="950ec-112">Remarks</span></span>

<span data-ttu-id="950ec-113">No modo padrão, o stub de servidor habilita o ambiente de memória somente quando o atributo de **\[ \_ alocação \] de habilitação** é usado.</span><span class="sxs-lookup"><span data-stu-id="950ec-113">In default mode, the server stub enables the memory environment only when the **\[enable\_allocate\]** attribute is used.</span></span> <span data-ttu-id="950ec-114">O ambiente de gerenciamento de memória deve ser habilitado para que a memória possa ser alocada usando [**RpcSmAllocate**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate).</span><span class="sxs-lookup"><span data-stu-id="950ec-114">The memory management environment must be enabled before memory can be allocated using [**RpcSmAllocate**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate).</span></span> <span data-ttu-id="950ec-115">No modo **uso** (quando você compila usando a opção [**/OSF**](-osf.md) ), o stub habilita esse ambiente automaticamente ou sob solicitação quando o atributo de **\[ \_ alocação \] de habilitação** é usado.</span><span class="sxs-lookup"><span data-stu-id="950ec-115">In **osf** mode (when you compile using the [**/osf**](-osf.md) switch), the stub enables this environment automatically, or on request when the **\[enable\_allocate\]** attribute is used.</span></span>

<span data-ttu-id="950ec-116">O stub do lado do cliente pode ser sensível ao ambiente de gerenciamento de memória do **RPCSS** .</span><span class="sxs-lookup"><span data-stu-id="950ec-116">The client side stub may be sensitive to the **Rpcss** memory management environment.</span></span> <span data-ttu-id="950ec-117">Se um stub de cliente confidencial for executado quando o pacote **RPCSS** estiver desabilitado, os alocadores/desalocadores de usuário padrão serão chamados (por exemplo, o [ \_ usuário MIDL \_ alocar](/windows/desktop/Rpc/the-midl-user-allocate-function)o /  [ \_ usuário MIDL \_ gratuito](/windows/desktop/Rpc/the-midl-user-free-function)).</span><span class="sxs-lookup"><span data-stu-id="950ec-117">If a sensitive client stub is executed when the **Rpcss** package is disabled, the default user allocator/deallocators are called (for example, [midl\_user\_allocate](/windows/desktop/Rpc/the-midl-user-allocate-function)/ [midl\_user\_free](/windows/desktop/Rpc/the-midl-user-free-function)).</span></span> <span data-ttu-id="950ec-118">Quando habilitado, o pacote **RPCSS** usa o par de alocador/desalocador do pacote.</span><span class="sxs-lookup"><span data-stu-id="950ec-118">When enabled, the **Rpcss** package uses the allocator/deallocator pair from the package.</span></span> <span data-ttu-id="950ec-119">No modo padrão, o cliente é confidencial somente quando o atributo **\[ habilitar \_ alocação \]** é usado.</span><span class="sxs-lookup"><span data-stu-id="950ec-119">In the default mode, the client is sensitive only when the **\[enable\_allocate\]** attribute is used.</span></span> <span data-ttu-id="950ec-120">Normalmente, o stub do lado do cliente opera no ambiente desabilitado.</span><span class="sxs-lookup"><span data-stu-id="950ec-120">Typically, the client side stub operates in the disabled environment.</span></span> <span data-ttu-id="950ec-121">No modo **uso** (quando você compila usando a opção [**/OSF**](-osf.md) ), o cliente sempre é sensível ao ambiente de gerenciamento de memória do **RPCSS** e, portanto, o atributo **\[ habilitar \_ alocação \]** não afetará os stubs do cliente.</span><span class="sxs-lookup"><span data-stu-id="950ec-121">In **osf** mode (when you compile using the [**/osf**](-osf.md) switch), the client is always sensitive to the **Rpcss** memory management environment and, therefore, the **\[enable\_allocate\]** attribute will not affect the client stubs.</span></span>

## <a name="see-also"></a><span data-ttu-id="950ec-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="950ec-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="950ec-123">Arquivo de configuração de aplicativo (ACF)</span><span class="sxs-lookup"><span data-stu-id="950ec-123">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="950ec-124">\_alocar usuário de MIDL \_</span><span class="sxs-lookup"><span data-stu-id="950ec-124">midl\_user\_allocate</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="950ec-125">usuário de MIDL \_ \_ gratuito</span><span class="sxs-lookup"><span data-stu-id="950ec-125">midl\_user\_free</span></span>](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[<span data-ttu-id="950ec-126">**/osf**</span><span class="sxs-lookup"><span data-stu-id="950ec-126">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="950ec-127">RpcSmDisableAllocate</span><span class="sxs-lookup"><span data-stu-id="950ec-127">RpcSmDisableAllocate</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmdisableallocate)
</dt> <dt>

[<span data-ttu-id="950ec-128">RpcSmEnableAllocate</span><span class="sxs-lookup"><span data-stu-id="950ec-128">RpcSmEnableAllocate</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmenableallocate)
</dt> <dt>

[<span data-ttu-id="950ec-129">RpcSmFree</span><span class="sxs-lookup"><span data-stu-id="950ec-129">RpcSmFree</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree)
</dt> </dl>

 

 