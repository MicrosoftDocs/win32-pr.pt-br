---
description: Requisitos de pessoas ao meu redor
ms.assetid: c7ab73fc-56a6-4b6c-820a-3f8e4a97cfaf
title: Requisitos de pessoas ao meu redor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6afb97800041e0fcd9a10a6d95334b832fb363
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828404"
---
# <a name="people-near-me-requirements"></a>Requisitos de pessoas ao meu redor

Para que [as pessoas ao meu redor](about-people-near-me.md) forneçam conectividade direta e fácil colaboração aos usuários para aplicativos de rede de mesmo nível do Windows, o seguinte é feito:

### <a name="people-discovery"></a>Descoberta de pessoas

A descoberta de pessoas permite que um usuário descubra e exiba o conjunto de pares que estão localizados na sub-rede local. Todos os computadores na sub-rede local devem anunciar os nomes dos pares conectados. Os pares listados após uma consulta de descoberta são o conjunto de usuários que executam o Windows Vista que são configurados para anunciar um apelido para outros usuários usando [pessoas ao meu redor](about-people-near-me.md). Esse recurso está desabilitado por padrão e deve ser habilitado pelo usuário conectado.

> [!Note]  
> Os pares remotos descobertos durante o processo de descoberta ' pessoas ao meu redor ' não são necessariamente os usuários previstos associados aos pares descobertos.

 

### <a name="extended-data-discovery"></a>Descoberta de dados estendidos

A descoberta de dados estendidos permite pesquisas de usuários que têm interesses específicos. Também é possível que os usuários especifiquem que desejam anunciar dados adicionais sobre eles mesmos. Por exemplo, os dados podem descrever interesses profissionais específicos em uma conferência do setor, além do apelido do usuário conectado.

### <a name="application-discovery"></a>Descoberta de aplicativos

A natureza exata da colaboração ad hoc habilitada por pessoas ao meu redor é específica para aplicativos. Por exemplo, a colaboração pode estar batendo ou compartilhando fotos, ambos exigindo aplicativos específicos. Para que as pessoas ao meu redor habilitem atividades de colaboração, o conjunto de aplicativos que estão disponíveis para cenários de pessoas ao meu redor também deve ser anunciado e detectável.

### <a name="subscription"></a>Assinatura

Usando uma assinatura, os aplicativos podem assinar para rastrear a presença, os aplicativos e as alterações de objetos de uma pessoa.

### <a name="invitation"></a>Convite

Depois que as pessoas, os interesses e os aplicativos forem descobertos, a colaboração do mesmo nível, usando um aplicativo pessoas ao meu redor, poderá começar um convite e uma troca de aceitação. O ponto de inicialização envia uma mensagem de convite para outro par ou pares. Os usuários que recebem o convite podem aceitar ou recusar o convite. Quando o convite for aceito, o aplicativo par apropriado para a atividade solicitada será iniciado.

### <a name="add-as-a-contact"></a>Adicionar como um contato

Se os usuários estabelecerem uma atividade de colaboração por meio de pessoas ao meu redor e quiserem manter contato ao longo do tempo, eles poderão adicionar um ao outro como um contato. Depois que isso for feito, eles poderão observar o status de presença de um usuário (como online, offline ou ausente) e convidá-los para uma atividade de colaboração a qualquer momento pela Internet. Qualquer atividade que fosse possível com a pessoa quando ela estava localizada próxima também é possível com um contato pela Internet.

### <a name="security"></a>Segurança

Para proteger os usuários e os dados que estão sendo trocados em uma atividade de colaboração de pares, os usuários têm controle de configuração sobre o que está sendo anunciado. Os usuários também devem aceitar um convite antes que a colaboração de mesmo nível possa começar. A atividade de colaboração é criptografada com um canal criptografado por protocolo SSL (SSL) (também conhecido como Schannel). O SSL é um protocolo criptográfico para proteger as comunicações baseadas em TCP. Para obter mais informações, consulte [Schannel](windows-vista-components-for-people-near-me.md). Esses requisitos têm suporte de um novo conjunto de componentes na arquitetura de [rede de sistemas pares do Windows](what-is-peer-networking-.md)no Windows Vista.

 

 



