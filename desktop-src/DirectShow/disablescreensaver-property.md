---
description: A propriedade DVDAdm. DisableScreenSaver ativa ou desativa a proteção de tela do sistema.
ms.assetid: 78a0512f-456a-45b6-8717-13593461a765
title: Propriedade DisableScreenSaver
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bc714dbbdc3e9b144f2d49cb54871cdf09baad5df39f8e18b962d7fc415d44a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821124"
---
# <a name="disablescreensaver-property"></a>Propriedade DisableScreenSaver

> [!Note]  
> esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `DVDAdm.DisableScreenSaver` propriedade ativa ou desativa a proteção de tela do sistema.

``` syntax
[ bDisabled = ] DVD.DVDAdm.DisableScreenSaver
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor booliano que indica se as configurações de proteção de tela do sistema estão desabilitadas para o aplicativo de DVD Player; verdadeiro significa que as configurações estão desabilitadas.

## <a name="remarks"></a>Comentários

Essa propriedade é de leitura/gravação com um valor padrão de true. Ao exibir um disco DVD-Video, um usuário normalmente não usa o mouse ou o teclado por longos períodos de tempo. o MSWebDVD ActiveX® controle, portanto, desabilita a proteção de tela do sistema por padrão. Objeto

## <a name="see-also"></a>Confira também

<dl> <dt>

[**RestoreScreenSaver**](restorescreensaver-method.md)
</dt> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



