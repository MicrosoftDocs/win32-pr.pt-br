---
title: Mapeando código de Visual Basic ADSI para código C++
description: A ADSI consiste em mais de 50 interfaces.
ms.assetid: 6316f504-265e-44d4-ba24-e6289065981b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c64a022569a95f38ec1da7a1cb7acf533eb04ca6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105811233"
---
# <a name="mapping-adsi-visual-basic-code-to-c-code"></a><span data-ttu-id="184bd-103">Mapeando código de Visual Basic ADSI para código C++</span><span class="sxs-lookup"><span data-stu-id="184bd-103">Mapping ADSI Visual Basic Code to C++ Code</span></span>

<span data-ttu-id="184bd-104">A ADSI consiste em mais de 50 interfaces.</span><span class="sxs-lookup"><span data-stu-id="184bd-104">ADSI consists of more than 50 interfaces.</span></span> <span data-ttu-id="184bd-105">A maioria das operações de diretório pode ser concluída usando apenas cinco interfaces.</span><span class="sxs-lookup"><span data-stu-id="184bd-105">Most directory operations can be completed using only five interfaces.</span></span> <span data-ttu-id="184bd-106">Eles são:</span><span class="sxs-lookup"><span data-stu-id="184bd-106">They are:</span></span>

-   [<span data-ttu-id="184bd-107">**IADsOpenDSObject**</span><span class="sxs-lookup"><span data-stu-id="184bd-107">**IADsOpenDSObject**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)
-   [<span data-ttu-id="184bd-108">**IADs**</span><span class="sxs-lookup"><span data-stu-id="184bd-108">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
-   [<span data-ttu-id="184bd-109">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="184bd-109">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [<span data-ttu-id="184bd-110">**IDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="184bd-110">**IDirectoryObject**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [<span data-ttu-id="184bd-111">**IDirectorySearch**</span><span class="sxs-lookup"><span data-stu-id="184bd-111">**IDirectorySearch**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

<span data-ttu-id="184bd-112">A tabela a seguir lista os mapeamentos do código ADSI VB/VBS para o código C++.</span><span class="sxs-lookup"><span data-stu-id="184bd-112">The following table lists mappings from ADSI VB/VBS code to C++ code.</span></span> <span data-ttu-id="184bd-113">Lembre-se de que essa não é uma lista completa.</span><span class="sxs-lookup"><span data-stu-id="184bd-113">Be aware that this is not a complete list.</span></span>



| <span data-ttu-id="184bd-114">Código VBS</span><span class="sxs-lookup"><span data-stu-id="184bd-114">VBS Code</span></span>                           | <span data-ttu-id="184bd-115">Código VC</span><span class="sxs-lookup"><span data-stu-id="184bd-115">VC Code</span></span>                                                               |
|------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="184bd-116">Set obj = GetObject ()</span><span class="sxs-lookup"><span data-stu-id="184bd-116">Set obj = GetObject()</span></span>              | <span data-ttu-id="184bd-117">HR = AdsGetObject ()</span><span class="sxs-lookup"><span data-stu-id="184bd-117">hr = AdsGetObject()</span></span>                                                   |
| <span data-ttu-id="184bd-118">obj. Put obj. Obtenha o obj. Primária</span><span class="sxs-lookup"><span data-stu-id="184bd-118">obj.Put obj.Get obj.Parent</span></span>         | <span data-ttu-id="184bd-119">IADs ou IDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="184bd-119">IADs or IDirectoryObject</span></span>                                              |
| <span data-ttu-id="184bd-120">obj. Criar obj. Excluir obj. MoveHere</span><span class="sxs-lookup"><span data-stu-id="184bd-120">obj.Create obj.Delete obj.MoveHere</span></span> | <span data-ttu-id="184bd-121">IADsContainer</span><span class="sxs-lookup"><span data-stu-id="184bd-121">IADsContainer</span></span>                                                         |
| <span data-ttu-id="184bd-122">Para cada...</span><span class="sxs-lookup"><span data-stu-id="184bd-122">For each…</span></span> <span data-ttu-id="184bd-123">em...</span><span class="sxs-lookup"><span data-stu-id="184bd-123">in…</span></span>                      | <span data-ttu-id="184bd-124">AdsBuildEnumerator() ADsEnumerateNext()</span><span class="sxs-lookup"><span data-stu-id="184bd-124">AdsBuildEnumerator() ADsEnumerateNext()</span></span>                               |
| <span data-ttu-id="184bd-125">Conexão, comando, conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="184bd-125">Connection, Command, RecordSet</span></span>     | <span data-ttu-id="184bd-126">IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="184bd-126">IDirectorySearch</span></span>                                                      |
| <span data-ttu-id="184bd-127">Descritor de segurança, ACL, ACE</span><span class="sxs-lookup"><span data-stu-id="184bd-127">Security descriptor, ACL, ACE</span></span>      | <span data-ttu-id="184bd-128">IADsSecurityDescriptor, IADsAccessControlList, IADsAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="184bd-128">IADsSecurityDescriptor, IADsAccessControlList, IADsAccessControlEntry</span></span> |



 

 

 




