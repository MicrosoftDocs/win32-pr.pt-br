---
description: O método GetLangFromLangID recupera uma cadeia de caracteres legível ao receber uma ID de idioma principal.
ms.assetid: 73cff3df-bfcd-4e51-bd41-51545ed82f09
title: Método GetLangFromLangID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23afddf746852028c26732eb658e786588f7e9ec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825779"
---
# <a name="getlangfromlangid-method"></a>Método GetLangFromLangID

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `GetLangFromLangID` método recupera uma cadeia de caracteres legível ao receber uma ID de idioma principal.

``` syntax
[ sLanguage = ] MSWebDVD.GetLangFromLangID(iPrimaryLangID)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iPrimaryLangID"></span><span id="iprimarylangid"></span><span id="IPRIMARYLANGID"></span>*iPrimaryLangID*
</dt> <dd>

Especifica a ID do idioma principal como um inteiro.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna uma representação de cadeia de caracteres do idioma que pode ser exibido na interface do usuário do aplicativo.

## <a name="remarks"></a>Comentários

Embora esse método seja nomeado `GetLangFromLangID` , o parâmetro que você passa é, na verdade, a ID do idioma principal, não a ID do idioma.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetAudioLanguage**](getaudiolanguage-method.md)
</dt> <dt>

[**GetDVDTextLanguageLCID**](getdvdtextlanguagelcid-method.md)
</dt> </dl>

 

 



