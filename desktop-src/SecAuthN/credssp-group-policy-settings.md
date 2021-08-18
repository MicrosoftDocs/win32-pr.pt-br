---
description: Para o protocolo CredSSP para delegar credenciais, você deve especificar a quais servidores podem ser delegados.
ms.assetid: 15ed9a62-2eee-4f29-92c5-ccf2754cdf13
title: CredSSP Política de Grupo Configurações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8efaaab1b49efba89c9fa5788f60df372991f388c474d531eff8f59205af441
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008694"
---
# <a name="credssp-group-policy-settings"></a>CredSSP Política de Grupo Configurações

Para [o protocolo CredSSP para](credential-security-support-provider.md) delegar credenciais, você deve especificar a quais servidores podem ser delegados. Para especificar esses servidores, modifique as configurações no snap-in do MMC (Editor Política de Grupo) Console de Gerenciamento Microsoft (MMC). As configurações do GPE que controlam a delegação estão em Configuração do **\| Computador Modelos Administrativos \| Delegação de Credenciais do \| Sistema**.

> [!Caution]  
> Essa não é uma delegação restrita. O CredSSP passa as credenciais completas do usuário para o servidor sem nenhuma restrição.

 

As configurações de política de grupo controlam a delegação dos seguintes tipos de credenciais.



| Tipo de credenciais                                                                                                                                 | Descrição                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Default_credentials"></span><span id="default_credentials"></span><span id="DEFAULT_CREDENTIALS"></span>Credenciais padrão<br/> | As credenciais obtidas quando o usuário faz logo Windows.<br/>                   |
| <span id="Fresh_credentials"></span><span id="fresh_credentials"></span><span id="FRESH_CREDENTIALS"></span>Novas credenciais<br/>         | As credenciais que o usuário é solicitado ao executar um aplicativo.<br/>       |
| <span id="Saved_credentials"></span><span id="saved_credentials"></span><span id="SAVED_CREDENTIALS"></span>Credenciais salvas<br/>         | As credenciais que são salvas usando [Gerenciador de Credenciais](credential-manager.md).<br/> |



 

Para incluir um servidor na categoria associada a uma configuração de política de grupo específica, adicione o SPN [*(Nome*](/windows/desktop/SecGloss/s-gly) da Entidade de Serviço) desse servidor à lista de servidores para essa configuração de política de grupo. O SPN pode conter um único caractere curinga.

 

