---
title: Implementação de arquivo de IEnumSTATPROPSTG-Compound
description: A implementação do arquivo composto da interface IEnumSTATPROPSTG é usada para enumerar Propriedades, resultando em estruturas STATPROPSTG, que contêm dados de propriedade estatística.
ms.assetid: 8fa536f4-cce6-47e4-a860-2f43e48fa469
keywords:
- IEnumSTATPROPSTG Strctd STG, implementação de arquivo composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbffce14016efdb4e2a77d60096b6776e6c2189
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917578"
---
# <a name="ienumstatpropstg-compound-file-implementation"></a><span data-ttu-id="3556e-104">Implementação de arquivo de IEnumSTATPROPSTG-Compound</span><span class="sxs-lookup"><span data-stu-id="3556e-104">IEnumSTATPROPSTG-Compound File Implementation</span></span>

<span data-ttu-id="3556e-105">A implementação do arquivo composto da interface [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) é usada para enumerar Propriedades, resultando em estruturas [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) , que contêm dados de propriedade estatística.</span><span class="sxs-lookup"><span data-stu-id="3556e-105">The compound file implementation of the [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) interface is used to enumerate properties, resulting in [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures, which contain statistical property data.</span></span> <span data-ttu-id="3556e-106">A implementação de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) gerencia os dados estatísticos e é associada a um objeto de armazenamento de arquivo composto atual.</span><span class="sxs-lookup"><span data-stu-id="3556e-106">The implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) manages the statistical data and is associated with a current compound file storage object.</span></span>

<span data-ttu-id="3556e-107">O Construtor na implementação COM de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) cria uma classe que lê todo o conjunto de propriedades e cria uma matriz estática que pode ser compartilhada quando **IEnumSTATPROPSTG:: clone** é chamado.</span><span class="sxs-lookup"><span data-stu-id="3556e-107">The constructor in the COM implementation of [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) creates a class that reads the entire property set, and creates a static array which can be shared when **IEnumSTATPROPSTG::Clone** is called.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="3556e-108">Quando usar</span><span class="sxs-lookup"><span data-stu-id="3556e-108">When to Use</span></span>

<span data-ttu-id="3556e-109">Chame a implementação do arquivo composto de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) para enumerar as estruturas [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) que contêm dados sobre as propriedades dentro do conjunto de propriedades atual.</span><span class="sxs-lookup"><span data-stu-id="3556e-109">Call the compound file implementation of [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) to enumerate the [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures that contain data about the properties within the current property set.</span></span> <span data-ttu-id="3556e-110">Ao usar a implementação do arquivo composto das interfaces de armazenamento de propriedade, chame [**IPropertyStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) para retornar um ponteiro para **IEnumSTATPROPSTG** para gerenciar o objeto de armazenamento de propriedade e os elementos dentro dele.</span><span class="sxs-lookup"><span data-stu-id="3556e-110">When using the compound file implementation of the property storage interfaces, call [**IPropertyStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) to return a pointer to **IEnumSTATPROPSTG** to manage the property storage object and the elements within it.</span></span>

## <a name="remarks"></a><span data-ttu-id="3556e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="3556e-111">Remarks</span></span>

<dl> <dt>

<span data-ttu-id="3556e-112"><span id="IEnumSTATPROPSTG__Next"></span><span id="ienumstatpropstg__next"></span><span id="IENUMSTATPROPSTG__NEXT"></span>[**IEnumSTATPROPSTG:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="3556e-112"><span id="IEnumSTATPROPSTG__Next"></span><span id="ienumstatpropstg__next"></span><span id="IENUMSTATPROPSTG__NEXT"></span>[**IEnumSTATPROPSTG::Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="3556e-113">Obtém a próxima uma ou mais estruturas [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) (o número é especificado pelo parâmetro *celt* ).</span><span class="sxs-lookup"><span data-stu-id="3556e-113">Gets the next one or more [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures (the number is specified by the *celt* parameter).</span></span> <span data-ttu-id="3556e-114">Retornará S \_ OK se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="3556e-114">Returns S\_OK if successful.</span></span>

</dd> <dt>

<span data-ttu-id="3556e-115"><span id="IEnumSTATPROPSTG__Skip"></span><span id="ienumstatpropstg__skip"></span><span id="IENUMSTATPROPSTG__SKIP"></span>[**IEnumSTATPROPSTG:: Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="3556e-115"><span id="IEnumSTATPROPSTG__Skip"></span><span id="ienumstatpropstg__skip"></span><span id="IENUMSTATPROPSTG__SKIP"></span>[**IEnumSTATPROPSTG::Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="3556e-116">Ignora o número de elementos especificados em *celt*.</span><span class="sxs-lookup"><span data-stu-id="3556e-116">Skips the number of elements specified in *celt*.</span></span> <span data-ttu-id="3556e-117">O próximo elemento a ser enumerado por meio de uma chamada para Next torna-se o elemento após os elementos ignorados.</span><span class="sxs-lookup"><span data-stu-id="3556e-117">The next element to be enumerated through a call to Next then becomes the element after the skipped elements.</span></span> <span data-ttu-id="3556e-118">Retorna S \_ OK se os elementos *celt* foram ignorados; retorna s \_ false se menos de *celt* elementos foram ignorados.</span><span class="sxs-lookup"><span data-stu-id="3556e-118">Returns S\_OK if *celt* elements were skipped; returns S\_FALSE if fewer than *celt* elements were skipped.</span></span>

</dd> <dt>

<span data-ttu-id="3556e-119"><span id="IEnumSTATPROPSTG__Reset"></span><span id="ienumstatpropstg__reset"></span><span id="IENUMSTATPROPSTG__RESET"></span>[**IEnumSTATPROPSTG:: Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="3556e-119"><span id="IEnumSTATPROPSTG__Reset"></span><span id="ienumstatpropstg__reset"></span><span id="IENUMSTATPROPSTG__RESET"></span>[**IEnumSTATPROPSTG::Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="3556e-120">Define o cursor para o início da enumeração.</span><span class="sxs-lookup"><span data-stu-id="3556e-120">Sets the cursor to the beginning of the enumeration.</span></span> <span data-ttu-id="3556e-121">Se for bem-sucedido, retornará S \_ OK, caso contrário, retornará STG \_ E \_ INVALIDHANDLE.</span><span class="sxs-lookup"><span data-stu-id="3556e-121">If successful, returns S\_OK, otherwise, returns STG\_E\_INVALIDHANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="3556e-122"><span id="IEnumSTATPROPSTG__Clone"></span><span id="ienumstatpropstg__clone"></span><span id="IENUMSTATPROPSTG__CLONE"></span>[**IEnumSTATPROPSTG:: clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="3556e-122"><span id="IEnumSTATPROPSTG__Clone"></span><span id="ienumstatpropstg__clone"></span><span id="IENUMSTATPROPSTG__CLONE"></span>[**IEnumSTATPROPSTG::Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="3556e-123">Usa o construtor para o [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) para criar uma cópia da matriz.</span><span class="sxs-lookup"><span data-stu-id="3556e-123">Uses the constructor for the [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) to create a copy of the array.</span></span> <span data-ttu-id="3556e-124">Como a classe que constrói a matriz estática realmente contém o objeto, essa função é adicionada principalmente à contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="3556e-124">Because the class that constructs the static array actually contains the object, this function mainly adds to the reference count.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="3556e-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3556e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3556e-126">**STATPROPSTG**</span><span class="sxs-lookup"><span data-stu-id="3556e-126">**STATPROPSTG**</span></span>](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dt>

[<span data-ttu-id="3556e-127">**IPropertyStorage:: enum**</span><span class="sxs-lookup"><span data-stu-id="3556e-127">**IPropertyStorage::Enum**</span></span>](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> </dl>

 

 