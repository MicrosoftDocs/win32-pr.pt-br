---
title: IAgentBalloon GetFontUnderline
description: IAgentBalloon GetFontUnderline
ms.assetid: 19886e94-8095-4650-bd88-34ea9d96ddaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5acf35453209679dc96c85b3017fbe76b19d53b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006105"
---
# <a name="iagentballoongetfontunderline"></a><span data-ttu-id="42c62-103">IAgentBalloon::GetFontUnderline</span><span class="sxs-lookup"><span data-stu-id="42c62-103">IAgentBalloon::GetFontUnderline</span></span>

<span data-ttu-id="42c62-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="42c62-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontUnderline(
   long * pbFontUnderline  // address of variable for underline setting
);                         // for font displayed in word balloon 
```

<span data-ttu-id="42c62-105">Indica se a fonte usada em um balão de palavra tem o estilo de sublinhado definido.</span><span class="sxs-lookup"><span data-stu-id="42c62-105">Indicates whether the font used in a word balloon has the underline style set.</span></span>

-   <span data-ttu-id="42c62-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="42c62-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="42c62-107"><span id="pbFontUnderline"></span><span id="pbfontunderline"></span><span id="PBFONTUNDERLINE"></span>*pbFontUnderline*</span><span class="sxs-lookup"><span data-stu-id="42c62-107"><span id="pbFontUnderline"></span><span id="pbfontunderline"></span><span id="PBFONTUNDERLINE"></span>*pbFontUnderline*</span></span>
</dt> <dd>

<span data-ttu-id="42c62-108">O endereço de um valor que recebe **true** se o estilo de sublinhado da fonte for definido e **false** se não.</span><span class="sxs-lookup"><span data-stu-id="42c62-108">The address of a value that receives **True** if the font underline style is set and **False** if not.</span></span>

</dd> </dl>

<span data-ttu-id="42c62-109">O estilo de fonte usado em um balão de palavras de caracteres é definido no editor de caracteres do agente da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="42c62-109">The font style used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="42c62-110">Ele não pode ser alterado por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="42c62-110">It cannot be changed by an application.</span></span> <span data-ttu-id="42c62-111">No entanto, o usuário pode substituir as configurações de fonte para todos os caracteres usando a folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="42c62-111">However, the user can override the font settings for all characters using the Microsoft Agent property sheet.</span></span>

 

 




