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
# <a name="getsubpicturelanguage-method"></a>Método GetSubpictureLanguage

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `GetSubpictureLanguage` método recupera o idioma para o fluxo de subimagem especificado.

``` syntax
[ sLang = ] MSWebDVD.GetSubpictureLanguage(iStream)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Especifica o número de fluxo da subimagem cujo idioma de texto você deseja recuperar como um inteiro.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna uma cadeia de caracteres legível que identifica o idioma do fluxo de áudio no título atual.

 

 



