---
description: Para obter controle mais detalhado sobre o comportamento de preenchimento automático ou para adicionar uma fonte personalizada de cadeias de caracteres de preenchimento automático, você deve gerenciar o objeto de AutoCompletar por conta própria.
ms.assetid: E1A7B1B0-2879-452E-9EBB-73F02B932200
title: Como habilitar o preenchimento automático manualmente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee4b327c6ccdd62fd921c56cfb046edb8527bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967905"
---
# <a name="how-to-enable-autocomplete-manually"></a><span data-ttu-id="9e54e-103">Como habilitar o preenchimento automático manualmente</span><span class="sxs-lookup"><span data-stu-id="9e54e-103">How to Enable Autocomplete Manually</span></span>

<span data-ttu-id="9e54e-104">Para obter controle mais detalhado sobre o comportamento de preenchimento automático ou para adicionar uma fonte personalizada de cadeias de caracteres de preenchimento automático, você deve gerenciar o objeto de AutoCompletar por conta própria.</span><span class="sxs-lookup"><span data-stu-id="9e54e-104">To gain more detailed control over the autocomplete behavior, or to add a custom source of autocomplete strings, you must manage the autocomplete object yourself.</span></span> <span data-ttu-id="9e54e-105">Você pode habilitar o preenchimento automático manualmente das seguintes maneiras.</span><span class="sxs-lookup"><span data-stu-id="9e54e-105">You can enable autocomplete manually in the following ways.</span></span>

## <a name="instructions"></a><span data-ttu-id="9e54e-106">Instruções</span><span class="sxs-lookup"><span data-stu-id="9e54e-106">Instructions</span></span>

### <a name="creating-a-simple-autocomplete-object"></a><span data-ttu-id="9e54e-107">Criando um objeto de preenchimento automático simples</span><span class="sxs-lookup"><span data-stu-id="9e54e-107">Creating a Simple Autocomplete Object</span></span>

<span data-ttu-id="9e54e-108">As etapas a seguir mostram como criar e inicializar um objeto de preenchimento automático simples.</span><span class="sxs-lookup"><span data-stu-id="9e54e-108">The following steps show how to create and initialize a simple autocomplete object.</span></span> <span data-ttu-id="9e54e-109">Um objeto de preenchimento automático simples conclui as cadeias de caracteres de uma única fonte.</span><span class="sxs-lookup"><span data-stu-id="9e54e-109">A simple autocomplete object completes strings from a single source.</span></span> <span data-ttu-id="9e54e-110">A verificação de erros foi omitida intencionalmente neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="9e54e-110">Error checking has been intentionally omitted in this example.</span></span>

1.  <span data-ttu-id="9e54e-111">Crie o objeto de preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="9e54e-111">Create the autocomplete object.</span></span>

    ```C++
    IAutoComplete *pac;

    HRESULT hr = CoCreateInstance(CLSID_AutoComplete, 
                                    NULL, 
                                  CLSCTX_INPROC_SERVER,
                                  IID_PPV_ARGS(&pac));
    ```

    

2.  <span data-ttu-id="9e54e-112">Crie a origem de AutoCompletar.</span><span class="sxs-lookup"><span data-stu-id="9e54e-112">Create the autocomplete source.</span></span> <span data-ttu-id="9e54e-113">Você pode usar uma [fonte de preenchimento automático predefinida](ac-ovw.md) ou pode escrever sua própria fonte personalizada.</span><span class="sxs-lookup"><span data-stu-id="9e54e-113">You can use a [predefined autocomplete source](ac-ovw.md) or you can write your own custom source.</span></span>

    <span data-ttu-id="9e54e-114">O código a seguir usa uma das fontes de preenchimento automático predefinidas.</span><span class="sxs-lookup"><span data-stu-id="9e54e-114">The following code uses one of the predefined autocomplete sources.</span></span>

    ```C++
    IUnknown *punkSource;

    hr = CoCreateInstance(CLSID_ACListISF, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&punkSource));
    ```

    

    <span data-ttu-id="9e54e-115">O código a seguir usa uma fonte de preenchimento automático personalizada.</span><span class="sxs-lookup"><span data-stu-id="9e54e-115">The following code uses a custom autocomplete source.</span></span> <span data-ttu-id="9e54e-116">Você pode escrever sua própria fonte de preenchimento automático implementando um objeto que expõe a interface [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring) .</span><span class="sxs-lookup"><span data-stu-id="9e54e-116">You can write your own autocomplete source by implementing an object that exposes the [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring) interface.</span></span> <span data-ttu-id="9e54e-117">O objeto também pode implementar, opcionalmente, as interfaces [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) e [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) .</span><span class="sxs-lookup"><span data-stu-id="9e54e-117">The object can also optionally implement the [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) and [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) interfaces.</span></span>

    ```C++
    CCustomAutoCompleteSource *pcacs = new CCustomAutoCompleteSource();

    hr = pcacs->QueryInterface(IID_PPV_ARGS(&punkSource));
    if(SUCCEEDED(hr))
    {
        // ...
    }

    pcacs->Release();
    ```

    

3.  <span data-ttu-id="9e54e-118">Defina as opções na fonte de preenchimento automático (opcional).</span><span class="sxs-lookup"><span data-stu-id="9e54e-118">Set the options on the autocomplete source (optional).</span></span>

    <span data-ttu-id="9e54e-119">Você pode personalizar o comportamento da fonte de preenchimento automático definindo suas opções se a origem expõe a interface [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) .</span><span class="sxs-lookup"><span data-stu-id="9e54e-119">You can customize the behavior of the autocomplete source by setting its options if the source exposes the [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) interface.</span></span> <span data-ttu-id="9e54e-120">Ao usar as fontes de preenchimento automático predefinidas, somente o CLSID \_ ACListISF exporta **IACList2**.</span><span class="sxs-lookup"><span data-stu-id="9e54e-120">When using the predefined autocomplete sources, only CLSID\_ACListISF exports **IACList2**.</span></span> <span data-ttu-id="9e54e-121">Para obter uma lista completa de opções e seus valores, consulte [**IACList2:: SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).</span><span class="sxs-lookup"><span data-stu-id="9e54e-121">For a complete list of options and their values, see [**IACList2::SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).</span></span>

    ```C++
    IACList2 *pal2;

    hr = punkSource->QueryInterface(IID_PPV_ARGS(&pal2));
    if (SUCCEEDED(hr))
    {
        hr = pal2->SetOptions(ACLO_FILESYSONLY);
        pal2->Release();
    }
    ```

    

4.  <span data-ttu-id="9e54e-122">Inicialize o objeto de preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="9e54e-122">Initialize the autocomplete object.</span></span>

    <span data-ttu-id="9e54e-123">Neste exemplo, **hwndEdit** é o identificador da janela de controle de edição para a qual o preenchimento automático deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="9e54e-123">In this example, **hwndEdit** is the handle of the edit control window for which autocomplete is to be enabled.</span></span> <span data-ttu-id="9e54e-124">Consulte [**IAutoComplete:: init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init) para obter uma descrição dos dois parâmetros finais não utilizados.</span><span class="sxs-lookup"><span data-stu-id="9e54e-124">See [**IAutoComplete::Init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init) for a description of the final two unused parameters.</span></span>

    ```C++
    hr = pac->Init(hwndEdit, punkSource, NULL, NULL);
    ```

    

5.  <span data-ttu-id="9e54e-125">Defina as opções do objeto preenchimento automático (opcional).</span><span class="sxs-lookup"><span data-stu-id="9e54e-125">Set the options of the autocomplete object (optional).</span></span>

    <span data-ttu-id="9e54e-126">Você pode personalizar o comportamento do objeto de preenchimento automático definindo suas opções.</span><span class="sxs-lookup"><span data-stu-id="9e54e-126">You can customize the behavior of the autocomplete object by setting its options.</span></span> <span data-ttu-id="9e54e-127">Para obter uma lista completa de opções e seus valores, consulte a documentação para [**IACList2:: SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).</span><span class="sxs-lookup"><span data-stu-id="9e54e-127">For a complete list of options and their values, see the documentation for [**IACList2::SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).</span></span>

    ```C++
    IAutoComplete2 *pac2;

    hr = pac->QueryInterface(IID_PPV_ARGS(&pac2));

    if (SUCCEEDED(hr))
    {
        hr = pac2->SetOptions(ACO_AUTOSUGGEST);
        pac2->Release();
    }
    ```

    

6.  <span data-ttu-id="9e54e-128">Libere os objetos.</span><span class="sxs-lookup"><span data-stu-id="9e54e-128">Release the objects.</span></span>

    > [!Note]  
    > <span data-ttu-id="9e54e-129">O objeto de preenchimento automático permanece anexado ao controle de edição mesmo depois que você o libera.</span><span class="sxs-lookup"><span data-stu-id="9e54e-129">The autocomplete object remains attached to the edit control even after you release it.</span></span> <span data-ttu-id="9e54e-130">Se você pretender ter a necessidade de acessar esses objetos mais tarde — se quiser alterar as opções de preenchimento automático posteriormente, por exemplo, não é necessário liberá-las neste ponto.</span><span class="sxs-lookup"><span data-stu-id="9e54e-130">If you foresee a need to access these objects later—if you want to change the autocomplete options at a later time, for example—it is not required that you release them at this point.</span></span>

     

    ```C++
    punkSource->Release();
    pac->Release();
    ```

    

### <a name="creating-a-compound-autocomplete-object"></a><span data-ttu-id="9e54e-131">Criando um objeto de preenchimento automático composto</span><span class="sxs-lookup"><span data-stu-id="9e54e-131">Creating a Compound Autocomplete Object</span></span>

<span data-ttu-id="9e54e-132">Um objeto de preenchimento automático composto corresponde A cadeias de caracteres de várias fontes.</span><span class="sxs-lookup"><span data-stu-id="9e54e-132">A compound autocomplete object matches against strings from multiple sources.</span></span> <span data-ttu-id="9e54e-133">Por exemplo, a barra de endereços do Windows Internet Explorer usa um objeto de preenchimento automático composto, pois o usuário pode começar a digitar o nome de um arquivo ou uma URL.</span><span class="sxs-lookup"><span data-stu-id="9e54e-133">For example, the Windows Internet Explorer Address bar uses a compound autocomplete object because the user might begin typing the name of a file or a URL.</span></span> <span data-ttu-id="9e54e-134">A maioria das etapas envolvidas na criação de um objeto de preenchimento automático composto é idêntica às etapas em "criando um objeto de AutoCompletamento simples".</span><span class="sxs-lookup"><span data-stu-id="9e54e-134">Most of the steps involved in creating a compound autocomplete object are identical to the steps in "Creating a Simple Autocomplete Object."</span></span> <span data-ttu-id="9e54e-135">Essas etapas são indicadas como tal.</span><span class="sxs-lookup"><span data-stu-id="9e54e-135">Those steps are indicated as such.</span></span>

1.  <span data-ttu-id="9e54e-136">Crie o objeto de preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="9e54e-136">Create the autocomplete object.</span></span> <span data-ttu-id="9e54e-137">Isso é o mesmo que a etapa 1 acima.</span><span class="sxs-lookup"><span data-stu-id="9e54e-137">This is the same as step 1 above.</span></span>

2.  <span data-ttu-id="9e54e-138">Crie o Gerenciador de objetos de fonte composta de preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="9e54e-138">Create the autocomplete compound source object manager.</span></span>

    <span data-ttu-id="9e54e-139">O objeto de fonte composta de preenchimento automático permite que várias fontes de preenchimento automático sejam combinadas em uma única origem de AutoCompletar.</span><span class="sxs-lookup"><span data-stu-id="9e54e-139">The autocomplete compound source object allows multiple autocomplete sources to be combined into a single autocomplete source.</span></span>

    ```C++
    IObjMgr *pom;

    hr = CoCreateInstance(CLSID_ACLMulti, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&pom));
    ```

    

3.  <span data-ttu-id="9e54e-140">Crie e defina opções para cada uma das fontes de preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="9e54e-140">Create and set options for each of the autocomplete sources.</span></span> <span data-ttu-id="9e54e-141">Repita as etapas 2 e 3 acima para cada fonte.</span><span class="sxs-lookup"><span data-stu-id="9e54e-141">Repeat steps 2 and 3 above for each source.</span></span>

4.  <span data-ttu-id="9e54e-142">Anexe cada fonte de preenchimento automático ao Gerenciador de objetos de origem.</span><span class="sxs-lookup"><span data-stu-id="9e54e-142">Attach each autocomplete source to the source object manager.</span></span>

    ```C++
    hr = pom->Append(punkSource1);
    hr = pom->Append(punkSource2);
    ```

    

5.  <span data-ttu-id="9e54e-143">Inicialize o objeto de preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="9e54e-143">Initialize the autocomplete object.</span></span>

    <span data-ttu-id="9e54e-144">Isso é o mesmo que a etapa 4 acima, exceto que, em vez de passar a fonte de AutoCompletar simples para [**IAutoComplete:: init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init), você passa o Gerenciador de objetos de origem composto.</span><span class="sxs-lookup"><span data-stu-id="9e54e-144">This is the same as step 4 above, except that instead of passing the simple autocomplete source to [**IAutoComplete::Init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init), you pass the compound source object manager.</span></span>

    ```C++
    hr = pac->Init(hwndEdit, pom, NULL, NULL);
    ```

    

6.  <span data-ttu-id="9e54e-145">Defina as opções do objeto preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="9e54e-145">Set the options of the autocomplete object.</span></span> <span data-ttu-id="9e54e-146">Isso é o mesmo que a etapa 5 acima.</span><span class="sxs-lookup"><span data-stu-id="9e54e-146">This is the same as step 5 above.</span></span>

7.  <span data-ttu-id="9e54e-147">Libere os objetos.</span><span class="sxs-lookup"><span data-stu-id="9e54e-147">Release the objects.</span></span>

    <span data-ttu-id="9e54e-148">Como no caso simples, você pode liberar os objetos assim que terminar de usá-los, mas também poderá mantê-los para alterar as opções posteriormente.</span><span class="sxs-lookup"><span data-stu-id="9e54e-148">As in the simple case, you can release the objects as soon as you are finished using them, but you can also retain them to change options later.</span></span>

    ```C++
    pac->Release();
    pom->Release();

    // Release each individual source.
    punkSource1->Release(); 
    punkSource2->Release();
    ```

    

 

 
