---
description: A propriedade DVDAdm fornece acesso ao objeto MSDVDAdm que contém métodos e propriedades para salvar informações do aplicativo e do usuário.
ms.assetid: eb73a851-7118-42f3-be99-1cf356d2e37a
title: Propriedade DVDAdm
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5adedea036393e68456cfd9f035882ae9c335063030518e808c57bced6d5b5b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079156"
---
# <a name="dvdadm-property"></a>Propriedade DVDAdm

> [!Note]  
> esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

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



 

 



