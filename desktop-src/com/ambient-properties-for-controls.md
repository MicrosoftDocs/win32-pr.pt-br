---
title: Propriedades de ambiente para controles
description: Propriedades de ambiente para controles
ms.assetid: 19aa3bc2-1605-43e1-acf4-ab782d012539
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e166a7186021b53798150968c9998fed243de00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364121"
---
# <a name="ambient-properties-for-controls"></a>Propriedades de ambiente para controles

Se um controle oferecer suporte a todas as propriedades de ambiente, ele deverá pelo menos respeitar os valores das seguintes propriedades de ambiente nas condições indicadas na tabela a seguir usando os DISPIDs padrão.



| Propriedade de ambiente            | DISPID          | Comentário/condições para uso                                                                                                                                                                                                                                                                |
|-----------------------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LocaleID<br/>         | -705<br/> | Se a localidade for significativa para o controle, por exemplo, para saída de texto<br/>                                                                                                                                                                                                                  |
| Modo <br/>        | -709<br/> | Se o controle se comporta de forma diferente no modo de usuário (Design) e no modo de execução<br/>                                                                                                                                                                                                          |
| UIDead<br/>           | -710<br/> | Se o controle reage a eventos de interface do usuário, ele deve honrar essa propriedade de ambiente<br/>                                                                                                                                                                                                 |
| ShowGrabHandles<br/>  | -711<br/> | Se o controle suportar o redimensionamento in-loco de si mesmo<br/>                                                                                                                                                                                                                             |
| Deshachurando<br/>     | -712<br/> | Se o controle oferecer suporte à ativação in-loco e à ativação da interface do usuário<br/>                                                                                                                                                                                                                   |
| DisplayAsDefault<br/> | -713<br/> | Somente se o controle estiver marcado como OLEMISC \_ ACTSLIKEBUTTON (o que significa que o suporte para mnemônicos de teclado é fornecido, portanto, [**IOleControl:: GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) e [**IOleControl:: onmnemônico**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) deve ser implementado).<br/> |



 

Conforme descrito anteriormente, o uso de ambientes requer [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) (para [**OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) como um mínimo), bem como [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) (para [**SetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setclientsite) e [**GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite)).

O OLEMISC \_ SETCLIENTSITEFIRST bit pode não ser necessariamente suportado por um contêiner. Nessas circunstâncias, um controle deve recorrer aos valores padrão para as propriedades de ambiente que ele requer.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controles](controls.md)
</dt> </dl>

 

 





