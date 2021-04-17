---
title: palavra-chave sh_section
description: A \_ palavra-chave \ sh section especifica que o objeto do sistema é um identificador para uma seção.
keywords:
- MIDL de palavra-chave sh_section
topic_type:
- apiref
api_name:
- sh_section keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 056112deb790e727206a5ac1a1a2a5043a68f5e1
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "105769672"
---
# <a name="sh_section-keyword"></a><span data-ttu-id="69bba-104">\_palavra-chave da seção sh</span><span class="sxs-lookup"><span data-stu-id="69bba-104">sh\_section keyword</span></span>

<span data-ttu-id="69bba-105">A palavra-chave da **\_ seção sh** especifica que um `system_handle` contém um identificador para uma seção.</span><span class="sxs-lookup"><span data-stu-id="69bba-105">The **sh\_section** keyword specifies that a `system_handle` holds a handle to a section.</span></span>

``` syntax
[system_handle(sh_section)]

[system_handle(sh_section, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="69bba-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69bba-106">Parameters</span></span>

<span data-ttu-id="69bba-107">Essa palavra-chave é um parâmetro para [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="69bba-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="69bba-108">A documentação [**system_handle**](system-handle.md) também contém detalhes sobre o uso opcional do parâmetro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="69bba-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="69bba-109">O comportamento padrão é de acordo com as `DUPLICATE_SAME_ACCESS` especificações de [função **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="69bba-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="69bba-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="69bba-110">Remarks</span></span>

<span data-ttu-id="69bba-111">Para usar essa palavra-chave com o `system_handle` atributo, o `-target` sinalizador deve ser definido como `NT100` (ou superior) durante a execução de midl.exe.</span><span class="sxs-lookup"><span data-stu-id="69bba-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="69bba-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="69bba-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GiveSection([in, system_handle(sh_section)] HANDLE section);

    HRESULT GetSectionToWatch([out, system_handle(sh_section, SECTION_MAP_READ)] HANDLE* pSection);
}
```

## <a name="requirements"></a><span data-ttu-id="69bba-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69bba-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="69bba-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69bba-114">Minimum supported client</span></span> | <span data-ttu-id="69bba-115">Atualização de aniversário do Windows 10 (versão 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="69bba-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="69bba-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69bba-116">Minimum supported server</span></span> | <span data-ttu-id="69bba-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="69bba-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="69bba-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="69bba-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69bba-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="69bba-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="69bba-120">Objetos e exibições de seção</span><span class="sxs-lookup"><span data-stu-id="69bba-120">Section Objects and Views</span></span>](/windows-hardware/drivers/kernel/section-objects-and-views)
</dt> <dt>

[<span data-ttu-id="69bba-121">Função **ZwCreateSection** (incluindo especificações de acesso)</span><span class="sxs-lookup"><span data-stu-id="69bba-121">**ZwCreateSection** function (including access specifications)</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-zwcreatesection)
</dt> </dl>
