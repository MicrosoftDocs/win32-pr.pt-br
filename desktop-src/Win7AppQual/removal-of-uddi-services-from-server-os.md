---
description: Remoção de serviços UDDI do sistema operacional do servidor
ms.assetid: 5ebc8c4c-acee-4658-8d36-30fbb17b1ef1
title: Remoção de serviços UDDI do sistema operacional do servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530c6aadbe4e1dce32f3cc2e212af823eb565b85b67c5f7f29b77015f75bc899
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328995"
---
# <a name="removal-of-uddi-services-from-server-operating-system"></a>Remoção de serviços UDDI do sistema operacional do servidor

## <a name="affected-platform"></a>Plataforma afetada

**Servidores** – Windows Server 2008 R2  



## <a name="feature-impact"></a>Impacto do recurso

**Gravidade –** Média  
**Frequência** – Baixa  

## <a name="description"></a>Descrição

A Microsoft removeu a função de servidor UDDI (Descrição Universal, Descoberta e Integração) do Windows Server 2008 R2. Versões futuras dos Serviços UDDI fazem parte do produto Microsoft BizTalk. Esse realinhamento de produto e consolidação posiciona a Microsoft para atender melhor ao mercado soa (arquitetura orientada a serviços).

A primeira versão pós-Windows Server 2008 dos Serviços UDDI será compatível com padrões UDDI v3.0. Ele será lançado como parte da versão BizTalk Server 2009. Para atender ao nosso compromisso de fornecer uma experiência de usuário satisfatória, ofereceremos um pacote de instalação do UDDI Services v3 para o Windows Server 2008 R2.

## <a name="manifestation"></a>Manifestação

A presença de versões anteriores dos componentes do UDDI Services no sistema bloqueia uma atualização para o Windows Server 2008 R2.

## <a name="mitigation-of-impact"></a>Mitigação de impacto

Os usuários que implantaram um site de Serviços UDDI do Windows Server 2003 ou Windows Server 2008 podem optar por não atualizar os servidores que executam os Serviços UDDI para o Windows Server 2008 R2. Eles também podem mover os Serviços UDDI para caixas dedicadas do Windows Server 2003 ou Windows Server 2008 se eles precisam atualizar as caixas atuais dos Serviços UDDI.

## <a name="solution"></a>Solução

A solução recomendada é implantar os Serviços UDDI v3.0 do BizTalk Server 2009 em um computador do Windows Server 2008 R2 e, em seguida, migrar o site antigo para o novo site. Os Serviços UDDI v3.0 fornece compatibilidade com compatibilidade com UDDI Services 2.0, portanto, todos os aplicativos que estão usando serviços UDDI não serão afetados.

Para fazer isso, execute estas etapas:

1.  Configurar um novo site do UDDI Services v3.0 em um computador já carregado com o Windows Server 2008 R2. (Observação: em uma configuração distribuída, um site UDDI v3.0 pode consistir em mais de um Windows Server 2008 R2.)
2.  Use a ferramenta de migração de dados UDDI para migrar os dados do banco de dados UDDI Services antigo para o novo banco de dados.
3.  Fazer o back-up do banco de dados UDDI Services antigo para garantir a capacidade de reação.
4.  Desinstale o software UDDI Services antigo e atualize essas caixas para Windows Server 2008 R2.

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [Site do Microsoft UDDI Services](https://msdn.microsoft.com/biztalk/dd789428.aspx)
-   [Especificações de UDDI](http://uddi.xml.org/specification)
-   [Download do UDDI Services v3.0 para Windows Server 2008 R2](https://www.microsoft.com/downloads/details.aspx?FamilyID=e4761835-70f0-4e8d-96c5-64818d54e06e)

 

 



