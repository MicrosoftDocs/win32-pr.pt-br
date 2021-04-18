---
description: Define o comportamento de solicitação do repositório protegido sempre que ele exibe uma interface do usuário.
ms.assetid: 413bcb33-5fe9-4ba1-b65f-3e53a7cbf70c
title: Estrutura de PST_PROMPTINFO (Pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_PROMPTINFO
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: da499ea3d6f5037e9f1e745771112840a462f11d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771773"
---
# <a name="pst_promptinfo-structure"></a><span data-ttu-id="5bd1d-103">Estrutura de PROMPTINFO de PST \_</span><span class="sxs-lookup"><span data-stu-id="5bd1d-103">PST\_PROMPTINFO structure</span></span>

<span data-ttu-id="5bd1d-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5bd1d-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="5bd1d-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="5bd1d-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="5bd1d-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="5bd1d-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="5bd1d-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="5bd1d-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="5bd1d-108">Define o comportamento de solicitação do repositório protegido sempre que ele exibe uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="5bd1d-108">Defines the prompting behavior of the Protected Store whenever it displays a user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bd1d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5bd1d-109">Syntax</span></span>


```C++
typedef struct {
  DWORD      cbSize;
  DWORD      dwPromptFlags;
  DWORD_PTR  hwndApp;
  LPCWSTR    szPrompt;
} PST_PROMPTINFO, *PPST_PROMPTINFO;
```



## <a name="members"></a><span data-ttu-id="5bd1d-110">Membros</span><span class="sxs-lookup"><span data-stu-id="5bd1d-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="5bd1d-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="5bd1d-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="5bd1d-112">O tamanho desta estrutura.</span><span class="sxs-lookup"><span data-stu-id="5bd1d-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="5bd1d-113">**dwPromptFlags**</span><span class="sxs-lookup"><span data-stu-id="5bd1d-113">**dwPromptFlags**</span></span>
</dt> <dd>

<span data-ttu-id="5bd1d-114">Este sinalizador é ignorado.</span><span class="sxs-lookup"><span data-stu-id="5bd1d-114">This flag is ignored.</span></span>



| <span data-ttu-id="5bd1d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="5bd1d-115">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="5bd1d-116">Significado</span><span class="sxs-lookup"><span data-stu-id="5bd1d-116">Meaning</span></span>                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="PST_PF_ALWAYS_SHOW"></span><span id="pst_pf_always_show"></span><dl> <span data-ttu-id="5bd1d-117"><dt>**PST \_ O PF \_ sempre \_ mostra**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="5bd1d-117"><dt>**PST\_PF\_ALWAYS\_SHOW**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="5bd1d-118">Solicita que o provedor mostre a caixa de diálogo de prompt para o usuário, mesmo que ele não seja necessário para esse acesso.</span><span class="sxs-lookup"><span data-stu-id="5bd1d-118">Requests that the provider show the prompt dialog to the user even if it is not required for this access.</span></span> <br/> |
| <span id="PST_PF_NEVER_SHOW"></span><span id="pst_pf_never_show"></span><dl> <span data-ttu-id="5bd1d-119"><dt>**PST \_ PF \_ nunca \_ Mostrar**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="5bd1d-119"><dt>**PST\_PF\_NEVER\_SHOW**</dt> <dt>0x00000002</dt></span></span> </dl>    | <span data-ttu-id="5bd1d-120">Não mostrar a caixa de diálogo de prompt para o usuário.</span><span class="sxs-lookup"><span data-stu-id="5bd1d-120">Do not show the prompt dialog to the user.</span></span><br/>                                                                 |



 

</dd> <dt>

<span data-ttu-id="5bd1d-121">**hwndApp**</span><span class="sxs-lookup"><span data-stu-id="5bd1d-121">**hwndApp**</span></span>
</dt> <dd>

<span data-ttu-id="5bd1d-122">O identificador para a janela pai da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="5bd1d-122">The handle to the parent window for the user interface.</span></span> <span data-ttu-id="5bd1d-123">O membro **hwndApp** determina onde a interface do usuário é exibida.</span><span class="sxs-lookup"><span data-stu-id="5bd1d-123">The **hwndApp** member determines where the user interface appears.</span></span> <span data-ttu-id="5bd1d-124">Se **NULL** for passado, a área de trabalho será considerada a janela pai.</span><span class="sxs-lookup"><span data-stu-id="5bd1d-124">If **NULL** is passed, the desktop is considered to be the parent window.</span></span>

</dd> <dt>

<span data-ttu-id="5bd1d-125">**szPrompt**</span><span class="sxs-lookup"><span data-stu-id="5bd1d-125">**szPrompt**</span></span>
</dt> <dd>

<span data-ttu-id="5bd1d-126">A cadeia de caracteres do prompt.</span><span class="sxs-lookup"><span data-stu-id="5bd1d-126">The prompt string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5bd1d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bd1d-127">Requirements</span></span>



| <span data-ttu-id="5bd1d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bd1d-128">Requirement</span></span> | <span data-ttu-id="5bd1d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="5bd1d-129">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5bd1d-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5bd1d-130">Header</span></span><br/> | <dl> <span data-ttu-id="5bd1d-131"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bd1d-131"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bd1d-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="5bd1d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bd1d-133">**DeleteItem**</span><span class="sxs-lookup"><span data-stu-id="5bd1d-133">**DeleteItem**</span></span>](ipstore-deleteitem.md)
</dt> <dt>

[<span data-ttu-id="5bd1d-134">**OpenItem**</span><span class="sxs-lookup"><span data-stu-id="5bd1d-134">**OpenItem**</span></span>](ipstore-openitem.md)
</dt> <dt>

[<span data-ttu-id="5bd1d-135">**ReadItem**</span><span class="sxs-lookup"><span data-stu-id="5bd1d-135">**ReadItem**</span></span>](ipstore-readitem.md)
</dt> <dt>

[<span data-ttu-id="5bd1d-136">**WriteItem**</span><span class="sxs-lookup"><span data-stu-id="5bd1d-136">**WriteItem**</span></span>](ipstore-writeitem.md)
</dt> </dl>

 

 
