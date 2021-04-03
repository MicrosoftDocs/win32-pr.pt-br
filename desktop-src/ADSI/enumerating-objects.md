---
title: Enumerando objetos
description: Para exibir o objeto filho de um contêiner, como uma UO (unidade organizacional), enumere o objeto de contêiner.
ms.assetid: 06995281-d269-42ce-839f-2938a2f6af22
ms.tgt_platform: multiple
keywords:
- Enumerando objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26b78f084f95ac59c909b326be10d42c4a6696a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822220"
---
# <a name="enumerating-objects"></a><span data-ttu-id="f4c9e-104">Enumerando objetos</span><span class="sxs-lookup"><span data-stu-id="f4c9e-104">Enumerating Objects</span></span>

<span data-ttu-id="f4c9e-105">Para exibir o objeto filho de um contêiner, como uma UO (unidade organizacional), enumere o objeto de contêiner.</span><span class="sxs-lookup"><span data-stu-id="f4c9e-105">To view the child object of a container, such as an organizational unit (OU), enumerate the container object.</span></span> <span data-ttu-id="f4c9e-106">Para tornar uma analogia com um sistema de arquivos, o objeto filho corresponderia aos arquivos no diretório, enquanto o contêiner, que é o objeto pai, corresponderia ao próprio diretório.</span><span class="sxs-lookup"><span data-stu-id="f4c9e-106">To make an analogy to a file system, the child object would correspond to files in the directory, while the container, which is the parent object, would correspond to the directory itself.</span></span> <span data-ttu-id="f4c9e-107">Você também pode usar a operação enumerar quando desejar obter o objeto pai de um objeto.</span><span class="sxs-lookup"><span data-stu-id="f4c9e-107">You may also use the enumerate operation when you want to get the parent object of an object.</span></span>

<span data-ttu-id="f4c9e-108">Ao enumerar um objeto, você realmente se associa a um objeto no diretório e uma interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) é retornada em cada objeto.</span><span class="sxs-lookup"><span data-stu-id="f4c9e-108">When you enumerate an object, you actually bind to an object in the directory, and an [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface is returned on each object.</span></span>

<span data-ttu-id="f4c9e-109">O exemplo de código a seguir mostra como enumerar os filhos de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="f4c9e-109">The following code example shows how to enumerate the children of a container.</span></span>


```VB
Dim ou As IADs
' Bind to an object using its DN.
On Error GoTo Cleanup

Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")

For each child in ou
    Debug.Print child.Name
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ou = Nothing
```



<span data-ttu-id="f4c9e-110">Você pode filtrar os tipos de objetos retornados da enumeração.</span><span class="sxs-lookup"><span data-stu-id="f4c9e-110">You can filter the types of objects returned from the enumeration.</span></span> <span data-ttu-id="f4c9e-111">Por exemplo, para exibir apenas usuários e grupos, use o exemplo de código a seguir antes da enumeração.</span><span class="sxs-lookup"><span data-stu-id="f4c9e-111">For example, to display only users and groups, use the following code example before the enumeration.</span></span>


```VB
Ou.Filter = Array("user", "group")
```



<span data-ttu-id="f4c9e-112">Se você tiver uma referência de objeto, poderá obter o pai do objeto usando a propriedade [**pai**](iads-property-methods.md) [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="f4c9e-112">If you have an object reference, you can get the object's parent using the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) [**Parent**](iads-property-methods.md) property.</span></span> <span data-ttu-id="f4c9e-113">O exemplo de código a seguir mostra como associar ao objeto pai.</span><span class="sxs-lookup"><span data-stu-id="f4c9e-113">The following code example shows how to bind to the parent object.</span></span>


```VB
parentPath = obj.Parent
Set parent = GetObject(parentPath)
```



<span data-ttu-id="f4c9e-114">Para obter mais informações, consulte [Enumerando objetos ADSI](enumerating-adsi-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f4c9e-114">For more information, see [Enumerating ADSI Objects](enumerating-adsi-objects.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4c9e-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f4c9e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4c9e-116">Pesquisando objetos</span><span class="sxs-lookup"><span data-stu-id="f4c9e-116">Searching for Objects</span></span>](searching-for-objects.md)
</dt> </dl>

 

 




