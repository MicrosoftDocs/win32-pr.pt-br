---
description: A TAPI 3,1 apresenta controles de telefone baseados em COM. Presume-se familiaridade com COM, automação OLE e scripts, como conhecimento do modelo de objeto TAPI 3. O conhecimento das funções de controle de telefone TAPI 2 também é útil.
ms.assetid: e56aef54-e358-429b-9f0f-c8776507d95f
title: Controle de telefone e o objeto de telefone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e9344d54a63efcf1692af361a5f8e88121981e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779302"
---
# <a name="phone-control-and-the-phone-object"></a>Controle de telefone e o objeto de telefone

A TAPI 3,1 apresenta controles de telefone baseados em COM. Presume-se familiaridade com COM, automação OLE e scripts, como conhecimento do modelo de objeto TAPI 3. O conhecimento das funções de controle de telefone TAPI 2 também é útil.

O controle de telefone é implementado em três níveis de recursos, cada um deles com base no anterior:

-   Objeto de telefone. O primeiro nível define como os dispositivos de telefone da TAPI 2. x (APIs, constantes e mensagens que começam com "Phone") são expostos no modelo de objeto TAPI 3,1. Isso envolve um novo objeto de telefone exposto da TAPI 3,1, com [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone) como a interface padrão no novo objeto. A interface **ITPhone** , junto com suas constantes associadas, tipos enumerados e eventos, geralmente expõe o mesmo nível de detalhes e funcionalidades das funções, constantes, estruturas e mensagens da TAPI 2. x, que começam com a palavra "telefone". Esse nível também envolve novas interfaces em vários objetos TAPI 3. x existentes para facilitar a criação de objetos de telefone e a associação de objetos de telefone com outros objetos aos quais eles estão relacionados.
-   Controle de telefone automatizado e tratamento de chamadas. O segundo nível consiste em uma interface adicional chamada [**ITAutomatedPhoneControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol) e suas constantes associadas, tipos enumerados e eventos. Essa é uma interface secundária no objeto do telefone. Se o dispositivo de telefone tiver sido aberto com o privilégio de proprietário, use o método **QueryInterface** na interface [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone) para obter um ponteiro de interface **ITAutomatedPhoneControl** .
-   Discagem de telefone do Windows 2000. O terceiro nível consiste em alterações no aplicativo de discagem de telefone do Windows 2000 para implementar interações de usuário específicas.

Os desenvolvedores da Microsoft ou de terceiros podem usar o modelo de objeto TAPI 3,1 para implementar aplicativos ou serviços mais avançados que envolvem telefones, incluindo um serviço que permite que os aparelhos USB (barramento serial universal), por exemplo, sejam usados para chamadas telefônicas, mesmo que nenhum usuário esteja conectado e nenhum outro aplicativo TAPI tenha sido iniciado explicitamente.

No TAPI 3,0, um telefone MSP tentou melhorar os dispositivos de telefone associados às linhas usadas para chamadas TAPI 3,0. Este desenvolvimento destina-se a dar suporte a modems com viva-voz alternados por software. Os aplicativos TAPI 3,1 que usam esse tipo de modem devem usar os objetos de telefone TAPI 3,1 para manipular o estado de Hookswitch do modem.

Para obter mais informações e uma lista de todas as interfaces associadas ao objeto de telefone, consulte [interfaces de objeto de telefone](phone-object-interfaces.md). As interfaces de controle de telefone expõem métodos que permitem o controle de conjuntos de telefone usando COM.

 

 



