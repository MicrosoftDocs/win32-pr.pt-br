---
title: palavra-chave sh_job
description: A \_ palavra-chave \ sh Job = especifica que o objeto do sistema é um identificador para um trabalho.
keywords:
- MIDL de palavra-chave sh_job
topic_type:
- apiref
api_name:
- sh_job
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: db24f9dc84f2bb56f57327090485b406ad1a437f
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "103930053"
---
# <a name="sh_job-keyword"></a><span data-ttu-id="c844f-104">\_palavra-chave sh Job</span><span class="sxs-lookup"><span data-stu-id="c844f-104">sh\_job keyword</span></span>

<span data-ttu-id="c844f-105">A palavra-chave **sh \_ Job** especifica que um `system_handle` contém um identificador para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="c844f-105">The **sh\_job** keyword specifies that a `system_handle` holds a handle to a job.</span></span>

``` syntax
[system_handle(sh_job)]

[system_handle(sh_job, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="c844f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c844f-106">Parameters</span></span>

<span data-ttu-id="c844f-107">Essa palavra-chave é um parâmetro para [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="c844f-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="c844f-108">A documentação [**system_handle**](system-handle.md) também contém detalhes sobre o uso opcional do parâmetro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="c844f-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="c844f-109">O comportamento padrão é de acordo com as `DUPLICATE_SAME_ACCESS` especificações de [função **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="c844f-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="c844f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="c844f-110">Remarks</span></span>

<span data-ttu-id="c844f-111">Para usar essa palavra-chave com o `system_handle` atributo, o `-target` sinalizador deve ser definido como `NT100` (ou superior) durante a execução de midl.exe.</span><span class="sxs-lookup"><span data-stu-id="c844f-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="c844f-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c844f-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT SetJob([in, system_handle(sh_job)] HANDLE job);

    HRESULT GetJobForAccounting([out, system_handle(sh_job, JOB_OBJECT_QUERY)] HANDLE* pJob);
}
```

## <a name="requirements"></a><span data-ttu-id="c844f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c844f-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="c844f-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c844f-114">Minimum supported client</span></span> | <span data-ttu-id="c844f-115">Atualização de aniversário do Windows 10 (versão 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="c844f-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="c844f-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c844f-116">Minimum supported server</span></span> | <span data-ttu-id="c844f-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="c844f-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="c844f-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="c844f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c844f-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="c844f-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="c844f-120">Objetos de trabalho</span><span class="sxs-lookup"><span data-stu-id="c844f-120">Job Objects</span></span>](../procthread/job-objects.md)
</dt> <dt>

[<span data-ttu-id="c844f-121">Segurança do objeto de trabalho e direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="c844f-121">Job Object Security and Access Rights</span></span>](../procthread/job-object-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="c844f-122">Função **CreateJobObject**</span><span class="sxs-lookup"><span data-stu-id="c844f-122">**CreateJobObject** function</span></span>](/windows/win32/api/winbase/nf-winbase-createjobobjecta)
</dt> </dl>
