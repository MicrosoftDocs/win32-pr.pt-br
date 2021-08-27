---
title: Propriedades de ambiente para controles
description: Propriedades de ambiente para controles
ms.assetid: 19aa3bc2-1605-43e1-acf4-ab782d012539
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 421a643873e818d8f5c0e006b4bb9049c1230c5f4e18525cdf7ed2b4175797bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994056"
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

 

 





