---
title: palavra-chave sh_pipe
description: A \_ palavra-chave \ sh pipeName especifica que o objeto do sistema é um identificador para um pipe.
keywords:
- MIDL de palavra-chave sh_pipe
topic_type:
- apiref
api_name:
- sh_pipe
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 9f9deab2bf5a751d3b2d5956d4d33a1d5b347e18
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "105814620"
---
# <a name="sh_pipe-keyword"></a><span data-ttu-id="231eb-104">\_palavra-chave sh pipe</span><span class="sxs-lookup"><span data-stu-id="231eb-104">sh\_pipe keyword</span></span>

<span data-ttu-id="231eb-105">A palavra-chave **sh \_ pipe** especifica que um `system_handle` contém um identificador para um pipe.</span><span class="sxs-lookup"><span data-stu-id="231eb-105">The **sh\_pipe** keyword specifies that a `system_handle` holds a handle to a pipe.</span></span>

``` syntax
[system_handle(sh_pipe)]

[system_handle(sh_pipe, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="231eb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="231eb-106">Parameters</span></span>

<span data-ttu-id="231eb-107">Essa palavra-chave é um parâmetro para [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="231eb-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="231eb-108">A documentação [**system_handle**](system-handle.md) também contém detalhes sobre o uso opcional do parâmetro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="231eb-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="231eb-109">O comportamento padrão é de acordo com as `DUPLICATE_SAME_ACCESS` especificações de [função **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="231eb-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="231eb-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="231eb-110">Remarks</span></span>

<span data-ttu-id="231eb-111">Para usar essa palavra-chave com o `system_handle` atributo, o `-target` sinalizador deve ser definido como `NT100` (ou superior) durante a execução de midl.exe.</span><span class="sxs-lookup"><span data-stu-id="231eb-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="231eb-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="231eb-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GetNewPipe([out, system_handle(sh_pipe)] HANDLE* mySidePipe);

    HRESULT PutReadOnlyPipe([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE theirSidePipe);
}
```

## <a name="requirements"></a><span data-ttu-id="231eb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="231eb-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="231eb-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="231eb-114">Minimum supported client</span></span> | <span data-ttu-id="231eb-115">Atualização de aniversário do Windows 10 (versão 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="231eb-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="231eb-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="231eb-116">Minimum supported server</span></span> | <span data-ttu-id="231eb-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="231eb-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="231eb-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="231eb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="231eb-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="231eb-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="231eb-120">Sobre pipes</span><span class="sxs-lookup"><span data-stu-id="231eb-120">About Pipes</span></span>](../ipc/about-pipes.md)
</dt> <dt>

[<span data-ttu-id="231eb-121">Segurança de arquivo e direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="231eb-121">File Security and Access Rights</span></span>](../fileio/file-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="231eb-122">Função **CreatePipe**</span><span class="sxs-lookup"><span data-stu-id="231eb-122">**CreatePipe** function</span></span>](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe)
</dt> <dt>

[<span data-ttu-id="231eb-123">Função **CreateNamedPipe**</span><span class="sxs-lookup"><span data-stu-id="231eb-123">**CreateNamedPipe** function</span></span>](/windows/win32/api/winbase/nf-winbase-createnamedpipea)
</dt> </dl>
