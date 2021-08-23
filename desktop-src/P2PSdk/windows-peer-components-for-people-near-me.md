---
description: Windows Componentes pares para pessoas ao meu redor
ms.assetid: aa9e7d4d-4131-4578-8bd1-298f04b826f9
title: Windows Componentes pares para pessoas ao meu redor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 762ea58aa9738bfe01e23844dd146e4de8a6a5f76433ef969b60b30fb5886db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011494"
---
# <a name="windows-peer-components-for-people-near-me"></a>Windows Componentes pares para pessoas ao meu redor

no principal Windows executável de rede de pares (P2phost.exe), a [arquitetura pessoas ao meu redor](people-near-me-architecture.md) usa os seguintes componentes:

### <a name="people-near-me"></a>Pessoas ao meu redor

O componente pessoas ao meu redor (PNM) inicia a descoberta usando a descoberta de serviços da Web na sub-rede local para os nomes de usuário dos computadores compatíveis com o PNM.

### <a name="people-near-me-publisher"></a>Pessoas ao meu redor Publisher

o componente pessoas ao meu redor Publisher publica os apelidos dos usuários conectados para indicar a disponibilidade para outros computadores usando o PNM na sub-rede local. O usuário conectado deve optar por publicar seu apelido antes de ser anunciado. O apelido é publicado na sub-rede usando a descoberta de serviços Web. Além disso, objetos e aplicativos também podem ser publicados. No entanto, o usuário deve especificar a publicação de objeto e aplicativo para os escopos '**pessoas ao meu redor**' ou '**todos**'.

### <a name="people-near-me-enumerator"></a>Enumerador pessoas ao meu redor

O componente do enumerador pessoas ao meu redor enumera a lista de usuários na sub-rede local. Usando essa lista, a descoberta de serviços da Web envia uma consulta de multicast e recebe as respostas. Depois que a lista de apelidos é obtida, um aplicativo pode usar a API para recuperar mais dados sendo publicados pelo usuário (que é criptografado usando [Schannel](windows-vista-components-for-people-near-me.md)), como a lista de aplicativos registrados e todos os objetos que estão sendo publicados.

O processo de pesquisa e enumeração não ocorre automaticamente, mas deve ser iniciado explicitamente por um usuário ou um aplicativo entrando no PNM. Os resultados da pesquisa são a lista de apelidos de outros usuários na mesma sub-rede que estão anunciando seus apelidos usando a API do PNM.

### <a name="publication-manager"></a>Gerenciador de publicação

O componente Gerenciador de publicação é responsável por publicar atualizações de presença, aplicativo ou objeto em contatos ou pessoas ao meu redor que são assinadas ou pesquisando dados.

### <a name="peer-signaling"></a>Sinalização de pares

O componente de sinalização de pares lida com a criação de conexões entre os pares para trocar dados. Para pessoas ao meu redor, a sinalização de pares é usada quando um usuário ou aplicativo envia a consulta unicast para um computador específico para sua chave pública, aplicativos e objetos.

### <a name="receive-invitation-handlerux"></a>Receber manipulador de convite/UX

O componente manipulador de convite/UX de recebimento recebe um convite de entrada de outra pessoa, solicita que o usuário determine se deseja iniciar o aplicativo associado ao convite e, em seguida, inicia o aplicativo com base no usuário que está aceitando o convite. Um convite é uma mensagem de outra pessoa para iniciar a atividade de colaboração usando um aplicativo específico que é instalado nos computadores do usuário e é anunciado pelo usuário que está sendo convidado.

### <a name="peer-security"></a>Segurança do par

Quando a presença, o aplicativo e o objeto são enviados, as informações são criptografadas usando um canal SSL ([Schannel](windows-vista-components-for-people-near-me.md)). O computador inicial usa a chave pública do computador convidado para negociar uma chave secreta que é usada para criptografar os dados subsequentes enviados entre os dois pares.

 

 



