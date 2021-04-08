---
title: IAgentSpeechInputProperties gettecla de atalho
description: IAgentSpeechInputProperties gettecla de atalho
ms.assetid: b93e5b46-b8f8-4ca4-8417-7626b97d8928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e672b26f97cfbe92bc71d0ceab165e100c3ecf92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004783"
---
# <a name="iagentspeechinputpropertiesgethotkey"></a><span data-ttu-id="db843-103">IAgentSpeechInputProperties::</span><span class="sxs-lookup"><span data-stu-id="db843-103">IAgentSpeechInputProperties::GetHotKey</span></span>

<span data-ttu-id="db843-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="db843-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHotKey(
BSTR * pbszHotCharKey  // address of variable for listening key 
);                        
```

<span data-ttu-id="db843-105">Recupera a atribuição de teclado atual para a chave de escuta de entrada de fala.</span><span class="sxs-lookup"><span data-stu-id="db843-105">Retrieves the current keyboard assignment for the speech input Listening key.</span></span>

-   <span data-ttu-id="db843-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="db843-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="db843-107"><span id="pbszHotCharKey"></span><span id="pbszhotcharkey"></span><span id="PBSZHOTCHARKEY"></span>*pbszHotCharKey*</span><span class="sxs-lookup"><span data-stu-id="db843-107"><span id="pbszHotCharKey"></span><span id="pbszhotcharkey"></span><span id="PBSZHOTCHARKEY"></span>*pbszHotCharKey*</span></span>
</dt> <dd>

<span data-ttu-id="db843-108">Endereço de um BSTR que recebe a configuração de atalho atual usada para abrir o canal de áudio para entrada de fala.</span><span class="sxs-lookup"><span data-stu-id="db843-108">Address of a BSTR that receives the current hotkey setting used to open the audio channel for speech input.</span></span>

</dd> </dl>

<span data-ttu-id="db843-109">Se [**Getabilited**](iagentspeechinputproperties--getenabled.md) retornar **false**, a consulta dessa configuração gerará um erro.</span><span class="sxs-lookup"><span data-stu-id="db843-109">If [**GetEnabled**](iagentspeechinputproperties--getenabled.md) returns **False**, querying this setting raises an error.</span></span>

## <a name="see-also"></a><span data-ttu-id="db843-110">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="db843-110">See Also</span></span>

[<span data-ttu-id="db843-111">**IAgentSpeechInputProperties:: getabilited**</span><span class="sxs-lookup"><span data-stu-id="db843-111">**IAgentSpeechInputProperties::GetEnabled**</span></span>](iagentspeechinputproperties--getenabled.md)


 

 




