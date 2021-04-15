---
title: Usando o objeto Active Desktop
description: Este artigo contém informações sobre o objeto ActiveDesktop que faz parte da API do shell do Windows. Esse objeto, por meio de sua interface IActiveDesktop, permite que você adicione, remova e altere itens na área de trabalho.
ms.assetid: 68d72b0f-f5e9-4fff-bb13-4c60d1dd7009
keywords:
- Objeto ActiveDesktop
- Área de trabalho ativa
- Enumeração, itens da área de trabalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7e61a4a9145386fc4c84a454aa79558b8d5df79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104453987"
---
# <a name="using-the-active-desktop-object"></a><span data-ttu-id="c752f-107">Usando o objeto Active Desktop</span><span class="sxs-lookup"><span data-stu-id="c752f-107">Using the Active Desktop Object</span></span>

<span data-ttu-id="c752f-108">\[Esse recurso tem suporte apenas no Windows XP ou anterior.</span><span class="sxs-lookup"><span data-stu-id="c752f-108">\[This feature is supported only under Windows XP or earlier.</span></span> <span data-ttu-id="c752f-109">\]</span><span class="sxs-lookup"><span data-stu-id="c752f-109">\]</span></span>

<span data-ttu-id="c752f-110">Este artigo contém informações sobre o objeto **ActiveDesktop** que faz parte da API do shell do Windows.</span><span class="sxs-lookup"><span data-stu-id="c752f-110">This article contains information on the **ActiveDesktop** object that is part of the Windows Shell API.</span></span> <span data-ttu-id="c752f-111">Esse objeto, por meio de sua interface [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) , permite que você adicione, remova e altere itens na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c752f-111">This object, through its [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface, enables you to add, remove, and change items on the desktop.</span></span>

## <a name="overview-of-the-active-desktop-interface"></a><span data-ttu-id="c752f-112">Visão geral da interface de área de trabalho ativa</span><span class="sxs-lookup"><span data-stu-id="c752f-112">Overview of the Active Desktop Interface</span></span>

-   [<span data-ttu-id="c752f-113">Acessando o Active Desktop</span><span class="sxs-lookup"><span data-stu-id="c752f-113">Accessing the Active Desktop</span></span>](#accessing-the-active-desktop)
-   [<span data-ttu-id="c752f-114">Adicionando um item da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="c752f-114">Adding a Desktop Item</span></span>](#adding-a-desktop-item)
-   [<span data-ttu-id="c752f-115">Enumerando os itens da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="c752f-115">Enumerating the Desktop Items</span></span>](#enumerating-the-desktop-items)

<span data-ttu-id="c752f-116">O Active Desktop é um recurso introduzido com o Microsoft Internet Explorer 4,0 que permite incluir documentos e itens HTML (como controles ActiveX da Microsoft e miniaplicativos Java) diretamente em sua área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c752f-116">The Active Desktop is a feature introduced with Microsoft Internet Explorer 4.0 that enables you to include HTML documents and items (such as Microsoft ActiveX Controls and Java applets) directly to your desktop.</span></span> <span data-ttu-id="c752f-117">A interface [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) , que faz parte da API do shell do Windows, é usada para adicionar, remover e modificar programaticamente os itens na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c752f-117">The [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface, which is part of the Windows Shell API, is used to programmatically add, remove, and modify the items on the desktop.</span></span> <span data-ttu-id="c752f-118">Itens de área de trabalho ativas também podem ser adicionados usando um arquivo de formato de definição de canal (CDF).</span><span class="sxs-lookup"><span data-stu-id="c752f-118">Active Desktop items can also be added using a Channel Definition Format (CDF) file.</span></span>

### <a name="accessing-the-active-desktop"></a><span data-ttu-id="c752f-119">Acessando o Active Desktop</span><span class="sxs-lookup"><span data-stu-id="c752f-119">Accessing the Active Desktop</span></span>

<span data-ttu-id="c752f-120">Para acessar o Active Desktop, um aplicativo cliente precisaria criar uma instância do objeto ActiveDesktop (CLSID \_ ActiveDesktop) com a função [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) e recuperar um ponteiro para a interface [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) do objeto.</span><span class="sxs-lookup"><span data-stu-id="c752f-120">To access the Active Desktop, a client application would need to create an instance of the ActiveDesktop object (CLSID\_ActiveDesktop) with the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function and retrieve a pointer to the object's [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface.</span></span>

<span data-ttu-id="c752f-121">O exemplo a seguir mostra como recuperar um ponteiro para a interface [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) .</span><span class="sxs-lookup"><span data-stu-id="c752f-121">The following sample shows how to retrieve a pointer to the [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface.</span></span>


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

//Insert code to call the IActiveDesktop methods

// Call the Release method
pActiveDesktop->Release();
```



### <a name="adding-a-desktop-item"></a><span data-ttu-id="c752f-122">Adicionando um item da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="c752f-122">Adding a Desktop Item</span></span>

<span data-ttu-id="c752f-123">Há três métodos que você pode usar para adicionar um item da área de trabalho: [**IActiveDesktop:: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem), [**IActiveDesktop:: AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui)e [**IActiveDesktop:: addurl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl).</span><span class="sxs-lookup"><span data-stu-id="c752f-123">There are three methods you can use to add a desktop item: [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem), [**IActiveDesktop::AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui), and [**IActiveDesktop::AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl).</span></span> <span data-ttu-id="c752f-124">Cada item da área de trabalho adicionado ao Active Desktop deve ter uma URL de origem diferente.</span><span class="sxs-lookup"><span data-stu-id="c752f-124">Each desktop item added to the Active Desktop must have a different source URL.</span></span>

<span data-ttu-id="c752f-125">Os métodos [**IActiveDesktop:: AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui) e [**IActiveDesktop:: addurl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl) fornecem a opção para exibir as várias interfaces de usuário que podem ser exibidas antes de adicionar um item da área de trabalho ao Active Desktop.</span><span class="sxs-lookup"><span data-stu-id="c752f-125">The [**IActiveDesktop::AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui) and [**IActiveDesktop::AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl) methods both provide the option to display the various user interfaces that can be displayed before adding a desktop item to the Active Desktop.</span></span> <span data-ttu-id="c752f-126">As interfaces verificam se os usuários desejam adicionar o item da área de trabalho ao seu Active Desktop.</span><span class="sxs-lookup"><span data-stu-id="c752f-126">The interfaces verify whether users want to add the desktop item to their Active Desktop.</span></span> <span data-ttu-id="c752f-127">As interfaces também notificam os usuários sobre os riscos de segurança que são garantidos pelas configurações da zona de segurança de URL e perguntarão aos usuários se eles gostariam de criar uma assinatura para esse item da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c752f-127">The interfaces also notify users of any security risks that are warranted by the URL security zone settings, and they ask users if they would like to create a subscription for this desktop item.</span></span> <span data-ttu-id="c752f-128">Os dois métodos também fornecem uma maneira de suprimir as interfaces do usuário.</span><span class="sxs-lookup"><span data-stu-id="c752f-128">Both methods also provide a way of suppressing the user interfaces.</span></span> <span data-ttu-id="c752f-129">O método [**IActiveDesktop:: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) requer uma chamada para [**IActiveDesktop:: ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) para atualizar o registro.</span><span class="sxs-lookup"><span data-stu-id="c752f-129">The [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) method requires a call to [**IActiveDesktop::ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) in order to update the registry.</span></span> <span data-ttu-id="c752f-130">Para o **IActiveDesktop:: AddDesktopItemWithUI**, o aplicativo cliente deve liberar imediatamente a interface [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) e, em seguida, usar a função [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para recuperar uma interface para uma instância do objeto **ActiveDesktop** que inclui o item da área de trabalho recém-adicionado.</span><span class="sxs-lookup"><span data-stu-id="c752f-130">For the **IActiveDesktop::AddDesktopItemWithUI**, the client application must immediately release the [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface and then use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function to retrieve an interface to an instance of the **ActiveDesktop** object that includes the newly added desktop item.</span></span>

<span data-ttu-id="c752f-131">O método [**IActiveDesktop:: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) adiciona o item da área de trabalho especificado ao Active Desktop sem nenhuma interface do usuário, a menos que as configurações da zona de segurança de URL o impeçam.</span><span class="sxs-lookup"><span data-stu-id="c752f-131">The [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) method adds the specified desktop item to the Active Desktop without any user interface, unless the URL security zone settings prevent it.</span></span> <span data-ttu-id="c752f-132">Se as configurações da zona de segurança da URL não permitirem que o item da área de trabalho seja adicionado sem avisar o usuário, o método falhará.</span><span class="sxs-lookup"><span data-stu-id="c752f-132">If the URL security zone settings do not allow the desktop item to be added without prompting the user, the method fails.</span></span> <span data-ttu-id="c752f-133">**IActiveDesktop:: AddDesktopItem** também requer uma chamada para [**IActiveDesktop:: ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) a fim de atualizar o registro.</span><span class="sxs-lookup"><span data-stu-id="c752f-133">**IActiveDesktop::AddDesktopItem** also requires a call to [**IActiveDesktop::ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) in order to update the registry.</span></span>

<span data-ttu-id="c752f-134">O exemplo a seguir demonstra como adicionar um item da área de trabalho com o método [**IActiveDesktop:: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) .</span><span class="sxs-lookup"><span data-stu-id="c752f-134">The following sample demonstrates how to add a desktop item with the [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) method.</span></span>


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;
COMPONENT compDesktopItem;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

// Initialize the COMPONENT structure
compDesktopItem.dwSize = sizeof(COMPONENT);

// Insert code that adds the information about the desktop item 
// to the COMPONENT structure

// Add the desktop item
pActiveDesktop->AddDesktopItem(&compDesktopItem,0);

// Save the changes to the registry
pActiveDesktop->ApplyChanges(AD_APPLY_ALL);
```



### <a name="enumerating-the-desktop-items"></a><span data-ttu-id="c752f-135">Enumerando os itens da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="c752f-135">Enumerating the Desktop Items</span></span>

<span data-ttu-id="c752f-136">Para enumerar os itens da área de trabalho instalados atualmente no Active Desktop, o aplicativo cliente precisa recuperar o número total de itens da área de trabalho instalados usando o método [**IActiveDesktop:: GetDesktopItemCount**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitemcount) e, em seguida, criando um loop que recupera a estrutura de [**componente**](/windows/desktop/api/shlobj_core/ns-shlobj_core-component) para cada item da área de trabalho chamando o método [**IActiveDesktop:: GetDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitem) usando o índice de item da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c752f-136">To enumerate the desktop items currently installed on the Active Desktop, the client application needs to retrieve the total number of desktop items installed using the [**IActiveDesktop::GetDesktopItemCount**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitemcount) method and then creating a loop that retrieves the [**COMPONENT**](/windows/desktop/api/shlobj_core/ns-shlobj_core-component) structure for each desktop item by calling the [**IActiveDesktop::GetDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitem) method using the desktop item index.</span></span>

<span data-ttu-id="c752f-137">O exemplo a seguir demonstra uma maneira de enumerar os itens da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c752f-137">The following sample demonstrates one way to enumerate the desktop items.</span></span>


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;
COMPONENT compDesktopItem;
int intCount;
int intIndex = 0;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

pActiveDesktop->GetDesktopItemCount(&intCount,0);

compDesktopItem.dwSize = sizeof(COMPONENT);

while(intIndex<=(intCount-1))
{
    //get the COMPONENT structure for the current desktop item
    pActiveDesktop->GetDesktopItem(intIndex, &compDesktopItem,0);

    //Insert code that processes the structure

    //Increment the index
    intIndex++;

    //Insert code to clean-up structure for next component
}

// Call the Release method
pActiveDesktop->Release();
```



 

 