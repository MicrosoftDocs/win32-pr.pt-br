---
description: O método GetSubpictureLanguage recupera a linguagem para o fluxo de subtítpico especificado.
ms.assetid: 2a2e6961-99c3-4200-b462-b381f9e37066
title: Método GetSubpictureLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdedc90789efb331b1438744a0f64a42782bf1d1e363170ce626ed023d2e542a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536926"
---
# <a name="getsubpicturelanguage-method"></a>Método GetSubpictureLanguage

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `GetSubpictureLanguage` método recupera o idioma para o fluxo de subpicture especificado.

``` syntax
[ sLang = ] MSWebDVD.GetSubpictureLanguage(iStream)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*Istream*
</dt> <dd>

Especifica o número do fluxo de subtítpio cujo idioma de texto você deseja recuperar como um Inteiro.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna uma cadeia de caracteres acessível por humanos que identifica o idioma do fluxo de áudio no título atual.

 

 



