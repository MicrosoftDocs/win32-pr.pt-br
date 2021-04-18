---
title: palavra-chave sh_token
description: A \_ palavra-chave \ sh token \ especifica que o objeto do sistema é um identificador para um token.
keywords:
- MIDL de palavra-chave sh_token
topic_type:
- apiref
api_name:
- sh_token keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: a33b070af5cd43a095fd6ad45a0dee86f1868171
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "105802179"
---
# <a name="sh_token-keyword"></a><span data-ttu-id="1cba8-104">\_palavra-chave sh token</span><span class="sxs-lookup"><span data-stu-id="1cba8-104">sh\_token keyword</span></span>

<span data-ttu-id="1cba8-105">A palavra-chave **sh \_ token** especifica que um `system_handle` contém um identificador para um token.</span><span class="sxs-lookup"><span data-stu-id="1cba8-105">The **sh\_token** keyword specifies that a `system_handle` holds a handle to a token.</span></span>

``` syntax
[system_handle(sh_token)]

[system_handle(sh_token, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="1cba8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1cba8-106">Parameters</span></span>

<span data-ttu-id="1cba8-107">Essa palavra-chave é um parâmetro para [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="1cba8-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="1cba8-108">A documentação [**system_handle**](system-handle.md) também contém detalhes sobre o uso opcional do parâmetro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="1cba8-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="1cba8-109">O comportamento padrão é de acordo com as `DUPLICATE_SAME_ACCESS` especificações de [função **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="1cba8-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cba8-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="1cba8-110">Remarks</span></span>

<span data-ttu-id="1cba8-111">Para usar essa palavra-chave com o `system_handle` atributo, o `-target` sinalizador deve ser definido como `NT100` (ou superior) durante a execução de midl.exe.</span><span class="sxs-lookup"><span data-stu-id="1cba8-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="1cba8-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1cba8-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT SetToken([in, system_handle(sh_token)] HANDLE token);

    HRESULT GetToken([out, system_handle(sh_token, TOKEN_QUERY)] HANDLE* pToken);
}
```

## <a name="requirements"></a><span data-ttu-id="1cba8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cba8-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="1cba8-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cba8-114">Minimum supported client</span></span> | <span data-ttu-id="1cba8-115">Atualização de aniversário do Windows 10 (versão 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="1cba8-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="1cba8-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cba8-116">Minimum supported server</span></span> | <span data-ttu-id="1cba8-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="1cba8-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="1cba8-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="1cba8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cba8-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="1cba8-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="1cba8-120">Tokens de acesso</span><span class="sxs-lookup"><span data-stu-id="1cba8-120">Access Tokens</span></span>](../secauthz/access-tokens.md)
</dt> <dt>

[<span data-ttu-id="1cba8-121">Direitos de acesso para objetos de Access-Token</span><span class="sxs-lookup"><span data-stu-id="1cba8-121">Access Rights for Access-Token Objects</span></span>](../secauthz/access-rights-for-access-token-objects.md)
</dt> </dl>
