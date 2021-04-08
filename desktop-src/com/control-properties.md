---
title: Propriedades de controle
description: Propriedades de controle
ms.assetid: 29c2cca3-9460-45d1-9591-026e8c18f26f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4749a7a7e408f6cd58951a72207ed801e4104d65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823010"
---
# <a name="control-properties"></a>Propriedades de controle

Além das propriedades definidas e implementadas pelo próprio controle, a tecnologia controles ActiveX também envolve:

<dl> <dt>

<span id="Ambient_properties"></span><span id="ambient_properties"></span><span id="AMBIENT_PROPERTIES"></span>Propriedades de ambiente
</dt> <dd>

Elas são expostas pelo contêiner por meio de um site do cliente de controle para fornecer valores ambientais que se aplicam a todos os controles inseridos no contêiner. Por exemplo, um contêiner pode fornecer uma cor de plano de fundo padrão ou uma fonte padrão que o controle possa usar. As propriedades de ambiente são expostas por meio de **IDispatch** implementadas no objeto do site de um contêiner. O contêiner chama o método [**IOleControl:: OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) do controle quando qualquer uma de suas propriedades de ambiente altera o valor. Em resposta, um controle pode precisar atualizar seu próprio estado interno ou Visual em resposta. O contêiner indica qual propriedade de ambiente mudou com o parâmetro DISPID ou pode passar DISPID \_ Unknown para indicar que várias propriedades de ambiente foram alteradas.

</dd> <dt>

<span id="Extended_properties"></span><span id="extended_properties"></span><span id="EXTENDED_PROPERTIES"></span>Propriedades estendidas
</dt> <dd>

Na verdade, eles são implementados por um contêiner para encapsular os controles que ele contém para fornecer propriedades gerenciadas por contêiner que aparecem como se fossem Propriedades de controle nativo. O contêiner pode agregar o controle, adicionando as propriedades estendidas para complementar ou substituir as propriedades do controle. O objeto agregado é chamado de controle estendido. Para o contêiner, o controle estendido aparece como o próprio controle e as propriedades estendidas parecem ser expostas pelo controle. O contêiner dá suporte a um controle estendido por meio de seu método de site do cliente [**IOleControlSite:: GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol). O método **GetExtendedControl** permite que os controles naveguem pelo site até o objeto de controle estendido fornecido para eles pelo contêiner, se o contêiner oferecer suporte a esse recurso. Um contêiner também pode optar por mostrar páginas de propriedades para seus controles estendidos, além das páginas que um controle normalmente especificaria por meio de [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages). Por isso, um controle precisa pedir a um contêiner para mostrar um quadro de propriedade antes que o controle tente fazer isso por conta própria. O controle chama [**IOleControlSite:: ShowPropertyFrame**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe) para fazer isso. Se o contêiner implementar essa função, ele mostrará o próprio quadro da propriedade; Se o método retornar um erro, o controle poderá mostrar o quadro de propriedade.

</dd> </dl>

Para mais informações, consulte os seguintes tópicos:

-   [Propriedades padrão](standard-properties.md)
-   [Objeto de fonte padrão](standard-font-object.md)
-   [Objeto de imagem padrão](standard-picture-object.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Métodos de controle](control-methods.md)
</dt> </dl>

 

 




