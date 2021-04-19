---
title: palavra-chave sh_process
description: A \_ palavra-chave \ sh Process \ especifica que o objeto do sistema é um identificador para um processo.
keywords:
- MIDL de palavra-chave sh_process
topic_type:
- apiref
api_name:
- sh_process
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 3652c6889c687173bbf7b397cddff4659c0329f1
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "105793781"
---
# <a name="sh_process-keyword"></a><span data-ttu-id="a46f2-104">\_palavra-chave sh Process</span><span class="sxs-lookup"><span data-stu-id="a46f2-104">sh\_process keyword</span></span>

<span data-ttu-id="a46f2-105">A palavra-chave **sh \_ process** especifica que um `system_handle` tem um identificador para um processo.</span><span class="sxs-lookup"><span data-stu-id="a46f2-105">The **sh\_process** keyword specifies that a `system_handle` holds a handle to a process.</span></span>

``` syntax
[system_handle(sh_process)]

[system_handle(sh_process, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="a46f2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a46f2-106">Parameters</span></span>

<span data-ttu-id="a46f2-107">Essa palavra-chave é um parâmetro para [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="a46f2-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="a46f2-108">A documentação [**system_handle**](system-handle.md) também contém detalhes sobre o uso opcional do parâmetro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="a46f2-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="a46f2-109">O comportamento padrão é de acordo com as `DUPLICATE_SAME_ACCESS` especificações de [função **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="a46f2-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="a46f2-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="a46f2-110">Remarks</span></span>

<span data-ttu-id="a46f2-111">Para usar essa palavra-chave com o `system_handle` atributo, o `-target` sinalizador deve ser definido como `NT100` (ou superior) durante a execução de midl.exe.</span><span class="sxs-lookup"><span data-stu-id="a46f2-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="a46f2-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a46f2-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GetStubProcess([out, system_handle(sh_process)] HANDLE* processHandle);

    HRESULT WatchProcess([in, system_handle(sh_process, PROCESS_QUERY_INFORMATION | PROCESS_QUERY_LIMITED_INFORMATION)] HANDLE processHandle);
}
```

## <a name="requirements"></a><span data-ttu-id="a46f2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a46f2-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="a46f2-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a46f2-114">Minimum supported client</span></span> | <span data-ttu-id="a46f2-115">Atualização de aniversário do Windows 10 (versão 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="a46f2-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="a46f2-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a46f2-116">Minimum supported server</span></span> | <span data-ttu-id="a46f2-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="a46f2-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="a46f2-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="a46f2-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a46f2-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="a46f2-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="a46f2-120">Sobre Processos e Threads</span><span class="sxs-lookup"><span data-stu-id="a46f2-120">About Processes and Threads</span></span>](../procthread/about-processes-and-threads.md)
</dt> <dt>

[<span data-ttu-id="a46f2-121">Direitos de acesso e segurança do processo</span><span class="sxs-lookup"><span data-stu-id="a46f2-121">Process Security and Access Rights</span></span>](../procthread/process-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="a46f2-122">Função **CreateProcess**</span><span class="sxs-lookup"><span data-stu-id="a46f2-122">**CreateProcess** function</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)
</dt> <dt>

[<span data-ttu-id="a46f2-123">Função **OpenProcess**</span><span class="sxs-lookup"><span data-stu-id="a46f2-123">**OpenProcess** function</span></span>](/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)
</dt> </dl>