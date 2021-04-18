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
# <a name="iagentcharacterexgetanimationnames"></a>IAgentCharacterEx:: getanimationnames

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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
