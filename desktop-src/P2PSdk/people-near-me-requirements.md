---
description: Pessoas ao meu Redor requisitos
ms.assetid: c7ab73fc-56a6-4b6c-820a-3f8e4a97cfaf
title: Pessoas ao meu Redor requisitos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ebbb904175184b6e9d06c807aa4b4ed645c93633114d6b9b64085e34dfa3683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518346"
---
# <a name="people-near-me-requirements"></a>Pessoas ao meu Redor requisitos

Para que o [Pessoas ao meu Redor](about-people-near-me.md) forneça conectividade perfeita e colaboração fácil para os usuários para Windows de rede par, o seguinte é feito:

### <a name="people-discovery"></a>Descoberta de Pessoas

A Descoberta de Pessoas permite que um usuário descubra e exibe o conjunto de pares localizados na sub-rede local. Todos os computadores na sub-rede local devem anunciar os nomes dos pares conectados. Os pares listados após uma consulta de descoberta são o conjunto de usuários que executam o Windows Vista configurado para anunciar um apelido para outros usuários usando Pessoas ao meu Redor [.](about-people-near-me.md) Essa funcionalidade é desabilitada por padrão e deve ser habilitada pelo usuário conectado.

> [!Note]  
> Os pares remotos descobertos durante o processo Pessoas ao meu Redor descoberta "Pessoas ao meu Redor" não são necessariamente os usuários previstos associados aos pares descobertos.

 

### <a name="extended-data-discovery"></a>Descoberta de Dados Estendida

A Descoberta de Dados Estendida permite pesquisas de usuários que têm interesses específicos. Também é possível que os usuários especifiquem que querem anunciar dados adicionais sobre si mesmos. Por exemplo, os dados podem delinear interesses profissionais específicos em uma conferência do setor, além do apelido do usuário conectado.

### <a name="application-discovery"></a>Descoberta de Aplicativo

A natureza exata da colaboração ad hoc habilitada pelo Pessoas ao meu Redor é específica para aplicativos. Por exemplo, a colaboração pode estar conversando ou compartilhando fotos, exigindo aplicativos específicos. Para que Pessoas ao meu Redor habilitar atividades de colaboração, o conjunto de aplicativos que estão disponíveis para Pessoas ao meu Redor cenários também deve ser anunciado e descobrivel.

### <a name="subscription"></a>Subscription

Usando uma assinatura, os aplicativos podem assinar para acompanhar a presença, os aplicativos e as alterações de objeto de uma pessoa.

### <a name="invitation"></a>Convite

Depois que as pessoas, os interesses e os aplicativos são descobertos, a colaboração ponto a ponto, usando um aplicativo Pessoas ao meu Redor, pode iniciar uma troca de convite e aceitação. O par iniciador envia uma mensagem de convite para outro par ou par. Os usuários que recebem o convite podem aceitar ou recusar o convite. Quando o convite é aceito, o aplicativo par apropriado para a atividade solicitada é lançado.

### <a name="add-as-a-contact"></a>Adicionar como um contato

Se os usuários estabelecerem uma atividade de colaboração por meio Pessoas ao meu Redor e quiserem manter o contato ao longo do tempo, eles poderão adicionar uns aos outros como um contato. Depois que isso for feito, eles poderão observar o status de presença de um usuário (como online, offline ou fora) e convidar para uma atividade de colaboração a qualquer momento pela Internet. Qualquer atividade que foi possível com a pessoa quando ela estava localizada nas proximidades também é possível com um contato pela Internet.

### <a name="security"></a>Segurança

Para proteger os usuários e os dados que estão sendo trocados em uma atividade de colaboração par, os usuários têm controle de configuração sobre o que está sendo anunciado. Os usuários também devem aceitar um convite antes que a colaboração de pares possa começar. A atividade de colaboração é criptografada com um canal criptografado por protocolo SSL (SSL) (também conhecido como Schannel). SSL é um protocolo criptográfico para proteger comunicações baseadas em TCP. Para obter mais informações, consulte [SChannel](windows-vista-components-for-people-near-me.md). Esses requisitos são suportados por um novo conjunto de componentes na [arquitetura Windows rede](what-is-peer-networking-.md)par no Windows Vista.

 

 



