---
description: O método IsAudioStreamEnabled recupera um valor que indica se o fluxo de áudio especificado está habilitado no título atual.
ms.assetid: df6c69a7-6eb0-4662-a3aa-f3f895b42cbc
title: Método IsAudioStreamEnabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2131376346f2a0311fc5acd8e0051292a12fb0145b44226363c7d891a5ef3c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817471"
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

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*Istream*
</dt> <dd>

Especifica o fluxo de áudio como um valor Inteiro de 0 a 7.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um valor booliana que indica se o fluxo de áudio especificado está disponível para o título atual. True significa que ele está disponível.

## <a name="remarks"></a>Comentários

Embora um disco possa conter até oito fluxos de áudio independentes, cada fluxo não está necessariamente disponível para cada título. Por exemplo, um título de filme principal pode ter três fluxos de áudio para inglês, espanhol e japonês, mas o título "Próximas atrações" pode ter apenas um fluxo de áudio em inglês. Sempre verifique se um fluxo está disponível para um título antes de definir a [**propriedade CurrentAudioStream.**](currentaudiostream-property.md)

 

 



