---
description: O método GetDVDTextLanguageLCID recupera o LCID (identificador de localidade) para o bloco de cadeia de caracteres de texto especificado.
ms.assetid: feaa1db8-2d33-4c32-8491-f3aa5555e3d3
title: Método GetDVDTextLanguageLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66d21b9870982b605d9deeb1e22882a525c5616
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500195"
---
# <a name="getdvdtextlanguagelcid-method"></a>Método GetDVDTextLanguageLCID

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `GetDVDTextLanguageLCID` método recupera o LCID (identificador de localidade) para o bloco de cadeia de caracteres de texto especificado.

``` syntax
[ iLCID = ] MSWebDVD.GetDVDTextLanguageLCID(iLangIndex)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*
</dt> <dd>

Especifica o bloco de linguagem de texto no disco como um inteiro.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um valor LCID que contém informações que especificam o idioma em que as cadeias de caracteres são gravadas.

## <a name="remarks"></a>Comentários

As cadeias de caracteres de texto complementares são armazenadas em blocos contíguos no disco. Cada idioma tem um bloco de cadeias de caracteres. Um aplicativo especifica esses blocos por um índice, que deve ser menor que o valor retornado por [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[Objeto MSWebDVD](mswebdvd-object.md)
</dt> <dt>

[**GetLangFromLangID**](getlangfromlangid-method.md)
</dt> </dl>

 

 



