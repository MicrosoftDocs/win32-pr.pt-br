---
description: O método GetLangFromLangID recupera uma cadeia de caracteres legível ao receber uma ID de idioma principal.
ms.assetid: 73cff3df-bfcd-4e51-bd41-51545ed82f09
title: Método GetLangFromLangID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6041f12c82f0e659928db9f5aa02fd916d3ff9907bf3114eb40c525b8b1d8d2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756746"
---
# <a name="getlangfromlangid-method"></a>Método GetLangFromLangID

> [!Note]  
> esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

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

 

 



