---
title: palavra-chave sh_thread
description: A \_ palavra-chave \ sh thread \ especifica que o objeto do sistema é um identificador para um thread.
keywords:
- MIDL de palavra-chave sh_thread
topic_type:
- apiref
api_name:
- sh_thread keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 2c82dc41d2b1c7cba740c897ef6cea9094979cc3
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104172411"
---
# <a name="sh_thread-keyword"></a><span data-ttu-id="dc952-104">\_palavra-chave sh thread</span><span class="sxs-lookup"><span data-stu-id="dc952-104">sh\_thread keyword</span></span>

<span data-ttu-id="dc952-105">A palavra-chave **sh \_ thread** especifica que um `system_handle` mantém um identificador para um thread.</span><span class="sxs-lookup"><span data-stu-id="dc952-105">The **sh\_thread** keyword specifies that a `system_handle` holds a handle to a thread.</span></span>

``` syntax
[system_handle(sh_thread)]

[system_handle(sh_thread, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="dc952-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc952-106">Parameters</span></span>

<span data-ttu-id="dc952-107">Essa palavra-chave é um parâmetro para [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="dc952-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="dc952-108">A documentação [**system_handle**](system-handle.md) também contém detalhes sobre o uso opcional do parâmetro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="dc952-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="dc952-109">O comportamento padrão é de acordo com as `DUPLICATE_SAME_ACCESS` especificações de [função **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="dc952-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc952-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc952-110">Remarks</span></span>

<span data-ttu-id="dc952-111">Para usar essa palavra-chave com o `system_handle` atributo, o `-target` sinalizador deve ser definido como `NT100` (ou superior) durante a execução de midl.exe.</span><span class="sxs-lookup"><span data-stu-id="dc952-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="dc952-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dc952-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT SetThread([in, system_handle(sh_process)] HANDLE threadHandle);
}
```

## <a name="requirements"></a><span data-ttu-id="dc952-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc952-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="dc952-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc952-114">Minimum supported client</span></span> | <span data-ttu-id="dc952-115">Atualização de aniversário do Windows 10 (versão 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="dc952-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="dc952-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc952-116">Minimum supported server</span></span> | <span data-ttu-id="dc952-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="dc952-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="dc952-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc952-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc952-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="dc952-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="dc952-120">Sobre Processos e Threads</span><span class="sxs-lookup"><span data-stu-id="dc952-120">About Processes and Threads</span></span>](../procthread/about-processes-and-threads.md)
</dt> <dt>

[<span data-ttu-id="dc952-121">Segurança de thread e direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="dc952-121">Thread Security and Access Rights</span></span>](../procthread/thread-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="dc952-122">Função **CreateThread**</span><span class="sxs-lookup"><span data-stu-id="dc952-122">**CreateThread** function</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)
</dt> <dt>

[<span data-ttu-id="dc952-123">Função **OpenThread**</span><span class="sxs-lookup"><span data-stu-id="dc952-123">**OpenThread** function</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread)
</dt> </dl>