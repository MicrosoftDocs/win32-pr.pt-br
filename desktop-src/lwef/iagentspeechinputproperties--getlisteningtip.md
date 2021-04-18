---
title: IAgentSpeechInputProperties GetListeningTip
description: IAgentSpeechInputProperties GetListeningTip
ms.assetid: b0488a54-03f8-43ce-935c-dd49c6ed5dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91218fb7935edb68458d540a8f35fe5402b317ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105797908"
---
# <a name="iagentspeechinputpropertiesgetlisteningtip"></a><span data-ttu-id="3e100-103">IAgentSpeechInputProperties::GetListeningTip</span><span class="sxs-lookup"><span data-stu-id="3e100-103">IAgentSpeechInputProperties::GetListeningTip</span></span>

<span data-ttu-id="3e100-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3e100-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetListeningTip(
long * pbListeningTip  // address of variable for listening tip flag
);                       
```

<span data-ttu-id="3e100-105">Recupera um valor que indica se a dica de escuta está habilitada para exibição.</span><span class="sxs-lookup"><span data-stu-id="3e100-105">Retrieves a value indicating whether the Listening Tip is enabled for display.</span></span>

-   <span data-ttu-id="3e100-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3e100-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="3e100-107"><span id="pbListeningTip"></span><span id="pblisteningtip"></span><span id="PBLISTENINGTIP"></span>*pbListeningTip*</span><span class="sxs-lookup"><span data-stu-id="3e100-107"><span id="pbListeningTip"></span><span id="pblisteningtip"></span><span id="PBLISTENINGTIP"></span>*pbListeningTip*</span></span>
</dt> <dd>

<span data-ttu-id="3e100-108">Endereço de uma variável que recebe **true** se a dica de escuta estiver habilitada para exibição ou **false** se a dica de escuta estiver desabilitada.</span><span class="sxs-lookup"><span data-stu-id="3e100-108">Address of a variable that receives **True** if the Listening Tip is enabled for display, or **False** if the Listening Tip is disabled.</span></span>

</dd> </dl>

<span data-ttu-id="3e100-109">Se [**Getabilited**](iagentspeechinputproperties--getenabled.md) retornar **false**, a consulta de qualquer outra propriedade de entrada de fala retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="3e100-109">If [**GetEnabled**](iagentspeechinputproperties--getenabled.md) returns **False**, querying any other speech input properties returns an error.</span></span>

## <a name="see-also"></a><span data-ttu-id="3e100-110">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="3e100-110">See Also</span></span>

[<span data-ttu-id="3e100-111">**IAgentSpeechInputProperties:: getabilited**</span><span class="sxs-lookup"><span data-stu-id="3e100-111">**IAgentSpeechInputProperties::GetEnabled**</span></span>](iagentspeechinputproperties--getenabled.md)


 

 




