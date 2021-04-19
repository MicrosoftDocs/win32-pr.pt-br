---
description: A classe CBasePropertyPage é uma classe abstrata para implementar uma página de propriedades. Use essa classe se você estiver escrevendo um filtro (ou outro objeto) que dê suporte a páginas de propriedades.
ms.assetid: 80e77827-ed2f-426e-aa6f-c2aa90031751
title: Classe CBasePropertyPage (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 168b2d450ec8efc30851286120d47ba6247fe6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780884"
---
# <a name="cbasepropertypage-class"></a><span data-ttu-id="8a902-104">Classe CBasePropertyPage</span><span class="sxs-lookup"><span data-stu-id="8a902-104">CBasePropertyPage class</span></span>

![hierarquia de classe CBasePropertyPage](images/cprop01.png)

<span data-ttu-id="8a902-106">A `CBasePropertyPage` classe é uma classe abstrata para implementar uma página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8a902-106">The `CBasePropertyPage` class is an abstract class for implementing a property page.</span></span> <span data-ttu-id="8a902-107">Use essa classe se você estiver escrevendo um filtro (ou outro objeto) que dê suporte a páginas de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8a902-107">Use this class if you are writing a filter (or other object) that supports property pages.</span></span>



| <span data-ttu-id="8a902-108">Variáveis de membro protegido</span><span class="sxs-lookup"><span data-stu-id="8a902-108">Protected Member Variables</span></span>                                             | <span data-ttu-id="8a902-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a902-109">Description</span></span>                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a902-110">**\_bDirty m**</span><span class="sxs-lookup"><span data-stu-id="8a902-110">**m\_bDirty**</span></span>](cbasepropertypage-m-bdirty.md)                        | <span data-ttu-id="8a902-111">Indica se alguma das propriedades foi alterada.</span><span class="sxs-lookup"><span data-stu-id="8a902-111">Indicates whether any of the properties have changed.</span></span>                                                                             |
| [<span data-ttu-id="8a902-112">**\_caixa de diálogo m**</span><span class="sxs-lookup"><span data-stu-id="8a902-112">**m\_DialogId**</span></span>](cbasepropertypage-m-dialogid.md)                    | <span data-ttu-id="8a902-113">Identificador de recurso da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8a902-113">Resource identifier for the dialog.</span></span>                                                                                               |
| [<span data-ttu-id="8a902-114">**m \_ Dlg**</span><span class="sxs-lookup"><span data-stu-id="8a902-114">**m\_Dlg**</span></span>](cbasepropertypage-m-dlg.md)                              | <span data-ttu-id="8a902-115">Identificador para a janela de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8a902-115">Handle to the dialog window.</span></span>                                                                                                      |
| [<span data-ttu-id="8a902-116">**\_HWND m**</span><span class="sxs-lookup"><span data-stu-id="8a902-116">**m\_hwnd**</span></span>](cbasepropertypage-m-hwnd.md)                            | <span data-ttu-id="8a902-117">Identificador para a janela de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8a902-117">Handle to the dialog window.</span></span>                                                                                                      |
| [<span data-ttu-id="8a902-118">**\_pPageSite m**</span><span class="sxs-lookup"><span data-stu-id="8a902-118">**m\_pPageSite**</span></span>](cbasepropertypage-m-ppagesite.md)                  | <span data-ttu-id="8a902-119">Ponteiro para a interface **IPropertyPageSite** do site da página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8a902-119">Pointer to the **IPropertyPageSite** interface of the property page site.</span></span>                                                         |
| [<span data-ttu-id="8a902-120">**\_título m**</span><span class="sxs-lookup"><span data-stu-id="8a902-120">**m\_TitleId**</span></span>](cbasepropertypage-m-titleid.md)                      | <span data-ttu-id="8a902-121">Identificador de recurso para uma cadeia de caracteres que contém o título da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8a902-121">Resource identifier for a string that contains the dialog title.</span></span>                                                                  |
| <span data-ttu-id="8a902-122">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="8a902-122">Public Methods</span></span>                                                         | <span data-ttu-id="8a902-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a902-123">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="8a902-124">**CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="8a902-124">**CBasePropertyPage**</span></span>](cbasepropertypage-cbasepropertypage.md)       | <span data-ttu-id="8a902-125">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="8a902-125">Constructor method.</span></span>                                                                                                               |
| [<span data-ttu-id="8a902-126">**~ CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="8a902-126">**~CBasePropertyPage**</span></span>](cbasepropertypage--cbasepropertypage.md)     | <span data-ttu-id="8a902-127">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="8a902-127">Destructor method.</span></span> <span data-ttu-id="8a902-128">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="8a902-128">Virtual.</span></span>                                                                                                       |
| [<span data-ttu-id="8a902-129">**OnActivate**</span><span class="sxs-lookup"><span data-stu-id="8a902-129">**OnActivate**</span></span>](cbasepropertypage-onactivate.md)                     | <span data-ttu-id="8a902-130">Chamado quando a página de propriedades é ativada.</span><span class="sxs-lookup"><span data-stu-id="8a902-130">Called when the property page is activated.</span></span> <span data-ttu-id="8a902-131">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="8a902-131">Virtual.</span></span>                                                                              |
| [<span data-ttu-id="8a902-132">**OnApplyChanges**</span><span class="sxs-lookup"><span data-stu-id="8a902-132">**OnApplyChanges**</span></span>](cbasepropertypage-onapplychanges.md)             | <span data-ttu-id="8a902-133">Chamado quando o usuário aplica alterações à página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8a902-133">Called when the user applies changes to the property page.</span></span> <span data-ttu-id="8a902-134">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="8a902-134">Virtual.</span></span>                                                               |
| [<span data-ttu-id="8a902-135">**OnConnect**</span><span class="sxs-lookup"><span data-stu-id="8a902-135">**OnConnect**</span></span>](cbasepropertypage-onconnect.md)                       | <span data-ttu-id="8a902-136">Fornece um ponteiro **IUnknown** para o objeto associado à página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8a902-136">Provides an **IUnknown** pointer to the object associated with the property page.</span></span> <span data-ttu-id="8a902-137">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="8a902-137">Virtual.</span></span>                                        |
| [<span data-ttu-id="8a902-138">**OnActivate**</span><span class="sxs-lookup"><span data-stu-id="8a902-138">**OnDeactivate**</span></span>](cbasepropertypage-ondeactivate.md)                 | <span data-ttu-id="8a902-139">Chamado quando a janela da caixa de diálogo é destruída.</span><span class="sxs-lookup"><span data-stu-id="8a902-139">Called when the dialog box window is destroyed.</span></span> <span data-ttu-id="8a902-140">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="8a902-140">Virtual.</span></span>                                                                          |
| [<span data-ttu-id="8a902-141">**Desconectar**</span><span class="sxs-lookup"><span data-stu-id="8a902-141">**OnDisconnect**</span></span>](cbasepropertypage-ondisconnect.md)                 | <span data-ttu-id="8a902-142">Chamado quando a página de propriedades deve liberar o objeto associado.</span><span class="sxs-lookup"><span data-stu-id="8a902-142">Called when the property page should release the associated object.</span></span> <span data-ttu-id="8a902-143">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="8a902-143">Virtual.</span></span>                                                      |
| [<span data-ttu-id="8a902-144">**OnReceiveMessage**</span><span class="sxs-lookup"><span data-stu-id="8a902-144">**OnReceiveMessage**</span></span>](cbasepropertypage-onreceivemessage.md)         | <span data-ttu-id="8a902-145">Chamado quando a caixa de diálogo recebe uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="8a902-145">Called when the dialog box receives a message.</span></span> <span data-ttu-id="8a902-146">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="8a902-146">Virtual.</span></span>                                                                           |
| <span data-ttu-id="8a902-147">Métodos IPropertyPage</span><span class="sxs-lookup"><span data-stu-id="8a902-147">IPropertyPage Methods</span></span>                                                  | <span data-ttu-id="8a902-148">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a902-148">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="8a902-149">**Activate**</span><span class="sxs-lookup"><span data-stu-id="8a902-149">**Activate**</span></span>](cbasepropertypage-activate.md)                         | <span data-ttu-id="8a902-150">Cria a janela da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8a902-150">Creates the dialog box window.</span></span>                                                                                                    |
| [<span data-ttu-id="8a902-151">**Aplicar**</span><span class="sxs-lookup"><span data-stu-id="8a902-151">**Apply**</span></span>](cbasepropertypage-apply.md)                               | <span data-ttu-id="8a902-152">Aplica os valores da página de propriedades atual ao objeto associado à página de propriedades</span><span class="sxs-lookup"><span data-stu-id="8a902-152">Applies the current property page values to the object associated with the property page</span></span>                                          |
| [<span data-ttu-id="8a902-153">**Desativar**</span><span class="sxs-lookup"><span data-stu-id="8a902-153">**Deactivate**</span></span>](cbasepropertypage-deactivate.md)                     | <span data-ttu-id="8a902-154">Destrói a janela da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8a902-154">Destroys the dialog window.</span></span>                                                                                                       |
| [<span data-ttu-id="8a902-155">**GetPageInfo**</span><span class="sxs-lookup"><span data-stu-id="8a902-155">**GetPageInfo**</span></span>](cbasepropertypage-getpageinfo.md)                   | <span data-ttu-id="8a902-156">Recupera informações sobre a página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8a902-156">Retrieves information about the property page.</span></span>                                                                                    |
| [<span data-ttu-id="8a902-157">**Ajuda**</span><span class="sxs-lookup"><span data-stu-id="8a902-157">**Help**</span></span>](cbasepropertypage-help.md)                                 | <span data-ttu-id="8a902-158">Chama a ajuda da página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8a902-158">Invokes the property page help.</span></span>                                                                                                   |
| [<span data-ttu-id="8a902-159">**IsPageDirty**</span><span class="sxs-lookup"><span data-stu-id="8a902-159">**IsPageDirty**</span></span>](cbasepropertypage-ispagedirty.md)                   | <span data-ttu-id="8a902-160">Indica se a página de propriedades foi alterada desde que foi ativada ou desde a chamada mais recente para **IPropertyPage:: apply**.</span><span class="sxs-lookup"><span data-stu-id="8a902-160">Indicates whether the property page has changed since it was activated or since the most recent call to **IPropertyPage::Apply**.</span></span> |
| [<span data-ttu-id="8a902-161">**Mover**</span><span class="sxs-lookup"><span data-stu-id="8a902-161">**Move**</span></span>](cbasepropertypage-move.md)                                 | <span data-ttu-id="8a902-162">Posiciona e redimensiona a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8a902-162">Positions and resizes the dialog box.</span></span>                                                                                             |
| [<span data-ttu-id="8a902-163">**Objetos**</span><span class="sxs-lookup"><span data-stu-id="8a902-163">**SetObjects**</span></span>](cbasepropertypage-setobjects.md)                     | <span data-ttu-id="8a902-164">Fornece ponteiros **IUnknown** para os objetos associados à página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8a902-164">Provides **IUnknown** pointers for the objects associated with the property page.</span></span>                                                 |
| [<span data-ttu-id="8a902-165">**SetPageSite**</span><span class="sxs-lookup"><span data-stu-id="8a902-165">**SetPageSite**</span></span>](cbasepropertypage-setpagesite.md)                   | <span data-ttu-id="8a902-166">Inicializa a página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8a902-166">Initializes the property page.</span></span>                                                                                                    |
| [<span data-ttu-id="8a902-167">**programa**</span><span class="sxs-lookup"><span data-stu-id="8a902-167">**Show**</span></span>](cbasepropertypage-show.md)                                 | <span data-ttu-id="8a902-168">Mostra ou oculta a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8a902-168">Shows or hides the dialog box.</span></span>                                                                                                    |
| [<span data-ttu-id="8a902-169">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="8a902-169">**TranslateAccelerator**</span></span>](cbasepropertypage-translateaccelerator.md) | <span data-ttu-id="8a902-170">Instrui a página de propriedades para processar um pressionamento de tecla.</span><span class="sxs-lookup"><span data-stu-id="8a902-170">Instructs the property page to process a keystroke.</span></span>                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="8a902-171">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a902-171">Remarks</span></span>

<span data-ttu-id="8a902-172">Uma página de propriedades é um objeto COM, portanto, você deve gerar um GUID para o identificador de classe (CLSID) e fornecer uma entrada na matriz [**CFactoryTemplate**](cfactorytemplate.md) .</span><span class="sxs-lookup"><span data-stu-id="8a902-172">A property page is a COM object, so you must generate a GUID for the class identifier (CLSID) and provide an entry in the [**CFactoryTemplate**](cfactorytemplate.md) array.</span></span> <span data-ttu-id="8a902-173">Para obter mais informações, consulte [DirectShow e com](directshow-and-com.md).</span><span class="sxs-lookup"><span data-stu-id="8a902-173">For more information, see [DirectShow and COM](directshow-and-com.md).</span></span> <span data-ttu-id="8a902-174">O exemplo a seguir mostra uma entrada de fábrica de classe típica:</span><span class="sxs-lookup"><span data-stu-id="8a902-174">The following example shows a typical class factory entry:</span></span>


```
CFactoryTemplate g_Templates[] =
{   
    { 
        L"My Property Page",
        &CLSID_MyPropPage,
        CMyProp::CreateInstance,
        NULL,
        NULL
    },
    /* Also include the template for your filter (not shown). */
};

```



<span data-ttu-id="8a902-175">O filtro deve expor a interface **ISpecifyPropertyPages** .</span><span class="sxs-lookup"><span data-stu-id="8a902-175">Your filter must expose the **ISpecifyPropertyPages** interface.</span></span> <span data-ttu-id="8a902-176">Essa interface contém um único método, **GetPages**, que retorna o CLSID da página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8a902-176">This interface contains a single method, **GetPages**, which returns the CLSID of the property page.</span></span> <span data-ttu-id="8a902-177">O exemplo a seguir mostra como implementar esse método:</span><span class="sxs-lookup"><span data-stu-id="8a902-177">The following example shows how to implement this method:</span></span>


```
STDMETHODIMP CMyFilter::GetPages(CAUUID *pPages)
{
    if (!pPages) return E_POINTER;

    pPages->cElems = 1;
    pPages->pElems = reinterpret_cast<GUID*>(CoTaskMemAlloc(sizeof(GUID)));
    if (pPages->pElems == NULL) 
    {
        return E_OUTOFMEMORY;
    }
    *(pPages->pElems) = CLSID_MyPropPage;
    return S_OK;
} 
```



<span data-ttu-id="8a902-178">Lembre-se de substituir o método **NonDelegatingQueryInterface** do filtro também.</span><span class="sxs-lookup"><span data-stu-id="8a902-178">Remember to override the filter's **NonDelegatingQueryInterface** method as well.</span></span> <span data-ttu-id="8a902-179">Para obter mais informações, consulte [DirectShow e com](directshow-and-com.md) e [**INonDelegatingUnknown**](inondelegatingunknown.md).</span><span class="sxs-lookup"><span data-stu-id="8a902-179">For more information, see [DirectShow and COM](directshow-and-com.md) and [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span>

<span data-ttu-id="8a902-180">Em seguida, crie a caixa de diálogo como um recurso em seu projeto e crie um recurso de cadeia de caracteres que contém o título da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8a902-180">Next, create the dialog as a resource in your project, and create a string resource that holds the dialog title.</span></span> <span data-ttu-id="8a902-181">Ambas as IDs de recurso são parâmetros para o construtor **CBasePropertyPage** .</span><span class="sxs-lookup"><span data-stu-id="8a902-181">Both of these resource IDs are parameters to the **CBasePropertyPage** constructor.</span></span> <span data-ttu-id="8a902-182">Manter a cadeia de título em um recurso torna mais fácil localizar sua página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8a902-182">Keeping the title string in a resource makes it easier to localize your property page.</span></span>

<span data-ttu-id="8a902-183">A classe **CBasePropertyPage** fornece uma estrutura para a interface **IPropertyPage** .</span><span class="sxs-lookup"><span data-stu-id="8a902-183">The **CBasePropertyPage** class provides a framework for the **IPropertyPage** interface.</span></span> <span data-ttu-id="8a902-184">Essa estrutura chama um número de métodos virtuais, incluindo [**CBasePropertyPage:: OnActivate**](cbasepropertypage-onactivate.md), [**CBasePropertyPage:: OnApplyChanges**](cbasepropertypage-onapplychanges.md)e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="8a902-184">This framework calls a number of virtual methods, including [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md), [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md), and so on.</span></span> <span data-ttu-id="8a902-185">Na classe base, esses métodos simplesmente retornam S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8a902-185">In the base class, these methods simply return S\_OK.</span></span> <span data-ttu-id="8a902-186">Sua classe derivada precisará substituir alguns ou todos esses métodos virtuais.</span><span class="sxs-lookup"><span data-stu-id="8a902-186">Your derived class will need to override some or all of these virtual methods.</span></span> <span data-ttu-id="8a902-187">Para obter detalhes, consulte os comentários para os métodos individuais.</span><span class="sxs-lookup"><span data-stu-id="8a902-187">For details, see the remarks for the individual methods.</span></span>

<span data-ttu-id="8a902-188">Para obter um exemplo estendido de como usar essa classe para criar uma página de propriedades, consulte [criando uma página de propriedades de filtro](creating-a-filter-property-page.md).</span><span class="sxs-lookup"><span data-stu-id="8a902-188">For an extended example of how to use this class to create a property page, see [Creating a Filter Property Page](creating-a-filter-property-page.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8a902-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a902-189">Requirements</span></span>



| <span data-ttu-id="8a902-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a902-190">Requirement</span></span> | <span data-ttu-id="8a902-191">Valor</span><span class="sxs-lookup"><span data-stu-id="8a902-191">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a902-192">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8a902-192">Header</span></span><br/>  | <dl> <span data-ttu-id="8a902-193"><dt>CProp. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8a902-193"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="8a902-194">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8a902-194">Library</span></span><br/> | <dl> <span data-ttu-id="8a902-195"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="8a902-195"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




