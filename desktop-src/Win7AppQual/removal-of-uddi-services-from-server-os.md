---
description: Remoção dos serviços UDDI do sistema operacional do servidor
ms.assetid: 5ebc8c4c-acee-4658-8d36-30fbb17b1ef1
title: Remoção dos serviços UDDI do sistema operacional do servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 960a4063d990a3b2cdac45cd933a1e7dfef41f88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116324"
---
# <a name="removal-of-uddi-services-from-server-operating-system"></a>Remoção dos serviços UDDI do sistema operacional do servidor

## <a name="affected-platform"></a>Plataforma afetada

**Servidores** -Windows Server 2008 R2  



## <a name="feature-impact"></a>Impacto do recurso

**Severidade** -média  
**Frequência** -baixa  

## <a name="description"></a>Descrição

A Microsoft removeu a função de servidor de serviços UDDI (descrição universal, descoberta e integração) do Windows Server 2008 R2. Versões futuras dos serviços UDDI serão parte do produto Microsoft BizTalk. Esta realinhamento e consolidação do produto posiciona a Microsoft para melhor atender ao mercado SOA (arquitetura orientada a serviços).

A primeira versão posterior ao Windows Server 2008 dos serviços UDDI será compatível com os padrões UDDI v 3.0. Ele será enviado como parte da versão BizTalk Server 2009. Para atender ao nosso compromisso de fornecer uma experiência de usuário satisfatória, oferecemos um pacote de instalação dos serviços UDDI V3 para o Windows Server 2008 R2.

## <a name="manifestation"></a>Manifestação

A presença de versões anteriores dos componentes dos serviços UDDI no sistema bloqueia uma atualização para o Windows Server 2008 R2.

## <a name="mitigation-of-impact"></a>Mitigação do impacto

Os usuários que implantaram um site dos serviços UDDI do Windows Server 2003 ou do Windows Server 2008 podem optar por não atualizar os servidores que executam os serviços UDDI para o Windows Server 2008 R2. Eles também podem mover os serviços UDDI para as caixas do Windows Server 2003 ou do Windows Server 2008 dedicadas se precisarem atualizar as caixas de serviços UDDI atuais.

## <a name="solution"></a>Solução

A solução recomendada é implantar os serviços UDDI v 3.0 do BizTalk Server 2009 em um computador com Windows Server 2008 R2 e, em seguida, migrar o site antigo para o novo site. Os serviços UDDI v 3.0 fornecem compatibilidade com versões anteriores com os serviços UDDI 2,0, de modo que qualquer aplicativo que esteja usando os serviços UDDI não será afetado.

Para fazer isso, execute estas etapas:

1.  Configure um novo site dos serviços UDDI v 3.0 em um computador já carregado com o Windows Server 2008 R2. (Observação: em uma configuração distribuída, um site do UDDI v 3.0 pode consistir em mais de um computador com Windows Server 2008 R2.)
2.  Use a ferramenta de migração de dados UDDI para migrar os dados do banco de dados dos serviços UDDI antigos para o novo banco de dado.
3.  Faça backup do banco de dados dos serviços UDDI antigos para garantir a funcionalidade de reversão.
4.  Desinstale o antigo software de serviços UDDI e, em seguida, atualize essas caixas para o Windows Server 2008 R2.

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [Site dos serviços UDDI da Microsoft](https://msdn.microsoft.com/biztalk/dd789428.aspx)
-   [Especificações de UDDI](http://uddi.xml.org/specification)
-   [Download dos serviços UDDI v 3.0 para Windows Server 2008 R2](https://www.microsoft.com/downloads/details.aspx?FamilyID=e4761835-70f0-4e8d-96c5-64818d54e06e)

 

 



