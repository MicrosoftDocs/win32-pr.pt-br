---
description: A interface ISCardDatabase fornece os métodos para executar as operações de banco de dados do Gerenciador de recursos de cartão inteligente.
ms.assetid: 56db3bc0-33c3-4b9c-a4a7-374fc491d8fd
title: Interface ISCardDatabase (Scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1ae74c813b4d95cc9d02694ca9edb5c030e4f342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752137"
---
# <a name="iscarddatabase-interface"></a><span data-ttu-id="b6a57-103">Interface ISCardDatabase</span><span class="sxs-lookup"><span data-stu-id="b6a57-103">ISCardDatabase interface</span></span>

<span data-ttu-id="b6a57-104">\[A interface **ISCardDatabase** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="b6a57-104">\[The **ISCardDatabase** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b6a57-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b6a57-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b6a57-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="b6a57-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b6a57-107">A interface **ISCardDatabase** fornece os métodos para executar as operações de banco de dados [*do Gerenciador de recursos*](../secgloss/r-gly.md) de [*cartão inteligente*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b6a57-107">The **ISCardDatabase** interface provides the methods for performing the [*smart card*](../secgloss/s-gly.md) [*resource manager's*](../secgloss/r-gly.md) database operations.</span></span> <span data-ttu-id="b6a57-108">Essas operações incluem a listagem de cartões inteligentes conhecidos, [*leitores*](../secgloss/r-gly.md)e grupos de leitores, além de recuperar as interfaces com suporte por um cartão inteligente e seu [*provedor de serviços primário*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b6a57-108">These operations include listing known smart cards, [*readers*](../secgloss/r-gly.md), and reader groups, plus retrieving the interfaces supported by a smart card and its [*primary service provider*](../secgloss/p-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="b6a57-109">O identificador do provedor de serviços primário é um GUID COM que pode ser usado para instanciar e usar os objetos COM para um cartão específico.</span><span class="sxs-lookup"><span data-stu-id="b6a57-109">The identifier of the primary service provider is a COM GUID that can be used to instantiate and use the COM objects for a specific card.</span></span>

 

<span data-ttu-id="b6a57-110">O exemplo a seguir mostra um uso típico da interface **ISCardDatabase** .</span><span class="sxs-lookup"><span data-stu-id="b6a57-110">The following example shows a typical use of the **ISCardDatabase** interface.</span></span> <span data-ttu-id="b6a57-111">Nesse caso, a interface **ISCardDatabase** é usada para listar todos os cartões inteligentes conhecidos.</span><span class="sxs-lookup"><span data-stu-id="b6a57-111">In this case, the **ISCardDatabase** interface is used to list all the known smart cards.</span></span>

<span data-ttu-id="b6a57-112">**Para enviar uma transação para um cartão específico**</span><span class="sxs-lookup"><span data-stu-id="b6a57-112">**To submit a transaction to a specific card**</span></span>

1.  <span data-ttu-id="b6a57-113">Crie uma interface **ISCardDatabase** .</span><span class="sxs-lookup"><span data-stu-id="b6a57-113">Create an **ISCardDatabase** interface.</span></span>
2.  <span data-ttu-id="b6a57-114">Chame [**ListCards**](iscarddatabase-listcards.md) para recuperar todos os cartões inteligentes conhecidos com base em uma [*cadeia de caracteres ATR*](../secgloss/a-gly.md) ou em suas interfaces com suporte.</span><span class="sxs-lookup"><span data-stu-id="b6a57-114">Call [**ListCards**](iscarddatabase-listcards.md) to retrieve all the known smart cards based on an [*ATR string*](../secgloss/a-gly.md) or their supported interfaces.</span></span>
3.  <span data-ttu-id="b6a57-115">Libere a interface **ISCardDatabase** .</span><span class="sxs-lookup"><span data-stu-id="b6a57-115">Release the **ISCardDatabase** interface.</span></span>

## <a name="members"></a><span data-ttu-id="b6a57-116">Membros</span><span class="sxs-lookup"><span data-stu-id="b6a57-116">Members</span></span>

<span data-ttu-id="b6a57-117">A interface **ISCardDatabase** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="b6a57-117">The **ISCardDatabase** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="b6a57-118">**ISCardDatabase** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b6a57-118">**ISCardDatabase** also has these types of members:</span></span>

-   [<span data-ttu-id="b6a57-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="b6a57-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b6a57-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="b6a57-120">Methods</span></span>

<span data-ttu-id="b6a57-121">A interface **ISCardDatabase** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b6a57-121">The **ISCardDatabase** interface has these methods.</span></span>



| <span data-ttu-id="b6a57-122">Método</span><span class="sxs-lookup"><span data-stu-id="b6a57-122">Method</span></span>                                                          | <span data-ttu-id="b6a57-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6a57-123">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6a57-124">**GetProviderCardId**</span><span class="sxs-lookup"><span data-stu-id="b6a57-124">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)   | <span data-ttu-id="b6a57-125">Recupera o identificador do [*provedor de serviços primário*](../secgloss/p-gly.md) para um cartão inteligente específico.</span><span class="sxs-lookup"><span data-stu-id="b6a57-125">Retrieves the identifier of the [*primary service provider*](../secgloss/p-gly.md) for a specific smart card.</span></span><br/> |
| [<span data-ttu-id="b6a57-126">**ListCardInterfaces**</span><span class="sxs-lookup"><span data-stu-id="b6a57-126">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md) | <span data-ttu-id="b6a57-127">Recupera os identificadores de interface (GUIDs) de todas as interfaces com suporte em um cartão inteligente específico.</span><span class="sxs-lookup"><span data-stu-id="b6a57-127">Retrieves the interface identifiers (GUIDs) of all the interfaces supported by a specific smart card.</span></span><br/>                                                                                 |
| [<span data-ttu-id="b6a57-128">**ListCards**</span><span class="sxs-lookup"><span data-stu-id="b6a57-128">**ListCards**</span></span>](iscarddatabase-listcards.md)                   | <span data-ttu-id="b6a57-129">Recupera todos os nomes de cartão inteligente que correspondem a um conjunto específico de GUIDs (identificadores de interface) ou uma [*cadeia de caracteres ATR*](../secgloss/a-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b6a57-129">Retrieves all the smart card names that match a specific set of interface identifiers (GUIDs) or an [*ATR string*](../secgloss/a-gly.md).</span></span><br/> |
| [<span data-ttu-id="b6a57-130">**ListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="b6a57-130">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)     | <span data-ttu-id="b6a57-131">Recupera os nomes dos [*grupos de leitores*](../secgloss/r-gly.md) dos quais o Gerenciador de recursos tem conhecimento.</span><span class="sxs-lookup"><span data-stu-id="b6a57-131">Retrieves the names of the [*reader groups*](../secgloss/r-gly.md) that the resource manager has knowledge of.</span></span><br/>                        |
| [<span data-ttu-id="b6a57-132">**ListReaders**</span><span class="sxs-lookup"><span data-stu-id="b6a57-132">**ListReaders**</span></span>](iscarddatabase-listreaders.md)               | <span data-ttu-id="b6a57-133">Recupere os nomes dos [*leitores*](../secgloss/r-gly.md) dos quais o Gerenciador de recursos tem conhecimento.</span><span class="sxs-lookup"><span data-stu-id="b6a57-133">Retrieve the names of the [*readers*](../secgloss/r-gly.md) of which the resource manager has knowledge.</span></span><br/>                                          |



 

## <a name="requirements"></a><span data-ttu-id="b6a57-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6a57-134">Requirements</span></span>



| <span data-ttu-id="b6a57-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6a57-135">Requirement</span></span> | <span data-ttu-id="b6a57-136">Valor</span><span class="sxs-lookup"><span data-stu-id="b6a57-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6a57-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6a57-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b6a57-138">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b6a57-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b6a57-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6a57-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b6a57-140">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b6a57-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b6a57-141">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b6a57-141">End of client support</span></span><br/>    | <span data-ttu-id="b6a57-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b6a57-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="b6a57-143">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="b6a57-143">End of server support</span></span><br/>    | <span data-ttu-id="b6a57-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b6a57-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="b6a57-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6a57-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6a57-146"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6a57-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="b6a57-147">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b6a57-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="b6a57-148"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b6a57-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b6a57-149">DLL</span><span class="sxs-lookup"><span data-stu-id="b6a57-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6a57-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6a57-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b6a57-151">IID</span><span class="sxs-lookup"><span data-stu-id="b6a57-151">IID</span></span><br/>                      | <span data-ttu-id="b6a57-152">IID \_ ISCardDatabase é definido como 1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="b6a57-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



 

 
