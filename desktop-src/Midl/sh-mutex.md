---
title: palavra-chave sh_mutex
description: A \_ palavra-chave \ sh mutex \ especifica que o objeto do sistema é um identificador para um mutex.
keywords:
- MIDL de palavra-chave sh_mutex
topic_type:
- apiref
api_name:
- sh_mutex
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 8616ded29d1d8c106af21e6cd1252535f4da8457
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105795517"
---
# <a name="sh_mutex-keyword"></a><span data-ttu-id="43d03-104">\_palavra-chave sh mutex</span><span class="sxs-lookup"><span data-stu-id="43d03-104">sh\_mutex keyword</span></span>

<span data-ttu-id="43d03-105">A palavra-chave **sh \_ mutex** especifica que um `system_handle` mantém um identificador para um mutex.</span><span class="sxs-lookup"><span data-stu-id="43d03-105">The **sh\_mutex** keyword specifies that a `system_handle` holds a handle to a mutex.</span></span>

``` syntax
[system_handle(sh_mutex)]

[system_handle(sh_mutex, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="43d03-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43d03-106">Parameters</span></span>

<span data-ttu-id="43d03-107">Essa palavra-chave é um parâmetro para [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="43d03-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="43d03-108">A documentação [**system_handle**](system-handle.md) também contém detalhes sobre o uso opcional do parâmetro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="43d03-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="43d03-109">O comportamento padrão é de acordo com as `DUPLICATE_SAME_ACCESS` especificações de [função **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="43d03-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="43d03-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="43d03-110">Remarks</span></span>

<span data-ttu-id="43d03-111">Para usar essa palavra-chave com o `system_handle` atributo, o `-target` sinalizador deve ser definido como `NT100` (ou superior) durante a execução de midl.exe.</span><span class="sxs-lookup"><span data-stu-id="43d03-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="43d03-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="43d03-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT WaitOnThisMutex([in, system_handle(sh_mutex)] HANDLE mutex);
}
```

## <a name="requirements"></a><span data-ttu-id="43d03-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43d03-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="43d03-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43d03-114">Minimum supported client</span></span> | <span data-ttu-id="43d03-115">Atualização de aniversário do Windows 10 (versão 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="43d03-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="43d03-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43d03-116">Minimum supported server</span></span> | <span data-ttu-id="43d03-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="43d03-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="43d03-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="43d03-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43d03-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="43d03-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="43d03-120">Objetos mutex</span><span class="sxs-lookup"><span data-stu-id="43d03-120">Mutex Objects</span></span>](../sync/mutex-objects.md)
</dt> <dt>

[<span data-ttu-id="43d03-121">Segurança do objeto de sincronização e direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="43d03-121">Synchronization Object Security and Access Rights</span></span>](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="43d03-122">Função **CreateMutex**</span><span class="sxs-lookup"><span data-stu-id="43d03-122">**CreateMutex** function</span></span>](/windows/win32/api/synchapi/nf-synchapi-createmutexa)
</dt> <dt>

[<span data-ttu-id="43d03-123">Função **CreateMutexEx**</span><span class="sxs-lookup"><span data-stu-id="43d03-123">**CreateMutexEx** function</span></span>](/windows/win32/api/synchapi/nf-synchapi-createmutexexa)
</dt> </dl>