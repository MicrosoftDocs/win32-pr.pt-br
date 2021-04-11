---
title: Exibindo contêineres como nós folha
description: Qualquer objeto no Active Directory Domain Services pode ser um contêiner de outros objetos.
ms.assetid: 38300ca5-745a-4640-9723-6052a9843f45
ms.tgt_platform: multiple
keywords:
- Exibindo contêineres como nós folha
- contêineres AD, exibindo como nós folha
- ANÚNCIO folha, exibindo contêineres como nós folha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1631526ed78132829a7576960a997b13cc232b5f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104293881"
---
# <a name="viewing-containers-as-leaf-nodes"></a><span data-ttu-id="10dd4-106">Exibindo contêineres como nós folha</span><span class="sxs-lookup"><span data-stu-id="10dd4-106">Viewing Containers as Leaf Nodes</span></span>

<span data-ttu-id="10dd4-107">Qualquer objeto no Active Directory Domain Services pode ser um contêiner de outros objetos.</span><span class="sxs-lookup"><span data-stu-id="10dd4-107">Any object in Active Directory Domain Services can be a container of other objects.</span></span> <span data-ttu-id="10dd4-108">Isso pode obstruir a interface do usuário, portanto, é possível declarar que um objeto de uma classe específica só seja exibido como uma folha na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="10dd4-108">This can clutter the user interface, so it is possible to declare that an object of a specific class be only be displayed as a leaf in the user interface.</span></span> <span data-ttu-id="10dd4-109">O atributo **treatAsLeaf** é um atributo de especificador de exibição com valor único que determina se os objetos dessa classe devem ser exibidos apenas como objetos folha.</span><span class="sxs-lookup"><span data-stu-id="10dd4-109">The **treatAsLeaf** attribute is a single-valued display specifier attribute that determines if objects of that class should be only be displayed as leaf objects.</span></span> <span data-ttu-id="10dd4-110">Esse atributo é um valor booliano que, se **verdadeiro**, indica que os objetos da classe só devem ser exibidos como elementos folha.</span><span class="sxs-lookup"><span data-stu-id="10dd4-110">This attribute is a Boolean value that, if **TRUE**, indicates that objects of the class should only be displayed as leaf elements.</span></span> <span data-ttu-id="10dd4-111">Se **for false**, indicará que os objetos da classe podem ser exibidos como um contêiner ou uma folha.</span><span class="sxs-lookup"><span data-stu-id="10dd4-111">If **FALSE**, indicates that objects of the class can be displayed as a container or a leaf.</span></span> <span data-ttu-id="10dd4-112">Como todos os atributos de especificador de exibição, o atributo **treatAsLeaf** é definido em uma base por localidade, portanto, esse atributo pode ser localizado conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="10dd4-112">Like all display specifier attributes, the **treatAsLeaf** attribute is set on a per-locale basis, so this attribute can be localized as required.</span></span> <span data-ttu-id="10dd4-113">Por exemplo, a **exibição de usuário** para o especificador de exibição do idioma inglês (0409) tem o atributo **TreatAsLeaf** definido como **true** por padrão.</span><span class="sxs-lookup"><span data-stu-id="10dd4-113">For example, the **User-Display** for the English locale (0409) display specifier has the **treatAsLeaf** attribute set to **TRUE** by default.</span></span> <span data-ttu-id="10dd4-114">Isso faz com que a interface do usuário exiba todos os objetos de **usuário** como objetos folha.</span><span class="sxs-lookup"><span data-stu-id="10dd4-114">This causes the user interface to display all **User** objects as leaf objects.</span></span>

<span data-ttu-id="10dd4-115">\*\*Para definir o valor do atributo \*\*treatAsLeaf\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="10dd4-115">**To set the value of the **treatAsLeaf** attribute**</span></span>

1.  <span data-ttu-id="10dd4-116">Associe-se ao atributo de exibição desejado na localidade desejada.</span><span class="sxs-lookup"><span data-stu-id="10dd4-116">Bind to the desired display attribute in the desired locale.</span></span> <span data-ttu-id="10dd4-117">Para obter mais informações e um exemplo de código, consulte [contêiner DisplaySpecifiers](displayspecifiers-container.md).</span><span class="sxs-lookup"><span data-stu-id="10dd4-117">For more information and a code example, see [DisplaySpecifiers Container](displayspecifiers-container.md).</span></span>
2.  <span data-ttu-id="10dd4-118">Use o método [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) para definir o atributo **treatAsLeaf** como **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="10dd4-118">Use the [**IADs::Put**](/windows/desktop/api/iads/nf-iads-iads-put) method to set the **treatAsLeaf** attribute to either **TRUE** or **FALSE**.</span></span>
3.  <span data-ttu-id="10dd4-119">Para confirmar as alterações no diretório, chame o método [**IADs:: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="10dd4-119">To commit changes to the directory, call the [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) method.</span></span>

 

 