---
description: Identificador para o objeto de política local.
ms.assetid: f5878d27-558b-4ef1-9401-1277e740c61d
title: LSA_HANDLE (Ntsecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07bd71a14666dde7bb92e439159a55dd71706612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011075"
---
# <a name="lsa_handle"></a><span data-ttu-id="8d664-103">identificador de LSA \_</span><span class="sxs-lookup"><span data-stu-id="8d664-103">LSA\_HANDLE</span></span>

<span data-ttu-id="8d664-104">O tipo de dados de **\_ identificador LSA** é um identificador para o objeto de [**política**](policy-object.md) local.</span><span class="sxs-lookup"><span data-stu-id="8d664-104">The **LSA\_HANDLE** data type is a handle to the local [**Policy**](policy-object.md) object.</span></span>


```C++
typedef PVOID LSA_HANDLE, *PLSA_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="8d664-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d664-105">Remarks</span></span>

<span data-ttu-id="8d664-106">Antes de poder usar a API de diretiva local, seu aplicativo deve abrir um identificador para um objeto de [**política**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="8d664-106">Before you can use the local policy API your application must open a handle to a [**Policy**](policy-object.md) object.</span></span> <span data-ttu-id="8d664-107">Para fazer isso, chame [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy).</span><span class="sxs-lookup"><span data-stu-id="8d664-107">To do this, call [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy).</span></span> <span data-ttu-id="8d664-108">Essa função retorna um identificador que seu aplicativo pode especificar em chamadas de função de política LSA subsequentes.</span><span class="sxs-lookup"><span data-stu-id="8d664-108">This function returns a handle that your application can then specify in subsequent LSA policy function calls.</span></span>

<span data-ttu-id="8d664-109">Cada identificador tem um conjunto associado de permissões que determinam as operações que seu aplicativo pode executar no objeto de [**política**](policy-object.md) usando o identificador.</span><span class="sxs-lookup"><span data-stu-id="8d664-109">Each handle has an associated set of permissions that determine the operations your application can perform on the [**Policy**](policy-object.md) object by using the handle.</span></span> <span data-ttu-id="8d664-110">Seu aplicativo pode abrir mais de um identificador para o objeto de **política** por vez.</span><span class="sxs-lookup"><span data-stu-id="8d664-110">Your application can open more than one handle to the **Policy** object at a time.</span></span> <span data-ttu-id="8d664-111">Quando um identificador não é mais necessário, seu aplicativo deve fechá-lo chamando [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose).</span><span class="sxs-lookup"><span data-stu-id="8d664-111">When a handle is no longer required, your application should close it by calling [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d664-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d664-112">Requirements</span></span>



| <span data-ttu-id="8d664-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d664-113">Requirement</span></span> | <span data-ttu-id="8d664-114">Valor</span><span class="sxs-lookup"><span data-stu-id="8d664-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d664-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d664-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8d664-116">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8d664-116">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8d664-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d664-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8d664-118">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8d664-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8d664-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8d664-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d664-120"><dt>Ntsecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d664-120"><dt>Ntsecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d664-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d664-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d664-122">**LsaClose**</span><span class="sxs-lookup"><span data-stu-id="8d664-122">**LsaClose**</span></span>](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)
</dt> <dt>

[<span data-ttu-id="8d664-123">**LsaOpenPolicy**</span><span class="sxs-lookup"><span data-stu-id="8d664-123">**LsaOpenPolicy**</span></span>](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)
</dt> </dl>

 

