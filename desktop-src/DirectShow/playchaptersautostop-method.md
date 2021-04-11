---
description: O método PlayChaptersAutoStop inicia a reprodução no capítulo especificado no título especificado e o número de capítulos especificado.
ms.assetid: ede19f02-6eda-42da-a108-06d78dc2e8a9
title: Método PlayChaptersAutoStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f542f890a54c755c9ea041c46f7cef3b4b7fd9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163763"
---
# <a name="playchaptersautostop-method"></a>Método PlayChaptersAutoStop

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `PlayChaptersAutoStop` método inicia a reprodução no capítulo especificado no título especificado e o número de capítulos especificado.

``` syntax
MSWebDVD.PlayChaptersAutoStop(iTitle, iChapter, iChapterCount)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Especifica o título como um valor inteiro.

</dd> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*
</dt> <dd>

Especifica o capítulo inicial como um valor inteiro.

</dd> <dt>

<span id="iChapterCount"></span><span id="ichaptercount"></span><span id="ICHAPTERCOUNT"></span>*iChapterCount*
</dt> <dd>

Especifica o número de capítulos a serem reproduzidos como um valor inteiro.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Quando o último capítulo foi reproduzido, esse método faz com que uma notificação de evento do [**\_ \_ capítulo \_ autostop**](ec-dvd-chapter-autostop.md) de um DVD do EC seja enviada para o aplicativo.

 

 



