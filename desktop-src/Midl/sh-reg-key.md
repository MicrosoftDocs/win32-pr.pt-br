---
title: palavra-chave sh_reg_key
description: A palavra-chave \ sh \_ reg \_ Key \ especifica que o objeto do sistema é um identificador para uma chave do registro.
keywords:
- MIDL de palavra-chave sh_reg_key
topic_type:
- apiref
api_name:
- sh_reg_key keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: cec526bed766534f82d5a1bc24c55050dea814ed
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "105766009"
---
# <a name="sh_reg_key-keyword"></a><span data-ttu-id="b0bc7-104">\_palavra-chave da chave de registro sh \_</span><span class="sxs-lookup"><span data-stu-id="b0bc7-104">sh\_reg\_key keyword</span></span>

<span data-ttu-id="b0bc7-105">A palavra-chave **sh \_ reg \_ Key** especifica que um `system_handle` mantém um identificador para uma chave do registro.</span><span class="sxs-lookup"><span data-stu-id="b0bc7-105">The **sh\_reg\_key** keyword specifies that a `system_handle` holds a handle to a registry key.</span></span>

``` syntax
[system_handle(sh_reg_key)]

[system_handle(sh_reg_key, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="b0bc7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0bc7-106">Parameters</span></span>

<span data-ttu-id="b0bc7-107">Essa palavra-chave é um parâmetro para [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="b0bc7-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="b0bc7-108">A documentação [**system_handle**](system-handle.md) também contém detalhes sobre o uso opcional do parâmetro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="b0bc7-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="b0bc7-109">O comportamento padrão é de acordo com as `DUPLICATE_SAME_ACCESS` especificações de [função **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="b0bc7-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0bc7-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0bc7-110">Remarks</span></span>

<span data-ttu-id="b0bc7-111">Para usar essa palavra-chave com o `system_handle` atributo, o `-target` sinalizador deve ser definido como `NT100` (ou superior) durante a execução de midl.exe.</span><span class="sxs-lookup"><span data-stu-id="b0bc7-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="b0bc7-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b0bc7-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GetConfigurationKey([out, system_handle(sh_reg_key)] HANDLE* key);

    HRESULT SetKeyForWatch([in, system_handle(sh_reg_key, KEY_READ)] HANDLE watchKey);
}
```

## <a name="requirements"></a><span data-ttu-id="b0bc7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0bc7-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="b0bc7-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0bc7-114">Minimum supported client</span></span> | <span data-ttu-id="b0bc7-115">Atualização de aniversário do Windows 10 (versão 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="b0bc7-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="b0bc7-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0bc7-116">Minimum supported server</span></span> | <span data-ttu-id="b0bc7-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="b0bc7-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="b0bc7-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0bc7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0bc7-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="b0bc7-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="b0bc7-120">Registro</span><span class="sxs-lookup"><span data-stu-id="b0bc7-120">Registry</span></span>](../sysinfo/registry.md)
</dt> <dt>

[<span data-ttu-id="b0bc7-121">Segurança da chave do registro e direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="b0bc7-121">Registry Key Security and Access Rights</span></span>](../sysinfo/registry-key-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="b0bc7-122">Função **RegOpenKeyEx**</span><span class="sxs-lookup"><span data-stu-id="b0bc7-122">**RegOpenKeyEx** function</span></span>](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)
</dt> <dt>
