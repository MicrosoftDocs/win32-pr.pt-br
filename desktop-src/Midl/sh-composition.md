---
title: palavra-chave sh_composition
description: A \_ palavra-chave \ sh composição \ especifica que o objeto do sistema é um identificador para uma superfície de composição.
keywords:
- MIDL de palavra-chave sh_composition
topic_type:
- apiref
api_name:
- sh_composition
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 5a7e723c65ca6320dbec4a2f8a379cfed2f85f72
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104172406"
---
# <a name="sh_composition-keyword"></a><span data-ttu-id="d8b63-104">\_palavra-chave de composição sh</span><span class="sxs-lookup"><span data-stu-id="d8b63-104">sh\_composition keyword</span></span>

<span data-ttu-id="d8b63-105">A palavra-chave de **\_ composição sh** especifica que um `system_handle` contém um identificador para uma superfície de composição.</span><span class="sxs-lookup"><span data-stu-id="d8b63-105">The **sh\_composition** keyword specifies that a `system_handle` holds a handle to a composition surface.</span></span>

``` syntax
[system_handle(sh_composition)]

[system_handle(sh_composition, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="d8b63-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8b63-106">Parameters</span></span>

<span data-ttu-id="d8b63-107">Essa palavra-chave é um parâmetro para [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="d8b63-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="d8b63-108">A documentação [**system_handle**](system-handle.md) também contém detalhes sobre o uso opcional do parâmetro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="d8b63-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="d8b63-109">O comportamento padrão é de acordo com as `DUPLICATE_SAME_ACCESS` especificações de [função **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="d8b63-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8b63-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8b63-110">Remarks</span></span>

<span data-ttu-id="d8b63-111">Para usar essa palavra-chave com o `system_handle` atributo, o `-target` sinalizador deve ser definido como `NT100` (ou superior) durante a execução de midl.exe.</span><span class="sxs-lookup"><span data-stu-id="d8b63-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="d8b63-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d8b63-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GetVisualSurface([out, system_handle(sh_composition)] HANDLE* visual);
}
```

## <a name="requirements"></a><span data-ttu-id="d8b63-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8b63-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="d8b63-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8b63-114">Minimum supported client</span></span> | <span data-ttu-id="d8b63-115">Atualização de aniversário do Windows 10 (versão 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="d8b63-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="d8b63-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8b63-116">Minimum supported server</span></span> | <span data-ttu-id="d8b63-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="d8b63-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="d8b63-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8b63-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8b63-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="d8b63-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="d8b63-120">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="d8b63-120">DirectComposition</span></span>](/windows/win32/api/_directcomp/)
</dt> <dt>

[<span data-ttu-id="d8b63-121">Função **DCompositionCreateSurfaceHandle**</span><span class="sxs-lookup"><span data-stu-id="d8b63-121">**DCompositionCreateSurfaceHandle** function</span></span>](/windows/win32/api/dcomp/nf-dcomp-dcompositioncreatesurfacehandle)
</dt> </dl>
