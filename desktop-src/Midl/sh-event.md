---
title: palavra-chave sh_event
description: A \_ palavra-chave \ sh Event \ especifica que o objeto do sistema é um identificador para um evento.
keywords:
- MIDL de palavra-chave sh_event
topic_type:
- apiref
api_name:
- sh_event
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 1a9b6dc7cc9dc4de4abd5dcc88a53588167db59d
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "105792911"
---
# <a name="sh_event-keyword"></a><span data-ttu-id="54c65-104">\_palavra-chave do evento sh</span><span class="sxs-lookup"><span data-stu-id="54c65-104">sh\_event keyword</span></span>

<span data-ttu-id="54c65-105">A palavra-chave do **\_ evento sh** especifica que um `system_handle` contém um identificador para um evento.</span><span class="sxs-lookup"><span data-stu-id="54c65-105">The **sh\_event** keyword specifies that a `system_handle` holds a handle to an event.</span></span>

``` syntax
[system_handle(sh_event)]

[system_handle(sh_event, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="54c65-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54c65-106">Parameters</span></span>

<span data-ttu-id="54c65-107">Essa palavra-chave é um parâmetro para [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="54c65-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="54c65-108">A documentação [**system_handle**](system-handle.md) também contém detalhes sobre o uso opcional do parâmetro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="54c65-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="54c65-109">O comportamento padrão é de acordo com as `DUPLICATE_SAME_ACCESS` especificações de [função **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="54c65-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="54c65-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="54c65-110">Remarks</span></span>

<span data-ttu-id="54c65-111">Para usar essa palavra-chave com o `system_handle` atributo, o `-target` sinalizador deve ser definido como `NT100` (ou superior) durante a execução de midl.exe.</span><span class="sxs-lookup"><span data-stu-id="54c65-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="54c65-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="54c65-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT NotifyThisEvent([in, system_handle(sh_event)] HANDLE listeningToThisEvent);
}
```

## <a name="requirements"></a><span data-ttu-id="54c65-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54c65-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="54c65-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54c65-114">Minimum supported client</span></span> | <span data-ttu-id="54c65-115">Atualização de aniversário do Windows 10 (versão 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="54c65-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="54c65-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54c65-116">Minimum supported server</span></span> | <span data-ttu-id="54c65-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="54c65-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="54c65-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="54c65-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54c65-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="54c65-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="54c65-120">Objetos de evento</span><span class="sxs-lookup"><span data-stu-id="54c65-120">Event Objects</span></span>](../sync/event-objects.md)
</dt> <dt>

[<span data-ttu-id="54c65-121">Segurança do objeto de sincronização e direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="54c65-121">Synchronization Object Security and Access Rights</span></span>](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="54c65-122">Função **CreateEvent**</span><span class="sxs-lookup"><span data-stu-id="54c65-122">**CreateEvent** function</span></span>](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[<span data-ttu-id="54c65-123">Função **CreateEventEx**</span><span class="sxs-lookup"><span data-stu-id="54c65-123">**CreateEventEx** function</span></span>](/windows/win32/api/synchapi/nf-synchapi-createeventexa)
</dt> </dl>
