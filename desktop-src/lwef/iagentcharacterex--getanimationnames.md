---
title: IAgentCharacterEx GetAnimationNames
description: IAgentCharacterEx GetAnimationNames
ms.assetid: d565b258-dc12-422b-a13d-aeec56057f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c9cb1bc1b51b0bead2f071e0cd8561ef055ef6b7eb7986b3be969208452331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478019"
---
# <a name="iagentcharacterexgetanimationnames"></a>IAgentCharacterEx:: getanimationnames

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetAnimationNames(
   IUnknown ** punkEnum // address of IUnknown interface
);
```

Recupera os nomes de animação de um caractere.

-   Retorna **S \_ OK** para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*
</dt> <dd>

O endereço da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para a coleção de animações do caractere.

</dd> </dl>

Essa função permite que você enumere os nomes das animações para um caractere. Os itens na coleção não têm propriedades, portanto, itens individuais não podem ser acessados diretamente. Para acessar a coleção, consulte punkEnum para a interface IEnumVARIANT:


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
> Para caracteres de ACF, a coleção retorna todas as animações que foram definidas para o caractere, adicionando àquelas que foram recuperadas com o método [**Get**](https://www.bing.com/search?q=**Get**) .
