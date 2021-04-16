---
description: Os tipos de dados para métodos de armazenamento protegidos.
ms.assetid: 4d494326-6d0f-4a12-83a2-3c3dd3ca9c1b
title: Tipos de Pstore (Pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f1c93af4ae6756a6489b828c50bac505241bdd3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751550"
---
# <a name="pstore-types"></a><span data-ttu-id="50fc3-103">Tipos de Pstore</span><span class="sxs-lookup"><span data-stu-id="50fc3-103">PStore Types</span></span>

<span data-ttu-id="50fc3-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="50fc3-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="50fc3-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="50fc3-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="50fc3-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="50fc3-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="50fc3-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="50fc3-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="50fc3-108">Os tipos de dados para métodos de armazenamento protegidos.</span><span class="sxs-lookup"><span data-stu-id="50fc3-108">The data types for Protected Storage methods.</span></span>


```C++
typedef DWORD PST_ACCESSMODE;
typedef DWORD PST_ACCESSCLAUSETYPE;
typedef DWORD PST_KEY;
```



<dl> <dt>

<span data-ttu-id="50fc3-109">**acesso ao PST \_**</span><span class="sxs-lookup"><span data-stu-id="50fc3-109">**PST\_ACCESSMODE**</span></span>
</dt> <dd>

<span data-ttu-id="50fc3-110">Define o modo de leitura ou gravação da regra de acesso.</span><span class="sxs-lookup"><span data-stu-id="50fc3-110">Defines the read or write mode of the access rule.</span></span>

</dd> <dt>

<span data-ttu-id="50fc3-111">**\_ACCESSCLAUSETYPE PST**</span><span class="sxs-lookup"><span data-stu-id="50fc3-111">**PST\_ACCESSCLAUSETYPE**</span></span>
</dt> <dd>

<span data-ttu-id="50fc3-112">Define o tipo de cláusula da regra de acesso.</span><span class="sxs-lookup"><span data-stu-id="50fc3-112">Defines the clause type of the access rule.</span></span>

</dd> <dt>

<span data-ttu-id="50fc3-113">**\_chave PST**</span><span class="sxs-lookup"><span data-stu-id="50fc3-113">**PST\_KEY**</span></span>
</dt> <dd>

<span data-ttu-id="50fc3-114">Define a chave para o item armazenado.</span><span class="sxs-lookup"><span data-stu-id="50fc3-114">Defines the key for the stored item.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="50fc3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50fc3-115">Requirements</span></span>



| <span data-ttu-id="50fc3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="50fc3-116">Requirement</span></span> | <span data-ttu-id="50fc3-117">Valor</span><span class="sxs-lookup"><span data-stu-id="50fc3-117">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="50fc3-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="50fc3-118">Header</span></span><br/> | <dl> <span data-ttu-id="50fc3-119"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="50fc3-119"><dt>Pstore.h</dt></span></span> </dl> |



 

 
