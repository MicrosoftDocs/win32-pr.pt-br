---
description: O método DVDAdm. RestoreScreenSaver restaura as configurações de proteção de tela do sistema.
ms.assetid: 606ab850-95bf-4c60-b7cf-e3a94ceee7a7
title: Método RestoreScreenSaver
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 684250b237105e391472237a5e7093855dd82ef5b59ffbbaa20ebecf386da302
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696966"
---
# <a name="restorescreensaver-method"></a>Método RestoreScreenSaver

> [!Note]  
> esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `DVDAdm.RestoreScreenSaver` método restaura as configurações de proteção de tela do sistema.

``` syntax
DVD.DVDAdm.RestoreScreenSaver()
```

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Em geral, um aplicativo de DVD desabilitará a proteção de tela do sistema na inicialização definindo a propriedade [**DisableScreenSaver**](disablescreensaver-property.md) como true e, em seguida, reabilitará novamente a proteção de tela quando o aplicativo de DVD for fechado chamando `RestoreScreenSaver` . Se um aplicativo não usar as configurações de proteção de tela do sistema, ele não precisará chamar esse método ou definir a propriedade **DisableScreenSaver** .

## <a name="see-also"></a>Confira também

<dl> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



