---
description: A propriedade DVDDirectory define ou recupera o diretório atual do volume de DVD atual.
ms.assetid: 0dbfdf28-cda5-41b2-82ce-114d9b940d91
title: Propriedade DVDDirectory
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2431d9255aa743698baeb9c4b8427ffa9bf5220a60182ac08c246e11f20bcec8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749096"
---
# <a name="dvddirectory-property"></a>Propriedade DVDDirectory

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A propriedade define ou recupera o diretório atual do volume `DVDDirectory` de DVD atual.

``` syntax
[ sDirPath = ] MSWebDVD.DVDDirectory
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor de cadeia de caracteres que indica o caminho para o diretório raiz do DVD.

## <a name="remarks"></a>Comentários

Essa propriedade é de leitura/gravação sem valor padrão. Use esse método para definir o caminho raiz quando houver mais de uma unidade de DVD em um sistema. Quando há apenas uma unidade no sistema e sua letra da unidade é maior que "C", o objeto MSWebDVD a localiza automaticamente. Para um disco DVD-Video padrão, o caminho raiz deve incluir o diretório de \_ vídeo ts:


```VB
MSWebDVD.DVDDirectory = "e:\\video_ts"
```



Alguns volumes de DVD podem ter seu vídeo em um diretório chamado algo diferente de "video \_ ts". A ideia geral é que um "volume de DVD" adicional (o conjunto de . Ifo. VOB e . Arquivos BUP que normalmente seriam armazenados no diretório VIDEO TS podem ser colocados em \_ um subdiretório no disco. Ao alterar a raiz para apontar para esse diretório, o MSWebDVD operará nesse volume de DVD separado. Um novo conjunto de menus, títulos e assim por diante estará disponível, independentemente dos títulos na raiz do VIDEO TS, que não estarão mais \_ acessíveis. Esses diretórios são chamados de "diretórios ocultos". O exemplo a seguir mostra como definir um diretório oculto como a raiz, em que "hidden" é um espaço reservado para qualquer nome que os autores de disco tenham dado ao diretório.


```VB
MSWebDVD.DVDDirectory = "d:\\webdvd\\hidden"
```



 

 



