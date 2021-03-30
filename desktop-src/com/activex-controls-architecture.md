---
title: Arquitetura de controles ActiveX
description: A tecnologia de controles ActiveX baseia-se em uma base de muitos objetos e interfaces de nível inferior no OLE. As interfaces exatas disponíveis em um controle variam de acordo com seus recursos. Esta seção examina mais detalhadamente os recursos que um controle pode fornecer.
ms.assetid: 42959a11-8bfb-4f7e-ba27-5dc1ed49cdaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0592d774e1930623803d0769fb7890709a2f21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635586"
---
# <a name="activex-controls-architecture"></a>Arquitetura de controles ActiveX

A tecnologia de controles ActiveX baseia-se em uma base de muitos objetos e interfaces de nível inferior no OLE. As interfaces exatas disponíveis em um controle variam de acordo com seus recursos. Esta seção examina mais detalhadamente os recursos que um controle pode fornecer.

Os controles ActiveX são usados para fornecer os blocos de construção para a criação de interfaces de usuário em aplicativos. Por exemplo, um botão que inicia alguma ação no aplicativo de contêiner quando ele é clicado é um controle simples. Os seguintes aspectos estão envolvidos no fornecimento desses blocos de construção de interface do usuário:

-   Um controle pode ser inserido em seu cliente de contêiner para dar suporte a alguma atividade de interface do usuário no cliente. Assim, um controle precisa fornecer uma representação visual de si mesmo quando ele é inserido no contêiner e precisa fornecer uma maneira de salvar seu estado, por exemplo, seus valores de propriedade e sua posição dentro de seu contêiner. O cliente deve oferecer suporte a um contêiner com objetos inseridos nele.
-   Ao ativar o controle usando um teclado ou mouse, o usuário final inicia alguma ação no aplicativo cliente. Portanto, um controle deve responder à atividade de teclado e deve ser capaz de se comunicar com seu cliente para que ele possa notificar seu contêiner de suas atividades e disparar eventos no cliente.
-   O cliente normalmente também fornece uma linguagem de programação por meio da qual o usuário final pode iniciar ações fornecidas pelas propriedades e métodos do controle. Portanto, um controle deve dar suporte à automação e a algum conjunto de recursos de tempo de design versus tempo de execução também.

Como resultado de sua função no fornecimento de blocos de construção de interface do usuário, um controle normalmente dá suporte a recursos nas seguintes áreas usando as tecnologias OLE, conforme indicado:

<dl> <dt>

<span id="Properties_and_methods"></span><span id="properties_and_methods"></span><span id="PROPERTIES_AND_METHODS"></span>Propriedades e métodos
</dt> <dd>

Como qualquer objeto OLE, um controle pode fornecer grande parte de sua funcionalidade por meio de um conjunto de interfaces de entrada com propriedades e métodos. O contêiner pode fornecer propriedades de ambiente adicionais e pode dar suporte à extensão das propriedades do controle por meio de agregação. Esses recursos são REST na automação OLE, páginas de propriedades, objetos conectáveis e tecnologias de controle ActiveX.

</dd> <dt>

<span id="Events"></span><span id="events"></span><span id="EVENTS"></span>LostFocus
</dt> <dd>

Além de fornecer propriedades e métodos, um controle ActiveX também pode fornecer interfaces de saída para notificar seu cliente de eventos. O cliente deve dar suporte ao tratamento desses eventos. Esses recursos usam a automação OLE e objetos conectáveis.

</dd> <dt>

<span id="Visual_representation"></span><span id="visual_representation"></span><span id="VISUAL_REPRESENTATION"></span>Representação visual
</dt> <dd>

Um controle pode dar suporte ao posicionamento e à exibição em seu contêiner. O contêiner posiciona o controle e determina seu tamanho. Esses recursos usam tecnologia de documento composto, incluindo tecnologia de arrastar e soltar OLE.

</dd> <dt>

<span id="Keyboard_handling"></span><span id="keyboard_handling"></span><span id="KEYBOARD_HANDLING"></span>Manuseio de teclado
</dt> <dd>

Um controle pode responder a aceleradores de teclado para que o usuário final possa iniciar ações executadas pelo controle. O contêiner gerencia a atividade de teclado para todos os seus controles inseridos. Esses recursos usam tecnologias de controle e documento composto.

</dd> <dt>

<span id="Persistence"></span><span id="persistence"></span><span id="PERSISTENCE"></span>Persistência
</dt> <dd>

Um controle pode salvar seu estado. O cliente gerencia a persistência de seus controles inseridos. Esses recursos usam tecnologias de armazenamento estruturado e de persistência de objeto.

</dd> <dt>

<span id="Registration_and_licensing"></span><span id="registration_and_licensing"></span><span id="REGISTRATION_AND_LICENSING"></span>Registro e licenciamento
</dt> <dd>

Um controle normalmente dá suporte a Autoregistro e cria um conjunto de entradas do registro quando ele é instanciado. Um controle também pode ser licenciado para ajudar a evitar o uso não autorizado.

</dd> </dl>

A maioria desses recursos envolve o controle e seu contêiner de cliente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controles ActiveX](activex-controls.md)
</dt> </dl>

 

 




