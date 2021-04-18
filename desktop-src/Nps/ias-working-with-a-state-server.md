---
title: Trabalhando com um servidor de estado
description: O NPS executa a autenticação usando um banco de dados configurado no site do servidor NPS.
ms.assetid: 8313ba91-5ed1-44d0-80db-cfb82c641100
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d79ff46802d53109c7bb8b40fe3a2db2480949e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105760406"
---
# <a name="working-with-a-state-server"></a>Trabalhando com um servidor de estado

> [!Note]  
> O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008. O conteúdo deste tópico aplica-se ao IAS e ao NPS. Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.

 

O NPS executa a autenticação usando um banco de dados configurado no site do servidor NPS. Esse banco de dados de autenticação pode ser o banco de dados do usuário para um domínio do Windows ou pode ser desenhado sobre as informações do usuário obtidas do Windows Active Directory. O diagrama a seguir ilustra uma configuração típica que mostra como o NPS interage com bancos de dados de autenticação como, por exemplo, um usuário de domínio do Windows ou Active Directory. O diagrama também mostra como o NPS pode interagir com um servidor de estado que é fornecido por terceiros. A principal finalidade de um servidor de estado é limitar o número de sessões de logon simultâneas que um único usuário pode executar.

![NPS interagindo com servidor de estado e bancos de dados de autenticação](images/ias02.png)

Há dois pontos de interação entre o NPS e o servidor de estado. Ocorre uma interação quando o NPS recebe uma solicitação de autenticação do NAS. O servidor de estado fornece informações de seu banco de dados para determinar se deseja aceitar ou negar a solicitação. A outra interação ocorre quando o NPS recebe solicitações de contabilização do NAS. O servidor de estado usa o formulário de informações dessas solicitações de contabilidade para atualizar seu banco de dados.

Para obter mais informações sobre servidores de estado, consulte:

-   [Considerações de design de servidor de estado](/windows/desktop/Nps/ias-state-server-design-considerations)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Serviço de autenticação da Internet e servidor de políticas de rede](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[Autenticação, autorização e contabilização RADIUS](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[Registrando em log com o servidor de políticas de rede](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> </dl>

 

 