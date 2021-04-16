---
description: Descreve um tipo ou um subtipo.
ms.assetid: 4b6b77d9-54ea-4101-9c8b-e525f9aa3816
title: Estrutura de PST_TYPEINFO (Pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_TYPEINFO
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: fc78d0570ff2e5cf66a9048d64143149564a51c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751126"
---
# <a name="pst_typeinfo-structure"></a><span data-ttu-id="d1374-103">Estrutura de TYPEINFO de PST \_</span><span class="sxs-lookup"><span data-stu-id="d1374-103">PST\_TYPEINFO structure</span></span>

<span data-ttu-id="d1374-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d1374-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="d1374-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="d1374-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="d1374-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="d1374-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="d1374-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="d1374-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="d1374-108">Descreve um tipo ou um subtipo.</span><span class="sxs-lookup"><span data-stu-id="d1374-108">Describes a type or a subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1374-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1374-109">Syntax</span></span>


```C++
typedef struct {
  DWORD  cbSize;
  LPWSTR szDisplayName;
} PST_TYPEINFO, *PPST_TYPEINFO;
```



## <a name="members"></a><span data-ttu-id="d1374-110">Membros</span><span class="sxs-lookup"><span data-stu-id="d1374-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="d1374-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="d1374-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="d1374-112">O tamanho desta estrutura.</span><span class="sxs-lookup"><span data-stu-id="d1374-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="d1374-113">**szDisplayName**</span><span class="sxs-lookup"><span data-stu-id="d1374-113">**szDisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="d1374-114">Um ponteiro para uma cadeia de caracteres larga que representa o nome de exibição do tipo.</span><span class="sxs-lookup"><span data-stu-id="d1374-114">A pointer to a wide character string that represents the display name for the type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d1374-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1374-115">Requirements</span></span>



| <span data-ttu-id="d1374-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1374-116">Requirement</span></span> | <span data-ttu-id="d1374-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d1374-117">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d1374-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1374-118">Header</span></span><br/> | <dl> <span data-ttu-id="d1374-119"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1374-119"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1374-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1374-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1374-121">**CreateSubtype**</span><span class="sxs-lookup"><span data-stu-id="d1374-121">**CreateSubtype**</span></span>](ipstore-createsubtype.md)
</dt> <dt>

[<span data-ttu-id="d1374-122">**CreateType**</span><span class="sxs-lookup"><span data-stu-id="d1374-122">**CreateType**</span></span>](ipstore-createtype.md)
</dt> <dt>

[<span data-ttu-id="d1374-123">**GetSubtypeInfo**</span><span class="sxs-lookup"><span data-stu-id="d1374-123">**GetSubtypeInfo**</span></span>](ipstore-getsubtypeinfo.md)
</dt> <dt>

[<span data-ttu-id="d1374-124">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="d1374-124">**GetTypeInfo**</span></span>](ipstore-gettypeinfo.md)
</dt> </dl>

 

 
