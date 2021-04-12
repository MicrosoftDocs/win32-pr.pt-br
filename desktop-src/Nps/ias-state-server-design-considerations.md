---
title: Considerações de design de servidor de estado
description: Dependendo do seu design, você pode precisar de um servidor para controlar os usuários que estão conectados à rede no momento.
ms.assetid: 2f8d268b-5518-4ad2-aed6-5971c913db6d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0ef654f3641138075acc667d733b20c94c4840
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364238"
---
# <a name="state-server-design-considerations"></a>Considerações de design de servidor de estado

> [!Note]  
> O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008. O conteúdo deste tópico aplica-se ao IAS e ao NPS. Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.

 

Dependendo do seu design, você pode precisar de um servidor para controlar os usuários que estão conectados à rede no momento. O principal desafio com o servidor de estado é manter as informações no banco de dados do servidor de estado em sincronia com quem está realmente conectado. Se as informações no servidor de estado estiverem fora de sincronia, os usuários poderão ter sucesso em ter várias sessões quando não estiverem autorizados a fazer isso. Além disso, os usuários que não têm várias sessões podem ser penalizados inadvertidamente.

O seguinte deve ser levado em consideração na implementação do servidor de Estado:

-   O servidor de Estado deve tomar a decisão online em alguns segundos. Por esse motivo, o servidor de Estado requer uma infraestrutura escalonável que possa dar suporte a muitas atualizações e consultas por segundo. Os bancos de dados relacionais não são apropriados para consultas grandes com atualizações simultâneas. Os bancos de dados relacionais são criados principalmente para manter o dado consistente e fornecer uma exibição consistente dos dados a todos os consumidores. Eles não são criados para atualizações rápidas.
-   A consistência transacional em atualizações entre vários objetos não é importante. Isso ocorre porque o servidor de estado pode tolerar uma pequena janela de oportunidade. No entanto, a consistência transacional de uma única atualização é importante para reduzir as chances de deixar o servidor de estado em um estado inconsistente se um dos servidores RADIUS for desligado no meio da atualização.
-   A persistência (salvar o estado da rede para o armazenamento persistente) não é importante porque as informações persistentes ficarão rapidamente fora de sincronia com o estado real da rede.
-   Se houver suporte para ISDN ou outras formas de multilink na rede, o servidor de estado deverá ser capaz de lidar com cenários que usam esses recursos.

Um design possível é implementar uma DLL de extensão de autenticação e uma DLL de extensão de autorização. Cada uma dessas DLLs pode se comunicar pela rede com um banco de dados. A DLL de extensão de autorização pode atualizar o banco de dados com informações sobre quem está conectado à rede no momento. A DLL de extensão de autenticação pode consultar o banco de dados para que essas informações decidam se deseja aceitar ou rejeitar a solicitação de autenticação de um usuário específico; Se o usuário já estiver conectado, a solicitação será rejeitada.

A vantagem de ter a DLL de extensão de autorização atualizar o banco de dados de servidor de estado é que a DLL de extensão de autorização tem acesso a mais informações sobre o usuário autenticado. A DLL de extensão de autorização tem acesso a todos os atributos de autorização do mecanismo de autorização do NPS. Por exemplo, alguns usuários podem ter autorizações que permitam ter várias sessões. O servidor de Estado deve tratar tais usuários como um caso especial.

 

 




