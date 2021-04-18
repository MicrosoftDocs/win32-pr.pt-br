---
description: Define os dados a serem usados na verificação de Authenticode da Microsoft dos dados do item.
ms.assetid: 73c0e84f-7d59-4efa-927d-af8d7305bc9d
title: Estrutura de PST_AUTHENTICODEDATA (Pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_AUTHENTICODEDATA
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: ff53526febcc8eab1a95285ffa3dcb59fe628238
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749926"
---
# <a name="pst_authenticodedata-structure"></a><span data-ttu-id="98ff8-103">Estrutura de AUTHENTICODEDATA de PST \_</span><span class="sxs-lookup"><span data-stu-id="98ff8-103">PST\_AUTHENTICODEDATA structure</span></span>

<span data-ttu-id="98ff8-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="98ff8-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="98ff8-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="98ff8-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="98ff8-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="98ff8-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="98ff8-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="98ff8-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="98ff8-108">Define os dados a serem usados na verificação de Authenticode da Microsoft dos dados do item.</span><span class="sxs-lookup"><span data-stu-id="98ff8-108">Defines data to be used in Microsoft Authenticode verification of item data.</span></span>

## <a name="syntax"></a><span data-ttu-id="98ff8-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98ff8-109">Syntax</span></span>


```C++
typedef struct {
  DWORD    cbSize;
  DWORD    dwModifiers;
  LPCWSTR  szRootCA;
  LPCWSTR  szIssuer;
  LPCWSTR  szPublisher;
  LPCWSTR  szProgramName;
} PST_AUTHENTICODEDATA, *PPST_AUTHENTICODE_DATA;
```



## <a name="members"></a><span data-ttu-id="98ff8-110">Membros</span><span class="sxs-lookup"><span data-stu-id="98ff8-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="98ff8-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="98ff8-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="98ff8-112">O tamanho desta estrutura.</span><span class="sxs-lookup"><span data-stu-id="98ff8-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="98ff8-113">**dwModifiers**</span><span class="sxs-lookup"><span data-stu-id="98ff8-113">**dwModifiers**</span></span>
</dt> <dd>

<span data-ttu-id="98ff8-114">Um valor que identifica o modificador que um de uma cadeia de chamadores deve verificar.</span><span class="sxs-lookup"><span data-stu-id="98ff8-114">A value that identifies the modifier that one of a chain of callers must verify.</span></span>



| <span data-ttu-id="98ff8-115">Valor</span><span class="sxs-lookup"><span data-stu-id="98ff8-115">Value</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="98ff8-116">Significado</span><span class="sxs-lookup"><span data-stu-id="98ff8-116">Meaning</span></span>                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_AC_SINGLE_CALLER"></span><span id="pst_ac_single_caller"></span><dl> <span data-ttu-id="98ff8-117"><dt>**PST \_ \_ \_ Chamador único de AC**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="98ff8-117"><dt>**PST\_AC\_SINGLE\_CALLER**</dt> <dt>0</dt></span></span> </dl>           | <span data-ttu-id="98ff8-118">Apenas um único nível na cadeia de chamadas para Pstore.</span><span class="sxs-lookup"><span data-stu-id="98ff8-118">Only a single level in the call chain to PStore.</span></span> <span data-ttu-id="98ff8-119">O chamador passa a verificação de verificação.</span><span class="sxs-lookup"><span data-stu-id="98ff8-119">The caller passes the verification check.</span></span> <span data-ttu-id="98ff8-120">A imagem especificada é o chamador imediato e é um aplicativo (. exe).</span><span class="sxs-lookup"><span data-stu-id="98ff8-120">The specified image is the immediate caller, and is an application (.exe).</span></span><br/>              |
| <span id="PST_AC_TOP_LEVEL_CALLER"></span><span id="pst_ac_top_level_caller"></span><dl> <span data-ttu-id="98ff8-121"><dt>**PST \_ \_ \_ \_ Chamador 1 de nível superior de AC**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="98ff8-121"><dt>**PST\_AC\_TOP\_LEVEL\_CALLER**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="98ff8-122">O chamador de nível superior deve passar na verificação, mas pode haver DLLs intermediárias.</span><span class="sxs-lookup"><span data-stu-id="98ff8-122">The top-level caller must pass the check, but there may be intermediate DLLs.</span></span> <span data-ttu-id="98ff8-123">A imagem especificada não é necessariamente o chamador imediato e é um aplicativo (. exe).</span><span class="sxs-lookup"><span data-stu-id="98ff8-123">The specified image is not necessarily the immediate caller, and is an application (.exe).</span></span><br/>           |
| <span id="PST_AC_IMMEDIATE_CALLER"></span><span id="pst_ac_immediate_caller"></span><dl> <span data-ttu-id="98ff8-124"><dt>**PST \_ \_ \_ Chamador imediato de AC**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="98ff8-124"><dt>**PST\_AC\_IMMEDIATE\_CALLER**</dt> <dt>2</dt></span></span> </dl>  | <span data-ttu-id="98ff8-125">O chamador imediato deve passar na verificação, mas não precisa ser o processo de nível superior.</span><span class="sxs-lookup"><span data-stu-id="98ff8-125">The immediate caller must pass the check, but need not be the top-level process.</span></span> <span data-ttu-id="98ff8-126">A imagem especificada é o chamador imediato, e a imagem pode ser um aplicativo (. exe) ou uma DLL.</span><span class="sxs-lookup"><span data-stu-id="98ff8-126">The specified image is the immediate caller, and the image can be an application (.exe) or a DLL.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="98ff8-127">**szRootCA**</span><span class="sxs-lookup"><span data-stu-id="98ff8-127">**szRootCA**</span></span>
</dt> <dd>

<span data-ttu-id="98ff8-128">Um ponteiro para uma cadeia de caracteres larga que representa a AC (autoridade de certificação) raiz do certificado; Use **NULL** para usar qualquer AC disponível.</span><span class="sxs-lookup"><span data-stu-id="98ff8-128">A pointer to a wide character string that represents the root certification authority (CA) for the certificate; use **NULL** to use any available CA.</span></span>

</dd> <dt>

<span data-ttu-id="98ff8-129">**szIssuer**</span><span class="sxs-lookup"><span data-stu-id="98ff8-129">**szIssuer**</span></span>
</dt> <dd>

<span data-ttu-id="98ff8-130">Um ponteiro para uma cadeia de caracteres larga que representa a autoridade de certificação que emitiu o certificado; Use **NULL** para usar qualquer AC disponível.</span><span class="sxs-lookup"><span data-stu-id="98ff8-130">A pointer to a wide character string that represents the CA that issued the certificate; use **NULL** to use any available CA.</span></span>

</dd> <dt>

<span data-ttu-id="98ff8-131">**szPublisher**</span><span class="sxs-lookup"><span data-stu-id="98ff8-131">**szPublisher**</span></span>
</dt> <dd>

<span data-ttu-id="98ff8-132">Um ponteiro para uma cadeia de caracteres larga que representa o fornecedor do software; Use **NULL** para usar qualquer AC disponível.</span><span class="sxs-lookup"><span data-stu-id="98ff8-132">A pointer to a wide character string that represents the software publisher; use **NULL** to use any available CA.</span></span>

</dd> <dt>

<span data-ttu-id="98ff8-133">**szProgramName**</span><span class="sxs-lookup"><span data-stu-id="98ff8-133">**szProgramName**</span></span>
</dt> <dd>

<span data-ttu-id="98ff8-134">Um ponteiro para uma cadeia de caracteres larga que representa o nome do programa; Use **NULL** para usar qualquer AC disponível.</span><span class="sxs-lookup"><span data-stu-id="98ff8-134">A pointer to a wide character string that represents the program name; use **NULL** to use any available CA.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98ff8-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98ff8-135">Requirements</span></span>



| <span data-ttu-id="98ff8-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="98ff8-136">Requirement</span></span> | <span data-ttu-id="98ff8-137">Valor</span><span class="sxs-lookup"><span data-stu-id="98ff8-137">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="98ff8-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="98ff8-138">Header</span></span><br/> | <dl> <span data-ttu-id="98ff8-139"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="98ff8-139"><dt>Pstore.h</dt></span></span> </dl> |



 

 
