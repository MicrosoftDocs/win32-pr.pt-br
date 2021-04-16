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
# <a name="getaudiolanguage-method"></a>Método GetAudioLanguage

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `GetAudioLanguage` método recupera uma cadeia de caracteres que indica qual idioma está disponível no fluxo de áudio especificado.

``` syntax
[ slang = ] MSWebDVD.GetAudioLanguage(iStream)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Especifica o número do fluxo de áudio no título atual como um inteiro.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna uma cadeia de caracteres legível que identifica o idioma do fluxo de áudio no título atual.

 

 



