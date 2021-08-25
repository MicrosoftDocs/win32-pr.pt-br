---
title: Considerações sobre design do servidor de estado
description: Dependendo do design, talvez você precise de um servidor para acompanhar os usuários que estão conectados à rede no momento.
ms.assetid: 2f8d268b-5518-4ad2-aed6-5971c913db6d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b39fa2460fbad5ffedd4a517da588cc0c951f734926c1219d750e28f71734c24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889476"
---
# <a name="state-server-design-considerations"></a>Considerações sobre design do servidor de estado

> [!Note]  
> O IAS (Serviço de Autenticação da Internet) foi renomeado como NPS (Servidor de Políticas de Rede) a partir do Windows Server 2008. O conteúdo deste tópico se aplica a IAS e NPS. Em todo o texto, o NPS é usado para se referir a todas as versões do serviço, incluindo as versões originalmente conhecidas como IAS.

 

Dependendo do design, talvez você precise de um servidor para acompanhar os usuários que estão conectados à rede no momento. O principal desafio com o servidor de estado é manter as informações no banco de dados do servidor de estado em sincronia com quem está realmente conectado. Se as informações no servidor de estado estão fora de sincronia, os usuários podem ter êxito em ter várias sessões quando não estão autorizados a fazer isso. Além disso, os usuários que não têm várias sessões podem ser inadvertidamente prejudicados.

O seguinte deve ser levado em consideração na implementação do servidor de estado:

-   O servidor de estado deve tomar a decisão online em alguns segundos. Por esse motivo, o servidor de estado requer uma infraestrutura escalonável que pode dar suporte a muitas atualizações e consultas por segundo. Bancos de dados relacionais não são apropriados para consultas tão grandes com atualizações simultâneas. Os bancos de dados relacionais são criado principalmente para manter os dados consistentes e fornecer uma exibição consistente dos dados para todos os consumidores. Elas não são criadas para atualizações rápidas.
-   A consistência transacional em atualizações entre vários objetos não é importante. Isso porque o servidor de estado pode tolerar uma pequena janela de oportunidade. No entanto, a consistência transacional de uma única atualização é importante para reduzir as chances de deixar o servidor de estado em um estado inconsistente se um dos servidores RADIUS for desligado no meio da atualização.
-   A persistência (salvar o estado da rede no armazenamento persistente) não é importante porque as informações persistentes sairão rapidamente de sincronia com o estado real da rede.
-   Se o ISDN ou outras formas de multilink têm suporte na rede, o servidor de estado deve ser capaz de lidar com cenários que usam esses recursos.

Um design possível é implementar uma DLL de Extensão de Autenticação e uma DLL de Extensão de Autorização. Cada uma dessas DLLs pode se comunicar pela rede com um banco de dados. A DLL de Extensão de Autorização pode atualizar o banco de dados com informações sobre quem está conectado à rede no momento. A DLL de Extensão de Autenticação pode consultar o banco de dados para obter essas informações para decidir se deve aceitar ou rejeitar a solicitação de autenticação de um usuário específico; se o usuário já estiver conectado, a solicitação será rejeitada.

A vantagem de fazer com que a DLL da Extensão de Autorização atualize o banco de dados do servidor de estado é que a DLL da Extensão de Autorização tem acesso a mais informações sobre o usuário autenticado. A DLL de Extensão de Autorização tem acesso a todos os atributos de autorização do mecanismo de autorização nps. Por exemplo, alguns usuários podem ter autorizações que permitem que eles tenham várias sessões. O servidor de estado deve tratar esses usuários como um caso especial.

 

 




