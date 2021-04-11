---
title: IAgentBalloon getabilited
description: IAgentBalloon getabilited
ms.assetid: 1a5ea6c0-6150-459f-95eb-a9c7598c1d94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd78245534b942e7972066ec90179172f7b556c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292806"
---
# <a name="iagentballoongetenabled"></a><span data-ttu-id="bc6f0-103">IAgentBalloon:: getabilited</span><span class="sxs-lookup"><span data-stu-id="bc6f0-103">IAgentBalloon::GetEnabled</span></span>

<span data-ttu-id="bc6f0-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bc6f0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetEnabled(
  long * pbEnabled  // address of variable for Enabled setting 
);                  // for word balloon
```

<span data-ttu-id="bc6f0-105">Recupera o valor da propriedade [**Enabled**](enabled-property.md) para um balão de palavra.</span><span class="sxs-lookup"><span data-stu-id="bc6f0-105">Retrieves the value of the [**Enabled**](enabled-property.md) property for a word balloon.</span></span>

-   <span data-ttu-id="bc6f0-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="bc6f0-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="bc6f0-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span><span class="sxs-lookup"><span data-stu-id="bc6f0-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="bc6f0-108">O endereço de uma variável que recebe **true** quando a palavra balão estiver habilitada e **false** quando for desabilitada.</span><span class="sxs-lookup"><span data-stu-id="bc6f0-108">The address of a variable that receives **True** when the word balloon is enabled and **False** when it is disabled.</span></span>

</dd> </dl>

<span data-ttu-id="bc6f0-109">O servidor Microsoft Agent exibe automaticamente o balão de palavras para saída falada, a menos que esteja desabilitada.</span><span class="sxs-lookup"><span data-stu-id="bc6f0-109">The Microsoft Agent server automatically displays the word balloon for spoken output, unless it is disabled.</span></span> <span data-ttu-id="bc6f0-110">O balão de palavras pode ser desabilitado para um caractere no editor de caracteres do Microsoft Agent ou (pelo usuário) para todos os caracteres na folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="bc6f0-110">The word balloon can be disabled for a character in the Microsoft Agent Character Editor, or (by the user) for all characters in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="bc6f0-111">Se o usuário desabilitar a palavra balão, o cliente não poderá restaurá-la.</span><span class="sxs-lookup"><span data-stu-id="bc6f0-111">If the user disables the word balloon, the client cannot restore it.</span></span>

 

 




