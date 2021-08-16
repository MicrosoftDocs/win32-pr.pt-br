---
description: Implementa as interfaces IAxiService e IeAxiServiceCallback.
ms.assetid: 39f2ee3a-d4fd-4091-acd6-3d6b715bea75
title: Objeto CIeAxiInstallerService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIeAxiInstallerService
api_type:
- COM
api_location: ''
ms.openlocfilehash: d8e96600762db414fa93316098d5ba87dabfbc3138f516d3d69f1740d0d33d2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783082"
---
# <a name="cieaxiinstallerservice-object"></a>Objeto CIeAxiInstallerService

O objeto **CIeAxiInstallerService** implementa as interfaces [**IAxiService**](ieaxiservice.md) e [**IeAxiServiceCallback**](ieaxiservicecallback.md) .

Este objeto não é declarado em um cabeçalho público. Os aplicativos devem defini-lo por conta própria. O fragmento IDL (Interface Definition Language) a seguir descreve esse objeto, incluindo seu CLSID.

``` syntax
[
        uuid(90F18417-F0F1-484E-9D3C-59DCEEE5DBD8)
]
    coclass CIeAxiInstallerService
    {
        [default] interface IeAxiService;
        interface IeAxiServiceCallback;
    }

```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows vista Business, Windows vista Enterprise, \[ somente os aplicativos de área de trabalho do Windows vista Ultimate\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAxiService**](ieaxiservice.md)
</dt> <dt>

[**IeAxiServiceCallback**](ieaxiservicecallback.md)
</dt> </dl>

 

 




