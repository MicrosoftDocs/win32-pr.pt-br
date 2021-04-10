---
description: Este tópico explica como criar e registrar manipuladores de propriedade para trabalhar com o sistema de propriedades do Windows.
ms.assetid: 3b54dd65-b7db-4e6a-bc3d-1008fdabcfa9
title: Inicializando manipuladores de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f8eb11bc44217e508313bfb477c65925b44216e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169748"
---
# <a name="initializing-property-handlers"></a><span data-ttu-id="f1cd8-103">Inicializando manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="f1cd8-103">Initializing Property Handlers</span></span>

<span data-ttu-id="f1cd8-104">Este tópico explica como criar e registrar manipuladores de propriedade para trabalhar com o sistema de propriedades do Windows.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-104">This topic explains how to create and register property handlers to work with the Windows property system.</span></span>

<span data-ttu-id="f1cd8-105">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="f1cd8-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="f1cd8-106">Manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="f1cd8-106">Property Handlers</span></span>](#property-handlers)
-   [<span data-ttu-id="f1cd8-107">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="f1cd8-107">Before You Begin</span></span>](#before-you-begin)
-   [<span data-ttu-id="f1cd8-108">Inicializando manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="f1cd8-108">Initializing Property Handlers</span></span>](#initializing-property-handlers)
-   [<span data-ttu-id="f1cd8-109">Armazenamento de propriedades na memória</span><span class="sxs-lookup"><span data-stu-id="f1cd8-109">In-Memory Property Store</span></span>](#in-memory-property-store)
-   [<span data-ttu-id="f1cd8-110">Lidando com valores de PROPVARIANT-Based</span><span class="sxs-lookup"><span data-stu-id="f1cd8-110">Dealing with PROPVARIANT-Based Values</span></span>](#dealing-with-propvariant-based-values)
-   [<span data-ttu-id="f1cd8-111">Suporte a metadados abertos</span><span class="sxs-lookup"><span data-stu-id="f1cd8-111">Supporting Open Metadata</span></span>](#supporting-open-metadata)
-   [<span data-ttu-id="f1cd8-112">Conteúdo de texto completo</span><span class="sxs-lookup"><span data-stu-id="f1cd8-112">Full-Text Contents</span></span>](#full-text-contents)
-   [<span data-ttu-id="f1cd8-113">Fornecendo valores para propriedades</span><span class="sxs-lookup"><span data-stu-id="f1cd8-113">Providing Values for Properties</span></span>](#providing-values-for-properties)
-   [<span data-ttu-id="f1cd8-114">Gravando valores de volta</span><span class="sxs-lookup"><span data-stu-id="f1cd8-114">Writing Back Values</span></span>](#writing-back-values)
-   [<span data-ttu-id="f1cd8-115">Implementando IPropertyStoreCapabilities</span><span class="sxs-lookup"><span data-stu-id="f1cd8-115">Implementing IPropertyStoreCapabilities</span></span>](#implementing-ipropertystorecapabilities)
-   [<span data-ttu-id="f1cd8-116">Registrando e distribuindo manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="f1cd8-116">Registering and Distributing Property Handlers</span></span>](#registering-and-distributing-property-handlers)
-   [<span data-ttu-id="f1cd8-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1cd8-117">Related topics</span></span>](#related-topics)

## <a name="property-handlers"></a><span data-ttu-id="f1cd8-118">Manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="f1cd8-118">Property Handlers</span></span>

<span data-ttu-id="f1cd8-119">Manipuladores de propriedade são uma parte crucial do sistema de propriedades.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-119">Property handlers are a crucial part of the property system.</span></span> <span data-ttu-id="f1cd8-120">Eles são invocados em processo pelo indexador para ler e indexar valores de propriedade e também são invocados pelo Windows Explorer em processo para ler e gravar valores de propriedade diretamente nos arquivos.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-120">They are invoked in-process by the indexer to read and index property values, and are also invoked by Windows Explorer in-process to read and write property values directly in the files.</span></span> <span data-ttu-id="f1cd8-121">Esses manipuladores precisam ser cuidadosamente escritos e testados para evitar o degradamento do desempenho ou a perda de dados nos arquivos afetados.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-121">These handlers need to be carefully written and tested to prevent degraded performance or the loss of data in the affected files.</span></span> <span data-ttu-id="f1cd8-122">Para obter mais informações sobre considerações específicas do indexador que afetam a implementação do manipulador de propriedades, consulte [desenvolvendo manipuladores de propriedade para o Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md).</span><span class="sxs-lookup"><span data-stu-id="f1cd8-122">For more information on indexer-specific considerations that affect property handler implementation, see [Developing Property Handlers for Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md).</span></span>

<span data-ttu-id="f1cd8-123">Este tópico discute um exemplo de formato de arquivo baseado em XML que descreve uma receita com uma extensão de nome de arquivo. recipe.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-123">This topic discusses a sample XML-based file format that describes a recipe with a .recipe file name extension.</span></span> <span data-ttu-id="f1cd8-124">A extensão de nome de arquivo. recipe é registrada como seu próprio formato de arquivo distinto, em vez de depender do formato de arquivo mais genérico. xml, cujo manipulador usa um fluxo secundário para armazenar propriedades.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-124">The .recipe file name extension is registered as its own distinct file format rather than relying on the more generic .xml file format, whose handler uses a secondary stream to store properties.</span></span> <span data-ttu-id="f1cd8-125">Recomendamos que você registre extensões de nome de arquivo exclusivas para seus tipos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-125">We recommend that you register unique file name extensions for your file types.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="f1cd8-126">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="f1cd8-126">Before You Begin</span></span>

<span data-ttu-id="f1cd8-127">Manipuladores de propriedade são objetos COM que criam a abstração [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para um formato de arquivo específico.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-127">Property handlers are COM objects that create the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) abstraction for a specific file format.</span></span> <span data-ttu-id="f1cd8-128">Eles lêem (analisam) e gravam esse formato de arquivo de forma que esteja em conformidade com sua especificação.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-128">They read (parse) and write this file format in a manner that conforms to its specification.</span></span> <span data-ttu-id="f1cd8-129">Alguns manipuladores de propriedades fazem seu trabalho com base em APIs que abstraim o acesso a um formato de arquivo específico.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-129">Some property handlers do their work based on APIs that abstract access to a specific file format.</span></span> <span data-ttu-id="f1cd8-130">Antes de desenvolver um manipulador de propriedades para seu formato de arquivo, você precisa entender como o formato de arquivo armazena propriedades e como essas propriedades (nomes e valores) são mapeadas para a abstração de armazenamento de propriedade.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-130">Before you develop a property handler for your file format, you need to understand how your file format stores properties, and how those properties (names and values) are mapped into the property store abstraction.</span></span>

<span data-ttu-id="f1cd8-131">Ao planejar sua implementação, lembre-se de que os manipuladores de propriedade são componentes de nível baixo que são carregados no contexto de processos como o Windows Explorer, o indexador do Windows Search e os aplicativos de terceiros que usam o modelo de programação de item de Shell.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-131">When planning your implementation, remember that property handlers are low-level components that are loaded in the context of processes like Windows Explorer, the Windows Search indexer, and third-party applications that use the Shell item programming model.</span></span> <span data-ttu-id="f1cd8-132">Como resultado, os manipuladores de propriedade não podem ser implementados em código gerenciado e devem ser implementados em C++.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-132">As a result, property handlers cannot be implemented in managed code, and should be implemented in C++.</span></span> <span data-ttu-id="f1cd8-133">Se o seu manipulador usar quaisquer APIs ou serviços para fazer seu trabalho, você deve garantir que esses serviços possam funcionar corretamente no (s) ambiente (es) em que o manipulador de propriedades está carregado.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-133">If your handler uses any APIs or services to do its work, you must ensure that those services can function properly in the environment(s) in which your property handler is loaded.</span></span>

> [!Note]  
> <span data-ttu-id="f1cd8-134">Manipuladores de propriedade sempre são associados a tipos de arquivo específicos; Portanto, se o formato de arquivo contiver propriedades que exigem um manipulador de propriedade personalizada, você sempre deverá registrar uma extensão de nome de arquivo exclusiva para cada formato de arquivo.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-134">Property handlers are always associated with specific file types; thus, if your file format contains properties that require a custom property handler, you should always register a unique file name extension for each file format.</span></span>

 

## <a name="initializing-property-handlers"></a><span data-ttu-id="f1cd8-135">Inicializando manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="f1cd8-135">Initializing Property Handlers</span></span>

<span data-ttu-id="f1cd8-136">Antes que uma propriedade seja usada pelo sistema, ela é inicializada chamando uma implementação de [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream).</span><span class="sxs-lookup"><span data-stu-id="f1cd8-136">Before a property is used by the system, it is initialized by calling an implementation of [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream).</span></span> <span data-ttu-id="f1cd8-137">O manipulador de propriedades deve ser inicializado fazendo com que o sistema atribua um fluxo em vez de deixar essa atribuição para a implementação do manipulador.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-137">The property handler should be initialized by having the system assign it a stream rather than leaving that assignment to the handler implementation.</span></span> <span data-ttu-id="f1cd8-138">Esse método de inicialização garante as seguintes coisas:</span><span class="sxs-lookup"><span data-stu-id="f1cd8-138">This method of initialization ensures the following things:</span></span>

-   <span data-ttu-id="f1cd8-139">O manipulador de propriedades pode ser executado em um processo restrito (um recurso de segurança importante) sem ter direitos de acesso para ler ou gravar arquivos diretamente, em vez de acessar seu conteúdo por meio do fluxo.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-139">The property handler can run in a restricted process (an important security feature) without having access rights to directly read or write files, rather accessing their content through the stream.</span></span>
-   <span data-ttu-id="f1cd8-140">O sistema pode ser confiável para lidar com o arquivo oplocks corretamente, que é uma medida de confiabilidade importante.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-140">The system can be trusted to handle the file oplocks correctly, which is an important reliability measure.</span></span>
-   <span data-ttu-id="f1cd8-141">O sistema de propriedades fornece um serviço de salvamento seguro automático sem nenhuma funcionalidade extra necessária da implementação do manipulador de propriedades.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-141">The property system provides an automatic safe saving service without any extra functionality required from the property handler implementation.</span></span> <span data-ttu-id="f1cd8-142">Consulte a seção [redação de valores](#writing-back-values) para obter mais informações sobre fluxos.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-142">See the [Writing Back Values](#writing-back-values) section for more information about streams.</span></span>
-   <span data-ttu-id="f1cd8-143">O uso do [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) abstrai sua implementação dos detalhes do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-143">Use of the [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) abstracts your implementation from file system details.</span></span> <span data-ttu-id="f1cd8-144">Isso permite que o manipulador ofereça suporte à inicialização por meio de armazenamentos alternativos, como uma pasta protocolo FTP (FTP) ou um arquivo compactado com uma extensão de nome de arquivo. zip.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-144">This enables the handler to support initialization through alternative storages such as a File Transfer Protocol (FTP) folder or a compressed file with a .zip file name extension.</span></span>

<span data-ttu-id="f1cd8-145">Há casos em que a inicialização com fluxos não é possível.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-145">There are cases where initialization with streams is not possible.</span></span> <span data-ttu-id="f1cd8-146">Nessas situações, há duas interfaces adicionais que os manipuladores de propriedade podem implementar: [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile) e [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem).</span><span class="sxs-lookup"><span data-stu-id="f1cd8-146">In those situations, there are two further interfaces that property handlers can implement: [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile) and [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem).</span></span> <span data-ttu-id="f1cd8-147">Se um manipulador de propriedades não implementar o [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), ele deverá recusar a execução no processo isolado no qual o indexador do sistema o colocaria por padrão se houvesse uma alteração no fluxo.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-147">If a property handler does not implement the [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), it must opt out of running in the isolated process into which the system indexer would place it by default if there were a change to the stream.</span></span> <span data-ttu-id="f1cd8-148">Para recusar esse recurso, defina o valor do registro a seguir.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-148">To opt out of this feature, set the following registry value.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         DisableProcessIsolation = 1
```

<span data-ttu-id="f1cd8-149">No entanto, é muito melhor implementar [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) e fazer uma inicialização baseada em fluxo.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-149">However, it is far better to implement [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) and do a stream-based initialization.</span></span> <span data-ttu-id="f1cd8-150">O manipulador de propriedades será mais seguro e confiável como resultado.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-150">Your property handler will be safer and more reliable as a result.</span></span> <span data-ttu-id="f1cd8-151">Desabilitar o isolamento de processo geralmente é destinado apenas a manipuladores de propriedade herdados e deve ser strenuously evitado por qualquer código novo.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-151">Disabling process isolation is generally intended only for legacy property handlers and should be strenuously avoided by any new code.</span></span>

<span data-ttu-id="f1cd8-152">Para examinar a implementação de um manipulador de propriedades em detalhes, examine o exemplo de código a seguir, que é uma implementação de [**IInitializeWithStream:: Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).</span><span class="sxs-lookup"><span data-stu-id="f1cd8-152">To examine the implementation of a property handler in detail, look at the following code example, which is an implementation of [**IInitializeWithStream::Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).</span></span> <span data-ttu-id="f1cd8-153">O manipulador é inicializado carregando um documento de receita baseado em XML por meio de um ponteiro para a instância [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) associada do documento.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-153">The handler is initialized by loading an XML-based recipe document through a pointer to that document's associated [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) instance.</span></span> <span data-ttu-id="f1cd8-154">A variável **\_ spDocEle** usada perto do final do exemplo de código é definida anteriormente no exemplo como um MSXML2:: IXMLDOMElementPtr.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-154">The **\_spDocEle** variable used near the end of the code example is defined earlier in the sample as an MSXML2::IXMLDOMElementPtr.</span></span>

> [!Note]  
> <span data-ttu-id="f1cd8-155">O seguinte e todos os exemplos de código subsequentes são obtidos do exemplo de manipulador de receita incluído no SDK (Software Development Kit) do Windows.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-155">The following and all subsequent code examples are taken from the recipe handler sample included in the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f1cd8-156">.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-156">.</span></span>

 


```
HRESULT CRecipePropertyStore::Initialize(IStream *pStream, DWORD grfMode)
{
    HRESULT hr = E_FAIL;
    
    try
    {
        if (!_spStream)
        {
            hr = _spDomDoc.CreateInstance(__uuidof(MSXML2::DOMDocument60));
            
            if (SUCCEEDED(hr))
            {
                if (VARIANT_TRUE == _spDomDoc->load(static_cast<IUnknown *>(pStream)))
                {
                    _spDocEle = _spDomDoc->documentElement;
                }
```



<span data-ttu-id="f1cd8-157">Â</span><span class="sxs-lookup"><span data-stu-id="f1cd8-157">Â</span></span> 

<span data-ttu-id="f1cd8-158">Depois que o próprio documento é carregado, as propriedades a serem exibidas no Windows Explorer são carregadas chamando o método **\_ GetProperties** protegido, conforme ilustrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-158">After the document itself is loaded, the properties to be displayed in Windows Explorer are loaded by calling the protected **\_LoadProperties** method, as illustrated in the following code example.</span></span> <span data-ttu-id="f1cd8-159">Esse processo é examinado em detalhes na próxima seção.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-159">This process is examined in detail in the next section.</span></span>


```
                if (_spDocEle)
                {
                    hr = _LoadProperties();
    
                    if (SUCCEEDED(hr))
                    {
                        _spStream = pStream;
                    }
                }
                else
                {
                    hr = E_FAIL;  // parse error
                }
            }
        }
        else
        {
            hr = E_UNEXPECTED;
        }
    }
    
    catch (_com_error &e)
    {
        hr = e.Error();
    }
    
    return hr;
}
```



<span data-ttu-id="f1cd8-160">Se o fluxo for somente leitura, mas o parâmetro *grfMode* contiver o \_ sinalizador ReadWrite STGM, a inicialização deverá falhar e retornar STG \_ e \_ ACCESSDENIED.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-160">If the stream is read-only but the *grfMode* parameter contains the STGM\_READWRITE flag, the initialization should fail and return STG\_E\_ACCESSDENIED.</span></span> <span data-ttu-id="f1cd8-161">Sem essa verificação, o Windows Explorer mostra os valores de propriedade como graváveis, embora não estejam, levando a uma experiência confusa para o usuário final.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-161">Without this check, Windows Explorer shows the property values as writable even though they are not, leading to a confusing end-user experience.</span></span>

<span data-ttu-id="f1cd8-162">O manipulador de propriedades é inicializado apenas uma vez em seu tempo de vida.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-162">The property handler is initialized only once in its lifetime.</span></span> <span data-ttu-id="f1cd8-163">Se uma segunda inicialização for solicitada, o manipulador deverá retornar `HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)` .</span><span class="sxs-lookup"><span data-stu-id="f1cd8-163">If a second initialization is requested, the handler should return `HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)`.</span></span>

## <a name="in-memory-property-store"></a><span data-ttu-id="f1cd8-164">Armazenamento de propriedades In-Memory</span><span class="sxs-lookup"><span data-stu-id="f1cd8-164">In-Memory Property Store</span></span>

<span data-ttu-id="f1cd8-165">Antes de examinar a implementação de **\_**, você deve entender a matriz **PropertyMap** usada no exemplo para mapear Propriedades no documento XML para as propriedades existentes no sistema de propriedades por meio de seus valores de pkey.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-165">Before looking at the implementation of **\_LoadProperties**, you should understand the **PropertyMap** array used in the sample to map properties in the XML document to existing properties in the property system through their PKEY values.</span></span>

<span data-ttu-id="f1cd8-166">Você não deve expor todos os elementos e atributos no arquivo XML como uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-166">You should not expose every element and attribute in the XML file as a property.</span></span> <span data-ttu-id="f1cd8-167">Em vez disso, selecione apenas aqueles que você acredita que serão úteis para os usuários finais na organização de seus documentos (neste caso, receitas).</span><span class="sxs-lookup"><span data-stu-id="f1cd8-167">Instead, select only those that you believe will be useful to end users in the organization of their documents (in this case, recipes).</span></span> <span data-ttu-id="f1cd8-168">Esse é um conceito importante para ter em mente ao desenvolver seus manipuladores de propriedade: a diferença entre as informações que são verdadeiramente úteis para cenários organizacionais e informações que pertencem aos detalhes do arquivo e que podem ser vistas abrindo o próprio arquivo.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-168">This is an important concept to keep in mind as you develop your property handlers: the difference between information that is truly useful for organizational scenarios, and information that belongs to the details of your file and can be seen by opening the file itself.</span></span> <span data-ttu-id="f1cd8-169">As propriedades não se destinam a ser uma duplicação completa de um arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-169">Properties are not intended to be a full duplication of an XML file.</span></span>


```
PropertyMap c_rgPropertyMap[] =
{
{ L"Recipe/Title", PKEY_Title, 
                   VT_LPWSTR, 
                   NULL, 
                   PKEY_Null },
{ L"Recipe/Comments", PKEY_Comment, 
                      VT_LPWSTR, 
                      NULL, 
                      PKEY_Null },
{ L"Recipe/Background", PKEY_Author, 
                        VT_VECTOR | VT_LPWSTR, 
                        L"Author", 
                        PKEY_Null },
{ L"Recipe/RecipeKeywords", PKEY_Keywords, 
                            VT_VECTOR | VT_LPWSTR, 
                            L"Keyword", 
                            PKEY_KeywordCount },
};
```



<span data-ttu-id="f1cd8-170">Aqui está a implementação completa do método **\_ LoadProperties** chamado por [**IInitializeWithStream:: Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).</span><span class="sxs-lookup"><span data-stu-id="f1cd8-170">Here is the full implementation of the **\_LoadProperties** method called by [**IInitializeWithStream::Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).</span></span>


```
HRESULT CRecipePropertyStore::_LoadProperties()
{
    HRESULT hr = E_FAIL;    
    
    if (_spCache)
    {
        hr = <mark type="const">S_OK</mark>;
    }
    else
    {
        // Create the in-memory property store.
        hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&_spCache));
    
        if (SUCCEEDED(hr))
        {
            // Cycle through each mapped property.
            for (UINT i = 0; i < ARRAYSIZE(c_rgPropertyMap); ++i)
            {
                _LoadProperty(c_rgPropertyMap[i]);
            }
    
            _LoadExtendedProperties();
            _LoadSearchContent();
        }
    }
    return hr;
}
```



<span data-ttu-id="f1cd8-171">O **\_ método** chama a função auxiliar do Shell [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) para criar um repositório de propriedades na memória (cache) para as propriedades manipuladas.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-171">The **\_LoadProperties** method calls the Shell helper function [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) to create an in-memory property store (cache) for the handled properties.</span></span> <span data-ttu-id="f1cd8-172">Usando um cache, as alterações são controladas para você.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-172">By using a cache, changes are tracked for you.</span></span> <span data-ttu-id="f1cd8-173">Isso libera você do rastreamento se um valor de propriedade foi alterado no cache, mas ainda não foi salvo no armazenamento persistente.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-173">This frees you from tracking whether a property value has been changed in the cache but not yet saved to persisted storage.</span></span> <span data-ttu-id="f1cd8-174">Ele também libera você de manter desnecessariamente os valores de propriedade que não foram alterados.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-174">It also frees you from needlessly persisting property values that have not changed.</span></span>

<span data-ttu-id="f1cd8-175">O método **\_ LoadProperties** também chama **\_ LoadProperty** cuja implementação é ilustrada no código a seguir) uma vez para cada propriedade mapeada.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-175">The **\_LoadProperties** method also calls **\_LoadProperty** whose implementation is illustrated in the following code) once for each mapped property.</span></span> <span data-ttu-id="f1cd8-176">**\_ LoadProperty** Obtém o valor da propriedade conforme especificado no elemento **PropertyMap** no fluxo XML e o atribui ao cache na memória por meio de uma chamada para [**IPropertyStoreCache:: SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate).</span><span class="sxs-lookup"><span data-stu-id="f1cd8-176">**\_LoadProperty** gets the value of the property as specified in the **PropertyMap** element in the XML stream and assigns it to the in-memory cache through a call to [**IPropertyStoreCache::SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate).</span></span> <span data-ttu-id="f1cd8-177">O \_ sinalizador normal do PSC na chamada para **IPropertyStoreCache:: SetValueAndState** indica que o valor da propriedade não foi alterado desde a hora em que inseriu o cache.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-177">The PSC\_NORMAL flag in the call to **IPropertyStoreCache::SetValueAndState** indicates that the property value has not been altered since the time it entered the cache.</span></span>


```
HRESULT CRecipePropertyStore::_LoadProperty(PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    
    MSXML2::IXMLDOMNodePtr spXmlNode(_spDomDoc->selectSingleNode(map.pszXPath));
    if (spXmlNode)
    {
        PROPVARIANT propvar = { 0 };
        propvar.vt = map.vt;
        
        if (map.vt == (VT_VECTOR | VT_LPWSTR))
        {
            hr = _LoadVectorProperty(spXmlNode, &propvar, map);
        }
        else
        {
            // If there is no value, set to VT_EMPTY to indicate
            // that it is not there. Do not return failure.
            if (spXmlNode->text.length() == 0)
            {
                propvar.vt = VT_EMPTY;
                hr = <mark type="const">S_OK</mark>;
            }
            else
            {
                // SimplePropVariantFromString is a helper function.
                // particular to the sample. It is found in Util.cpp.
                hr = SimplePropVariantFromString(spXmlNode->text, &propvar);
            }
        }
    
        if (S_OK == hr)
        {
            hr = _spCache->SetValueAndState(map.key, &propvar, PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    return hr;
}
```



## <a name="dealing-with-propvariant-based-values"></a><span data-ttu-id="f1cd8-178">Lidando com valores de PROPVARIANT-Based</span><span class="sxs-lookup"><span data-stu-id="f1cd8-178">Dealing with PROPVARIANT-Based Values</span></span>

<span data-ttu-id="f1cd8-179">Na implementação de **\_ LoadProperty**, um valor de propriedade é fornecido na forma de um [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span><span class="sxs-lookup"><span data-stu-id="f1cd8-179">In the implementation of **\_LoadProperty**, a property value is provided in the form of a [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span> <span data-ttu-id="f1cd8-180">Um conjunto de APIs no Software Development Kit (SDK) é fornecido para converter de tipos primitivos como **PWSTR** ou **int** para ou de tipos **PROPVARIANT** .</span><span class="sxs-lookup"><span data-stu-id="f1cd8-180">A set of APIs in the software development kit (SDK) is provided to convert from primitive types such as **PWSTR** or **int** to or from **PROPVARIANT** types.</span></span> <span data-ttu-id="f1cd8-181">Essas APIs são encontradas em Propvarutil. h.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-181">These APIs are found in Propvarutil.h.</span></span>

<span data-ttu-id="f1cd8-182">Por exemplo, para converter um [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) em uma cadeia de caracteres, você pode usar [**PropVariantToString**](/windows/win32/api/propvarutil/nf-propvarutil-propvarianttostring) conforme ilustrado aqui.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-182">For example, to convert a [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) to a string, you can use [**PropVariantToString**](/windows/win32/api/propvarutil/nf-propvarutil-propvarianttostring) as illustrated here.</span></span>


```
PropVariantToString(REFPROPVARIANT propvar, PWSTR psz, UINT cch);
```



<span data-ttu-id="f1cd8-183">Para inicializar um PROPVARIANT de uma cadeia de caracteres, você pode usar [**InitPropVariantFromString**](/windows/win32/api/propvarutil/nf-propvarutil-initpropvariantfromstring).</span><span class="sxs-lookup"><span data-stu-id="f1cd8-183">To initialize a PROPVARIANT from a string, you can use [**InitPropVariantFromString**](/windows/win32/api/propvarutil/nf-propvarutil-initpropvariantfromstring).</span></span>


```
InitPropVariantFromString(PCWSTR psz, PROPVARIANT *ppropvar);
```



<span data-ttu-id="f1cd8-184">Como você pode ver em qualquer um dos arquivos de receita incluídos no exemplo, pode haver mais de uma palavra-chave em cada arquivo.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-184">As you can see in any of the recipe files included in the sample, there can be more than one keyword in each file.</span></span> <span data-ttu-id="f1cd8-185">Para considerar isso, o sistema de propriedades dá suporte a cadeias de caracteres com valores múltiplos representados como um vetor de cadeias de caracteres (por exemplo, "VT \_ vector \| VT \_ LPWSTR").</span><span class="sxs-lookup"><span data-stu-id="f1cd8-185">To account for this, the property system supports multi-valued strings represented as a vector of strings (for instance "VT\_VECTOR \| VT\_LPWSTR").</span></span> <span data-ttu-id="f1cd8-186">O método **\_ loadvetorproperty** no exemplo usa valores baseados em vetor.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-186">The **\_LoadVectorProperty** method in the example uses vector-based values.</span></span>


```
HRESULT CRecipePropertyStore::_LoadVectorProperty
                                (MSXML2::IXMLDOMNode *pNodeParent,
                                 PROPVARIANT *ppropvar,
                                 struct PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = pNodeParent->selectNodes(map.pszSubNodeName);
    
    if (spList)
    {
        UINT cElems = spList->length;
        ppropvar->calpwstr.cElems = cElems;
        ppropvar->calpwstr.pElems = (PWSTR*)CoTaskMemAlloc(sizeof(PWSTR)*cElems);
    
        if (ppropvar->calpwstr.pElems)
        {
            for (UINT i = 0; (SUCCEEDED(hr) && i < cElems); ++i)
            {
                hr = SHStrDup(spList->item[i]->text, 
                              &(ppropvar->calpwstr.pElems[i]));
            }
    
            if (SUCCEEDED(hr))
            {
                if (!IsEqualPropertyKey(map.keyCount, PKEY_Null))
                {
                    PROPVARIANT propvarCount = { VT_UI4 };
                    propvarCount.uintVal = cElems;
                    
                    _spCache->SetValueAndState(map.keyCount,
                                               &propvarCount, 
                                               PSC_NORMAL);
                }
            }
            else
            {
                PropVariantClear(ppropvar);
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
    }
    
    return hr;
}
```



<span data-ttu-id="f1cd8-187">Se um valor não existir no arquivo, não retorne um erro.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-187">If a value does not exist in the file, do not return an error.</span></span> <span data-ttu-id="f1cd8-188">Em vez disso, defina o valor como VT \_ vazio e retorne **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-188">Instead, set the value to VT\_EMPTY and return **S\_OK**.</span></span> <span data-ttu-id="f1cd8-189">\_O VT vazio indica que o valor da propriedade não existe.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-189">VT\_EMPTY indicates that the property value does not exist.</span></span>

## <a name="supporting-open-metadata"></a><span data-ttu-id="f1cd8-190">Suporte a metadados abertos</span><span class="sxs-lookup"><span data-stu-id="f1cd8-190">Supporting Open Metadata</span></span>

<span data-ttu-id="f1cd8-191">Este exemplo usa um formato de arquivo baseado em XML.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-191">This example uses an XML-based file format.</span></span> <span data-ttu-id="f1cd8-192">Seu esquema pode ser estendido para dar suporte a propriedades que não foram consideradas durante developmet, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-192">Its schema can be extended to support properties that were not thought of during developmet, for example.</span></span> <span data-ttu-id="f1cd8-193">Esse sistema é conhecido como metadados abertos.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-193">This system is known as open metadata.</span></span> <span data-ttu-id="f1cd8-194">Este exemplo estende o sistema de propriedades criando um nó sob o elemento **recipe** chamado **ExtendedProperties**, conforme ilustrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-194">This example extends the property system by creating a node under the **Recipe** element called **ExtendedProperties**, as illustrated in the following code example.</span></span>


```
<ExtendedProperties>
    <Property 
        Name="{65A98875-3C80-40AB-ABBC-EFDAF77DBEE2}, 100"
        EncodedValue="HJKHJDHKJHK"/>
</ExtendedProperties>
```



<span data-ttu-id="f1cd8-195">Para carregar propriedades estendidas persistentes durante a inicialização, implemente o método **\_ extendeproperties** , conforme ilustrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-195">To load persisted extended properties during initialization, implement the **\_LoadExtendedProperties** method, as illustrated in the following code example.</span></span>


```
HRESULT CRecipePropertyStore::_LoadExtendedProperties()
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = 
                  _spDomDoc->selectNodes(L"Recipe/ExtendedProperties/Property");
    
    if (spList)
    {
        UINT cElems = spList->length;
        
        for (UINT i = 0; i < cElems; ++i)
        {
            MSXML2::IXMLDOMElementPtr spElement;
            
            if (SUCCEEDED(spList->item[i]->QueryInterface(IID_PPV_ARGS(&spElement))))
            {
                PROPERTYKEY key;
                _bstr_t bstrPropName = spElement->getAttribute(L"Name").bstrVal;
    
                if (!!bstrPropName &&
                    (SUCCEEDED(PropertyKeyFromString(bstrPropName, &key))))
                {
                    PROPVARIANT propvar = { 0 };
                    _bstr_t bstrEncodedValue = 
                               spElement->getAttribute(L"EncodedValue").bstrVal;
                   
                    if (!!bstrEncodedValue)
                    {
                        // DeserializePropVariantFromString is a helper function
                        // particular to the sample. It is found in Util.cpp.
                        hr = DeserializePropVariantFromString(bstrEncodedValue, 
                                                              &propvar);
                    }
```



<span data-ttu-id="f1cd8-196">As APIs de serialização declaradas em propsys. h são usadas para serializar e desserializar os tipos [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) em blobs de dados e a codificação Base64 é usada para serializar esses BLOBs em cadeias de caracteres que podem ser salvas no XML.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-196">Serialization APIs declared in Propsys.h are used to serialize and deserialize [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) types into blobs of data, and then Base64 encoding is used to serialize those blobs into strings that can be saved in the XML.</span></span> <span data-ttu-id="f1cd8-197">Essas cadeias de caracteres são armazenadas no atributo **EncodedValue** do elemento **ExtendedProperties** .</span><span class="sxs-lookup"><span data-stu-id="f1cd8-197">These strings are stored in the **EncodedValue** attribute of the **ExtendedProperties** element.</span></span> <span data-ttu-id="f1cd8-198">O seguinte método de utilitário, implementado no arquivo util. cpp de exemplo, executa a serialização.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-198">The following utility method, implemented in the sample's Util.cpp file, performs the serialization.</span></span> <span data-ttu-id="f1cd8-199">Ele começa com uma chamada para a função [**StgSerializePropVariant**](/windows/win32/api/propvarutil/nf-propvarutil-stgserializepropvariant) para executar a serialização binária, conforme ilustrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-199">It begins with a call to the [**StgSerializePropVariant**](/windows/win32/api/propvarutil/nf-propvarutil-stgserializepropvariant) function to perform the binary serialization, as illustrated in the following code example.</span></span>


```
HRESULT SerializePropVariantAsString(const PROPVARIANT *ppropvar, PWSTR *pszOut)
{
    SERIALIZEDPROPERTYVALUE *pBlob;
    ULONG cbBlob;
    HRESULT hr = StgSerializePropVariant(ppropvar, &pBlob, &cbBlob);
```



<span data-ttu-id="f1cd8-200">Em seguida, a função [**CryptBinaryToString**](/windows/win32/api/wincrypt/nf-wincrypt-cryptbinarytostringa)Â, declarada em Wincrypt. h, executa a conversão base64.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-200">Next, the [**CryptBinaryToString**](/windows/win32/api/wincrypt/nf-wincrypt-cryptbinarytostringa)Â function, declared in Wincrypt.h, performs the Base64 conversion.</span></span>


```
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        DWORD cchString;
        
        if (CryptBinaryToString((BYTE *)pBlob, 
                                cbBlob,
                                CRYPT_STRING_BASE64, 
                                NULL, 
                                &cchString))
        {
            *pszOut = (PWSTR)CoTaskMemAlloc(sizeof(WCHAR) *cchString);
    
            if (*pszOut)
            {
                if (CryptBinaryToString((BYTE *)pBlob, 
                                         cbBlob,
                                         CRYPT_STRING_BASE64,
                                         *pszOut, 
                                         &cchString))
                {
                    hr = <mark type="const">S_OK</mark>;
                }
                else
                {
                    CoTaskMemFree(*pszOut);
                }
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }
        }
    }
    
    return <mark type="const">S_OK</mark>;}
```



<span data-ttu-id="f1cd8-201">A função **DeserializePropVariantFromString** , também encontrada em util. cpp, reverte a operação, desserializando valores do arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-201">The **DeserializePropVariantFromString** function, also found in Util.cpp, reverses the operation, deserializing values from the XML file.</span></span>

<span data-ttu-id="f1cd8-202">Para obter informações sobre o suporte para metadados abertos, consulte "tipos de arquivo que dão suporte a metadados abertos" em [tipos de arquivo](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="f1cd8-202">For information about support for open metadata, see "File Types that Support Open Metadata" in [File Types](../shell/fa-file-types.md).</span></span>

## <a name="full-text-contents"></a><span data-ttu-id="f1cd8-203">Conteúdo do Full-Text</span><span class="sxs-lookup"><span data-stu-id="f1cd8-203">Full-Text Contents</span></span>

<span data-ttu-id="f1cd8-204">Os manipuladores de propriedade também podem facilitar uma pesquisa de texto completo do conteúdo do arquivo, e eles são uma maneira fácil de fornecer essa funcionalidade se o formato de arquivo não for excessivamente complicado.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-204">Property handlers can also facilitate a full-text search of the file contents, and they are an easy way to provide that functionality if the file format is not overly complicated.</span></span> <span data-ttu-id="f1cd8-205">Há uma maneira alternativa e mais eficiente de fornecer o texto completo do arquivo por meio da implementação da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="f1cd8-205">There is an alternative, more powerful way to provide the full text of the file through the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface implementation.</span></span>

<span data-ttu-id="f1cd8-206">A tabela a seguir resume os benefícios de cada abordagem usando o [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ou o [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="f1cd8-206">The following table summarizes the benefits of each approach using either [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) or [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>



| <span data-ttu-id="f1cd8-207">Funcionalidade</span><span class="sxs-lookup"><span data-stu-id="f1cd8-207">Capability</span></span>                                   | <span data-ttu-id="f1cd8-208">Visio</span><span class="sxs-lookup"><span data-stu-id="f1cd8-208">IFilter</span></span>                      | <span data-ttu-id="f1cd8-209">IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="f1cd8-209">IPropertyStore</span></span> |
|----------------------------------------------|------------------------------|----------------|
| <span data-ttu-id="f1cd8-210">Permite write-back em arquivos?</span><span class="sxs-lookup"><span data-stu-id="f1cd8-210">Allows write back to files?</span></span>                  | <span data-ttu-id="f1cd8-211">Não</span><span class="sxs-lookup"><span data-stu-id="f1cd8-211">No</span></span>                           | <span data-ttu-id="f1cd8-212">Sim</span><span class="sxs-lookup"><span data-stu-id="f1cd8-212">Yes</span></span>            |
| <span data-ttu-id="f1cd8-213">Fornece uma combinação de conteúdo e propriedades?</span><span class="sxs-lookup"><span data-stu-id="f1cd8-213">Provides mix of content and properties?</span></span>      | <span data-ttu-id="f1cd8-214">Sim</span><span class="sxs-lookup"><span data-stu-id="f1cd8-214">Yes</span></span>                          | <span data-ttu-id="f1cd8-215">Sim</span><span class="sxs-lookup"><span data-stu-id="f1cd8-215">Yes</span></span>            |
| <span data-ttu-id="f1cd8-216">Multilíngüe?</span><span class="sxs-lookup"><span data-stu-id="f1cd8-216">Multilingual?</span></span>                                | <span data-ttu-id="f1cd8-217">Sim</span><span class="sxs-lookup"><span data-stu-id="f1cd8-217">Yes</span></span>                          | <span data-ttu-id="f1cd8-218">Não</span><span class="sxs-lookup"><span data-stu-id="f1cd8-218">No</span></span>             |
| <span data-ttu-id="f1cd8-219">MIME/inserido?</span><span class="sxs-lookup"><span data-stu-id="f1cd8-219">MIME/Embedded?</span></span>                               | <span data-ttu-id="f1cd8-220">Sim</span><span class="sxs-lookup"><span data-stu-id="f1cd8-220">Yes</span></span>                          | <span data-ttu-id="f1cd8-221">Não</span><span class="sxs-lookup"><span data-stu-id="f1cd8-221">No</span></span>             |
| <span data-ttu-id="f1cd8-222">Limites de texto?</span><span class="sxs-lookup"><span data-stu-id="f1cd8-222">Text boundaries?</span></span>                             | <span data-ttu-id="f1cd8-223">Sentença, parágrafo, capítulo</span><span class="sxs-lookup"><span data-stu-id="f1cd8-223">Sentence, paragraph, chapter</span></span> | <span data-ttu-id="f1cd8-224">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f1cd8-224">None</span></span>           |
| <span data-ttu-id="f1cd8-225">Implementação com suporte para SPS/SQL Server?</span><span class="sxs-lookup"><span data-stu-id="f1cd8-225">Implementation supported for SPS/SQL Server?</span></span> | <span data-ttu-id="f1cd8-226">Sim</span><span class="sxs-lookup"><span data-stu-id="f1cd8-226">Yes</span></span>                          | <span data-ttu-id="f1cd8-227">Não</span><span class="sxs-lookup"><span data-stu-id="f1cd8-227">No</span></span>             |
| <span data-ttu-id="f1cd8-228">Implementação</span><span class="sxs-lookup"><span data-stu-id="f1cd8-228">Implementation</span></span>                               | <span data-ttu-id="f1cd8-229">Complex</span><span class="sxs-lookup"><span data-stu-id="f1cd8-229">Complex</span></span>                      | <span data-ttu-id="f1cd8-230">Simples</span><span class="sxs-lookup"><span data-stu-id="f1cd8-230">Simple</span></span>         |



 

<span data-ttu-id="f1cd8-231">No exemplo de manipulador de receitas, o formato de arquivo de receita não tem requisitos complexos, portanto, somente [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) foi implementado para suporte de texto completo.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-231">In the recipe handler sample, the recipe file format does not have any complex requirements, so only [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) has been implemented for full-text support.</span></span> <span data-ttu-id="f1cd8-232">A pesquisa de texto completo é implementada para os nós XML nomeados na matriz a seguir.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-232">Full-text search is implemented for the XML nodes named in the following array.</span></span>


```
const PWSTR c_rgszContentXPath[] = {
    L"Recipe/Ingredients/Item",
    L"Recipe/Directions/Step",
    L"Recipe/RecipeInfo/Yield",
    L"Recipe/RecipeKeywords/Keyword",
};
```



<span data-ttu-id="f1cd8-233">O sistema de propriedades contém a `System.Search.Contents` \_ Propriedade (conteúdo de pesquisa PKEY \_ ), que foi criada para fornecer conteúdo de texto completo ao indexador.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-233">The property system contains the `System.Search.Contents` (PKEY\_Search\_Contents) property, which was created to provide full-text content to the indexer.</span></span> <span data-ttu-id="f1cd8-234">O valor dessa propriedade nunca é exibido diretamente na interface do usuário; o texto de todos os nós XML nomeados na matriz acima é concatenado em uma única cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-234">This property's value is never displayed directly in the UI; the text from all of the XML nodes named in the array above are concatenated into a single string.</span></span> <span data-ttu-id="f1cd8-235">Essa cadeia de caracteres é fornecida ao indexador como o conteúdo de texto completo do arquivo de receita por meio de uma chamada para [**IPropertyStoreCache:: SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate) , conforme ilustrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-235">That string is then provided to the indexer as the full-text content of the recipe file through a call to [**IPropertyStoreCache::SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate) as illustrated in the following code example.</span></span>


```
HRESULT CRecipePropertyStore::_LoadSearchContent()
{
    HRESULT hr = S_FALSE;
    _bstr_t bstrContent;
    
    for (UINT i = 0; i < ARRAYSIZE(c_rgszContentXPath); ++i)
    {
        MSXML2::IXMLDOMNodeListPtr spList = 
                                  _spDomDoc->selectNodes(c_rgszContentXPath[i]);
    
        if (spList)
        {
            UINT cElems = spList->length;
            
            for (UINT elt = 0; elt < cElems; ++elt)
            {
                bstrContent += L" ";
                bstrContent += spList->item[elt]->text;
            }
        }
    }
    
    if (bstrContent.length() > 0)
    {
        PROPVARIANT propvar = { VT_LPWSTR };
        hr = SHStrDup(bstrContent, &(propvar.pwszVal));
    
        if (SUCCEEDED(hr))
        {
            hr = _spCache->SetValueAndState(PKEY_Search_Contents, 
                                            &propvar, 
                                            PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    
    return hr;}
```



## <a name="providing-values-for-properties"></a><span data-ttu-id="f1cd8-236">Fornecendo valores para propriedades</span><span class="sxs-lookup"><span data-stu-id="f1cd8-236">Providing Values for Properties</span></span>

<span data-ttu-id="f1cd8-237">Quando usado para ler valores, os manipuladores de propriedades geralmente são invocados por um dos seguintes motivos:</span><span class="sxs-lookup"><span data-stu-id="f1cd8-237">When used to read values, property handlers are usually invoked for one of the following reasons:</span></span>

-   <span data-ttu-id="f1cd8-238">Para enumerar todos os valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-238">To enumerate all property values.</span></span>
-   <span data-ttu-id="f1cd8-239">Para obter o valor de uma propriedade específica.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-239">To get the value of a specific property.</span></span>

<span data-ttu-id="f1cd8-240">Para enumeração, um manipulador de propriedades é solicitado a enumerar suas propriedades durante a indexação ou quando a caixa de diálogo Propriedades solicita que as propriedades sejam exibidas no **outro** grupo.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-240">For enumeration, a property handler is asked to enumerate its properties either during indexing or when the properties dialog box asks for properties to display in the **Other** group.</span></span> <span data-ttu-id="f1cd8-241">A indexação passa constantemente como uma operação em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-241">Indexing goes on constantly as a background operation.</span></span> <span data-ttu-id="f1cd8-242">Sempre que um arquivo é alterado, o indexador é notificado e ele indexa novamente o arquivo solicitando que o manipulador de propriedades enumere suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-242">Whenever a file changes, the indexer is notified, and it re-indexes the file by asking the property handler to enumerate its properties.</span></span> <span data-ttu-id="f1cd8-243">Portanto, é essencial que os manipuladores de propriedade sejam implementados com eficiência e retornam valores de propriedade o mais rápido possível.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-243">Therefore, it is critical that property handlers are implemented efficiently and return property values as quickly as possible.</span></span> <span data-ttu-id="f1cd8-244">Enumere todas as propriedades para as quais você tem valores, assim como faria para qualquer coleção, mas não enumere propriedades que envolvem cálculos de uso intensivo de memória ou solicitações de rede que poderiam torná-los lentos para serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-244">Enumerate all the properties for which you have values, just as you would for any collection, but do not enumerate properties that involve memory-intensive calculations or network requests that could make them slow to retrieve.</span></span>

<span data-ttu-id="f1cd8-245">Ao escrever um manipulador de propriedades, normalmente você precisa considerar os dois conjuntos de propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-245">When writing a property handler, you usually need to consider the following two sets of properties.</span></span>

-   <span data-ttu-id="f1cd8-246">Propriedades primárias: Propriedades às quais o tipo de arquivo dá suporte nativamente.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-246">Primary properties: Properties that your file type supports natively.</span></span> <span data-ttu-id="f1cd8-247">Por exemplo, um manipulador de propriedade de foto para metadados de EXIF (arquivo de imagem intercambiável) dá suporte nativo `System.Photo.FNumber` .</span><span class="sxs-lookup"><span data-stu-id="f1cd8-247">For example, a photo property handler for Exchangeable Image File (EXIF) metadata natively supports `System.Photo.FNumber`.</span></span>
-   <span data-ttu-id="f1cd8-248">Propriedades estendidas: Propriedades às quais o tipo de arquivo dá suporte como parte dos metadados abertos.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-248">Extended properties: Properties that your file type supports as part of open metadata.</span></span>

<span data-ttu-id="f1cd8-249">Como o exemplo usa o cache na memória, a implementação de métodos [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) é apenas uma questão de delegar a esse cache, conforme ilustrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-249">Because the sample uses in-memory cache, implementing [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) methods is just a matter of delegating to that cache, as illustrated in the following code example.</span></span>


```
IFACEMETHODIMP GetCount(__out DWORD *pcProps)
{ return _spCache->GetCount(pcProps); }

IFACEMETHODIMP GetAt(DWORD iProp, __out PROPERTYKEY *pkey)
{ return _spCache->GetAt(iProp, pkey); }

IFACEMETHODIMP GetValue(REFPROPERTYKEY key, __out PROPVARIANT *pPropVar)
{ return _spCache->GetValue(key, pPropVar); }
```



<span data-ttu-id="f1cd8-250">Se você optar por não delegar ao cache na memória, deverá implementar seus métodos para fornecer> seguinte comportamento esperado:</span><span class="sxs-lookup"><span data-stu-id="f1cd8-250">If you choose not to delegate to the in-memory cache, you must implement your methods to provide> the following expected behavior:</span></span>

-   <span data-ttu-id="f1cd8-251">[**IPropertyStore:: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)): se não houver propriedades, esse método retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-251">[**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)): If there are no properties, this method returns **S\_OK**.</span></span>
-   <span data-ttu-id="f1cd8-252">[**IPropertyStore:: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)): se *iProp* for maior ou igual a *CProps*, esse método retornará e \_ INVALIDARG e a estrutura apontada pelo parâmetro *PKEY* será preenchida com zeros.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-252">[**IPropertyStore::GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)): If *iProp* is greater than or equal to *cProps*, this method returns E\_INVALIDARG and the structure pointed to by the *pkey* parameter is filled with zeroes.</span></span>
-   <span data-ttu-id="f1cd8-253">[**IPropertyStore:: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) e [**IPropertyStore:: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) refletem o estado atual do manipulador de propriedades.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-253">[**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) and [**IPropertyStore::GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) reflect the current state of the property handler.</span></span> <span data-ttu-id="f1cd8-254">Se um [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) é adicionado ou removido do arquivo por meio de [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), esses dois métodos devem refletir que mudam na próxima vez que forem chamados.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-254">If a [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) is added to or removed from the file through [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), these two methods must reflect that change the next time they are called.</span></span>
-   <span data-ttu-id="f1cd8-255">[**IPropertyStore:: GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)): se esse método for solicitado para um valor que não existe, ele retornará **S \_ OK** com o valor relatado como VT \_ vazio.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-255">[**IPropertyStore::GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)): If this method is asked for a value that does not exist, it returns **S\_OK** with the value reported as VT\_EMPTY.</span></span>

## <a name="writing-back-values"></a><span data-ttu-id="f1cd8-256">Gravando valores de volta</span><span class="sxs-lookup"><span data-stu-id="f1cd8-256">Writing Back Values</span></span>

<span data-ttu-id="f1cd8-257">Quando o manipulador de propriedades grava o valor de uma propriedade usando [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), ele não grava o valor no arquivo até que [**IPropertyStore:: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-257">When the property handler writes the value of a property using [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), it does not write the value to the file until [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) is called.</span></span> <span data-ttu-id="f1cd8-258">O cache na memória pode ser útil para implementar esse esquema.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-258">The in-memory cache can be useful in implementing this scheme.</span></span> <span data-ttu-id="f1cd8-259">No código de exemplo, a implementação **IPropertyStore:: SetValue** simplesmente define o novo valor no cache na memória e define o estado dessa propriedade como PSC \_ sujo.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-259">In the sample code the **IPropertyStore::SetValue** implementation simply sets the new value in the in-memory cache and sets the state of that property to PSC\_DIRTY.</span></span>


```
HRESULT CRecipePropertyStore::SetValue(REFPROPERTYKEY key, const PROPVARIANT *pPropVar)
    {
    
    HRESULT hr = E_FAIL;
    
    if (IsEqualPropertyKey(key, PKEY_Search_Contents))
    {
        // This property is read-only
        hr = HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED);  
    }
    else
    {
        hr = _spCache->SetValueAndState(key, pPropVar, PSC_DIRTY);
    }
    
    return hr;
}
```



<span data-ttu-id="f1cd8-260">Em qualquer implementação de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , o seguinte comportamento é esperado de [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="f1cd8-260">In any [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) implementation, the following behavior is expected from [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)):</span></span>

-   <span data-ttu-id="f1cd8-261">Se a propriedade já existir, o valor da propriedade será definido.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-261">If the property already exists, the value of the property is set.</span></span>
-   <span data-ttu-id="f1cd8-262">Se a propriedade não existir, a nova propriedade será adicionada e seu valor definido.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-262">If the property does not exist, the new property is added and its value set.</span></span>
-   <span data-ttu-id="f1cd8-263">Se o valor da propriedade não puder ser persistido com a mesma precisão fornecida (por exemplo, truncamento devido a limitações de tamanho no formato de arquivo), o valor será definido o máximo possível e os S inplaces \_ \_ serão retornados.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-263">If the property value cannot be persisted at the same accuracy as given (for instance, truncation due to size limitations in the file format), the value is set as far as possible and INPLACE\_S\_TRUNCATED is returned.</span></span>
-   <span data-ttu-id="f1cd8-264">Se a propriedade não for suportada pelo manipulador de propriedade, `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` será retornado.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-264">If the property is not supported by the property handler, `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` is returned.</span></span>
-   <span data-ttu-id="f1cd8-265">Se houver outro motivo pelo qual o valor da propriedade não pode ser definido, como o arquivo que está sendo bloqueado ou falta de direitos para editar através de ACLs (listas de controle de acesso), STG \_ E \_ ACCESSDENIED será retornado.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-265">If there is another reason that the property value cannot be set, such as the file being locked or lack of rights to edit through access control lists (ACLs), then STG\_E\_ACCESSDENIED is returned.</span></span>

<span data-ttu-id="f1cd8-266">Uma grande vantagem de usar fluxos, como o exemplo, é a confiabilidade.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-266">One major advantage of using streams, as the sample, is reliability.</span></span> <span data-ttu-id="f1cd8-267">Os manipuladores de propriedades sempre devem considerar que não podem deixar um arquivo em um estado inconsistente no caso de uma falha catastrófica.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-267">Property handlers must always consider that they cannot leave a file in an inconsistent state in the case of a catastrophic failure.</span></span> <span data-ttu-id="f1cd8-268">É óbvio que a corrupção dos arquivos de um usuário deve ser evitada e a melhor maneira de fazer isso é com um mecanismo de "cópia na gravação".</span><span class="sxs-lookup"><span data-stu-id="f1cd8-268">Corrupting a user's files obviously should be avoided, and the best way to do this is with a "copy-on-write" mechanism.</span></span> <span data-ttu-id="f1cd8-269">Se o seu manipulador de propriedades usar um fluxo para acessar um arquivo, você obterá esse comportamento automaticamente; o sistema grava todas as alterações no fluxo, substituindo o arquivo pela nova cópia somente durante a operação de confirmação.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-269">If your property handler uses a stream to access a file, you get this behavior automatically; the system writes any changes to the stream, replacing the file with the new copy only during the commit operation.</span></span>

<span data-ttu-id="f1cd8-270">Para substituir esse comportamento e controlar o processo de salvamento de arquivos manualmente, você pode recusar o comportamento de salvamento seguro definindo o valor ManualSafeSave na entrada do registro do manipulador, conforme ilustrado aqui.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-270">To override this behavior and control the file saving process manually, you can opt out of the safe save behavior by setting the ManualSafeSave value in your handler's registry entry as illustrated here.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         ManualSafeSave = 1
```

<span data-ttu-id="f1cd8-271">Quando um manipulador Especifica o valor de ManualSafeSave, o fluxo com o qual ele é inicializado não é um fluxo transacionado (STGM \_ transacionado).</span><span class="sxs-lookup"><span data-stu-id="f1cd8-271">When a handler specifies the ManualSafeSave value, the stream with which it is initialized is not a transacted stream (STGM\_TRANSACTED).</span></span> <span data-ttu-id="f1cd8-272">O próprio manipulador deve implementar a função de salvamento seguro para garantir que o arquivo não seja corrompido se a operação de salvamento for interrompida.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-272">The handler itself must implement the safe save function to ensure that the file is not corrupted if the save operation is interrupted.</span></span> <span data-ttu-id="f1cd8-273">Se o manipulador implementar a gravação in-loco, ele gravará no fluxo que ele recebeu.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-273">If the handler implements in-place writing, it will write to the stream that it is given.</span></span> <span data-ttu-id="f1cd8-274">Se o manipulador não oferecer suporte a esse recurso, ele deverá recuperar um fluxo com o qual gravar a cópia atualizada do arquivo usando [**IDestinationStreamFactory:: GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream).</span><span class="sxs-lookup"><span data-stu-id="f1cd8-274">If the handler does not support this feature, then it must retrieve a stream with which to write the updated copy of the file using [**IDestinationStreamFactory::GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream).</span></span> <span data-ttu-id="f1cd8-275">Depois que o manipulador terminar a gravação, ele deverá chamar [**IPropertyStore:: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) no fluxo original para concluir a operação e substituir o conteúdo do fluxo original pela nova cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-275">After the handler is done writing, it should call [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) on the original stream to complete the operation, and replace the contents of the original stream with the new copy of the file.</span></span>

<span data-ttu-id="f1cd8-276">ManualSafeSave também será a situação padrão se você não inicializar o manipulador com um fluxo.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-276">ManualSafeSave is also the default situation if you do not initialize your handler with a stream.</span></span> <span data-ttu-id="f1cd8-277">Sem um fluxo original para receber o conteúdo do fluxo temporário, você deve usar o [**ReplaceFile**](/windows/win32/api/winbase/nf-winbase-replacefilea) para executar uma substituição atômica do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-277">Without an original stream to receive the contents of the temporary stream, you must use [**ReplaceFile**](/windows/win32/api/winbase/nf-winbase-replacefilea) to perform an atomic replacement of the source file.</span></span>

<span data-ttu-id="f1cd8-278">Formatos de arquivo grandes que serão usados de forma que produza arquivos maiores que 1 MB devem implementar o suporte para a gravação de propriedades in-loco; caso contrário, o comportamento de desempenho não atende às expectativas dos clientes do sistema de propriedades.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-278">Large file formats that will be used in a way that produces files greater than 1 MB should implement support for in-place property writing; otherwise, the performance behavior does not meet the expectations of clients of the property system.</span></span> <span data-ttu-id="f1cd8-279">Nesse cenário, o tempo necessário para gravar propriedades não deve ser afetado pelo tamanho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-279">In this scenario, the time required to write properties should not be affected by the file size.</span></span>

<span data-ttu-id="f1cd8-280">Para arquivos muito grandes, por exemplo, um arquivo de vídeo de 1 GB ou mais, uma solução diferente é necessária.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-280">For very large files, for example a video file of 1 GB or more, a different solution is required.</span></span> <span data-ttu-id="f1cd8-281">Se não houver espaço suficiente no arquivo para executar a gravação in-loco, o manipulador poderá falhar na atualização da propriedade se a quantidade de espaço reservado para gravação de propriedades in-loco tiver sido esgotada.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-281">If there is not enough space in the file to perform in-place writing, the handler may fail the property update if the amount of space reserved for in-place property writing has been exhausted.</span></span> <span data-ttu-id="f1cd8-282">Essa falha ocorre para evitar o mau desempenho resultante de 2 GB de e/s (1 para ler, 1 para gravar).</span><span class="sxs-lookup"><span data-stu-id="f1cd8-282">This failure occurs to avoid poor performance arising from 2 GB of IO (1 to read, 1 to write).</span></span> <span data-ttu-id="f1cd8-283">Devido a essa falha em potencial, esses formatos de arquivo devem reservar espaço suficiente para a gravação de propriedades in-loco.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-283">Because of this potential failure, these file formats should reserve enough space for in-place property writing.</span></span>

<span data-ttu-id="f1cd8-284">Se o arquivo tiver espaço suficiente em seu cabeçalho para gravar metadados e se a gravação desses metadados não fizer com que o arquivo aumente ou diminua, talvez seja seguro gravar no local.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-284">If the file has enough space in its header to write metadata, and if the writing of that metadata does not cause the file to grow or shrink, it might be safe to write in-place.</span></span> <span data-ttu-id="f1cd8-285">Recomendamos 64 KB como ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-285">We recommend 64 KB as a starting point.</span></span> <span data-ttu-id="f1cd8-286">Gravar no local é equivalente ao manipulador solicitando ManualSafeSave e chamando [**IStream:: Commit**](/windows/win32/api/objidl/nf-objidl-istream-commit) na implementação de [**IPropertyStore:: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85))e tem um desempenho muito melhor do que a cópia em gravação.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-286">Writing in-place is equivalent to the handler asking for ManualSafeSave and calling [**IStream::Commit**](/windows/win32/api/objidl/nf-objidl-istream-commit) in the implementation of [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), and has much better performance than copy-on-write.</span></span> <span data-ttu-id="f1cd8-287">Se o tamanho do arquivo for alterado devido a alterações no valor da propriedade, a gravação in-loco não deve ser tentada devido ao potencial de um arquivo corrompido no caso de um encerramento anormal.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-287">If the file size changes due to property value changes, writing in-place should not be attempted because of the potential for a corrupted file in the event of an abnormal termination.</span></span>

> [!Note]  
> <span data-ttu-id="f1cd8-288">Por motivos de desempenho, recomendamos que a opção ManualSafeSave seja usada com manipuladores de propriedade que trabalham com arquivos que são 100 KB ou maiores.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-288">For performance reasons we recommend that the ManualSafeSave option be used with property handlers working with files that are 100 KB or larger.</span></span>

 

<span data-ttu-id="f1cd8-289">Conforme ilustrado na implementação de exemplo a seguir de [**IPropertyStore:: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), o manipulador para ManualSafeSave é registrado para ilustrar a opção de salvamento seguro manual.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-289">As illustrated in the following sample implementation of [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), the handler for ManualSafeSave is registered to illustrate the manual safe save option.</span></span> <span data-ttu-id="f1cd8-290">O método **\_ SaveCacheToDom** grava os valores de propriedade armazenados no cache na memória para o objeto XMLdocument.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-290">The **\_SaveCacheToDom** method writes the property values stored in the in-memory cache to the XMLdocument object.</span></span>


```
HRESULT CRecipePropertyStore::Commit()
{
    HRESULT hr = E_UNEXPECTED;
    if (_pCache)
    {
        // Check grfMode to ensure writes are allowed.
        hr = STG_E_ACCESSDENIED;
        if (_grfMode & STGM_READWRITE)
        {
            // Save the internal value cache to XML DOM object.
            hr = _SaveCacheToDom();
            if (SUCCEEDED(hr))
            {
                // Reset the output stream.
                LARGE_INTEGER liZero = {};
                hr = _pStream->Seek(liZero, STREAM_SEEK_SET, NULL);
```



<span data-ttu-id="f1cd8-291">Em seguida, pergunte se o pecificada dá suporte a [**IDestinationStreamFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory).</span><span class="sxs-lookup"><span data-stu-id="f1cd8-291">Next, ask whether the pecified supports [**IDestinationStreamFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory).</span></span>


```
                        if (SUCCEEDED(hr))
                        {
                            // Write the XML out to the temprorary stream and commit it.
                            VARIANT varStream = {};
                            varStream.vt = VT_UNKNOWN;
                            varStream.punkVal = pStreamCommit;
                            hr = _pDomDoc->save(varStream);
                            if (SUCCEEDED(hr))
                            {
                                hr = pStreamCommit->Commit(STGC_DEFAULT);_
```



<span data-ttu-id="f1cd8-292">Em seguida, confirme o fluxo original, que grava os dados de volta no arquivo original de maneira segura.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-292">Next, commit the original stream, which writes the data back to the original file in a safe manner.</span></span>


```
                        if (SUCCEEDED(hr))
                                {
                                    // Commit the real output stream.
                                    _pStream->Commit(STGC_DEFAULT);
                                }
                            }

                            pStreamCommit->Release();
                        }

                        pSafeCommit->Release();
                    }
                }
            }
        }
    }
```



<span data-ttu-id="f1cd8-293">Em seguida, examine a implementação de **\_ SaveCacheToDom** .</span><span class="sxs-lookup"><span data-stu-id="f1cd8-293">Then examine the **\_SaveCacheToDom** implementation.</span></span>


```
// Saves the values in the internal cache back to the internal DOM object.
HRESULT CRecipePropertyStore::_SaveCacheToDom()
{
    // Iterate over each property in the internal value cache.
    DWORD cProps;  
```



<span data-ttu-id="f1cd8-294">Em seguida, obtenha o número de propriedades armazenadas no cache na memória.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-294">Next, get the number of properties stored in the in-memory cache.</span></span>


```
HRESULT hr = _pCache->GetCount(&cProps);          
            
```



<span data-ttu-id="f1cd8-295">Agora, itere pelas propriedades para determinar se o valor de uma propriedade foi alterado desde que foi carregado na memória.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-295">Now iterate through the properties to determine whether the value of a property has been changed since it was loaded into memory.</span></span>


```
    for (UINT i = 0; SUCCEEDED(hr) && (i < cProps); ++i)
    {
        PROPERTYKEY key;
        hr = _pCache->GetAt(i, &key); 
```



<span data-ttu-id="f1cd8-296">O método [**IPropertyStoreCache:: GetState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-getstate) Obtém o estado da propriedade no cache.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-296">The [**IPropertyStoreCache::GetState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-getstate) method gets the state of the property in the cache.</span></span> <span data-ttu-id="f1cd8-297">O \_ sinalizador incorreto do PSC, que foi definido na implementação [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) , marca uma propriedade como alterada.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-297">The PSC\_DIRTY flag, which was set in the [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) implementation, marks a property as changed.</span></span>


```
        if (SUCCEEDED(hr))
        {
            // check the cache state; only save dirty properties
            PSC_STATE psc;
            hr = _pCache->GetState(key, &psc);
            if (SUCCEEDED(hr) && psc == PSC_DIRTY)
            {
                // get the cached value
                PROPVARIANT propvar = {};
                hr = _pCache->GetValue(key, &propvar); 
```



<span data-ttu-id="f1cd8-298">Mapeie a propriedade para o nó XML, conforme especificado na matriz de **exemplo \_ rgPropertyMap** .</span><span class="sxs-lookup"><span data-stu-id="f1cd8-298">Map the property to the XML node as specified in the **eg\_rgPropertyMap** array.</span></span>


```
if (SUCCEEDED(hr))
                {
                    // save as a native property if the key is in the property map
                    BOOL fIsNativeProperty = FALSE;
                    for (UINT i = 0; i < ARRAYSIZE(g_rgPROPERTYMAP); ++i)
                    {
                        if (IsEqualPropertyKey(key, *g_rgPROPERTYMAP[i].pkey))
                        {
                            fIsNativeProperty = TRUE;
                            hr = _SaveProperty(propvar, g_rgPROPERTYMAP[i]);
                            break;
                        }     
```



<span data-ttu-id="f1cd8-299">Se uma propriedade não estiver no mapa, ela será uma nova propriedade que foi definida pelo Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-299">If a property is not in the map, it is a new property that was set by Windows Explorer.</span></span> <span data-ttu-id="f1cd8-300">Como há suporte para metadados abertos, salve a nova propriedade na seção **ExtendedProperties** do XML.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-300">Because open metadata is supported, save the new property in the **ExtendedProperties** section of the XML.</span></span>


```
                    
                    // Otherwise, save as an extended property.
                    if (!fIsNativeProperty)
                    {
                        hr = _SaveExtendedProperty(key, propvar);
                    }

                    PropVariantClear(&propvar);
                }
            }
        }
    }

    return hr;    
```



## <a name="implementing-ipropertystorecapabilities"></a><span data-ttu-id="f1cd8-301">Implementando IPropertyStoreCapabilities</span><span class="sxs-lookup"><span data-stu-id="f1cd8-301">Implementing IPropertyStoreCapabilities</span></span>

<span data-ttu-id="f1cd8-302">[**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) informa a interface do usuário do Shell se uma determinada propriedade pode ser editada na interface do usuário do Shell.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-302">[**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) informs the Shell UI whether a particular property can be edited in the Shell UI.</span></span> <span data-ttu-id="f1cd8-303">É importante observar que isso se refere apenas à capacidade de editar a propriedade na interface do usuário, não se você pode chamar [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) com êxito na propriedade.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-303">It is important to note that this relates only to the ability to edit the property in the UI, not whether you can successfully call [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) on the property.</span></span> <span data-ttu-id="f1cd8-304">Uma propriedade que provokes um valor de retorno de S \_ false de [**IPropertyStoreCapabilities:: IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) ainda pode ser capaz de ser definida por meio de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-304">A property that provokes a return value of S\_FALSE from [**IPropertyStoreCapabilities::IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) might still be capable of being set through an application.</span></span>


```
interface IPropertyStoreCapabilities : IUnknown
{
    HRESULT IsPropertyWritable([in] REFPROPERTYKEY key);
}
```



<span data-ttu-id="f1cd8-305">[**IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) retorna **S \_ OK** para indicar que os usuários finais devem ter permissão para editar a propriedade diretamente; S \_ false indica que eles não deveriam.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-305">[**IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) returns **S\_OK** to indicate that end users should be allowed to edit the property directly; S\_FALSE indicates that they should not.</span></span> <span data-ttu-id="f1cd8-306">\_O falso pode significar que os aplicativos são responsáveis por gravar a propriedade, não pelos usuários.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-306">S\_FALSE can mean that applications are responsible for writing the property, not users.</span></span> <span data-ttu-id="f1cd8-307">O Shell desabilita os controles de edição conforme apropriado, com base nos resultados de chamadas para esse método.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-307">The Shell disables editing controls as appropriate based on the results of calls to this method.</span></span> <span data-ttu-id="f1cd8-308">Um manipulador que não implementa [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) é considerado para dar suporte a metadados abertos por meio do suporte para a gravação de qualquer propriedade.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-308">A handler that does not implement [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) is assumed to support open metadata through support for the writing of any property.</span></span>

<span data-ttu-id="f1cd8-309">Se você estiver criando um manipulador que manipula somente as propriedades somente leitura, deverá implementar o método **Initialize** ([**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)ou [**IINITIALIZEWITHFILE**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)) para que ele retorne STG \_ E \_ ACCESSDENIED quando chamado com o sinalizador de STGM \_ ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-309">If you are building a handler that handles only read-only properties, then you should implement your **Initialize** method ([**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem), or [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)) so that it returns STG\_E\_ACCESSDENIED when called with the STGM\_READWRITE flag.</span></span>

<span data-ttu-id="f1cd8-310">Algumas propriedades têm seu atributo [isInnate](./propdesc-schema-typeinfo.md) definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-310">Some properties have their [isInnate](./propdesc-schema-typeinfo.md) attribute set to **true**.</span></span> <span data-ttu-id="f1cd8-311">As propriedades inato têm as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="f1cd8-311">Innate properties have the following characteristics:</span></span>

-   <span data-ttu-id="f1cd8-312">A propriedade geralmente é calculada de alguma forma.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-312">The property is usually calculated in some way.</span></span> <span data-ttu-id="f1cd8-313">Por exemplo, `System.Image.BitDepth` é calculado a partir da própria imagem.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-313">For instance, `System.Image.BitDepth` is calculated from the image itself.</span></span>
-   <span data-ttu-id="f1cd8-314">A alteração da propriedade não faz sentido sem alterar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-314">Changing the property would not make sense without changing the file.</span></span> <span data-ttu-id="f1cd8-315">Por exemplo, `System.Image.Dimensions` a alteração não redimensionaria a imagem, portanto, não faz sentido permitir que o usuário a altere.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-315">For instance, changing `System.Image.Dimensions` would not resize the image, so it does not make sense to allow the user to change it.</span></span>
-   <span data-ttu-id="f1cd8-316">Em alguns casos, essas propriedades são fornecidas automaticamente pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-316">In some cases, these properties are provided automatically by the system.</span></span> <span data-ttu-id="f1cd8-317">Os exemplos incluem `System.DateModified` , que é fornecido pelo sistema de arquivos, e `System.SharedWith` , que se baseia em quem o usuário está compartilhando o arquivo.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-317">Examples include `System.DateModified`, which is provided by the file system, and `System.SharedWith`, which is based on who the user is sharing the file with.</span></span>

<span data-ttu-id="f1cd8-318">Devido a essas características, as propriedades marcadas como *IsInnate* são fornecidas ao usuário na interface de usuário do Shell somente como propriedades somente leitura.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-318">Due to these characteristics, properties marked as *IsInnate* are provided to the user in the Shell UI only as read-only properties.</span></span> <span data-ttu-id="f1cd8-319">Se uma propriedade estiver marcada como *IsInnate*, o sistema de propriedades não armazenará essa propriedade no manipulador de propriedades.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-319">If a property is marked as *IsInnate*, the property system does not store that property in the property handler.</span></span> <span data-ttu-id="f1cd8-320">Portanto, os manipuladores de propriedade não precisam de código especial para considerar essas propriedades em suas implementações.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-320">Therefore, property handlers do not need special code to account for these properties in their implementations.</span></span> <span data-ttu-id="f1cd8-321">Se o valor do atributo *IsInnate* não for explicitamente declarado para uma determinada propriedade, o valor padrão será **false**.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-321">If the value of the *IsInnate* attribute is not explicitly stated for a particular property, the default value is **false**.</span></span>

## <a name="registering-and-distributing-property-handlers"></a><span data-ttu-id="f1cd8-322">Registrando e distribuindo manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="f1cd8-322">Registering and Distributing Property Handlers</span></span>

<span data-ttu-id="f1cd8-323">Com o manipulador de propriedade implementado, ele deve ser registrado e sua extensão de nome de arquivo associada ao manipulador.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-323">With the property handler implemented, it must be registered and its file name extension associated with the handler.</span></span> <span data-ttu-id="f1cd8-324">Para obter mais informações, consulte [registrando e distribuindo manipuladores de propriedade](./prophand-reg-dist.md).</span><span class="sxs-lookup"><span data-stu-id="f1cd8-324">For more information, see [Registering and Distributing Property Handlers](./prophand-reg-dist.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1cd8-325">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1cd8-325">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1cd8-326">Noções básicas sobre manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="f1cd8-326">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="f1cd8-327">Usando nomes de tipos</span><span class="sxs-lookup"><span data-stu-id="f1cd8-327">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="f1cd8-328">Usando listas de propriedades</span><span class="sxs-lookup"><span data-stu-id="f1cd8-328">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
</dt> <dt>

[<span data-ttu-id="f1cd8-329">Registrando e distribuindo manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="f1cd8-329">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="f1cd8-330">Práticas recomendadas e perguntas frequentes do manipulador de propriedades</span><span class="sxs-lookup"><span data-stu-id="f1cd8-330">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
