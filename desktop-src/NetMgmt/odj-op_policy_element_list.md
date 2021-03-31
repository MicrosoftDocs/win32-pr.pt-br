---
title: OP_POLICY_ELEMENT_LIST
description: Definição de IDL de OP_POLICY_ELEMENT_LIST
ms.assetid: 1eebbdd2-655b-4bd3-938c-6bc687ffe7bb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 3c46e7208e6c142b9f58a7704be9bd3461c845b2
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "103642949"
---
# <a name="op_policy_element_list-structure"></a><span data-ttu-id="db024-103">Estrutura de OP_POLICY_ELEMENT_LIST</span><span class="sxs-lookup"><span data-stu-id="db024-103">OP_POLICY_ELEMENT_LIST structure</span></span>

<span data-ttu-id="db024-104">Define uma chave de registro raiz e uma matriz de elementos de chave do registro a serem configurados sob essa chave.</span><span class="sxs-lookup"><span data-stu-id="db024-104">Defines  a root registry key and an array of registry key elements to be configured under that key.</span></span>

## <a name="syntax"></a><span data-ttu-id="db024-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db024-105">Syntax</span></span>

```C++
typedef struct _OP_POLICY_ELEMENT_LIST
{
    [string] wchar_t                            *pSource;
    ULONG                                       ulRootKeyId;
    ULONG                                       cElements;
    [size_is(cElements)]    POP_POLICY_ELEMENT  pElements;
} OP_POLICY_ELEMENT_LIST, *POP_POLICY_ELEMENT_LIST;
```

## <a name="members"></a><span data-ttu-id="db024-106">Membros</span><span class="sxs-lookup"><span data-stu-id="db024-106">Members</span></span>

### <a name="psource"></a><span data-ttu-id="db024-107">pSource</span><span class="sxs-lookup"><span data-stu-id="db024-107">pSource</span></span>

<span data-ttu-id="db024-108">Contém o caminho do arquivo de Política de Grupo do qual os elementos contidos foram originados.</span><span class="sxs-lookup"><span data-stu-id="db024-108">Contains the path of the Group Policy file that the contained elements were sourced from.</span></span>

### <a name="ulrootkeyid"></a><span data-ttu-id="db024-109">ulRootKeyId</span><span class="sxs-lookup"><span data-stu-id="db024-109">ulRootKeyId</span></span>

<span data-ttu-id="db024-110">Contém o identificador da chave do registro raiz; no momento, deve ser definido como HKEY_LOCAL_MACHINE.</span><span class="sxs-lookup"><span data-stu-id="db024-110">Contains the identifier of the root registry key; currently must be set to HKEY_LOCAL_MACHINE.</span></span>

### <a name="celements"></a><span data-ttu-id="db024-111">cElements</span><span class="sxs-lookup"><span data-stu-id="db024-111">cElements</span></span>

<span data-ttu-id="db024-112">Contém o número de elementos em pElements.</span><span class="sxs-lookup"><span data-stu-id="db024-112">Contains the number of elements in pElements.</span></span>

### <a name="pelements"></a><span data-ttu-id="db024-113">pElements</span><span class="sxs-lookup"><span data-stu-id="db024-113">pElements</span></span>

<span data-ttu-id="db024-114">Contém uma matriz de elementos de OP_POLICY_ELEMENT.</span><span class="sxs-lookup"><span data-stu-id="db024-114">Contains an array of OP_POLICY_ELEMENT elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="db024-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="db024-115">See also</span></span>

[<span data-ttu-id="db024-116">**Definições de IDL de ingresso no domínio offline**</span><span class="sxs-lookup"><span data-stu-id="db024-116">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="db024-117">**\_elemento de política op \_**</span><span class="sxs-lookup"><span data-stu-id="db024-117">**OP\_POLICY\_ELEMENT**</span></span>](odj-op_policy_element.md)
