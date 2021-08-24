---
description: O provedor de serviços NLA (reconhecimento de local de rede) é vital para computadores ou dispositivos que podem ser movidos entre redes diferentes e para a seleção de configurações ideais quando há mais de uma disponível.
ms.assetid: 307f384d-e59a-4fc5-8f6a-ed81a102df60
title: A função de NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f44d517fc9f32d4fb61eb2b4d9b61c473bc946066e670fcb51f0ca2c753e692
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733336"
---
# <a name="the-role-of-nla"></a>A função de NLA

O provedor de serviços NLA (reconhecimento de local de rede) é vital para computadores ou dispositivos que podem ser movidos entre redes diferentes e para a seleção de configurações ideais quando há mais de uma disponível. Por exemplo, um roaming de computador sem fio entre redes físicas pode usar NLA para determinar a configuração adequada com base nas informações sobre sua conexão de rede disponível. A NLA também comprova valioso quando um computador com hospedagem múltipla tem uma conexão física com uma rede, enquanto também está conectado a outra rede por meio de uma conexão discada ou de um túnel.

No passado, os desenvolvedores tinham que obter informações sobre uma interface de rede lógica e, portanto, tomar decisões sobre a conectividade de rede, com base em uma infinidade de informações de rede diferentes. Nessas circunstâncias, os desenvolvedores tinham que escolher a interface de rede apropriada com base no endereço IP, a sub-rede da interface, o nome DNS (sistema de nomes de domínio) associado à interface, o endereço MAC de uma NIC, um nome de rede sem fio ou outras informações de rede. O NLA alivia esse problema fornecendo uma interface padrão para enumerar informações de anexo de rede lógica, correlacioná-las com informações de interface de rede física e, em seguida, fornecer notificação quando as informações retornadas anteriormente forem invalidadas.

O NLA fornece as seguintes informações de local de rede:

<dl> <dt>

<span id="Logical_Network_Identity"></span><span id="logical_network_identity"></span><span id="LOGICAL_NETWORK_IDENTITY"></span>Identidade de rede lógica
</dt> <dd>

A NLA tenta primeiro identificar uma rede lógica por seu nome de domínio DNS. Se uma rede lógica não tiver um nome de domínio, a NLA identificará a rede de informações estáticas personalizadas armazenadas no registro e, por fim, do seu endereço de sub-rede.

</dd> <dt>

<span id="Logical_Network_Interfaces"></span><span id="logical_network_interfaces"></span><span id="LOGICAL_NETWORK_INTERFACES"></span>Interfaces de rede lógica
</dt> <dd>

Para cada rede à qual um computador está conectado, a NLA fornece um *adaptadorname* que identifica exclusivamente uma interface física, como uma NIC, ou uma interface lógica, como uma conexão RAS. O Adaptadorname pode ser usado com funções disponíveis na API do auxiliar de IP para obter características de interface adicionais.

</dd> </dl>

A NLA implementa a rede lógica como uma classe de serviço, com uma GUID de classe e propriedades associadas. Cada rede lógica para a qual a NLA retorna informações é uma instância dessa classe de serviço.

 

 



