---
description: Contém informações sobre a cláusula de acesso para o armazenamento protegido.
ms.assetid: 59634ada-4879-4ae7-b757-dfa6a88549af
title: Estrutura de PST_ACCESSCLAUSE (Pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSCLAUSE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 3536b92bf1d014090f124976b8f4a16e25beb444
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749408"
---
# <a name="pst_accessclause-structure"></a><span data-ttu-id="dc871-103">Estrutura de ACCESSCLAUSE de PST \_</span><span class="sxs-lookup"><span data-stu-id="dc871-103">PST\_ACCESSCLAUSE structure</span></span>

<span data-ttu-id="dc871-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="dc871-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="dc871-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="dc871-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="dc871-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="dc871-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="dc871-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="dc871-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="dc871-108">Contém informações sobre a cláusula de acesso para o armazenamento protegido.</span><span class="sxs-lookup"><span data-stu-id="dc871-108">Contains information about the access clause for the protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc871-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dc871-109">Syntax</span></span>


```C++
typedef struct {
  DWORD                cbSize;
  PST_ACCESSCLAUSETYPE ClauseType;
  DWORD                cbClauseData;
  BYTE                 *pbClauseData;
} PST_ACCESSCLAUSE, *PPST_ACCESSCLAUSE;
```



## <a name="members"></a><span data-ttu-id="dc871-110">Membros</span><span class="sxs-lookup"><span data-stu-id="dc871-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="dc871-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="dc871-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="dc871-112">O tamanho desta estrutura.</span><span class="sxs-lookup"><span data-stu-id="dc871-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="dc871-113">**Cláusulatype**</span><span class="sxs-lookup"><span data-stu-id="dc871-113">**ClauseType**</span></span>
</dt> <dd>

<span data-ttu-id="dc871-114">O tipo de dados apontado pelo membro **pbClauseData** .</span><span class="sxs-lookup"><span data-stu-id="dc871-114">The type of data that is pointed to by the **pbClauseData** member.</span></span> <span data-ttu-id="dc871-115">Para obter mais informações, consulte [**Pstore Types**](pstore-types.md).</span><span class="sxs-lookup"><span data-stu-id="dc871-115">For more information, see [**PStore Types**](pstore-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc871-116">**cbClauseData**</span><span class="sxs-lookup"><span data-stu-id="dc871-116">**cbClauseData**</span></span>
</dt> <dd>

<span data-ttu-id="dc871-117">O tamanho dos dados apontados pelo membro **pbClauseData** .</span><span class="sxs-lookup"><span data-stu-id="dc871-117">The size of the data that is pointed to by the **pbClauseData** member.</span></span>

</dd> <dt>

<span data-ttu-id="dc871-118">**pbClauseData**</span><span class="sxs-lookup"><span data-stu-id="dc871-118">**pbClauseData**</span></span>
</dt> <dd>

<span data-ttu-id="dc871-119">Um ponteiro para os dados da cláusula de acesso.</span><span class="sxs-lookup"><span data-stu-id="dc871-119">A pointer to the access clause data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc871-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc871-120">Requirements</span></span>



| <span data-ttu-id="dc871-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc871-121">Requirement</span></span> | <span data-ttu-id="dc871-122">Valor</span><span class="sxs-lookup"><span data-stu-id="dc871-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dc871-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dc871-123">Header</span></span><br/> | <dl> <span data-ttu-id="dc871-124"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc871-124"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc871-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc871-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc871-126">**\_ACCESSRULE PST**</span><span class="sxs-lookup"><span data-stu-id="dc871-126">**PST\_ACCESSRULE**</span></span>](pst-accessrule.md)
</dt> </dl>

 

 
