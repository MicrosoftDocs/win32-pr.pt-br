---
title: Recomendações de implantação de RPC sobre HTTP
description: Esta seção documenta as práticas recomendadas e as configurações de implantação recomendadas para alcançar a segurança e o desempenho máximos ao usar RPC sobre HTTP.
ms.assetid: 83938a7d-77d0-45e8-b0a3-7b32ef768d83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8871686d1fc8b87bcd6fb7ac4314b1977252f23a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005975"
---
# <a name="rpc-over-http-deployment-recommendations"></a>Recomendações de implantação de RPC sobre HTTP

Esta seção documenta as práticas recomendadas e as configurações de implantação recomendadas para alcançar a segurança e o desempenho máximos ao usar RPC sobre HTTP. As várias configurações encontradas aqui se aplicam a diferentes organizações com base em vários requisitos de tamanho, orçamento e segurança. Cada configuração também fornece considerações de implantação úteis para determinar qual é a melhor para um determinado cenário.

Para obter informações sobre cenários de RPC sobre HTTP em grande volume, consulte [balanceamento de carga do Microsoft RPC](rpc-load-balancing.md).

As seguintes recomendações se aplicam a todas as configurações:

-   Use versões do Windows que dão suporte a RPC sobre HTTP v2.
-   Coloque o IIS no computador que executa o proxy RPC no modo IIS 6,0.
-   Não permitir acesso anônimo ao diretório virtual do proxy RPC.
-   Nunca habilite a chave do registro AllowAnonymous.
-   Faça com que seus clientes RPC sobre HTTP usem o **CertificateSubjectField** (consulte [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) para obter mais informações) para verificar se o proxy RPC ao qual você se CONECTOU é o proxy RPC que você espera.
-   Configure a chave do registro **ValidPorts** para conter somente computadores aos quais os clientes RPC sobre http serão conectados.
-   Não use curingas na chave **ValidPorts** ; Isso pode economizar tempo, mas um computador completamente inesperado também pode se ajustar ao curinga.
-   Use SSL em clientes RPC sobre HTTP. Se as diretrizes estabelecidas nessas seções forem seguidas, o cliente RPC sobre HTTP não poderá se conectar sem usar SSL.
-   Configure o RPC sobre clientes HTTP para usar a criptografia RPC, além de usar SSL. Se o cliente RPC sobre HTTP não puder acessar o KDC, ele só poderá usar Negotiate e NTLM.
-   Configure computadores cliente para usar o NTLMv2. Defina a chave do registro **LmCompatibilityLevel** como 2 ou superior. Consulte **msdn.Microsoft.com** para obter mais informações sobre a chave **LmCompatibilityLevel** .
-   Execute um web farm de máquinas de proxy RPC com a configuração descrita acima.
-   Implante um firewall entre a Internet e o proxy RPC.
-   Para obter um desempenho ideal, configure o IIS para enviar uma breve resposta para códigos de erro que não são bem-sucedidos. Como o consumidor da resposta do IIS é um processo automatizado, não há necessidade de que as explicações amigáveis do usuário sejam enviadas ao cliente; Eles serão simplesmente ignorados pelo cliente RPC sobre HTTP.

Os objetivos básicos do proxy RPC de uma perspectiva de segurança, desempenho e capacidade de gerenciamento são os seguintes:

-   Forneça um único ponto de entrada para tráfego RPC sobre HTTP na rede do servidor. Ter um único ponto de entrada para tráfego RPC sobre HTTP em uma rede de servidor tem dois benefícios principais. Primeiro, como o proxy RPC está voltado para a Internet, a maioria das organizações isola essas máquinas em uma rede especial chamada rede de perímetro não confiável, que é separada da rede organizacional normal. Os servidores em uma rede de perímetro não confiável são gerenciados com muito cuidado, configurados e monitorados para poder resistir a ataques da Internet. Quanto menos computadores em uma rede de perímetro não confiável, mais fácil é configurar, gerenciar, monitorar e mantê-los seguros. Em segundo lugar, como um único Web farm com proxies RPC instalados pode atender a qualquer número de servidores RPC sobre HTTP que residem na rede corporativa, faz muito sentido separar o proxy RPC do servidor RPC sobre HTTP e fazer com que o proxy RPC resida em uma rede de perímetro não confiável. Se o proxy RPC estava no mesmo computador que o servidor RPC sobre HTTP, as organizações seriam forçadas a colocar todos os seus servidores back-end em uma rede de perímetro não confiável, o que tornaria muito mais difícil manter a rede de perímetro não confiável segura. A separação da função do proxy RPC e do servidor RPC sobre HTTP ajuda as organizações a manter o número de máquinas em uma rede de perímetro não confiável gerenciável e, portanto, mais segura.
-   Serve como um fusível de segurança para a rede do servidor. O proxy RPC é projetado como um fusível ininteligível para a rede do servidor – se algo der errado no proxy RPC, ele simplesmente irá para a proteção e, portanto, protegerá o verdadeiro servidor RPC sobre HTTP. Se as práticas recomendadas descritas nesta seção tiverem sido seguidas até agora, o tráfego RPC sobre HTTP é criptografado com a criptografia RPC, além do SSL. A criptografia de RPC em si é entre o cliente e o servidor, não entre o cliente e o proxy. Isso significa que o proxy não entende e não pode descriptografar o tráfego RPC recebido. Ele só entende algumas sequências de controle enviadas a ele pelo cliente lidando com o estabelecimento de conexão, controle de fluxo e outros detalhes de túnel. Ele não tem acesso aos dados que o cliente RPC sobre HTTP envia para o servidor. Além disso, o cliente RPC sobre HTTP deve autenticar de forma independente o proxy RPC e o servidor RPC sobre HTTP. Isso proporciona defesa profunda. Se o computador proxy RPC for comprometido, devido a algum erro de configuração ou uma violação de segurança de algum tipo, os dados que passam por ele ainda estarão protegidos contra violação. Um invasor que obteria o controle do proxy RPC pode, no máximo, interromper o tráfego, mas não lê-lo nem adulterar isso. É aí que a função de fusível do proxy RPC entra em cena – ela é inútil sem que a segurança do tráfego RPC sobre HTTP seja comprometida.
-   Distribua algumas das verificações de acesso e o trabalho de descriptografia entre vários computadores que executam o proxy RPC em um Web farm. Ao funcionar bem em um Web farm, o proxy RPC permite que as organizações descarreguem a descriptografia de SSL e algumas das verificações de acesso, liberando assim mais capacidade no servidor back-end para processamento. O uso de um Web farm de máquinas proxy RPC também permite que uma organização aumente sua capacidade de resistir a ataques de DoS (negação de serviço) aumentando a capacidade em seus servidores front-end.

Nas diretrizes definidas até agora, as organizações ainda têm opções. Cada organização tem opções e comprometimentos entre a inconveniência do usuário, a segurança e o custo:

-   **Usar autenticação básica ou autenticação integrada do Windows para autenticar no proxy RPC?** O RPC sobre HTTP atualmente dá suporte apenas a NTLM – ele não dá suporte a Kerberos. Além disso, se houver um proxy HTTP ou um firewall entre o cliente RPC sobre HTTP e o proxy RPC que insere o *por meio* do pragma no cabeçalho HTTP, a autenticação NTLM não funcionará. Quando esse não for o caso, as organizações poderão escolher entre a autenticação básica e NTLM. A vantagem da autenticação básica é que ela é mais rápida e simples e, portanto, oferece menos oportunidades para ataques de negação de serviço. Mas o NTLM é mais seguro. Dependendo das prioridades de uma organização, ele pode escolher básico, NTLM ou permitir que seus usuários escolham entre os dois. Se apenas um for escolhido, será melhor desativar o outro do diretório virtual do proxy RPC para reduzir o risco de ataque.
-   **Usar o mesmo conjunto de credenciais para o proxy RPC e o servidor RPC sobre HTTP, ou usar credenciais diferentes para cada um?** A compensação para essa decisão é entre a conveniência e a segurança do usuário. Poucos usuários gostam de inserir várias credenciais. No entanto, se ocorrer uma violação de segurança em uma rede de perímetro não confiável, ter conjuntos de credenciais separados para o proxy RPC e o servidor RPC sobre HTTP fornece proteção adicional. Observe que, se credenciais separadas forem usadas e um conjunto de credenciais for as credenciais de domínio do usuário, é aconselhável usar as credenciais de domínio do usuário para o servidor RPC sobre HTTP e não para o proxy RPC.

 

 




