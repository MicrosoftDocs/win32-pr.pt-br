---
title: Cadeias de caracteres inseridas
description: As estruturas de informações não conterão cadeias de caracteres inseridas. Isso melhora o alinhamento das estruturas de informações e permite a flexibilidade do OEM nas principais funções.
ms.assetid: a3272a0a-5352-4847-84fd-113b4467c32c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365a9c71ed50971661f9ad06855024ecba2796f1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636261"
---
# <a name="embedded-strings"></a><span data-ttu-id="db707-104">Cadeias de caracteres inseridas</span><span class="sxs-lookup"><span data-stu-id="db707-104">Embedded Strings</span></span>

<span data-ttu-id="db707-105">As estruturas de informações não conterão cadeias de caracteres inseridas.</span><span class="sxs-lookup"><span data-stu-id="db707-105">Information structures will not contain embedded strings.</span></span> <span data-ttu-id="db707-106">Isso melhora o alinhamento das estruturas de informações e permite a flexibilidade do OEM nas principais funções.</span><span class="sxs-lookup"><span data-stu-id="db707-106">This improves the alignment of the information structures and allows for OEM flexibility in the core functions.</span></span>

<span data-ttu-id="db707-107">Qualquer campo de informações retornado em uma chamada de enumeração que pode ser usado posteriormente como uma chave para a chamada para uma função de gerenciamento de rede GetInfo é garantido como presente no buffer de enumeração.</span><span class="sxs-lookup"><span data-stu-id="db707-107">Any information field that is returned in an enumeration call that can be subsequently used as a key for the call to a GetInfo network management function is guaranteed to be present in the enumeration buffer.</span></span> <span data-ttu-id="db707-108">Se a cadeia de caracteres de informações de comprimento variável que especificasse o valor do campo de chave não couber, toda a estrutura de comprimento fixo da entrada não será retornada.</span><span class="sxs-lookup"><span data-stu-id="db707-108">If the variable-length information string that would specify the key field value will not fit, then the entire fixed-length structure for the entry is not returned.</span></span> <span data-ttu-id="db707-109">Outros campos de comprimento variável serão retornados como um ponteiro **NULL** para o caso em que a cadeia de caracteres não couber.</span><span class="sxs-lookup"><span data-stu-id="db707-109">Other variable-length fields will be returned as a **NULL** pointer for the case in which the string does not fit.</span></span>

 

 




