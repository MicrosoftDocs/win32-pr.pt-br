---
title: IAgentBalloon GetFontStrikethru
description: IAgentBalloon GetFontStrikethru
ms.assetid: b5c253e8-dca7-44a6-b63b-a33e6e793a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2001ec0125949144843d500f125b3502e94723db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364408"
---
# <a name="iagentballoongetfontstrikethru"></a><span data-ttu-id="de79d-103">IAgentBalloon::GetFontStrikethru</span><span class="sxs-lookup"><span data-stu-id="de79d-103">IAgentBalloon::GetFontStrikethru</span></span>

<span data-ttu-id="de79d-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="de79d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontStrikethru(
   long * pbFontStrikethru  // address of variable for strikethrough setting 
);                          // for font displayed in word balloon 
```

<span data-ttu-id="de79d-105">Indica se a fonte usada em um balão de palavra tem o estilo tachado definido.</span><span class="sxs-lookup"><span data-stu-id="de79d-105">Indicates whether the font used in a word balloon has the strikethrough style set.</span></span>

-   <span data-ttu-id="de79d-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="de79d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="de79d-107"><span id="pbFontStrikethru"></span><span id="pbfontstrikethru"></span><span id="PBFONTSTRIKETHRU"></span>*pbFontStrikethru*</span><span class="sxs-lookup"><span data-stu-id="de79d-107"><span id="pbFontStrikethru"></span><span id="pbfontstrikethru"></span><span id="PBFONTSTRIKETHRU"></span>*pbFontStrikethru*</span></span>
</dt> <dd>

<span data-ttu-id="de79d-108">O endereço de um valor que recebe **true** se o estilo tachado da fonte for definido e **false** se não.</span><span class="sxs-lookup"><span data-stu-id="de79d-108">The address of a value that receives **True** if the font strikethrough style is set and **False** if not.</span></span>

</dd> </dl>

<span data-ttu-id="de79d-109">O estilo de fonte usado em um balão de palavras de caracteres é definido no editor de caracteres do agente da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="de79d-109">The font style used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="de79d-110">Ele não pode ser alterado por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="de79d-110">It cannot be changed by an application.</span></span> <span data-ttu-id="de79d-111">No entanto, o usuário pode substituir as configurações de fonte para todos os caracteres usando a folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="de79d-111">However, the user can override the font settings for all characters using the Microsoft Agent property sheet.</span></span>

 

 




