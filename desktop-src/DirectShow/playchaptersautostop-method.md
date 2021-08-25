---
description: O método PlayChaptersAutoStop inicia a reprodução no capítulo especificado no título especificado e no número de capítulos especificados.
ms.assetid: ede19f02-6eda-42da-a108-06d78dc2e8a9
title: Método PlayChaptersAutoStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58c518496f81f4ca4e662bf8dbc821f2378cd38d27c7546356144910c0c5ba72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830736"
---
# <a name="playchaptersautostop-method"></a>Método PlayChaptersAutoStop

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O método inicia a reprodução no capítulo especificado no título especificado e no `PlayChaptersAutoStop` número de capítulos especificados.

``` syntax
MSWebDVD.PlayChaptersAutoStop(iTitle, iChapter, iChapterCount)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Especifica o título como um valor Inteiro.

</dd> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*
</dt> <dd>

Especifica o capítulo inicial como um valor Inteiro.

</dd> <dt>

<span id="iChapterCount"></span><span id="ichaptercount"></span><span id="ICHAPTERCOUNT"></span>*iChapterCount*
</dt> <dd>

Especifica o número de capítulos a reproduzir como um valor Inteiro.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Quando o último capítulo tiver sido interpretado, esse método faz com que uma notificação de evento [**EC \_ DVD CHAPTER \_ \_ AUTOSTOP**](ec-dvd-chapter-autostop.md) seja enviada ao aplicativo.

 

 



