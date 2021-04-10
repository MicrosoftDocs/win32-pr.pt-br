---
description: Descreve como usar os métodos comuns das interfaces de coleção.
ms.assetid: 6ea311c0-a155-47de-ad40-62b0cbeb6e8f
title: Trabalhando com interfaces de coleção de OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7cda84243347680d91a6f3a5255f7ebf4e66932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170118"
---
# <a name="working-with-xps-om-collection-interfaces"></a><span data-ttu-id="feb2c-103">Trabalhando com interfaces de coleção de OM XPS</span><span class="sxs-lookup"><span data-stu-id="feb2c-103">Working with XPS OM Collection Interfaces</span></span>

<span data-ttu-id="feb2c-104">Descreve como usar os métodos comuns das interfaces de coleção.</span><span class="sxs-lookup"><span data-stu-id="feb2c-104">Describes how to use the common methods of the collection interfaces.</span></span>

## <a name="contents"></a><span data-ttu-id="feb2c-105">Sumário</span><span class="sxs-lookup"><span data-stu-id="feb2c-105">Contents</span></span>

<span data-ttu-id="feb2c-106">Os métodos descritos nesta seção são mostrados na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="feb2c-106">The methods described in this section are shown in the list that follows.</span></span> <span data-ttu-id="feb2c-107">Nem todas as interfaces de coleção oferecem suporte a cada um desses métodos, e algumas interfaces também oferecem suporte a métodos que não estão descritos nesta página.</span><span class="sxs-lookup"><span data-stu-id="feb2c-107">Not all collection interfaces support each of these methods, and some interfaces also support methods that are not described on this page.</span></span> <span data-ttu-id="feb2c-108">Para obter a lista de métodos com suporte por uma interface específica, consulte a descrição da descrição dessa interface.</span><span class="sxs-lookup"><span data-stu-id="feb2c-108">For the list of methods supported by a specific interface, refer to the description of that interface's description.</span></span>

<dl>

[<span data-ttu-id="feb2c-109">Método Append</span><span class="sxs-lookup"><span data-stu-id="feb2c-109">Append Method</span></span>](#append-method)  
[<span data-ttu-id="feb2c-110">Método GetAt</span><span class="sxs-lookup"><span data-stu-id="feb2c-110">GetAt Method</span></span>](#getat-method)  
[<span data-ttu-id="feb2c-111">Método GetCount</span><span class="sxs-lookup"><span data-stu-id="feb2c-111">GetCount Method</span></span>](#getcount-method)  
[<span data-ttu-id="feb2c-112">Método InsertAt</span><span class="sxs-lookup"><span data-stu-id="feb2c-112">InsertAt Method</span></span>](#insertat-method)  
[<span data-ttu-id="feb2c-113">Método RemoveAt</span><span class="sxs-lookup"><span data-stu-id="feb2c-113">RemoveAt Method</span></span>](#removeat-method)  
[<span data-ttu-id="feb2c-114">Método SetAt</span><span class="sxs-lookup"><span data-stu-id="feb2c-114">SetAt Method</span></span>](#setat-method)  
</dl>

[<span data-ttu-id="feb2c-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="feb2c-115">See also</span></span>](#see-also)

## <a name="append-method"></a><span data-ttu-id="feb2c-116">Método Append</span><span class="sxs-lookup"><span data-stu-id="feb2c-116">Append Method</span></span>

<span data-ttu-id="feb2c-117">Anexa um objeto ao final da coleção.</span><span class="sxs-lookup"><span data-stu-id="feb2c-117">Appends an object to the end of the collection.</span></span>

<span data-ttu-id="feb2c-118">**Sintaxe genérica**</span><span class="sxs-lookup"><span data-stu-id="feb2c-118">**Generic Syntax**</span></span>


```C++
HRESULT Append(
  [in]  Object *object
);
```



<span data-ttu-id="feb2c-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="feb2c-119">**Description**</span></span>

<span data-ttu-id="feb2c-120">Para o final da coleção, esse método acrescenta um objeto que é passado na lista de parâmetros, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="feb2c-120">To the end of the collection, this method appends an object that is passed in the parameter list, as shown in the following diagram.</span></span>

![uma figura que mostra como Append adiciona uma entrada à coleção](images/generic-append.png)

## <a name="getat-method"></a><span data-ttu-id="feb2c-122">Método GetAt</span><span class="sxs-lookup"><span data-stu-id="feb2c-122">GetAt Method</span></span>

<span data-ttu-id="feb2c-123">Obtém um objeto de um local especificado na coleção.</span><span class="sxs-lookup"><span data-stu-id="feb2c-123">Gets an object from a specified location in the collection.</span></span>

<span data-ttu-id="feb2c-124">**Sintaxe genérica**</span><span class="sxs-lookup"><span data-stu-id="feb2c-124">**Generic Syntax**</span></span>


```C++
HRESULT GetAt(
  [in]           UINT32 index,
  [out, retval]  Object **object
);
```



<span data-ttu-id="feb2c-125">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="feb2c-125">**Description**</span></span>

<span data-ttu-id="feb2c-126">Grava o objeto que é armazenado no local da coleção especificado pelo *índice* para a variável referenciada por *Object*.</span><span class="sxs-lookup"><span data-stu-id="feb2c-126">Writes the object that is stored at the collection's location specified by *index* to the variable referenced by *object*.</span></span> <span data-ttu-id="feb2c-127">Essa ação não altera o conteúdo da coleção.</span><span class="sxs-lookup"><span data-stu-id="feb2c-127">This action does not change the collection's contents.</span></span> <span data-ttu-id="feb2c-128">O diagrama a seguir ilustra esse processo.</span><span class="sxs-lookup"><span data-stu-id="feb2c-128">The following diagram illustrates this process.</span></span>

![uma figura que mostra como o GetAt recupera uma entrada da coleção](images/generic-getat.png)

## <a name="getcount-method"></a><span data-ttu-id="feb2c-130">Método GetCount</span><span class="sxs-lookup"><span data-stu-id="feb2c-130">GetCount Method</span></span>

<span data-ttu-id="feb2c-131">Obtém o número de objetos armazenados na coleção.</span><span class="sxs-lookup"><span data-stu-id="feb2c-131">Gets the number of objects stored in the collection.</span></span>

<span data-ttu-id="feb2c-132">**Sintaxe genérica**</span><span class="sxs-lookup"><span data-stu-id="feb2c-132">**Generic Syntax**</span></span>


```C++
HRESULT GetCount(
  [out, retval]  UINT32 *count
);
```



<span data-ttu-id="feb2c-133">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="feb2c-133">**Description**</span></span>

<span data-ttu-id="feb2c-134">Grava o número de objetos que estão atualmente armazenados na coleção na variável referenciada por *Count*.</span><span class="sxs-lookup"><span data-stu-id="feb2c-134">Writes the number of objects that are currently stored in the collection into the variable referenced by *count*.</span></span> <span data-ttu-id="feb2c-135">Essa ação não altera o conteúdo da coleção.</span><span class="sxs-lookup"><span data-stu-id="feb2c-135">This action does not change the collection's contents.</span></span> <span data-ttu-id="feb2c-136">O diagrama a seguir ilustra esse processo.</span><span class="sxs-lookup"><span data-stu-id="feb2c-136">The following diagram illustrates this process.</span></span>

![uma figura que mostra como GetCount Obtém o número de entradas na coleção](images/generic-getcount.png)

## <a name="insertat-method"></a><span data-ttu-id="feb2c-138">Método InsertAt</span><span class="sxs-lookup"><span data-stu-id="feb2c-138">InsertAt Method</span></span>

<span data-ttu-id="feb2c-139">Insere um objeto em um local especificado da coleção.</span><span class="sxs-lookup"><span data-stu-id="feb2c-139">Inserts an object at a specified location of the collection.</span></span>

<span data-ttu-id="feb2c-140">**Sintaxe genérica**</span><span class="sxs-lookup"><span data-stu-id="feb2c-140">**Generic Syntax**</span></span>


```C++
HRESULT InsertAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



<span data-ttu-id="feb2c-141">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="feb2c-141">**Description**</span></span>

<span data-ttu-id="feb2c-142">O objeto passado no *objeto* é inserido na coleção no local especificado pelo *índice*.</span><span class="sxs-lookup"><span data-stu-id="feb2c-142">The object that is passed in *object* is inserted into the collection at the location specified by *index*.</span></span> <span data-ttu-id="feb2c-143">Antes de inserir o novo *objeto*, esse método move-se por 1 o objeto que ocupava anteriormente o local no *índice* e move todos os ponteiros de interface subsequentemente para *índice*.</span><span class="sxs-lookup"><span data-stu-id="feb2c-143">Before inserting the new *object*, this method moves by 1 the object that has previously occupied the location at *index* and moves all interface pointers subsequent to *index*.</span></span> <span data-ttu-id="feb2c-144">O diagrama a seguir ilustra esse processo.</span><span class="sxs-lookup"><span data-stu-id="feb2c-144">The following diagram illustrates this process.</span></span>

![uma figura que mostra como o InsertAt adiciona uma entrada à coleção](images/generic-insertat.png)

## <a name="removeat-method"></a><span data-ttu-id="feb2c-146">Método RemoveAt</span><span class="sxs-lookup"><span data-stu-id="feb2c-146">RemoveAt Method</span></span>

<span data-ttu-id="feb2c-147">Remove o objeto de um local especificado na coleção.</span><span class="sxs-lookup"><span data-stu-id="feb2c-147">Removes the object from a specified location in the collection.</span></span>

<span data-ttu-id="feb2c-148">**Sintaxe genérica**</span><span class="sxs-lookup"><span data-stu-id="feb2c-148">**Generic Syntax**</span></span>


```C++
HRESULT RemoveAt(
  [in]  UINT32 index
);
```



<span data-ttu-id="feb2c-149">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="feb2c-149">**Description**</span></span>

<span data-ttu-id="feb2c-150">Esse método libera o objeto do local especificado pelo *índice* e, em seguida, compacta a coleção reduzindo por 1 o índice de cada ponteiro subsequentemente para *indexar*.</span><span class="sxs-lookup"><span data-stu-id="feb2c-150">This method releases the object from the location specified by *index*, then compacts the collection by reducing by 1 the index of each pointer subsequent to *index*.</span></span> <span data-ttu-id="feb2c-151">O diagrama a seguir ilustra esse processo.</span><span class="sxs-lookup"><span data-stu-id="feb2c-151">The following diagram illustrates this process.</span></span>

![uma figura que mostra como RemoveAt remove uma entrada da coleção](images/generic-removeat.png)

## <a name="setat-method"></a><span data-ttu-id="feb2c-153">Método SetAt</span><span class="sxs-lookup"><span data-stu-id="feb2c-153">SetAt Method</span></span>

<span data-ttu-id="feb2c-154">Substitui o objeto em um local especificado na coleção.</span><span class="sxs-lookup"><span data-stu-id="feb2c-154">Replaces the object at a specified location in the collection.</span></span>

<span data-ttu-id="feb2c-155">**Sintaxe genérica**</span><span class="sxs-lookup"><span data-stu-id="feb2c-155">**Generic Syntax**</span></span>


```C++
HRESULT SetAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



<span data-ttu-id="feb2c-156">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="feb2c-156">**Description**</span></span>

<span data-ttu-id="feb2c-157">Esse método primeiro libera o objeto no local referenciado pelo *índice* e, em seguida, substitui esse objeto pelo que é passado no *objeto*.</span><span class="sxs-lookup"><span data-stu-id="feb2c-157">This method first releases the object at the location referenced by *index*, then replaces that object with the one that is passed in *object*.</span></span> <span data-ttu-id="feb2c-158">O diagrama a seguir ilustra esse processo.</span><span class="sxs-lookup"><span data-stu-id="feb2c-158">The following diagram illustrates this process.</span></span>

![uma figura que mostra como SetAt substitui uma entrada na coleção](images/generic-setat.png)

## <a name="see-also"></a><span data-ttu-id="feb2c-160">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="feb2c-160">See Also</span></span>

<dl>

[<span data-ttu-id="feb2c-161">**IXpsOMColorProfileResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="feb2c-161">**IXpsOMColorProfileResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresourcecollection)  
[<span data-ttu-id="feb2c-162">**IXpsOMDashCollection**</span><span class="sxs-lookup"><span data-stu-id="feb2c-162">**IXpsOMDashCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection)  
[<span data-ttu-id="feb2c-163">**IXpsOMDocumentCollection**</span><span class="sxs-lookup"><span data-stu-id="feb2c-163">**IXpsOMDocumentCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)  
[<span data-ttu-id="feb2c-164">**IXpsOMFontResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="feb2c-164">**IXpsOMFontResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresourcecollection)  
[<span data-ttu-id="feb2c-165">**IXpsOMGeometryFigureCollection**</span><span class="sxs-lookup"><span data-stu-id="feb2c-165">**IXpsOMGeometryFigureCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)  
[<span data-ttu-id="feb2c-166">**IXpsOMGradientStopCollection**</span><span class="sxs-lookup"><span data-stu-id="feb2c-166">**IXpsOMGradientStopCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstopcollection)  
[<span data-ttu-id="feb2c-167">**IXpsOMImageResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="feb2c-167">**IXpsOMImageResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection)  
[<span data-ttu-id="feb2c-168">**IXpsOMNameCollection**</span><span class="sxs-lookup"><span data-stu-id="feb2c-168">**IXpsOMNameCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)  
[<span data-ttu-id="feb2c-169">**IXpsOMPageReferenceCollection**</span><span class="sxs-lookup"><span data-stu-id="feb2c-169">**IXpsOMPageReferenceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)  
[<span data-ttu-id="feb2c-170">**IXpsOMPartUriCollection**</span><span class="sxs-lookup"><span data-stu-id="feb2c-170">**IXpsOMPartUriCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection)  
[<span data-ttu-id="feb2c-171">**IXpsOMRemoteDictionaryResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="feb2c-171">**IXpsOMRemoteDictionaryResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)  
[<span data-ttu-id="feb2c-172">**IXpsOMSignatureBlockResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="feb2c-172">**IXpsOMSignatureBlockResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresourcecollection)  
[<span data-ttu-id="feb2c-173">**IXpsOMVisualCollection**</span><span class="sxs-lookup"><span data-stu-id="feb2c-173">**IXpsOMVisualCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)  
[<span data-ttu-id="feb2c-174">**IXpsSignatureBlockCollection**</span><span class="sxs-lookup"><span data-stu-id="feb2c-174">**IXpsSignatureBlockCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection)  
[<span data-ttu-id="feb2c-175">**IXpsSignatureCollection**</span><span class="sxs-lookup"><span data-stu-id="feb2c-175">**IXpsSignatureCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)  
[<span data-ttu-id="feb2c-176">**IXpsSignatureRequestCollection**</span><span class="sxs-lookup"><span data-stu-id="feb2c-176">**IXpsSignatureRequestCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection)  
</dl>

 

 



