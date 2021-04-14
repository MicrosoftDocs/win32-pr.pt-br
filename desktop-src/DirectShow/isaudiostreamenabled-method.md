---
description: O método IsAudioStreamEnabled recupera um valor que indica se o fluxo de áudio especificado está habilitado no título atual.
ms.assetid: df6c69a7-6eb0-4662-a3aa-f3f895b42cbc
title: Método IsAudioStreamEnabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92df59479e5729c392eb25b6c6c075a52b4835b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500136"
---
# <a name="isaudiostreamenabled-method"></a>Método IsAudioStreamEnabled

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `IsAudioStreamEnabled` método recupera um valor que indica se o fluxo de áudio especificado está habilitado no título atual.

``` syntax
[bEnabled = ] MSWebDVD.IsAudioStreamEnabled(iStream)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Especifica o fluxo de áudio como um valor inteiro de 0 a 7.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um valor booliano que indica se o fluxo de áudio especificado está disponível para o título atual. Verdadeiro significa que está disponível.

## <a name="remarks"></a>Comentários

Embora um disco possa conter até oito fluxos de áudio independentes, cada fluxo não está necessariamente disponível para cada título. Por exemplo, um título de filme principal pode ter três fluxos de áudio para inglês, espanhol e japonês, mas o título "chegando Attractions" pode ter apenas um fluxo de áudio em inglês. Sempre verifique se um fluxo está disponível para um título antes de definir a propriedade [**CurrentAudioStream**](currentaudiostream-property.md) .

 

 



