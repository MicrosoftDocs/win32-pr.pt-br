---
description: 'O \_ tipo de \_ dados identificador de enumeração LSA é usado pela função LSA que enumera objetos TrustedDomain: LsaEnumerateTrustedDomainsEx.'
ms.assetid: 99dad3aa-cb92-4b7e-8a18-2c977cb2737c
title: LSA_ENUMERATION_HANDLE (Ntsecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db71e9522a188956a7aa838b11ba74f08bde39c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758155"
---
# <a name="lsa_enumeration_handle"></a><span data-ttu-id="bd9c7-103">\_identificador de enumeração LSA \_</span><span class="sxs-lookup"><span data-stu-id="bd9c7-103">LSA\_ENUMERATION\_HANDLE</span></span>

<span data-ttu-id="bd9c7-104">O tipo de dados **\_ \_ identificador de enumeração LSA** é usado pela função LSA que enumera objetos [**TrustedDomain**](trusteddomain-object.md) : [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex).</span><span class="sxs-lookup"><span data-stu-id="bd9c7-104">The **LSA\_ENUMERATION\_HANDLE** data type is used by the LSA function that enumerates [**TrustedDomain**](trusteddomain-object.md) objects: [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex).</span></span> <span data-ttu-id="bd9c7-105">Essa função foi projetada para que você possa fazer várias chamadas para enumerar todos os objetos de um determinado tipo no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bd9c7-105">This function is designed so that you can make multiple calls to enumerate all the objects of a given type in the database.</span></span>

<span data-ttu-id="bd9c7-106">Na chamada de função de enumeração inicial, você passa um ponteiro para uma variável de **\_ \_ identificador de enumeração LSA** que é inicializada como zero.</span><span class="sxs-lookup"><span data-stu-id="bd9c7-106">On the initial enumeration function call, you pass in a pointer to an **LSA\_ENUMERATION\_HANDLE** variable that is initialized to zero.</span></span> <span data-ttu-id="bd9c7-107">A função atualiza esse valor.</span><span class="sxs-lookup"><span data-stu-id="bd9c7-107">The function updates this value.</span></span> <span data-ttu-id="bd9c7-108">Se a função retornar um valor que indica que há mais objetos a serem enumerados, chame a função novamente e passe o valor de **\_ \_ identificador de enumeração LSA** atualizado para obter uma enumeração continuando do ponto em que a enumeração anterior parou.</span><span class="sxs-lookup"><span data-stu-id="bd9c7-108">If the function returns a value that indicates there are more objects to enumerate, call the function again and pass in the updated **LSA\_ENUMERATION\_HANDLE** value to obtain an enumeration continuing from the point where the previous enumeration left off.</span></span>


```C++
typedef ULONG LSA_ENUMERATION_HANDLE, *PLSA_ENUMERATION_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="bd9c7-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd9c7-109">Requirements</span></span>



| <span data-ttu-id="bd9c7-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd9c7-110">Requirement</span></span> | <span data-ttu-id="bd9c7-111">Valor</span><span class="sxs-lookup"><span data-stu-id="bd9c7-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bd9c7-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd9c7-112">Minimum supported client</span></span><br/> | <span data-ttu-id="bd9c7-113">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bd9c7-113">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bd9c7-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd9c7-114">Minimum supported server</span></span><br/> | <span data-ttu-id="bd9c7-115">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bd9c7-115">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bd9c7-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bd9c7-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd9c7-117"><dt>Ntsecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd9c7-117"><dt>Ntsecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd9c7-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd9c7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd9c7-119">**LsaEnumerateTrustedDomainsEx**</span><span class="sxs-lookup"><span data-stu-id="bd9c7-119">**LsaEnumerateTrustedDomainsEx**</span></span>](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)
</dt> </dl>

 

 




