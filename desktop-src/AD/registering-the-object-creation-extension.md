---
title: Registrando a extensão de criação de objeto
description: Quando uma DLL de extensão de criação de objeto no Active Directory Domain Services é criada, ela deve ser registrada com o registro do Windows e Active Directory Domain Services para fazer COM e os snap-ins administrativos do MMC Active Directory cientes da extensão.
ms.assetid: 6e950c6c-1a4f-4de0-9be1-004c31d4734c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27d8e2a50c2340d678fd43e546d68525afbc8a7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103917108"
---
# <a name="registering-the-object-creation-extension"></a><span data-ttu-id="de1be-103">Registrando a extensão de criação de objeto</span><span class="sxs-lookup"><span data-stu-id="de1be-103">Registering the Object Creation Extension</span></span>

<span data-ttu-id="de1be-104">Quando uma DLL de extensão de criação de objeto no Active Directory Domain Services é criada, ela deve ser registrada com o registro do Windows e Active Directory Domain Services para fazer COM e os snap-ins administrativos do MMC Active Directory cientes da extensão.</span><span class="sxs-lookup"><span data-stu-id="de1be-104">When an object creation extension DLL in Active Directory Domain Services is created, it must be registered with the Windows registry and Active Directory Domain Services to make COM and the Active Directory administrative MMC snap-ins aware of the extension.</span></span>

## <a name="registering-in-the-windows-registry"></a><span data-ttu-id="de1be-105">Registrando no registro do Windows</span><span class="sxs-lookup"><span data-stu-id="de1be-105">Registering in the Windows Registry</span></span>

<span data-ttu-id="de1be-106">Como todos os servidores COM, uma extensão de criação de objeto deve ser registrada no registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="de1be-106">Like all COM servers, an object creation extension must be registered in the Windows registry.</span></span> <span data-ttu-id="de1be-107">A extensão é registrada sob a seguinte chave:</span><span class="sxs-lookup"><span data-stu-id="de1be-107">The extension is registered under the following key:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      <extension CLSID>
         InProcServer32
            (Default) = <extension path>
            ThreadingModel = Apartment
```

<span data-ttu-id="de1be-108">" &lt; CLSID &gt; de extensão" é a representação de cadeia de caracteres do CLSID, conforme produzido pela função [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .</span><span class="sxs-lookup"><span data-stu-id="de1be-108">"&lt;extension CLSID&gt;" is the string representation of the CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span> <span data-ttu-id="de1be-109">" &lt; caminho &gt; de extensão" contém o caminho e o nome de arquivo da DLL de extensão.</span><span class="sxs-lookup"><span data-stu-id="de1be-109">"&lt;extension path&gt;" contains the path and file name of the extension DLL.</span></span> <span data-ttu-id="de1be-110">O valor de **ThreadingModel** para todas as extensões de criação de objeto deve ser "Apartment".</span><span class="sxs-lookup"><span data-stu-id="de1be-110">The **ThreadingModel** value for all object creation extensions must be "Apartment".</span></span>

## <a name="registering-with-active-directory-domain-services"></a><span data-ttu-id="de1be-111">Registrando com Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="de1be-111">Registering with Active Directory Domain Services</span></span>

<span data-ttu-id="de1be-112">O registro da extensão de criação de objeto é específico de uma localidade.</span><span class="sxs-lookup"><span data-stu-id="de1be-112">Object creation extension registration is specific to one locale.</span></span> <span data-ttu-id="de1be-113">Se a extensão de criação de objeto se aplicar a todas as localidades, ela deverá ser registrada no objeto **displaySpecifier** da classe de objeto em todos os subcontêineres de localidade no recipiente DisplaySpecifiers.</span><span class="sxs-lookup"><span data-stu-id="de1be-113">If the object creation extension applies to all locales, it must be registered in the object class's **displaySpecifier** object in all of the locale subcontainers in the DisplaySpecifiers container.</span></span> <span data-ttu-id="de1be-114">Se a extensão de criação de objeto for localizada para uma determinada localidade, registre-a no objeto **displaySpecifier** no subcontêiner dessa localidade.</span><span class="sxs-lookup"><span data-stu-id="de1be-114">If the object creation extension is localized for a certain locale, register it in the **displaySpecifier** object in that locale's subcontainer.</span></span> <span data-ttu-id="de1be-115">Para obter mais informações sobre o contêiner DisplaySpecifiers e as localidades, consulte [Exibir especificadores](display-specifiers.md) e [contêiner DisplaySpecifiers](displayspecifiers-container.md).</span><span class="sxs-lookup"><span data-stu-id="de1be-115">For more information about the DisplaySpecifiers container and locales, see [Display Specifiers](display-specifiers.md) and [DisplaySpecifiers Container](displayspecifiers-container.md).</span></span>

<span data-ttu-id="de1be-116">Há dois atributos DisplaySpecifier em que uma extensão de criação de objeto pode ser registrada.</span><span class="sxs-lookup"><span data-stu-id="de1be-116">There are two DisplaySpecifier attributes that an object creation extension can be registered under.</span></span> <span data-ttu-id="de1be-117">Esses são **creationWizard** e **createWizardExt**.</span><span class="sxs-lookup"><span data-stu-id="de1be-117">These are **creationWizard** and **createWizardExt**.</span></span>

<span data-ttu-id="de1be-118">O atributo **creationWizard** identifica as extensões de criação de objeto primário para substituir o assistente de criação de objeto nativo ou existente em Active Directory snap-ins administrativos. Uma extensão de criação primária fornece o primeiro conjunto de páginas e é hospedada da mesma maneira que as páginas nativas.</span><span class="sxs-lookup"><span data-stu-id="de1be-118">The **creationWizard** attribute identifies primary object creation extensions to replace the existing or native object creation wizard in Active Directory administrative snap-ins. A primary creation extension provides the first set of pages and is hosted in the same way as native pages.</span></span> <span data-ttu-id="de1be-119">Este atributo é de valor único e requer o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="de1be-119">This attribute is single-valued and requires the following format:</span></span>


```C++
<CLSID>
```



<span data-ttu-id="de1be-120">O " &lt; CLSID &gt; " é a representação de cadeia de caracteres do CLSID do objeto com, conforme produzido pela função [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .</span><span class="sxs-lookup"><span data-stu-id="de1be-120">The "&lt;CLSID&gt;" is the string representation of the COM object's CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span>

<span data-ttu-id="de1be-121">O atributo **createWizardExt** identifica extensões de criação de objeto secundário.</span><span class="sxs-lookup"><span data-stu-id="de1be-121">The **createWizardExt** attribute identifies secondary object creation extensions.</span></span> <span data-ttu-id="de1be-122">Uma extensão de criação secundária adiciona páginas de assistente às páginas nativas ou à extensão primária.</span><span class="sxs-lookup"><span data-stu-id="de1be-122">A secondary creation extension adds wizard pages to the native pages or primary extension.</span></span> <span data-ttu-id="de1be-123">Esse atributo tem valores múltiplos e requer o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="de1be-123">This attribute is multi-valued and requires the following format:</span></span>


```C++
<order number>,<CLSID>
```



<span data-ttu-id="de1be-124">O " &lt; número do pedido &gt; " é um número sem sinal que representa a posição da página no assistente.</span><span class="sxs-lookup"><span data-stu-id="de1be-124">The "&lt;order number&gt;" is an unsigned number that represents the page's position in the wizard.</span></span> <span data-ttu-id="de1be-125">Quando um assistente de criação é exibido, os valores são classificados usando uma comparação do "número de &lt; ordem" de cada valor &gt; .</span><span class="sxs-lookup"><span data-stu-id="de1be-125">When a creation wizard is displayed, the values are sorted using a comparison of each value's "&lt;order number&gt;".</span></span> <span data-ttu-id="de1be-126">Se mais de um valor tiver o mesmo " &lt; número do pedido &gt; ", essas páginas serão carregadas na ordem em que são lidas do servidor de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="de1be-126">If more than one value has the same "&lt;order number&gt;", those pages are loaded in the order they are read from the Active Directory server.</span></span> <span data-ttu-id="de1be-127">Se possível, você deve usar um " &lt; número de pedido" não existente &gt; (ou seja, um que não tenha sido usado por outros valores na propriedade).</span><span class="sxs-lookup"><span data-stu-id="de1be-127">If possible, you should use a non-existing "&lt;order number&gt;" (that is, one that has not been used by other values in the property).</span></span> <span data-ttu-id="de1be-128">Não há uma posição de início prescrita e as lacunas são permitidas na &lt; sequência "número do pedido &gt; ".</span><span class="sxs-lookup"><span data-stu-id="de1be-128">There is no prescribed starting position, and gaps are allowed in the "&lt;order number&gt;" sequence.</span></span>

<span data-ttu-id="de1be-129">O " &lt; CLSID &gt; " é a representação de cadeia de caracteres do CLSID do objeto com, conforme produzido pela função [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .</span><span class="sxs-lookup"><span data-stu-id="de1be-129">The "&lt;CLSID&gt;" is the string representation of the COM object's CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span>

 

 