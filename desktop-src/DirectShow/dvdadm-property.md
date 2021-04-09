---
description: A propriedade DVDAdm fornece acesso ao objeto MSDVDAdm que contém métodos e propriedades para salvar informações do aplicativo e do usuário.
ms.assetid: eb73a851-7118-42f3-be99-1cf356d2e37a
title: Propriedade DVDAdm
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c3d81742fc6e643d6ee805a76c14d07d45d1924
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087627"
---
# <a name="dvdadm-property"></a>Propriedade DVDAdm

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `DVDAdm` propriedade fornece acesso ao objeto [MSDVDAdm](msdvdadm-object.md) que contém métodos e propriedades para salvar informações do aplicativo e do usuário.

``` syntax
        MSWebDVD.DVDAdm
```

## <a name="remarks"></a>Comentários

Esta propriedade é somente leitura sem valor padrão. Não é necessário criar uma referência separada para o objeto **MSDVDAdm** . Para acessar os métodos e as propriedades do objeto, use a `DVDAdm` propriedade, conforme mostrado no exemplo a seguir.

## <a name="examples"></a>Exemplos


```VB
DVD.DVDAdm.DisableScreenSaver = true
```



 

 



