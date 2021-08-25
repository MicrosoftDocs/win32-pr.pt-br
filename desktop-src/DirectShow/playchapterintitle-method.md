---
description: O método PlayChapterInTitle reproduz o capítulo especificado no título especificado.
ms.assetid: 784b0612-133b-465c-b1da-d9dac26e1b20
title: Método PlayChapterInTitle
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 407684ecf8db6053a4d166a4ed069f9cabf0b36f983dd04bfdf9cf85e6c8dc2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830866"
---
# <a name="playchapterintitle-method"></a>Método PlayChapterInTitle

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `PlayChapterInTitle` método reproduz o capítulo especificado no título especificado.

``` syntax
MSWebDVD.PlayChapterInTitle(iTitle, iChapter)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Especifica o título como um valor Inteiro.

</dd> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*
</dt> <dd>

Especifica o capítulo como um valor Inteiro.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Esse método inicia a reprodução no capítulo especificado e continua a reproduzir indefinidamente. Se você quiser reproduzir apenas um capítulo específico, use [**PlayChaptersAutoStop**](playchaptersautostop-method.md).

 

 



