---
description: O método GetAudioLanguage recupera uma cadeia de caracteres que indica qual idioma está disponível no fluxo de áudio especificado.
ms.assetid: 5ff12058-eb00-4a2c-8d39-88282f68f001
title: Método GetAudioLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af71ad7943fe5442ded09f0b599c64c4b7215dac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500199"
---
# <a name="getaudiolanguage-method"></a><span data-ttu-id="a8adb-103">Método GetAudioLanguage</span><span class="sxs-lookup"><span data-stu-id="a8adb-103">GetAudioLanguage Method</span></span>

> [!Note]  
> <span data-ttu-id="a8adb-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a8adb-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="a8adb-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="a8adb-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="a8adb-106">O `GetAudioLanguage` método recupera uma cadeia de caracteres que indica qual idioma está disponível no fluxo de áudio especificado.</span><span class="sxs-lookup"><span data-stu-id="a8adb-106">The `GetAudioLanguage` method retrieves a string indicating which language is available on the specified audio stream.</span></span>

``` syntax
[ slang = ] MSWebDVD.GetAudioLanguage(iStream)
```

## <a name="parameters"></a><span data-ttu-id="a8adb-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8adb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8adb-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="a8adb-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="a8adb-109">Especifica o número do fluxo de áudio no título atual como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="a8adb-109">Specifies the audio stream number in the current title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8adb-110">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a8adb-110">Return Value</span></span>

<span data-ttu-id="a8adb-111">Retorna uma cadeia de caracteres legível que identifica o idioma do fluxo de áudio no título atual.</span><span class="sxs-lookup"><span data-stu-id="a8adb-111">Returns a human-readable string identifying the language of the audio stream in the current title.</span></span>

 

 



