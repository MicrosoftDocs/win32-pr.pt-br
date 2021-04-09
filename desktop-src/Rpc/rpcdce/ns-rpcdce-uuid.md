---
title: UUID
description: Fornece uma designação exclusiva de um objeto, como uma interface, um vetor de ponto de entrada de gerente ou um objeto de cliente.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/09/2019
ms.openlocfilehash: 95d2d420502a5d92af64c902ffa82c709639d872
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104084253"
---
# <a name="uuid-structure"></a><span data-ttu-id="1a42d-103">Estrutura UUID</span><span class="sxs-lookup"><span data-stu-id="1a42d-103">UUID structure</span></span>

<span data-ttu-id="1a42d-104">A estrutura **UUID** define um UUID (identificador universal exclusivo).</span><span class="sxs-lookup"><span data-stu-id="1a42d-104">The **UUID** structure defines a Universally Unique Identifier (UUID).</span></span> <span data-ttu-id="1a42d-105">Um **UUID** fornece uma designação exclusiva de um objeto, como uma interface, um vetor de ponto de entrada de gerente ou um objeto de cliente.</span><span class="sxs-lookup"><span data-stu-id="1a42d-105">A **UUID** provides a unique designation of an object such as an interface, a manager entry-point vector, or a client object.</span></span>

<span data-ttu-id="1a42d-106">A estrutura do **UUID** é um `typedef` sinônimo para a estrutura de [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) .</span><span class="sxs-lookup"><span data-stu-id="1a42d-106">The **UUID** structure is a `typedef`'d synonym for the [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a42d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a42d-107">Syntax</span></span>

```cpp
typedef GUID UUID;
```

## <a name="remarks"></a><span data-ttu-id="1a42d-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a42d-108">Remarks</span></span>

<span data-ttu-id="1a42d-109">As bibliotecas de tempo de execução RPC usam **UUID** s para verificar a compatibilidade entre clientes e servidores e para selecionar entre várias implementações de uma interface.</span><span class="sxs-lookup"><span data-stu-id="1a42d-109">The RPC run-time libraries use **UUID** s to check for compatibility between clients and servers, and to select among multiple implementations of an interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a42d-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a42d-110">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="1a42d-111">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="1a42d-111">**Header**</span></span> | <span data-ttu-id="1a42d-112">Definido em rpcdce. h; incluir RPC. h</span><span class="sxs-lookup"><span data-stu-id="1a42d-112">Defined in rpcdce.h; include rpc.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="1a42d-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a42d-113">See also</span></span>

<span data-ttu-id="1a42d-114">[GUID](/windows/win32/api/guiddef/ns-guiddef-guid) 
 do [UUID \_ VETOR](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)</span><span class="sxs-lookup"><span data-stu-id="1a42d-114">[GUID](/windows/win32/api/guiddef/ns-guiddef-guid)
[UUID\_VECTOR](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)</span></span>