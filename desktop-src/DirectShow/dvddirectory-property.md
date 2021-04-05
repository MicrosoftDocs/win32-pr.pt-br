---
description: A propriedade DVDDirectory define ou recupera o diretório atual do volume de DVD atual.
ms.assetid: 0dbfdf28-cda5-41b2-82ce-114d9b940d91
title: Propriedade DVDDirectory
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36515c931fb8669db814886dfff12a4bf85bde28
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825794"
---
# <a name="dvddirectory-property"></a>Propriedade DVDDirectory

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `DVDDirectory` propriedade define ou recupera o diretório atual do volume de DVD atual.

``` syntax
[ sDirPath = ] MSWebDVD.DVDDirectory
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor de cadeia de caracteres que indica o caminho para o diretório raiz do DVD.

## <a name="remarks"></a>Comentários

Esta propriedade é de leitura/gravação sem valor padrão. Use esse método para definir o caminho raiz quando houver mais de uma unidade de DVD em um sistema. Quando há apenas uma unidade no sistema e sua letra de unidade é maior que "C", o objeto MSWebDVD a localiza automaticamente. Para um disco DVD-Video padrão, o caminho raiz deve incluir o \_ diretório de vídeo TS:


```VB
MSWebDVD.DVDDirectory = "e:\\video_ts"
```



Alguns volumes de DVD podem ter seus vídeos em um diretório chamado algo diferente de "vídeo \_ TS". A ideia geral é que um "volume de DVD" adicional (o conjunto de. IFO. VOB e. Arquivos BUP que normalmente seriam armazenados no \_ diretório TS de vídeo) podem ser colocados em um subdiretório no disco. Ao alterar a raiz para apontar para esse diretório, o MSWebDVD funcionará nesse volume de DVD separado. Um novo conjunto de menus, títulos e assim por diante estará disponível, independentemente dos títulos na raiz TS de vídeo \_ , que não estará mais acessível. Esses diretórios são chamados de "diretórios ocultos". O exemplo a seguir mostra como definir um diretório oculto como a raiz, onde "Hidden" é um espaço reservado para qualquer nome que o disco autorizou para o diretório.


```VB
MSWebDVD.DVDDirectory = "d:\\webdvd\\hidden"
```



 

 



