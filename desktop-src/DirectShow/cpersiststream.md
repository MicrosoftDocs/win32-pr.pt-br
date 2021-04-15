---
description: CPersistStream é a classe base para propriedades persistentes de filtros (ou seja, propriedades de filtro em grafos salvos).
ms.assetid: 8073e2be-aaf9-4b01-a7d5-bab5c1dcc19b
title: Classe CPersistStream
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream
api_type:
- COM
api_location: ''
ms.openlocfilehash: 690a0f45fab7c3612d215a859798460abc81728e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500233"
---
# <a name="cpersiststream-class"></a><span data-ttu-id="77c13-103">Classe CPersistStream</span><span class="sxs-lookup"><span data-stu-id="77c13-103">CPersistStream class</span></span>

![hierarquia de classe CPersistStream](images/pstrm01.png)

<span data-ttu-id="77c13-105">`CPersistStream` é a classe base para propriedades persistentes de filtros (ou seja, propriedades de filtro em grafos salvos).</span><span class="sxs-lookup"><span data-stu-id="77c13-105">`CPersistStream` is the base class for persistent properties of filters (that is, filter properties in saved graphs).</span></span>

<span data-ttu-id="77c13-106">A maneira mais simples de usar o `CPersistStream` é:</span><span class="sxs-lookup"><span data-stu-id="77c13-106">The simplest way to use `CPersistStream` is to:</span></span>

1.  <span data-ttu-id="77c13-107">Organize para o filtro para herdar esta classe.</span><span class="sxs-lookup"><span data-stu-id="77c13-107">Arrange for your filter to inherit this class.</span></span>
2.  <span data-ttu-id="77c13-108">Implemente [**WriteToStream**](cpersiststream-writetostream.md) e [**ReadFromStream**](cpersiststream-readfromstream.md) em sua classe.</span><span class="sxs-lookup"><span data-stu-id="77c13-108">Implement [**WriteToStream**](cpersiststream-writetostream.md) and [**ReadFromStream**](cpersiststream-readfromstream.md) in your class.</span></span> <span data-ttu-id="77c13-109">Eles substituirão as funções aqui, que não fazem nada, mas agem como espaços reservados.</span><span class="sxs-lookup"><span data-stu-id="77c13-109">These will override the functions here, which do nothing but act as placeholders.</span></span>
3.  <span data-ttu-id="77c13-110">Altere seu **NonDelegatingQueryInterface** para tratar de **IPersistStream**.</span><span class="sxs-lookup"><span data-stu-id="77c13-110">Change your **NonDelegatingQueryInterface** to handle **IPersistStream**.</span></span>
4.  <span data-ttu-id="77c13-111">Implemente [**SIZEMAX**](cpersiststream-sizemax.md) para retornar um limite superior no número de bytes de dados que você salvar.</span><span class="sxs-lookup"><span data-stu-id="77c13-111">Implement [**SizeMax**](cpersiststream-sizemax.md) to return an upper bound on the number of bytes of data you save.</span></span>

    <span data-ttu-id="77c13-112">Se você salvar dados Unicode™, lembre-se de que um WCHAR é 2 bytes.</span><span class="sxs-lookup"><span data-stu-id="77c13-112">If you save Unicode™ data, remember that a WCHAR is 2 bytes.</span></span>

5.  <span data-ttu-id="77c13-113">Quando seus dados forem alterados, chame [**SetDirty**](cpersiststream-setdirty.md).</span><span class="sxs-lookup"><span data-stu-id="77c13-113">When your data changes, call [**SetDirty**](cpersiststream-setdirty.md).</span></span>

## <a name="version-numbers"></a><span data-ttu-id="77c13-114">Números de versão</span><span class="sxs-lookup"><span data-stu-id="77c13-114">Version Numbers</span></span>

<span data-ttu-id="77c13-115">Em algum momento, você pode decidir alterar ou estender o formato dos seus dados.</span><span class="sxs-lookup"><span data-stu-id="77c13-115">At some point you might decide to alter or extend the format of your data.</span></span> <span data-ttu-id="77c13-116">Em seguida, você desejará ter um número de versão em todos os fluxos salvos antigos para que possa dizer quando lê-los, se eles representam a forma antiga ou nova.</span><span class="sxs-lookup"><span data-stu-id="77c13-116">You will then wish you had a version number in all the old saved streams so you can tell, when you read them, whether they represent the old or new form.</span></span> <span data-ttu-id="77c13-117">Para ajudá-lo, essa classe grava e lê um número de versão.</span><span class="sxs-lookup"><span data-stu-id="77c13-117">To assist you, this class writes and reads a version number.</span></span> <span data-ttu-id="77c13-118">Quando ele é gravado, ele chama [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) para consultar a versão do software que está sendo usado no momento.</span><span class="sxs-lookup"><span data-stu-id="77c13-118">When it writes, it calls [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) to inquire as to the version of the software being used at the moment.</span></span> <span data-ttu-id="77c13-119">(Na verdade, esse é um número de versão do layout de dados no arquivo.) Ele grava isso como a primeira coisa nos dados.</span><span class="sxs-lookup"><span data-stu-id="77c13-119">(In effect, this is a version number of the data layout in the file.) It writes this as the first thing in the data.</span></span> <span data-ttu-id="77c13-120">Se você quiser alterar a versão, implemente (substitua) **GetSoftwareVersion**.</span><span class="sxs-lookup"><span data-stu-id="77c13-120">If you want to change the version, implement (override) **GetSoftwareVersion**.</span></span> <span data-ttu-id="77c13-121">Ele lê o número de versão do arquivo em **mPS \_ dwFileVersion** antes de chamar [**ReadFromStream**](cpersiststream-readfromstream.md), portanto, no **ReadFromStream** , você pode verificar se o **MPS \_ dwFileVersion** está lendo um arquivo de versão antiga.</span><span class="sxs-lookup"><span data-stu-id="77c13-121">It reads the version number from the file into **mPS\_dwFileVersion** before calling [**ReadFromStream**](cpersiststream-readfromstream.md), so in **ReadFromStream** you can check **mPS\_dwFileVersion** to see if you are reading an old version file.</span></span> <span data-ttu-id="77c13-122">Normalmente, você deve aceitar arquivos cuja versão não é mais nova do que a versão do software que o está lendo.</span><span class="sxs-lookup"><span data-stu-id="77c13-122">Usually you should accept files whose version is no newer than the software version that is reading them.</span></span>

<span data-ttu-id="77c13-123">**CPersistStream** implementa [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream).</span><span class="sxs-lookup"><span data-stu-id="77c13-123">**CPersistStream** implements [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream).</span></span> <span data-ttu-id="77c13-124">Para obter mais informações de implementação, consulte a referência COM no SDK da plataforma Microsoft.</span><span class="sxs-lookup"><span data-stu-id="77c13-124">For more implementation information, see the COM Reference in the Microsoft Platform SDK.</span></span>



| <span data-ttu-id="77c13-125">Membros de Dados Protegidos</span><span class="sxs-lookup"><span data-stu-id="77c13-125">Protected Data Members</span></span>                                          | <span data-ttu-id="77c13-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="77c13-126">Description</span></span>                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="77c13-127">\_DwFileVersion mPS</span><span class="sxs-lookup"><span data-stu-id="77c13-127">mPS\_dwFileVersion</span></span>                                              | <span data-ttu-id="77c13-128">Número de versão do arquivo.</span><span class="sxs-lookup"><span data-stu-id="77c13-128">Version number of the file.</span></span>                                                   |
| <span data-ttu-id="77c13-129">\_FDirty mPS</span><span class="sxs-lookup"><span data-stu-id="77c13-129">mPS\_fDirty</span></span>                                                     | <span data-ttu-id="77c13-130">Os dados para esse fluxo devem ser salvos.</span><span class="sxs-lookup"><span data-stu-id="77c13-130">Data for this stream must be saved.</span></span>                                           |
| <span data-ttu-id="77c13-131">Funções de membro</span><span class="sxs-lookup"><span data-stu-id="77c13-131">Member Functions</span></span>                                                | <span data-ttu-id="77c13-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="77c13-132">Description</span></span>                                                                   |
| [<span data-ttu-id="77c13-133">**CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="77c13-133">**CPersistStream**</span></span>](cpersiststream-cpersiststream.md)         | <span data-ttu-id="77c13-134">Constrói um objeto **CPersistStream** .</span><span class="sxs-lookup"><span data-stu-id="77c13-134">Constructs a **CPersistStream** object.</span></span>                                       |
| [<span data-ttu-id="77c13-135">**Com SetDirty**</span><span class="sxs-lookup"><span data-stu-id="77c13-135">**SetDirty**</span></span>](cpersiststream-setdirty.md)                     | <span data-ttu-id="77c13-136">Indica que o objeto deve ser salvo no fluxo.</span><span class="sxs-lookup"><span data-stu-id="77c13-136">Indicates that the object must be saved to the stream.</span></span>                        |
| <span data-ttu-id="77c13-137">Funções de membro substituíveis</span><span class="sxs-lookup"><span data-stu-id="77c13-137">Overridable Member Functions</span></span>                                    | <span data-ttu-id="77c13-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="77c13-138">Description</span></span>                                                                   |
| [<span data-ttu-id="77c13-139">**GetClassID**</span><span class="sxs-lookup"><span data-stu-id="77c13-139">**GetClassID**</span></span>](cpersiststream-getclassid.md)                 | <span data-ttu-id="77c13-140">Recupera o identificador de classe deste fluxo.</span><span class="sxs-lookup"><span data-stu-id="77c13-140">Retrieves the class identifier of this stream.</span></span>                                |
| [<span data-ttu-id="77c13-141">**GetSoftwareVersion**</span><span class="sxs-lookup"><span data-stu-id="77c13-141">**GetSoftwareVersion**</span></span>](cpersiststream-getsoftwareversion.md) | <span data-ttu-id="77c13-142">Recupera o número de versão para este formato de arquivo.</span><span class="sxs-lookup"><span data-stu-id="77c13-142">Retrieves the version number for this file format.</span></span>                            |
| [<span data-ttu-id="77c13-143">**ReadFromStream**</span><span class="sxs-lookup"><span data-stu-id="77c13-143">**ReadFromStream**</span></span>](cpersiststream-readfromstream.md)         | <span data-ttu-id="77c13-144">Lê os dados do filtro do fluxo.</span><span class="sxs-lookup"><span data-stu-id="77c13-144">Reads the filter's data from the stream.</span></span>                                      |
| [<span data-ttu-id="77c13-145">**SizeMax**</span><span class="sxs-lookup"><span data-stu-id="77c13-145">**SizeMax**</span></span>](cpersiststream-sizemax.md)                       | <span data-ttu-id="77c13-146">Recupera o número de bytes necessários para os dados (sem incluir o número de versão).</span><span class="sxs-lookup"><span data-stu-id="77c13-146">Retrieves the number of bytes needed for data (not including version number).</span></span> |
| [<span data-ttu-id="77c13-147">**WriteToStream**</span><span class="sxs-lookup"><span data-stu-id="77c13-147">**WriteToStream**</span></span>](cpersiststream-writetostream.md)           | <span data-ttu-id="77c13-148">Grava os dados do filtro no fluxo.</span><span class="sxs-lookup"><span data-stu-id="77c13-148">Writes the filter's data to the stream.</span></span>                                       |
| <span data-ttu-id="77c13-149">Métodos IPersistStream</span><span class="sxs-lookup"><span data-stu-id="77c13-149">IPersistStream Methods</span></span>                                          | <span data-ttu-id="77c13-150">Descrição</span><span class="sxs-lookup"><span data-stu-id="77c13-150">Description</span></span>                                                                   |
| [<span data-ttu-id="77c13-151">**GetSizeMax**</span><span class="sxs-lookup"><span data-stu-id="77c13-151">**GetSizeMax**</span></span>](cpersiststream-getsizemax.md)                 | <span data-ttu-id="77c13-152">Recupera o número de bytes necessários para os dados (incluindo o número de versão).</span><span class="sxs-lookup"><span data-stu-id="77c13-152">Retrieves the number of bytes needed for data (including version number).</span></span>     |
| [<span data-ttu-id="77c13-153">**IsDirty**</span><span class="sxs-lookup"><span data-stu-id="77c13-153">**IsDirty**</span></span>](cpersiststream-isdirty.md)                       | <span data-ttu-id="77c13-154">Verifica se o objeto deve ser salvo.</span><span class="sxs-lookup"><span data-stu-id="77c13-154">Checks if the object must be saved.</span></span>                                           |
| [<span data-ttu-id="77c13-155">**Carregar**</span><span class="sxs-lookup"><span data-stu-id="77c13-155">**Load**</span></span>](cpersiststream-load.md)                             | <span data-ttu-id="77c13-156">Carrega os dados do fluxo na memória.</span><span class="sxs-lookup"><span data-stu-id="77c13-156">Loads the data from the stream into memory.</span></span>                                   |
| [<span data-ttu-id="77c13-157">**Salvar**</span><span class="sxs-lookup"><span data-stu-id="77c13-157">**Save**</span></span>](cpersiststream-save.md)                             | <span data-ttu-id="77c13-158">Salva os dados da memória no fluxo.</span><span class="sxs-lookup"><span data-stu-id="77c13-158">Saves the data from memory to the stream.</span></span>                                     |



 

 

 
