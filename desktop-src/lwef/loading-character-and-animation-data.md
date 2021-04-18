---
title: Carregando dados de caractere e animação
description: Carregando dados de caractere e animação
ms.assetid: cd674513-fd68-49bb-a43f-12b07adddf3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed77524c4e3cbbcae725b87c3671914f2261fa1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105789219"
---
# <a name="loading-character-and-animation-data"></a>Carregando dados de caractere e animação

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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



 

 




