---
description: Implemente uma página de propriedades como parte da criação de uma página de propriedades de filtro para um filtro DirectShow personalizado.
ms.assetid: ed71f26b-0812-4be8-96a4-b9f5dde45540
title: Etapa 4. Criar a página de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d32cd9eacc98af5f273897a3837390ab5cc75f7a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406849"
---
# <a name="step-4-create-the-property-page"></a><span data-ttu-id="8685b-104">Etapa 4.</span><span class="sxs-lookup"><span data-stu-id="8685b-104">Step 4.</span></span> <span data-ttu-id="8685b-105">Criar a página de propriedades</span><span class="sxs-lookup"><span data-stu-id="8685b-105">Create the Property Page</span></span>

<span data-ttu-id="8685b-106">Neste ponto, o filtro dá suporte a tudo o que ele precisa para uma página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8685b-106">At this point the filter supports everything that it needs for a property page.</span></span> <span data-ttu-id="8685b-107">A próxima etapa é implementar a própria página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8685b-107">The next step is implementing the property page itself.</span></span> <span data-ttu-id="8685b-108">Comece derivando uma nova classe de **CBasePropertyPage.**</span><span class="sxs-lookup"><span data-stu-id="8685b-108">Start by deriving a new class from **CBasePropertyPage**.</span></span> <span data-ttu-id="8685b-109">O exemplo a seguir mostra parte da declaração, incluindo algumas variáveis de membro particular que serão usadas posteriormente no exemplo:</span><span class="sxs-lookup"><span data-stu-id="8685b-109">The following example shows part of the declaration, including some private member variables that will be used later in the example:</span></span>


```C++
class CGrayProp : public CBasePropertyPage
{
private:
    ISaturation *m_pGray;    // Pointer to the filter's custom interface.
    long        m_lVal       // Store the old value, so we can revert.
    long        m_lNewVal;   // New value.
public:
    /* ... */
};
```



<span data-ttu-id="8685b-110">Em seguida, crie um recurso de caixa de diálogo no editor de recursos, juntamente com um recurso de cadeia de caracteres para o título da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8685b-110">Next, create a dialog resource in the resource editor, along with a string resource for the dialog title.</span></span> <span data-ttu-id="8685b-111">A cadeia de caracteres aparecerá na guia da página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8685b-111">The string will appear in the tab for the property page.</span></span> <span data-ttu-id="8685b-112">As duas IDs de recurso são argumentos para o construtor **CBasePropertyPage:**</span><span class="sxs-lookup"><span data-stu-id="8685b-112">The two resource IDs are arguments to the **CBasePropertyPage** constructor:</span></span>


```C++
CGrayProp::CGrayProp(IUnknown *pUnk) : 
  CBasePropertyPage(NAME("GrayProp"), pUnk, IDD_PROPPAGE, IDS_PROPPAGE_TITLE),
  m_pGray(0)
{ }
```



<span data-ttu-id="8685b-113">A ilustração a seguir mostra o recurso de caixa de diálogo para a página de propriedades de exemplo.</span><span class="sxs-lookup"><span data-stu-id="8685b-113">The following illustration shows the dialog resource for the example property page.</span></span>

![caixa de diálogo da página de propriedades](images/proppage.png)

<span data-ttu-id="8685b-115">Agora você está pronto para implementar a página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8685b-115">Now you are ready to implement the property page.</span></span> <span data-ttu-id="8685b-116">Aqui estão os métodos em **CBasePropertyPage** para substituir:</span><span class="sxs-lookup"><span data-stu-id="8685b-116">Here are the methods in **CBasePropertyPage** to override:</span></span>

-   <span data-ttu-id="8685b-117">**OnConnect** é chamado quando o cliente cria a página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8685b-117">**OnConnect** is called when the client creates the property page.</span></span> <span data-ttu-id="8685b-118">Ele define o **ponteiro IUnknown** para o filtro.</span><span class="sxs-lookup"><span data-stu-id="8685b-118">It sets the **IUnknown** pointer to the filter.</span></span>
-   <span data-ttu-id="8685b-119">**OnActivate** é chamado quando a caixa de diálogo é criada.</span><span class="sxs-lookup"><span data-stu-id="8685b-119">**OnActivate** is called when the dialog is created.</span></span>
-   <span data-ttu-id="8685b-120">**OnReceiveMessage** é chamado quando a caixa de diálogo recebe uma mensagem de janela.</span><span class="sxs-lookup"><span data-stu-id="8685b-120">**OnReceiveMessage** is called when the dialog receives a window message.</span></span>
-   <span data-ttu-id="8685b-121">**OnApplyChanges é** chamado quando o usuário confirma as alterações de propriedade clicando no **botão OK** **ou Aplicar.**</span><span class="sxs-lookup"><span data-stu-id="8685b-121">**OnApplyChanges** is called when the user commits the property changes by clicking the **OK** or **Apply** button.</span></span>
-   <span data-ttu-id="8685b-122">**OnDisconnect** é chamado quando o usuário descarta a folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8685b-122">**OnDisconnect** is called when the user dismisses the property sheet.</span></span>

<span data-ttu-id="8685b-123">O restante deste tutorial descreve cada um desses métodos.</span><span class="sxs-lookup"><span data-stu-id="8685b-123">The remainder of this tutorial describes each of these methods.</span></span>

<span data-ttu-id="8685b-124">Próximo: [Etapa 5. Armazene um Ponteiro para o Filtro](step-5--store-a-pointer-to-the-filter.md).</span><span class="sxs-lookup"><span data-stu-id="8685b-124">Next: [Step 5. Store a Pointer to the Filter](step-5--store-a-pointer-to-the-filter.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8685b-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8685b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8685b-126">Criando uma página de propriedades de filtro</span><span class="sxs-lookup"><span data-stu-id="8685b-126">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



