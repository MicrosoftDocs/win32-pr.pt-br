---
description: O método GetSubpictureLanguage recupera o idioma para o fluxo de subimagem especificado.
ms.assetid: 2a2e6961-99c3-4200-b462-b381f9e37066
title: Método GetSubpictureLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f87d1bf95ee13a1a15e631e2bc53477b62b789a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105810231"
---
# <a name="getsubpicturelanguage-method"></a><span data-ttu-id="a221e-103">Método GetSubpictureLanguage</span><span class="sxs-lookup"><span data-stu-id="a221e-103">GetSubpictureLanguage Method</span></span>

> [!Note]  
> <span data-ttu-id="a221e-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a221e-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="a221e-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="a221e-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="a221e-106">O `GetSubpictureLanguage` método recupera o idioma para o fluxo de subimagem especificado.</span><span class="sxs-lookup"><span data-stu-id="a221e-106">The `GetSubpictureLanguage` method retrieves the language for the specified subpicture stream.</span></span>

``` syntax
[ sLang = ] MSWebDVD.GetSubpictureLanguage(iStream)
```

## <a name="parameters"></a><span data-ttu-id="a221e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a221e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a221e-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="a221e-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="a221e-109">Especifica o número de fluxo da subimagem cujo idioma de texto você deseja recuperar como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="a221e-109">Specifies the subpicture stream number whose text language you want to retrieve as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a221e-110">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a221e-110">Return Value</span></span>

<span data-ttu-id="a221e-111">Retorna uma cadeia de caracteres legível que identifica o idioma do fluxo de áudio no título atual.</span><span class="sxs-lookup"><span data-stu-id="a221e-111">Returns a human-readable string identifying the language of the audio stream in the current title.</span></span>

 

 



