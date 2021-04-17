---
title: Associação tardia versus acesso de vtable no modelo de extensão ADSI
description: Uma interface dupla habilita o acesso Direct vtable a todas as suas funções, enquanto uma interface de expedição não.
ms.assetid: 6ecc0821-7cf0-4075-81c0-8bebaedab2a4
ms.tgt_platform: multiple
keywords:
- vinculação tardia versus acesso vtable no ADSI do modelo de extensão ADSI
- ADSI de extensões, associação tardia versus acesso vtable no modelo de extensão ADSI
- ADSI ADSI, código de exemplo Visual Basic, usando IADsDualInf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f95431fcde9a194f28cd103d93faa3f182c1968
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105762843"
---
# <a name="late-binding-vs-vtable-access-in-the-adsi-extension-model"></a><span data-ttu-id="d06c0-106">Associação tardia versus acesso de vtable no modelo de extensão ADSI</span><span class="sxs-lookup"><span data-stu-id="d06c0-106">Late Binding vs. Vtable Access in the ADSI Extension Model</span></span>

<span data-ttu-id="d06c0-107">Uma interface dupla habilita o acesso Direct vtable a todas as suas funções, enquanto uma interface de expedição não.</span><span class="sxs-lookup"><span data-stu-id="d06c0-107">A dual interface enables direct vtable access to all its functions while a dispatch interface does not.</span></span> <span data-ttu-id="d06c0-108">Um cliente C/C++ pode consultar um ponteiro de interface dupla e usar o acesso Direct vtable para invocar suas funções.</span><span class="sxs-lookup"><span data-stu-id="d06c0-108">A C/C++ client can query for a dual interface pointer and use direct vtable access to invoke its functions.</span></span> <span data-ttu-id="d06c0-109">Isso fornece acesso mais rápido do que chamar a função usando as funções [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) e [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) .</span><span class="sxs-lookup"><span data-stu-id="d06c0-109">This provides faster access than invoking the function using the [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) and [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) functions.</span></span> <span data-ttu-id="d06c0-110">Isso é especialmente verdadeiro no modelo de extensão, porque todas as interfaces duplas em um objeto de extensão devem delegar suas **GetIDsOfNames** e **invocar** funções de volta para o agregador (ADSI) primeiro.</span><span class="sxs-lookup"><span data-stu-id="d06c0-110">This is especially true in the extension model, because all dual interfaces in an extension object must delegate their **GetIDsOfNames** and **Invoke** functions back to the aggregator (ADSI) first.</span></span> <span data-ttu-id="d06c0-111">Em seguida, o agregador deve executar etapas internas adicionais para identificar qual objeto de extensão, possivelmente incluindo o agregador em si, fornece suporte para a função chamada e redirecionar a chamada para o objeto apropriado.</span><span class="sxs-lookup"><span data-stu-id="d06c0-111">The aggregator then must perform extra internal steps to identify which extension object, possibly including the aggregator itself, provides support for the function called and redirect the call to the appropriate object.</span></span>

<span data-ttu-id="d06c0-112">Visual Basic também invoca uma função de interface dupla usando o acesso direto a uma vtable, se ela tiver um ponteiro para a interface e o acesso ao tipo de dados da biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="d06c0-112">Visual Basic also invokes a dual-interface function using direct access to a vtable, if it has a pointer to the interface and access to type data from the type library.</span></span> <span data-ttu-id="d06c0-113">Os clientes ADSI escritos em Visual Basic podem especificar um ponteiro para uma interface dupla, por exemplo, [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), explicitamente e, portanto, habilitar o acesso vtable a funções na interface.</span><span class="sxs-lookup"><span data-stu-id="d06c0-113">ADSI clients written in Visual Basic can specify a pointer to a dual interface, for example, [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), explicitly, and thus enable vtable access to functions in the interface.</span></span>


```VB
Dim inf as IADs
 
Set inf = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com") ' An object that supports IADsDualInf.
inf.Get("name") 'IADs.Get() will be invoked through direct vtable access.
```



<span data-ttu-id="d06c0-114">Como uma interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) não dá suporte ao acesso vtable, este exemplo não se aplica.</span><span class="sxs-lookup"><span data-stu-id="d06c0-114">Because an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface does not support vtable access, this example does not apply.</span></span> <span data-ttu-id="d06c0-115">Ou seja, uma função de expedição é sempre invocada apenas pelas funções [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) e [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) .</span><span class="sxs-lookup"><span data-stu-id="d06c0-115">That is, a dispatch function is always invoked through the [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) and [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) functions only.</span></span>

<span data-ttu-id="d06c0-116">As versões atuais do VBScript e do JScript também não dão suporte ao acesso vtable.</span><span class="sxs-lookup"><span data-stu-id="d06c0-116">Current releases of VBScript and JScript also do not support vtable access.</span></span> <span data-ttu-id="d06c0-117">Portanto, uma interface dupla em um ambiente VBScript ou JScript é executada como uma interface de expedição.</span><span class="sxs-lookup"><span data-stu-id="d06c0-117">Therefore, a dual interface in a VBScript or JScript environment performs like a dispatch interface.</span></span>

 

 