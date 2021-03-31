---
title: Páginas de propriedades para uso com especificadores de exibição
description: Active Directory Domain Services fornecer um mecanismo para adicionar páginas à folha de propriedades exibida para um objeto de diretório a partir dos snap-ins administrativos Active Directory ou do shell do Windows.
ms.assetid: c1dd84e2-50f9-4903-a4b5-4473515e4d0e
ms.tgt_platform: multiple
keywords:
- exibir o anúncio de especificadores, páginas de propriedades para uso com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c204f4d378e66cda5bc02684cb51cc707ba3d6f2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103823641"
---
# <a name="property-pages-for-use-with-display-specifiers"></a><span data-ttu-id="8848f-104">Páginas de propriedades para uso com especificadores de exibição</span><span class="sxs-lookup"><span data-stu-id="8848f-104">Property Pages for Use with Display Specifiers</span></span>

<span data-ttu-id="8848f-105">Active Directory Domain Services fornecer um mecanismo para adicionar páginas à folha de propriedades exibida para um objeto de diretório a partir dos snap-ins administrativos Active Directory ou do shell do Windows.</span><span class="sxs-lookup"><span data-stu-id="8848f-105">Active Directory Domain Services provide a mechanism for adding pages to the property sheet displayed for a directory object from the Active Directory administrative snap-ins or the Windows shell.</span></span> <span data-ttu-id="8848f-106">Para adicionar uma página à folha de propriedades, implemente uma extensão de folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8848f-106">To add a page to the property sheet, implement a property sheet extension.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="8848f-107">Público do desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="8848f-107">Developer Audience</span></span>

<span data-ttu-id="8848f-108">Esta documentação pressupõe que o leitor esteja familiarizado com a operação COM e o desenvolvimento de componentes usando o C++.</span><span class="sxs-lookup"><span data-stu-id="8848f-108">This documentation assumes that the reader is familiar with COM operation and component development using C++.</span></span> <span data-ttu-id="8848f-109">No momento, não é possível criar uma extensão de folha de propriedades Active Directory usando Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8848f-109">It is not currently possible to create an Active Directory property sheet extension using Visual Basic.</span></span>

## <a name="creating-an-active-directory-property-sheet-extension"></a><span data-ttu-id="8848f-110">Criando uma extensão de folha de propriedades Active Directory</span><span class="sxs-lookup"><span data-stu-id="8848f-110">Creating an Active Directory Property Sheet Extension</span></span>

<span data-ttu-id="8848f-111">Uma *extensão de folha de propriedades* é um servidor em processamento com que implementa determinadas interfaces e é registrado com Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="8848f-111">A *property sheet extension* is a COM in-proc server that implements certain interfaces and is registered with Active Directory Domain Services.</span></span> <span data-ttu-id="8848f-112">Para criar uma extensão de folha de propriedades, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="8848f-112">To create a property sheet extension, perform the following steps.</span></span>

<span data-ttu-id="8848f-113">**Para criar uma extensão de folha de propriedades Active Directory**</span><span class="sxs-lookup"><span data-stu-id="8848f-113">**To create an Active Directory property sheet extension**</span></span>

1.  <span data-ttu-id="8848f-114">Crie a DLL de extensão da folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8848f-114">Create the property sheet extension DLL.</span></span> <span data-ttu-id="8848f-115">Uma extensão de folha de propriedades é um servidor em processamento COM que, no mínimo, implementa as interfaces [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) e [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) .</span><span class="sxs-lookup"><span data-stu-id="8848f-115">A property sheet extension is a COM in-proc server that, at a minimum, implements the [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) and [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) interfaces.</span></span> <span data-ttu-id="8848f-116">Para obter mais informações, consulte [implementando o objeto com da página de propriedades](implementing-the-property-page-com-object.md).</span><span class="sxs-lookup"><span data-stu-id="8848f-116">For more information, see [Implementing the Property Page COM Object](implementing-the-property-page-com-object.md).</span></span>
2.  <span data-ttu-id="8848f-117">Instale a extensão da folha de propriedades nos computadores em que a extensão da folha de propriedades deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="8848f-117">Install the property sheet extension on the computers where the property sheet extension is to be used.</span></span> <span data-ttu-id="8848f-118">Para fazer isso, crie um pacote de Microsoft Windows Installer para a DLL de extensão da folha de propriedades e implante o pacote adequadamente usando a política de grupo.</span><span class="sxs-lookup"><span data-stu-id="8848f-118">To do this, create a Microsoft Windows Installer package for the property sheet extension DLL and deploy the package appropriately using the group policy.</span></span> <span data-ttu-id="8848f-119">Para obter mais informações, consulte [distribuindo componentes da interface do usuário](distributing-user-interface-components.md).</span><span class="sxs-lookup"><span data-stu-id="8848f-119">For more information, see [Distributing User Interface Components](distributing-user-interface-components.md).</span></span>
3.  <span data-ttu-id="8848f-120">Registre a extensão da folha de propriedades no registro do Windows e com Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="8848f-120">Register the property sheet extension in the Windows registry and with Active Directory Domain Services.</span></span> <span data-ttu-id="8848f-121">Para obter mais informações, consulte [registrando o objeto com da página de propriedades em um especificador de exibição](registering-the-property-page-com-object-in-a-display-specifier.md).</span><span class="sxs-lookup"><span data-stu-id="8848f-121">For more information, see [Registering the Property Page COM Object in a Display Specifier](registering-the-property-page-com-object-in-a-display-specifier.md).</span></span>

 

 