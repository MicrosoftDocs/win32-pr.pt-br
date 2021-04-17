---
description: O método PlayChapter inicia a reprodução do capítulo especificado dentro do título atual.
ms.assetid: d0318a0d-4ff4-42f2-b009-996b7ff0f632
title: Método PlayChapter
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bab4600d8d4fc09c4b63fa423c66823e92e95a2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105789825"
---
# <a name="playchapter-method"></a>Método PlayChapter

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `PlayChapter` método inicia a reprodução do capítulo especificado dentro do título atual.

``` syntax
MSWebDVD.PlayChapter(iChapter)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*
</dt> <dd>

Especifica o índice do capítulo no título atual como um inteiro.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Quando o final do capítulo especificado for atingido, esse método continuará a reproduzir os capítulos subsequentes, se existirem. Se você quiser reproduzir apenas um capítulo especificado, use [**PlayChaptersAutoStop**](playchaptersautostop-method.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**PlayChapterInTitle**](playchapterintitle-method.md)
</dt> </dl>

 

 



