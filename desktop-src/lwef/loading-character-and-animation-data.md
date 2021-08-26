---
title: Carregando dados de caractere e animação
description: Carregando dados de caractere e animação
ms.assetid: cd674513-fd68-49bb-a43f-12b07adddf3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0e387a6122ab08513763878678d99941ef65d8ed11822eed8639fccd6e3815d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961426"
---
# <a name="loading-character-and-animation-data"></a>Carregando dados de caractere e animação

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Depois de ter um ponteiro para a interface [**IAgentEx**](iagentex.md) , você pode usar o método [**Load**](load-method.md) para carregar um caractere e recuperar sua interface [**IAgentCharacterEx**](iagentcharacterex.md) . Há três possibilidades diferentes para o caminho de carga de um caractere. O primeiro é compatível com o Microsoft Agent 1,5, em que o caminho especificado é o caminho completo e o nome do arquivo de um caractere. A segunda possibilidade é especificar apenas o nome do arquivo, nesse caso, o Agent examina seu diretório chars. A última possibilidade é fornecer um parâmetro VARIANT vazio que faz com que o caractere padrão seja carregado.


```
   // Create a variant to store the filename of the character to load

   const LPWSTR kpwszCharacter = L"merlin.acs";

   VariantInit(&vPath);

   vPath.vt = VT_BSTR;
   vPath.bstrVal = SysAllocString(kpwszCharacter);

   // Load the character

   hRes = pAgentEx->Load(vPath, &lCharID, &lRequestID);

   // Get its IAgentCharacterEx interface

   hRes = pAgentEx->GetCharacterEx(lCharID, &pCharacterEx);
```



Você pode usar essa interface para acessar os métodos do caractere:


```
   // Show the character.  The first parameter tells Microsoft
   // Agent to show the character by playing an animation.

   hRes = pCharacterEx->Show(FALSE, &lRequestID);

   // Make the character speak

   bszSpeak = SysAllocString(L"Hello World!");

   hRes = pCharacterEx->Speak(bszSpeak, NULL, &lRequestID);

   SysFreeString(bszSpeak);
```



Quando você não precisar mais dos serviços do Microsoft Agent, como quando o aplicativo cliente é desligado, libere suas interfaces. Observe que a liberação da interface de caracteres não descarrega o caractere. Chame o método [**Unload**](unload-method.md) para fazer isso antes de liberar a interface [**IAgentEx**](iagentex.md) :


```
// Clean up

if (pCharacterEx) {

   // Release the character interface

   pCharacterEx->Release();

   // Unload the character.  NOTE:  releasing the character
   // interface does NOT make the character go away.  You must
   // call Unload.

   pAgentEx->Unload(lCharID);
}
   
// Release the Agent

pAgentEx->Release();

VariantClear(&vPath);
```



 

 




