---
title: IAgentCharacterEx GetAnimationNames
description: IAgentCharacterEx GetAnimationNames
ms.assetid: d565b258-dc12-422b-a13d-aeec56057f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31dcb7ea34a9f0d833f8c1665a092fe4f3a30e7
ms.sourcegitcommit: baa7cd1709e48672f5f07ff83a9c9d5699c0efcd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/14/2021
ms.locfileid: "105759783"
---
# <a name="iagentcharacterexgetanimationnames"></a><span data-ttu-id="7244d-103">IAgentCharacterEx:: getanimationnames</span><span class="sxs-lookup"><span data-stu-id="7244d-103">IAgentCharacterEx::GetAnimationNames</span></span>

<span data-ttu-id="7244d-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7244d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetAnimationNames(
   IUnknown ** punkEnum // address of IUnknown interface
);
```

<span data-ttu-id="7244d-105">Recupera os nomes de animação de um caractere.</span><span class="sxs-lookup"><span data-stu-id="7244d-105">Retrieves the animation names for a character.</span></span>

-   <span data-ttu-id="7244d-106">Retorna **S \_ OK** para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7244d-106">Returns **S\_OK** to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="7244d-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span><span class="sxs-lookup"><span data-stu-id="7244d-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span></span>
</dt> <dd>

<span data-ttu-id="7244d-108">O endereço da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para a coleção de animações do caractere.</span><span class="sxs-lookup"><span data-stu-id="7244d-108">The address of the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface for the character's animation collection.</span></span>

</dd> </dl>

<span data-ttu-id="7244d-109">Essa função permite que você enumere os nomes das animações para um caractere.</span><span class="sxs-lookup"><span data-stu-id="7244d-109">This function enables you to enumerate the names of the animations for a character.</span></span> <span data-ttu-id="7244d-110">Os itens na coleção não têm propriedades, portanto, itens individuais não podem ser acessados diretamente.</span><span class="sxs-lookup"><span data-stu-id="7244d-110">Items in the collection have no properties, so individual items cannot be accessed directly.</span></span> <span data-ttu-id="7244d-111">Para acessar a coleção, consulte punkEnum para a interface IEnumVARIANT:</span><span class="sxs-lookup"><span data-stu-id="7244d-111">To access the collection, query punkEnum for the IEnumVARIANT interface:</span></span>


```c++
IEnumVARIANT pEnum;
VARIANT vAnimName;
DWORD dwRetrieved;

hRes = punkEnum->QueryInterface(IID_IEnumVARIANT, (LPVOID *)&pEnum);

if (SUCCEEDED(hRes)) {

    while (TRUE) {

         hRes = pEnum->Next(1, &vAnimName, &dwRetrieved);

         if (hRes != NOERROR)
            break;

         // vAnimName.bstrVal is the animation name

         VariantClear(&vAnimName);
    } 

    pEnum->Release();
}

punkEnum->Release();
```



> [!Note]  
> <span data-ttu-id="7244d-112">Para caracteres de ACF, a coleção retorna todas as animações que foram definidas para o caractere, adicionando àquelas que foram recuperadas com o método [**Get**](https://www.bing.com/search?q=**Get**) .</span><span class="sxs-lookup"><span data-stu-id="7244d-112">For ACF characters, the collection returns all the animations that have been defined for the character, adding to the ones that have been retrieved with the [**Get**](https://www.bing.com/search?q=**Get**) method.</span></span>
