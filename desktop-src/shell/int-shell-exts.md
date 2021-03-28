---
description: Grande parte da implementação de um objeto de manipulador de extensão de Shell é ditada por seu tipo. No entanto, há alguns elementos comuns. Este tópico discute os aspectos da implementação que são compartilhados por todos os manipuladores de extensão do Shell.
ms.assetid: ce21ca0f-157c-4f69-bcf9-dc259c3bac80
title: Inicializando manipuladores de extensão do Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6a27b6273c5e342dc4caf545fb3593cdad66261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968207"
---
# <a name="initializing-shell-extension-handlers"></a><span data-ttu-id="c7a6e-105">Inicializando manipuladores de extensão do Shell</span><span class="sxs-lookup"><span data-stu-id="c7a6e-105">Initializing Shell Extension Handlers</span></span>

<span data-ttu-id="c7a6e-106">Grande parte da implementação de um objeto de manipulador de extensão de Shell é ditada por seu tipo.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-106">Much of the implementation of a Shell extension handler object is dictated by its type.</span></span> <span data-ttu-id="c7a6e-107">No entanto, há alguns elementos comuns.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-107">There are, however, some common elements.</span></span> <span data-ttu-id="c7a6e-108">Este tópico discute os aspectos da implementação que são compartilhados por todos os manipuladores de extensão do Shell.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-108">This topic discusses those aspects of implementation that are shared by all Shell extension handlers.</span></span>

<span data-ttu-id="c7a6e-109">Todos os manipuladores de extensão do shell são objetos COM (Component Object Model) em processo.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-109">All Shell extension handlers are in-process Component Object Model (COM) objects.</span></span> <span data-ttu-id="c7a6e-110">Eles devem ser atribuídos a um GUID e registrados conforme descrito em [Registrando manipuladores de extensão do Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="c7a6e-110">They must be assigned a GUID and registered as described in [Registering Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="c7a6e-111">Eles são implementados como DLLs e devem exportar as seguintes funções padrão:</span><span class="sxs-lookup"><span data-stu-id="c7a6e-111">They are implemented as DLLs and must export the following standard functions:</span></span>

-   <span data-ttu-id="c7a6e-112">[**DllMain**](../dlls/dllmain.md).</span><span class="sxs-lookup"><span data-stu-id="c7a6e-112">[**DllMain**](../dlls/dllmain.md).</span></span> <span data-ttu-id="c7a6e-113">O ponto de entrada padrão para a DLL.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-113">The standard entry point to the DLL.</span></span>
-   <span data-ttu-id="c7a6e-114">[**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject).</span><span class="sxs-lookup"><span data-stu-id="c7a6e-114">[**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject).</span></span> <span data-ttu-id="c7a6e-115">Expõe a fábrica de classes do objeto.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-115">Exposes the object's class factory.</span></span>
-   <span data-ttu-id="c7a6e-116">[**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow).</span><span class="sxs-lookup"><span data-stu-id="c7a6e-116">[**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow).</span></span> <span data-ttu-id="c7a6e-117">COM chama essa função para determinar se o objeto está atendendo a clientes.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-117">COM calls this function to determine whether the object is serving any clients.</span></span> <span data-ttu-id="c7a6e-118">Caso contrário, o sistema pode descarregar a DLL e liberar a memória associada.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-118">If not, the system can unload the DLL and free the associated memory.</span></span>

<span data-ttu-id="c7a6e-119">Como todos os objetos COM, os manipuladores de extensão do Shell devem implementar uma interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e uma [fábrica de classes](../com/implementing-iclassfactory.md).</span><span class="sxs-lookup"><span data-stu-id="c7a6e-119">Like all COM objects, Shell extension handlers must implement an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface and a [class factory](../com/implementing-iclassfactory.md).</span></span> <span data-ttu-id="c7a6e-120">A maioria também deve implementar uma interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) ou [**ISHELLEXTINIT**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) no Windows XP ou anterior.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-120">Most must also implement either an [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) or [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface in Windows XP or earlier.</span></span> <span data-ttu-id="c7a6e-121">Elas foram substituídas por [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) e [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-121">These were replaced by [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) and [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) in Windows Vista.</span></span> <span data-ttu-id="c7a6e-122">O Shell usa essas interfaces para inicializar o manipulador.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-122">The Shell uses these interfaces to initialize the handler.</span></span>

<span data-ttu-id="c7a6e-123">A interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) deve ser implementada pelo seguinte:</span><span class="sxs-lookup"><span data-stu-id="c7a6e-123">The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface must be implemented by the following:</span></span>

-   <span data-ttu-id="c7a6e-124">Manipuladores de ícone</span><span class="sxs-lookup"><span data-stu-id="c7a6e-124">Icon handlers</span></span>
-   <span data-ttu-id="c7a6e-125">Manipuladores de dados</span><span class="sxs-lookup"><span data-stu-id="c7a6e-125">Data handlers</span></span>
-   <span data-ttu-id="c7a6e-126">Descartar manipuladores</span><span class="sxs-lookup"><span data-stu-id="c7a6e-126">Drop handlers</span></span>

<span data-ttu-id="c7a6e-127">A interface [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) deve ser implementada pelo seguinte:</span><span class="sxs-lookup"><span data-stu-id="c7a6e-127">The [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface must be implemented by the following:</span></span>

-   <span data-ttu-id="c7a6e-128">Manipuladores de menu de atalho</span><span class="sxs-lookup"><span data-stu-id="c7a6e-128">Shortcut menu handlers</span></span>
-   <span data-ttu-id="c7a6e-129">Manipuladores de arrastar e soltar</span><span class="sxs-lookup"><span data-stu-id="c7a6e-129">Drag-and-drop handlers</span></span>
-   <span data-ttu-id="c7a6e-130">Manipuladores de folha de propriedades</span><span class="sxs-lookup"><span data-stu-id="c7a6e-130">Property sheet handlers</span></span>

<span data-ttu-id="c7a6e-131">Os seguintes assuntos são discutidos no restante deste tópico:</span><span class="sxs-lookup"><span data-stu-id="c7a6e-131">The following subjects are discussed in the remainder of this topic:</span></span>

-   [<span data-ttu-id="c7a6e-132">Implementando IPersistFile</span><span class="sxs-lookup"><span data-stu-id="c7a6e-132">Implementing IPersistFile</span></span>](#implementing-ipersistfile)
-   [<span data-ttu-id="c7a6e-133">Implementando IShellExtInit</span><span class="sxs-lookup"><span data-stu-id="c7a6e-133">Implementing IShellExtInit</span></span>](#implementing-ishellextinit)
-   [<span data-ttu-id="c7a6e-134">Personalização de InfoTip</span><span class="sxs-lookup"><span data-stu-id="c7a6e-134">Infotip Customization</span></span>](#infotip-customization)
-   [<span data-ttu-id="c7a6e-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c7a6e-135">Related topics</span></span>](#related-topics)

## <a name="implementing-ipersistfile"></a><span data-ttu-id="c7a6e-136">Implementando IPersistFile</span><span class="sxs-lookup"><span data-stu-id="c7a6e-136">Implementing IPersistFile</span></span>

<span data-ttu-id="c7a6e-137">A interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) foi projetada para permitir que um objeto seja carregado ou salvo em um arquivo de disco.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-137">The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is designed to permit an object to be loaded from or saved to a disk file.</span></span> <span data-ttu-id="c7a6e-138">Ele tem seis métodos além de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), cinco de sua própria e o método [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) que ele herda de [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist).</span><span class="sxs-lookup"><span data-stu-id="c7a6e-138">It has six methods in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), five of its own, and the [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) method that it inherits from [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist).</span></span> <span data-ttu-id="c7a6e-139">Com extensões de Shell, **IPersist** é usado apenas para inicializar um objeto de manipulador de extensão de Shell.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-139">With Shell extensions, **IPersist** is used only to initialize a Shell extension handler object.</span></span> <span data-ttu-id="c7a6e-140">Como normalmente não há necessidade de ler ou gravar no disco, somente os métodos **GetClassID** e [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) exigem uma implementação sem token.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-140">Because there is typically no need to read from or write to the disk, only the **GetClassID** and [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) methods require a nontoken implementation.</span></span>

<span data-ttu-id="c7a6e-141">O Shell chama [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) primeiro e a função retorna o identificador de classe (CLSID) do objeto do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-141">The Shell calls [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) first, and the function returns the class identifier (CLSID) of the extension handler object.</span></span> <span data-ttu-id="c7a6e-142">Em seguida, o Shell chama [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) e passa em dois valores.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-142">The Shell then calls [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) and passes in two values.</span></span> <span data-ttu-id="c7a6e-143">O primeiro, *pszFile*, é uma cadeia de caracteres Unicode com o nome do arquivo ou da pasta em que o Shell está prestes a operar.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-143">The first, *pszFile*, is a Unicode string with the name of the file or folder that Shell is about to operate on.</span></span> <span data-ttu-id="c7a6e-144">O segundo é *dwMode*, que indica o modo de acesso do arquivo.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-144">The second is *dwMode*, which indicates the file access mode.</span></span> <span data-ttu-id="c7a6e-145">Como normalmente não há necessidade de acessar arquivos, o *dwMode* geralmente é zero.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-145">Because there is normally no need to access files, *dwMode* is typically zero.</span></span> <span data-ttu-id="c7a6e-146">O método armazena esses valores conforme necessário para referência posterior.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-146">The method stores these values as needed for later reference.</span></span>

<span data-ttu-id="c7a6e-147">O fragmento de código a seguir ilustra como um manipulador de extensão de shell típico implementa os métodos [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) e [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) .</span><span class="sxs-lookup"><span data-stu-id="c7a6e-147">The following code fragment illustrates how a typical Shell extension handler implements the [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) and [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) methods.</span></span> <span data-ttu-id="c7a6e-148">Ele foi projetado para lidar com ANSI ou Unicode.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-148">It is designed to handle either ANSI or Unicode.</span></span> <span data-ttu-id="c7a6e-149">CLSID \_ SampleExtHandler é o GUID do objeto do manipulador de extensão e CSampleShellExtension é o nome da classe usada para implementar a interface.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-149">CLSID\_SampleExtHandler is the extension handler object's GUID, and CSampleShellExtension is the name of the class used to implement the interface.</span></span> <span data-ttu-id="c7a6e-150">As variáveis **m \_ szFileName** e **m \_ dwMode** são variáveis privadas que são usadas para armazenar o nome do arquivo e os sinalizadores de acesso.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-150">The **m\_szFileName** and **m\_dwMode** variables are private variables that are used to store the file's name and access flags.</span></span>


```C++
class CSampleShellExtension : public IPersistFile
{
    // Method declarations not included

    private:
    WCHAR m_szFileName[MAX_PATH];    // The file name
    DWORD m_dwMode;                  // The file access mode
}

IFACEMETHODIMP CSampleShellExtension::GetClassID(__out CLSID *pCLSID)
{
    *pCLSID = CLSID_SampleExtHandler;
}

IFACEMETHODIMP CSampleShellExtension::Load(PCWSTR pszFile, DWORD dwMode)
{
    m_dwMode = dwMode;
    return StringCchCopy(m_szFileName, ARRAYSIZE(m_szFileName), pszFile); 
}

// The implementation sample is continued in the next section.
```



## <a name="implementing-ishellextinit"></a><span data-ttu-id="c7a6e-151">Implementando IShellExtInit</span><span class="sxs-lookup"><span data-stu-id="c7a6e-151">Implementing IShellExtInit</span></span>

<span data-ttu-id="c7a6e-152">A interface [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) tem apenas um método, [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), além de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="c7a6e-152">The [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface has only one method, [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="c7a6e-153">O método tem três parâmetros que o Shell pode usar para passar vários tipos de informações.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-153">The method has three parameters that the Shell can use to pass in various types of information.</span></span> <span data-ttu-id="c7a6e-154">Os valores passados dependem do tipo de manipulador e alguns podem ser definidos como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-154">The values passed in depend on the type of handler, and some can be set to **NULL**.</span></span>

-   <span data-ttu-id="c7a6e-155">*pidlFolder* mantém o ponteiro de uma pasta para uma lista de identificadores de item (PIDL).</span><span class="sxs-lookup"><span data-stu-id="c7a6e-155">*pidlFolder* holds a folder's pointer to an item identifier list (PIDL).</span></span> <span data-ttu-id="c7a6e-156">Este é um PIDL absoluto.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-156">This is an absolute PIDL.</span></span> <span data-ttu-id="c7a6e-157">Para extensões de folha de propriedades, esse valor é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-157">For property sheet extensions, this value is **NULL**.</span></span> <span data-ttu-id="c7a6e-158">Para extensões de menu de atalho, é o PIDL da pasta que contém o item cujo menu de atalho está sendo exibido.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-158">For shortcut menu extensions, it is the PIDL of the folder that contains the item whose shortcut menu is being displayed.</span></span> <span data-ttu-id="c7a6e-159">Para manipuladores do tipo "arrastar e soltar" não padrão, é o PIDL da pasta de destino.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-159">For nondefault drag-and-drop handlers, it is the PIDL of the target folder.</span></span>
-   <span data-ttu-id="c7a6e-160">*pDataObject* mantém um ponteiro para a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de um objeto de dados.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-160">*pDataObject* holds a pointer to a data object's [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) interface.</span></span> <span data-ttu-id="c7a6e-161">O objeto de dados contém um ou mais nomes de arquivo no formato [CF \_ HDROP](dragdrop.md) .</span><span class="sxs-lookup"><span data-stu-id="c7a6e-161">The data object holds one or more file names in [CF\_HDROP](dragdrop.md) format.</span></span>
-   <span data-ttu-id="c7a6e-162">*hRegKey* mantém uma chave do registro para o tipo de objeto ou pasta de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-162">*hRegKey* holds a registry key for the file object or folder type.</span></span>

<span data-ttu-id="c7a6e-163">O método [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) armazena o nome do arquivo, o ponteiro do [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) e a chave do registro conforme necessário para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-163">The [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method stores the file name, [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer, and registry key as needed for later use.</span></span> <span data-ttu-id="c7a6e-164">O fragmento de código a seguir ilustra uma implementação de **IShellExtInit:: Initialize**.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-164">The following code fragment illustrates an implementation of **IShellExtInit::Initialize**.</span></span> <span data-ttu-id="c7a6e-165">Para simplificar, este exemplo supõe que o objeto de dados contenha apenas um único arquivo.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-165">For simplicity, this example assumes that the data object contains only a single file.</span></span> <span data-ttu-id="c7a6e-166">Em geral, o objeto de dados pode conter vários arquivos, cada um deles precisará ser extraído.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-166">In general, the data object might contain multiple files, each of which will need to be extracted.</span></span>


```C++
// This code continues the CSampleShellExtension sample shown in the
// "Implementing IPersistFile" section above.

class CSampleShellExtension : public IShellExtInit
{
    // Method declarations not included
    
    private:
    // IDList of the folder for extensions invoked on the folder, such as 
    // background context menu handlers or nondefault drag-and-drop handlers. 
    PIDLIST_ABSOLUTE m_pidlFolder;
    
    // The data object contains an expression of the items that the handler is 
    // being initialized for. Use SHCreateShellItemArrayFromDataObject to 
    // convert this object to an array of items. Use SHGetItemFromObject if you
    // are only interested in a single Shell item. If you need a file system
    // path, use IShellItem::GetDisplayName(SIGDN_FILESYSPATH, ...).
    IDataObject *m_pdtobj;
    
    // For context menu handlers, the registry key provides access to verb 
    // instance data that might be stored there. This is a rare feature to use 
    // so most extensions do not need this variable.
    HKEY m_hRegKey;             
}
    
// This method must be very efficient. Do not do any unnecessary work here.
// Use Initialize to acquire resources that will be used later.

IFACEMETHODIMP CSampleShellExtension::Initialize(__in_opt PCIDLIST_ABSOLUTE pidlFolder,
                                                 __in_opt IDataObject *pDataObject, 
                                                 __in_opt HKEY hRegKey) 
{ 
    // In some cases, handlers are initialized multiple times. Therefore, 
    // clear any previous state here.
    CoTaskMemFree(m_pidlFolder);
    m_pidlFolder = NULL;
    
    if (m_pdtobj)
    { 
        m_pdtobj->Release(); 
    }
    
    if (m_hRegKey)
    {
        RegCloseKey(m_hRegKey);
        m_hRegKey = NULL;
    }
    
    // Capture the inputs for use later.
    HRESULT hr = S_OK;
    
    if (pidlFolder)
    {
        m_pidlFolder = ILClone(pidlFolder);   // Make a copy to use later.
        hr = m_pidlFolder ? S_OK : E_OUTOFMEMORY;
    }
    
    if (SUCCEEDED(hr))
    {
        // If a data object pointer was passed into the method, save it and
        // extract the file name. 
        if (pDataObject) 
        { 
            m_pdtobj = pDataObject; 
            m_pdtobj->AddRef(); 
        }
    
        // It is uncommon to use the registry handle, but if you need it,
        // duplicate it now.
        if (hRegKey)
        {
            LSTATUS const result = RegOpenKeyEx(hRegKey, NULL, 0, KEY_READ, &m_hRegKey); 
            hr = HRESULT_FROM_WIN32(result);
        }
    }
    
    return hr;
}
```



## <a name="infotip-customization"></a><span data-ttu-id="c7a6e-167">Personalização de InfoTip</span><span class="sxs-lookup"><span data-stu-id="c7a6e-167">Infotip Customization</span></span>

<span data-ttu-id="c7a6e-168">Há duas maneiras de personalizar o Infotips.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-168">There are two ways to customize infotips.</span></span> <span data-ttu-id="c7a6e-169">Uma maneira é implementar um objeto que dê suporte a [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) e, em seguida, registrar o objeto sob a subchave apropriada no registro (veja abaixo).</span><span class="sxs-lookup"><span data-stu-id="c7a6e-169">One way is to implement an object that supports [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) and then register the object under the proper subkey in the registry (see below).</span></span> <span data-ttu-id="c7a6e-170">Como alternativa, você pode especificar uma cadeia de caracteres fixa ou uma lista de determinadas propriedades de arquivo a serem exibidas.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-170">Alternatively, you can specify either a fixed string or a list of certain file properties to be displayed.</span></span>

<span data-ttu-id="c7a6e-171">Para exibir uma cadeia de caracteres fixa para uma extensão de namespace, crie uma subchave chamada **InfoTip** abaixo da chave CLSID de sua extensão de namespace.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-171">To display a fixed string for a namespace extension, create a subkey called **InfoTip** beneath the CLSID key of your namespace extension.</span></span> <span data-ttu-id="c7a6e-172">Defina os dados dessa subchave como a cadeia de caracteres que você deseja exibir.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-172">Set the data of that subkey to be the string you want to be displayed.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID}
         InfoTip = InfoTip string for your namespace extension
```

<span data-ttu-id="c7a6e-173">Para exibir uma cadeia de caracteres fixa para um tipo de arquivo, crie uma subchave chamada **InfoTip** abaixo da chave **ProgID** do tipo de arquivo para o qual você deseja fornecer Infotips.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-173">To display a fixed string for a file type, create a subkey called **InfoTip** beneath the **ProgID** key of the file type for which you want to supply infotips.</span></span> <span data-ttu-id="c7a6e-174">Defina os dados dessa subchave como a cadeia de caracteres que você deseja exibir.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-174">Set the data of that subkey to be the string you want to be displayed.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = InfoTip string for all files of this type
```

<span data-ttu-id="c7a6e-175">Se você quiser que o Shell mostre determinadas propriedades de arquivo em InfoTip para um tipo de arquivo específico, crie uma subchave chamada **InfoTip** abaixo da chave **ProgID** desse tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-175">If you want the Shell to show certain file properties in the infotip for a specific file type, create a subkey called **InfoTip** beneath the **ProgID** key of that file type.</span></span> <span data-ttu-id="c7a6e-176">Defina os dados dessa subchave como uma lista delineada por ponto-e-vírgula de nomes de propriedade canônicas ou {fmtid}, pares de PID em que *propName* é um nome de propriedade canônica e *{fmtid}, PID* é um [**par fmtid/PID**](./objects.md).</span><span class="sxs-lookup"><span data-stu-id="c7a6e-176">Set the data of that subkey to be a semicolon-delineated list of canonical property names or {fmtid}, pid pairs where *propname* is a canonical property name and *{fmtid},pid* is a [**FMTID/PID pair**](./objects.md).</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = propname;propname;{fmtid},pid;{fmtid},pid
```

<span data-ttu-id="c7a6e-177">Os nomes de propriedade a seguir podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="c7a6e-177">The following property names can be used.</span></span>



| <span data-ttu-id="c7a6e-178">Nome da propriedade</span><span class="sxs-lookup"><span data-stu-id="c7a6e-178">Property Name</span></span>    | <span data-ttu-id="c7a6e-179">Descrição</span><span class="sxs-lookup"><span data-stu-id="c7a6e-179">Description</span></span>                   | <span data-ttu-id="c7a6e-180">Recuperado de</span><span class="sxs-lookup"><span data-stu-id="c7a6e-180">Retrieved From</span></span>                                                                            |
|------------------|-------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7a6e-181">Autor</span><span class="sxs-lookup"><span data-stu-id="c7a6e-181">Author</span></span>           | <span data-ttu-id="c7a6e-182">Autor do documento</span><span class="sxs-lookup"><span data-stu-id="c7a6e-182">Author of the document</span></span>        | [<span data-ttu-id="c7a6e-183">**autor do PIDSI \_**</span><span class="sxs-lookup"><span data-stu-id="c7a6e-183">**PIDSI\_AUTHOR**</span></span>](../stg/the-summary-information-property-set.md)                             |
| <span data-ttu-id="c7a6e-184">Título</span><span class="sxs-lookup"><span data-stu-id="c7a6e-184">Title</span></span>            | <span data-ttu-id="c7a6e-185">Título do documento</span><span class="sxs-lookup"><span data-stu-id="c7a6e-185">Title of the document</span></span>         | [<span data-ttu-id="c7a6e-186">**título do PIDSI \_**</span><span class="sxs-lookup"><span data-stu-id="c7a6e-186">**PIDSI\_TITLE**</span></span>](../stg/the-summary-information-property-set.md)                              |
| <span data-ttu-id="c7a6e-187">Assunto</span><span class="sxs-lookup"><span data-stu-id="c7a6e-187">Subject</span></span>          | <span data-ttu-id="c7a6e-188">Resumo do assunto</span><span class="sxs-lookup"><span data-stu-id="c7a6e-188">Subject summary</span></span>               | [<span data-ttu-id="c7a6e-189">**assunto do PIDSI \_**</span><span class="sxs-lookup"><span data-stu-id="c7a6e-189">**PIDSI\_SUBJECT**</span></span>](../stg/the-summary-information-property-set.md)                            |
| <span data-ttu-id="c7a6e-190">Comentário</span><span class="sxs-lookup"><span data-stu-id="c7a6e-190">Comment</span></span>          | <span data-ttu-id="c7a6e-191">Comentários do documento</span><span class="sxs-lookup"><span data-stu-id="c7a6e-191">Document comments</span></span>             | <span data-ttu-id="c7a6e-192">[**PIDSI \_**](../stg/the-summary-information-property-set.md) Propriedades de comentário ou pasta/unidade</span><span class="sxs-lookup"><span data-stu-id="c7a6e-192">[**PIDSI\_COMMENT**](../stg/the-summary-information-property-set.md) or folder/drive properties</span></span> |
| <span data-ttu-id="c7a6e-193">PageCount</span><span class="sxs-lookup"><span data-stu-id="c7a6e-193">PageCount</span></span>        | <span data-ttu-id="c7a6e-194">Número de páginas</span><span class="sxs-lookup"><span data-stu-id="c7a6e-194">Number of pages</span></span>               | [<span data-ttu-id="c7a6e-195">**PIDSI \_ PageCount**</span><span class="sxs-lookup"><span data-stu-id="c7a6e-195">**PIDSI\_PAGECOUNT**</span></span>](../stg/the-summary-information-property-set.md)                          |
| <span data-ttu-id="c7a6e-196">Name</span><span class="sxs-lookup"><span data-stu-id="c7a6e-196">Name</span></span>             | <span data-ttu-id="c7a6e-197">Nome amigável</span><span class="sxs-lookup"><span data-stu-id="c7a6e-197">Friendly name</span></span>                 | <span data-ttu-id="c7a6e-198">Exibição de pasta padrão</span><span class="sxs-lookup"><span data-stu-id="c7a6e-198">Standard folder view</span></span>                                                                      |
| <span data-ttu-id="c7a6e-199">OriginalLocation</span><span class="sxs-lookup"><span data-stu-id="c7a6e-199">OriginalLocation</span></span> | <span data-ttu-id="c7a6e-200">Local do arquivo original</span><span class="sxs-lookup"><span data-stu-id="c7a6e-200">Location of original file</span></span>     | <span data-ttu-id="c7a6e-201">Pasta do porta-arquivos e pasta lixeira</span><span class="sxs-lookup"><span data-stu-id="c7a6e-201">Briefcase folder and Recycle Bin folder</span></span>                                                   |
| <span data-ttu-id="c7a6e-202">DateDeleted</span><span class="sxs-lookup"><span data-stu-id="c7a6e-202">DateDeleted</span></span>      | <span data-ttu-id="c7a6e-203">O arquivo de data foi excluído</span><span class="sxs-lookup"><span data-stu-id="c7a6e-203">Date file was deleted</span></span>         | <span data-ttu-id="c7a6e-204">Pasta da lixeira</span><span class="sxs-lookup"><span data-stu-id="c7a6e-204">Recycle Bin folder</span></span>                                                                        |
| <span data-ttu-id="c7a6e-205">Tipo</span><span class="sxs-lookup"><span data-stu-id="c7a6e-205">Type</span></span>             | <span data-ttu-id="c7a6e-206">Tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="c7a6e-206">Type of file</span></span>                  | <span data-ttu-id="c7a6e-207">Exibição de detalhes da pasta padrão</span><span class="sxs-lookup"><span data-stu-id="c7a6e-207">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="c7a6e-208">Tamanho</span><span class="sxs-lookup"><span data-stu-id="c7a6e-208">Size</span></span>             | <span data-ttu-id="c7a6e-209">Tamanho do arquivo</span><span class="sxs-lookup"><span data-stu-id="c7a6e-209">Size of file</span></span>                  | <span data-ttu-id="c7a6e-210">Exibição de detalhes da pasta padrão</span><span class="sxs-lookup"><span data-stu-id="c7a6e-210">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="c7a6e-211">SyncCopyIn</span><span class="sxs-lookup"><span data-stu-id="c7a6e-211">SyncCopyIn</span></span>       | <span data-ttu-id="c7a6e-212">O mesmo que OriginalLocation</span><span class="sxs-lookup"><span data-stu-id="c7a6e-212">Same as OriginalLocation</span></span>      | <span data-ttu-id="c7a6e-213">O mesmo que OriginalLocation</span><span class="sxs-lookup"><span data-stu-id="c7a6e-213">Same as OriginalLocation</span></span>                                                                  |
| <span data-ttu-id="c7a6e-214">Modificado</span><span class="sxs-lookup"><span data-stu-id="c7a6e-214">Modified</span></span>         | <span data-ttu-id="c7a6e-215">Data da última modificação</span><span class="sxs-lookup"><span data-stu-id="c7a6e-215">Date last modified</span></span>            | <span data-ttu-id="c7a6e-216">Exibição de detalhes da pasta padrão</span><span class="sxs-lookup"><span data-stu-id="c7a6e-216">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="c7a6e-217">Criado</span><span class="sxs-lookup"><span data-stu-id="c7a6e-217">Created</span></span>          | <span data-ttu-id="c7a6e-218">Data de criação</span><span class="sxs-lookup"><span data-stu-id="c7a6e-218">Date created</span></span>                  | <span data-ttu-id="c7a6e-219">Exibição de detalhes da pasta padrão</span><span class="sxs-lookup"><span data-stu-id="c7a6e-219">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="c7a6e-220">Acessíveis</span><span class="sxs-lookup"><span data-stu-id="c7a6e-220">Accessed</span></span>         | <span data-ttu-id="c7a6e-221">Data do último acesso</span><span class="sxs-lookup"><span data-stu-id="c7a6e-221">Date last accessed</span></span>            | <span data-ttu-id="c7a6e-222">Exibição de detalhes da pasta padrão</span><span class="sxs-lookup"><span data-stu-id="c7a6e-222">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="c7a6e-223">Inpasta</span><span class="sxs-lookup"><span data-stu-id="c7a6e-223">InFolder</span></span>         | <span data-ttu-id="c7a6e-224">Diretório que contém o arquivo</span><span class="sxs-lookup"><span data-stu-id="c7a6e-224">Directory containing the file</span></span> | <span data-ttu-id="c7a6e-225">Resultados da pesquisa de documentos</span><span class="sxs-lookup"><span data-stu-id="c7a6e-225">Document search results</span></span>                                                                   |
| <span data-ttu-id="c7a6e-226">Rank</span><span class="sxs-lookup"><span data-stu-id="c7a6e-226">Rank</span></span>             | <span data-ttu-id="c7a6e-227">Qualidade de correspondência de pesquisa</span><span class="sxs-lookup"><span data-stu-id="c7a6e-227">Quality of search match</span></span>       | <span data-ttu-id="c7a6e-228">Resultados da pesquisa de documentos</span><span class="sxs-lookup"><span data-stu-id="c7a6e-228">Document search results</span></span>                                                                   |
| <span data-ttu-id="c7a6e-229">FreeSpace</span><span class="sxs-lookup"><span data-stu-id="c7a6e-229">FreeSpace</span></span>        | <span data-ttu-id="c7a6e-230">Espaço de armazenamento disponível</span><span class="sxs-lookup"><span data-stu-id="c7a6e-230">Available storage space</span></span>       | <span data-ttu-id="c7a6e-231">Unidades de disco</span><span class="sxs-lookup"><span data-stu-id="c7a6e-231">Disk drives</span></span>                                                                               |
| <span data-ttu-id="c7a6e-232">NumberOfVisits</span><span class="sxs-lookup"><span data-stu-id="c7a6e-232">NumberOfVisits</span></span>   | <span data-ttu-id="c7a6e-233">Número de visitas</span><span class="sxs-lookup"><span data-stu-id="c7a6e-233">Number of visits</span></span>              | <span data-ttu-id="c7a6e-234">Pasta Favoritos</span><span class="sxs-lookup"><span data-stu-id="c7a6e-234">Favorites folder</span></span>                                                                          |
| <span data-ttu-id="c7a6e-235">Atributos</span><span class="sxs-lookup"><span data-stu-id="c7a6e-235">Attributes</span></span>       | <span data-ttu-id="c7a6e-236">Atributos do arquivo</span><span class="sxs-lookup"><span data-stu-id="c7a6e-236">File Attributes</span></span>               | <span data-ttu-id="c7a6e-237">Exibição de detalhes da pasta padrão</span><span class="sxs-lookup"><span data-stu-id="c7a6e-237">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="c7a6e-238">Empresa</span><span class="sxs-lookup"><span data-stu-id="c7a6e-238">Company</span></span>          | <span data-ttu-id="c7a6e-239">Nome da empresa</span><span class="sxs-lookup"><span data-stu-id="c7a6e-239">Company name</span></span>                  | [<span data-ttu-id="c7a6e-240">**\_empresa PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="c7a6e-240">**PIDDSI\_COMPANY**</span></span>](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)   |
| <span data-ttu-id="c7a6e-241">Categoria</span><span class="sxs-lookup"><span data-stu-id="c7a6e-241">Category</span></span>         | <span data-ttu-id="c7a6e-242">Categoria do documento</span><span class="sxs-lookup"><span data-stu-id="c7a6e-242">Document category</span></span>             | [<span data-ttu-id="c7a6e-243">**\_categoria PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="c7a6e-243">**PIDDSI\_CATEGORY**</span></span>](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)  |
| <span data-ttu-id="c7a6e-244">Direitos autorais</span><span class="sxs-lookup"><span data-stu-id="c7a6e-244">Copyright</span></span>        | <span data-ttu-id="c7a6e-245">Direitos autorais da mídia</span><span class="sxs-lookup"><span data-stu-id="c7a6e-245">Media copyright</span></span>               | [<span data-ttu-id="c7a6e-246">**\_direitos autorais do PIDMSI**</span><span class="sxs-lookup"><span data-stu-id="c7a6e-246">**PIDMSI\_COPYRIGHT**</span></span>](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md) |
| <span data-ttu-id="c7a6e-247">HTMLInfoTipFile</span><span class="sxs-lookup"><span data-stu-id="c7a6e-247">HTMLInfoTipFile</span></span>  | <span data-ttu-id="c7a6e-248">Arquivo InfoTip HTML</span><span class="sxs-lookup"><span data-stu-id="c7a6e-248">HTML InfoTip file</span></span>             | <span data-ttu-id="c7a6e-249">Arquivo de Desktop.ini para a pasta</span><span class="sxs-lookup"><span data-stu-id="c7a6e-249">Desktop.ini file for folder</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="c7a6e-250">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c7a6e-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7a6e-251">Registrando manipuladores de extensão do Shell</span><span class="sxs-lookup"><span data-stu-id="c7a6e-251">Registering Shell Extension Handlers</span></span>](reg-shell-exts.md)
</dt> </dl>

 

 
