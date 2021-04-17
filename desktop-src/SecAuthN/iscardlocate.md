---
description: A interface ISCardLocate fornece serviços para localizar um cartão inteligente por seu nome.
ms.assetid: add00705-69d5-4562-a74f-94c6864f6bd8
title: Interface ISCardLocate (Scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate
- ISCardLocate.ConfigureCardGuidSearch
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e65a8315e796db032dfa6e9cb8898d19437bad05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748465"
---
# <a name="iscardlocate-interface"></a><span data-ttu-id="accb0-103">Interface ISCardLocate</span><span class="sxs-lookup"><span data-stu-id="accb0-103">ISCardLocate interface</span></span>

<span data-ttu-id="accb0-104">\[A interface **ISCardLocate** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="accb0-104">\[The **ISCardLocate** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="accb0-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="accb0-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="accb0-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="accb0-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="accb0-107">A interface **ISCardLocate** fornece serviços para localizar um [*cartão inteligente*](../secgloss/s-gly.md) por seu nome.</span><span class="sxs-lookup"><span data-stu-id="accb0-107">The **ISCardLocate** interface provides services for locating a [*smart card*](../secgloss/s-gly.md) by its name.</span></span>

<span data-ttu-id="accb0-108">Essa interface pode exibir a interface do [*usuário*](../secgloss/u-gly.md) do cartão inteligente, se necessário.</span><span class="sxs-lookup"><span data-stu-id="accb0-108">This interface can display the smart card [*user interface*](../secgloss/u-gly.md) if it is required.</span></span>

<span data-ttu-id="accb0-109">O cenário a seguir mostra um uso típico da interface **ISCardLocate** .</span><span class="sxs-lookup"><span data-stu-id="accb0-109">The following scenario shows a typical use of the **ISCardLocate** interface.</span></span> <span data-ttu-id="accb0-110">A interface **ISCardLocate** é usada para criar uma APDU ( [*unidade de dados de protocolo de aplicativo*](../secgloss/a-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="accb0-110">The **ISCardLocate** interface is used to build an [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

<span data-ttu-id="accb0-111">**Para localizar um cartão específico usando seu nome**</span><span class="sxs-lookup"><span data-stu-id="accb0-111">**To locate a specific card using its name**</span></span>

1.  <span data-ttu-id="accb0-112">Crie uma interface **ISCardLocate** .</span><span class="sxs-lookup"><span data-stu-id="accb0-112">Create an **ISCardLocate** interface.</span></span>
2.  <span data-ttu-id="accb0-113">Chame [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) para procurar um nome de cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="accb0-113">Call [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) to search for a smart card name.</span></span>
3.  <span data-ttu-id="accb0-114">Chame [**FindCard**](iscardlocate-findcard.md) para pesquisar o cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="accb0-114">Call [**FindCard**](iscardlocate-findcard.md) to search for the smart card.</span></span>
4.  <span data-ttu-id="accb0-115">Interpretar os resultados.</span><span class="sxs-lookup"><span data-stu-id="accb0-115">Interpret the results.</span></span>
5.  <span data-ttu-id="accb0-116">Libere a interface **ISCardLocate** .</span><span class="sxs-lookup"><span data-stu-id="accb0-116">Release the **ISCardLocate** interface.</span></span>

## <a name="members"></a><span data-ttu-id="accb0-117">Membros</span><span class="sxs-lookup"><span data-stu-id="accb0-117">Members</span></span>

<span data-ttu-id="accb0-118">A interface **ISCardLocate** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="accb0-118">The **ISCardLocate** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="accb0-119">**ISCardLocate** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="accb0-119">**ISCardLocate** also has these types of members:</span></span>

-   [<span data-ttu-id="accb0-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="accb0-120">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="accb0-121">Métodos</span><span class="sxs-lookup"><span data-stu-id="accb0-121">Methods</span></span>

<span data-ttu-id="accb0-122">A interface **ISCardLocate** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="accb0-122">The **ISCardLocate** interface has these methods.</span></span>



| <span data-ttu-id="accb0-123">Método</span><span class="sxs-lookup"><span data-stu-id="accb0-123">Method</span></span>                                                                  | <span data-ttu-id="accb0-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="accb0-124">Description</span></span>                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| <span data-ttu-id="accb0-125">**ConfigureCardGuidSearch**</span><span class="sxs-lookup"><span data-stu-id="accb0-125">**ConfigureCardGuidSearch**</span></span>                                             | <span data-ttu-id="accb0-126">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="accb0-126">Reserved for future use.</span></span><br/>                                        |
| [<span data-ttu-id="accb0-127">**ConfigureCardNameSearch**</span><span class="sxs-lookup"><span data-stu-id="accb0-127">**ConfigureCardNameSearch**</span></span>](iscardlocate-configurecardnamesearch.md) | <span data-ttu-id="accb0-128">Especifica o nome do cartão a ser usado na pesquisa.</span><span class="sxs-lookup"><span data-stu-id="accb0-128">Specifies the card name to be used in the search.</span></span><br/>               |
| [<span data-ttu-id="accb0-129">**FindCard**</span><span class="sxs-lookup"><span data-stu-id="accb0-129">**FindCard**</span></span>](iscardlocate-findcard.md)                               | <span data-ttu-id="accb0-130">Pesquisa o cartão inteligente e abre uma conexão válida com ele.</span><span class="sxs-lookup"><span data-stu-id="accb0-130">Searches for the smart card and opens a valid connection to it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="accb0-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="accb0-131">Requirements</span></span>



| <span data-ttu-id="accb0-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="accb0-132">Requirement</span></span> | <span data-ttu-id="accb0-133">Valor</span><span class="sxs-lookup"><span data-stu-id="accb0-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="accb0-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="accb0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="accb0-135">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="accb0-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="accb0-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="accb0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="accb0-137">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="accb0-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="accb0-138">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="accb0-138">End of client support</span></span><br/>    | <span data-ttu-id="accb0-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="accb0-139">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="accb0-140">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="accb0-140">End of server support</span></span><br/>    | <span data-ttu-id="accb0-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="accb0-141">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="accb0-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="accb0-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="accb0-143"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="accb0-143"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="accb0-144">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="accb0-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="accb0-145"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="accb0-145"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="accb0-146">DLL</span><span class="sxs-lookup"><span data-stu-id="accb0-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="accb0-147"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="accb0-147"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="accb0-148">IID</span><span class="sxs-lookup"><span data-stu-id="accb0-148">IID</span></span><br/>                      | <span data-ttu-id="accb0-149">IID \_ ISCardLocate é definido como 1461AACD-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="accb0-149">IID\_ISCardLocate is defined as 1461AACD-6810-11D0-918F-00AA00C18068</span></span><br/>         |



 

 
