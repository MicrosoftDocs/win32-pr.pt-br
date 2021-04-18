---
title: palavra-chave sh_semaphore
description: A \_ palavra-chave \ sh Semaphore \ especifica que o objeto do sistema é um identificador para um semáforo.
keywords:
- MIDL de palavra-chave sh_semaphore
topic_type:
- apiref
api_name:
- sh_semaphore
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 2a5c33e4c44b67e3106a48cde244abaf13f41ad5
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "105802177"
---
# <a name="sh_semaphore-keyword"></a><span data-ttu-id="9dc4e-104">SH \_ palavra-chave Semaphore</span><span class="sxs-lookup"><span data-stu-id="9dc4e-104">sh\_semaphore keyword</span></span>

<span data-ttu-id="9dc4e-105">A palavra-chave **sh \_ Semaphore** especifica que um `system_handle` contém um identificador para um semáforo.</span><span class="sxs-lookup"><span data-stu-id="9dc4e-105">The **sh\_semaphore** keyword specifies that a `system_handle` holds a handle to a semaphore.</span></span>

``` syntax
[system_handle(sh_semaphore)]

[system_handle(sh_semaphore, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="9dc4e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9dc4e-106">Parameters</span></span>

<span data-ttu-id="9dc4e-107">Essa palavra-chave é um parâmetro para [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="9dc4e-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="9dc4e-108">A documentação [**system_handle**](system-handle.md) também contém detalhes sobre o uso opcional do parâmetro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="9dc4e-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="9dc4e-109">O comportamento padrão é de acordo com as `DUPLICATE_SAME_ACCESS` especificações de [função **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="9dc4e-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dc4e-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="9dc4e-110">Remarks</span></span>

<span data-ttu-id="9dc4e-111">Para usar essa palavra-chave com o `system_handle` atributo, o `-target` sinalizador deve ser definido como `NT100` (ou superior) durante a execução de midl.exe.</span><span class="sxs-lookup"><span data-stu-id="9dc4e-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="9dc4e-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9dc4e-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT SignalThisSemaphore([in, system_handle(sh_semaphore)] HANDLE semaphore);
}
```

## <a name="requirements"></a><span data-ttu-id="9dc4e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9dc4e-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="9dc4e-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9dc4e-114">Minimum supported client</span></span> | <span data-ttu-id="9dc4e-115">Atualização de aniversário do Windows 10 (versão 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="9dc4e-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="9dc4e-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9dc4e-116">Minimum supported server</span></span> | <span data-ttu-id="9dc4e-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="9dc4e-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="9dc4e-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="9dc4e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dc4e-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="9dc4e-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="9dc4e-120">Objetos de semáforo</span><span class="sxs-lookup"><span data-stu-id="9dc4e-120">Semaphore Objects</span></span>](../sync/semaphore-objects.md)
</dt> <dt>

[<span data-ttu-id="9dc4e-121">Segurança do objeto de sincronização e direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="9dc4e-121">Synchronization Object Security and Access Rights</span></span>](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="9dc4e-122">Função **CreateSemaphore**</span><span class="sxs-lookup"><span data-stu-id="9dc4e-122">**CreateSemaphore** function</span></span>](/windows/win32/api/winbase/nf-winbase-createsemaphorea)
</dt> <dt>

[<span data-ttu-id="9dc4e-123">Função **CreateSemaphoreEx**</span><span class="sxs-lookup"><span data-stu-id="9dc4e-123">**CreateSemaphoreEx** function</span></span>](/windows/win32/api/winbase/nf-winbase-createsemaphoreexa)
</dt> </dl>
