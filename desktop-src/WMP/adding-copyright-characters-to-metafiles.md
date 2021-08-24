---
title: Adicionando caracteres de direitos autorais a metaarquivos
description: Os caracteres para os símbolos de registro de direitos autorais e marcas registradas (\ 169; ou \ 174;) podem não ser exibidos corretamente se o metarquivo não for codificado usando o esquema de codificação UTF-8.
ms.assetid: 9124c8d4-1fc1-4163-ada9-d96af58f8b98
keywords:
- Adicionando caracteres de direitos autorais a metaarquivos Windows Media Player
topic_type:
- apiref
api_name:
- Adding Copyright Characters to Metafiles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b0ab5fc4e539331406bb776a4bcdacbed6578a234dd9e84a3c358cdbe9936ad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865156"
---
# <a name="adding-copyright-characters-to-metafiles"></a>Adicionando caracteres de direitos autorais a metaarquivos

Os caracteres de símbolos de registro de direitos autorais e marcas comerciais (© ou®) podem não ser exibidos corretamente se o metarquivo não for codificado usando o esquema de codificação UTF-8. Nesse caso, para exibir qualquer um desses símbolos corretamente para todos os usuários, você pode usar os equivalentes ASCII (c) e (r) dentro do elemento de **direitos autorais** , conforme mostrado no código a seguir.


```
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>
```



Se o metarquivo for codificado usando UTF-8, os símbolos de direitos autorais e marcas comerciais serão exibidos corretamente.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Windows Referência de elementos de metarquivo de mídia**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




