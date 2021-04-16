---
description: O método DVDAdm. RestoreScreenSaver restaura as configurações de proteção de tela do sistema.
ms.assetid: 606ab850-95bf-4c60-b7cf-e3a94ceee7a7
title: Método RestoreScreenSaver
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b747aa21815bb37cc7db2296347c9890a06914
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105754212"
---
# <a name="restorescreensaver-method"></a>Método RestoreScreenSaver

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

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

 

 



