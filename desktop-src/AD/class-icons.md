---
title: Ícones de classe
description: O ícone usado para representar um objeto de classe pode ser especificado no atributo iconPath no contêiner DisplaySpecifiers.
ms.assetid: 0ff8da8a-d3d3-4a15-8103-4fe6ec307427
ms.tgt_platform: multiple
keywords:
- nomes de exibição de classe anúncios, ícones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691d4ef22babeded12ec9b951f92247df99521b6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103917146"
---
# <a name="class-icons"></a><span data-ttu-id="9dfe9-104">Ícones de classe</span><span class="sxs-lookup"><span data-stu-id="9dfe9-104">Class Icons</span></span>

<span data-ttu-id="9dfe9-105">O ícone usado para representar um objeto de classe pode ser especificado no atributo **iconPath** no contêiner DisplaySpecifiers.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-105">The icon used to represent a class object can be specified in the **iconPath** attribute in the DisplaySpecifiers container.</span></span> <span data-ttu-id="9dfe9-106">Além disso, cada classe pode armazenar vários Estados de ícone.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-106">Moreover, each class can store multiple icon states.</span></span> <span data-ttu-id="9dfe9-107">Por exemplo, uma classe de pasta pode ter ícones para os Estados aberto, fechado e desabilitado.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-107">For example, a folder class can have icons for the open, closed, and disabled states.</span></span> <span data-ttu-id="9dfe9-108">A implementação atual aceita um máximo de dezesseis Estados de ícone diferentes por classe.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-108">The current implementation accepts a maximum of sixteen different icon states per class.</span></span>

<span data-ttu-id="9dfe9-109">O atributo **iconPath** pode ser especificado de uma das duas maneiras.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-109">The **iconPath** attribute can be specified in one of two ways.</span></span>


```C++
<state>,<icon file name>
```



<span data-ttu-id="9dfe9-110">ou</span><span class="sxs-lookup"><span data-stu-id="9dfe9-110">or</span></span>


```C++
<state>,<module file name>,<resource ID>
```



<span data-ttu-id="9dfe9-111">Nesses exemplos, o " &lt; estado &gt; " é um inteiro com um valor entre 0 e 15.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-111">In these examples, the "&lt;state&gt;" is an integer with a value between 0 and 15.</span></span> <span data-ttu-id="9dfe9-112">O valor 0 é definido como o estado padrão ou fechado do ícone.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-112">The value 0 is defined to be the default or closed state of the icon.</span></span> <span data-ttu-id="9dfe9-113">O valor 1 é definido para ser o estado aberto do ícone.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-113">The value 1 is defined to be the open state of the icon.</span></span> <span data-ttu-id="9dfe9-114">O valor 2 é o estado desabilitado.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-114">The value 2 is the disabled state.</span></span> <span data-ttu-id="9dfe9-115">Todos os outros valores são definidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-115">All other values are application-defined.</span></span>

<span data-ttu-id="9dfe9-116">O " &lt; nome do arquivo &gt; de ícone" é o caminho e o nome de arquivo de um arquivo de ícone que contém a imagem do ícone.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-116">The "&lt;icon file name&gt;" is the path and file name of an icon file that contains the icon image.</span></span>

<span data-ttu-id="9dfe9-117">O " &lt; nome do arquivo &gt; de módulo" é o caminho e o nome de arquivo de um módulo, como um exe ou dll, que contém a imagem de ícone em um recurso.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-117">The "&lt;module file name&gt;" is the path and file name of a module, such as an EXE or DLL, that contains the icon image in a resource.</span></span> <span data-ttu-id="9dfe9-118">O " &lt; ID do recurso &gt; " é um inteiro que especifica o identificador de recurso do recurso de ícone dentro do módulo.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-118">The "&lt;resource ID&gt;" is an integer that specifies the resource identifier of the icon resource within the module.</span></span>

## <a name="adding-a-value-to-the-iconpath-attribute"></a><span data-ttu-id="9dfe9-119">Adicionando um valor ao atributo **iconPath**</span><span class="sxs-lookup"><span data-stu-id="9dfe9-119">Adding a Value to the **iconPath** Attribute</span></span>

<span data-ttu-id="9dfe9-120">Para adicionar um valor ao atributo **iconPath** , execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-120">To add a value to the **iconPath** attribute, perform the following steps.</span></span>

1.  <span data-ttu-id="9dfe9-121">Determine se o valor do atributo existe.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-121">Determine if the value for the attribute exists.</span></span> <span data-ttu-id="9dfe9-122">Se um valor for para ser substituído, primeiro exclua o valor existente usando o método [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) com o parâmetro *lnControlCode* definido como **\_ Propriedade ADS \_ delete** e o parâmetro *vProp* definido como o valor a ser removido.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-122">If a value is to be replaced, first, delete the existing value using the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method with the *lnControlCode* parameter set to **ADS\_PROPERTY\_DELETE** and the *vProp* parameter set to the value to be removed.</span></span> <span data-ttu-id="9dfe9-123">Não use a **\_ Propriedade ADS \_ Clear** ou **a \_ \_ atualização da propriedade ADS** para *lnControlCode*.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-123">Do not use **ADS\_PROPERTY\_CLEAR** or **ADS\_PROPERTY\_UPDATE** for *lnControlCode*.</span></span>
2.  <span data-ttu-id="9dfe9-124">Crie a cadeia de caracteres que representa os dados de ícone de atributo.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-124">Create the string that represents the attribute icon data.</span></span> <span data-ttu-id="9dfe9-125">Para obter um exemplo, consulte o formato acima.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-125">For an example, see the format above.</span></span>
3.  <span data-ttu-id="9dfe9-126">Para adicionar o novo valor, use o método [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) com o parâmetro *lnControlCode* definido como **propriedade \_ de \_ acréscimo do ADS**.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-126">To add the new value, use the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method with the *lnControlCode* parameter set to **ADS\_PROPERTY\_APPEND**.</span></span>
4.  <span data-ttu-id="9dfe9-127">Para confirmar as alterações no diretório, chame [**IADs:: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span><span class="sxs-lookup"><span data-stu-id="9dfe9-127">To commit changes to the directory, call [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span></span>

 

 