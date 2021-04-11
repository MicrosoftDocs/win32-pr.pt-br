---
title: ODJ_SID
description: Definição de IDL de ODJ_SID
ms.assetid: 1d06f725-6cd4-42cf-b171-c78a095690cb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: dd51f2e8a54eaf5be566e5a25f013ca1d87b9341
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104008555"
---
# <a name="odj_sid-structure"></a><span data-ttu-id="cb8e7-103">Estrutura de ODJ_SID</span><span class="sxs-lookup"><span data-stu-id="cb8e7-103">ODJ_SID structure</span></span>

<span data-ttu-id="cb8e7-104">Contém um SID (identificador de segurança).</span><span class="sxs-lookup"><span data-stu-id="cb8e7-104">Contains a Security Identifier (SID).</span></span>

## <a name="syntax"></a><span data-ttu-id="cb8e7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cb8e7-105">Syntax</span></span>

```C++
typedef struct _ODJ_SID
{
    UCHAR Revision;
    UCHAR SubAuthorityCount;
    SID_IDENTIFIER_AUTHORITY IdentifierAuthority;
    [size_is(SubAuthorityCount)] ULONG SubAuthority[*];
}   ODJ_SID, *PODJ_SID;
```

## <a name="members"></a><span data-ttu-id="cb8e7-106">Membros</span><span class="sxs-lookup"><span data-stu-id="cb8e7-106">Members</span></span>

### <a name="revision"></a><span data-ttu-id="cb8e7-107">Revisão</span><span class="sxs-lookup"><span data-stu-id="cb8e7-107">Revision</span></span>

<span data-ttu-id="cb8e7-108">Deve ser definido como a revisão de SID.</span><span class="sxs-lookup"><span data-stu-id="cb8e7-108">Must be set to the SID revision.</span></span>

### <a name="subauthoritycount"></a><span data-ttu-id="cb8e7-109">SubAuthorityCount</span><span class="sxs-lookup"><span data-stu-id="cb8e7-109">SubAuthorityCount</span></span>

<span data-ttu-id="cb8e7-110">Deve ser definido como o número de elementos na subautoridade.</span><span class="sxs-lookup"><span data-stu-id="cb8e7-110">Must be set to the number of elements in SubAuthority.</span></span>

### <a name="identifierauthority"></a><span data-ttu-id="cb8e7-111">IdentifierAuthority</span><span class="sxs-lookup"><span data-stu-id="cb8e7-111">IdentifierAuthority</span></span>

<span data-ttu-id="cb8e7-112">Deve ser definido como o identificador de autoridade SID.</span><span class="sxs-lookup"><span data-stu-id="cb8e7-112">Must be set to the SID authority identifier.</span></span>

### <a name="subauthority"></a><span data-ttu-id="cb8e7-113">Subautoridade</span><span class="sxs-lookup"><span data-stu-id="cb8e7-113">SubAuthority</span></span>

<span data-ttu-id="cb8e7-114">Deve conter uma matriz de subautoridades SID.</span><span class="sxs-lookup"><span data-stu-id="cb8e7-114">Must contain an array of SID sub authorities.</span></span>

## <a name="see-also"></a><span data-ttu-id="cb8e7-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb8e7-115">See also</span></span>

[<span data-ttu-id="cb8e7-116">**Definições de IDL de ingresso no domínio offline**</span><span class="sxs-lookup"><span data-stu-id="cb8e7-116">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="cb8e7-117">**\_autoridade de \_ identificador \_ Sid ODJ**</span><span class="sxs-lookup"><span data-stu-id="cb8e7-117">**ODJ\_SID\_IDENTIFIER\_AUTHORITY**</span></span>](odj-sid_identifier_authority.md)
