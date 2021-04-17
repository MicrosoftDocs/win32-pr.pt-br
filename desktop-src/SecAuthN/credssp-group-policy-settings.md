---
description: Para o protocolo CredSSP para delegar credenciais, você deve especificar a quais servidores podem ser delegadas.
ms.assetid: 15ed9a62-2eee-4f29-92c5-ccf2754cdf13
title: Configurações de Política de Grupo CredSSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a159b7a162df3eda692462a3d3972159e61797e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747512"
---
# <a name="credssp-group-policy-settings"></a>Configurações de Política de Grupo CredSSP

Para o [protocolo CredSSP](credential-security-support-provider.md) para delegar credenciais, você deve especificar a quais servidores podem ser delegadas. Para especificar esses servidores, modifique as configurações no snap-in do GPE (console de gerenciamento Microsoft) do editor de Política de Grupo (MMC). As configurações de GPE que controlam a delegação estão em **configuração do computador \| modelos administrativos \| delegação de \| credenciais do sistema**.

> [!Caution]  
> Essa não é uma delegação restrita. O CredSSP passa as credenciais completas do usuário para o servidor sem nenhuma restrição.

 

As configurações de política de grupo controlam a delegação dos seguintes tipos de credenciais.



| Tipo de credenciais                                                                                                                                 | Descrição                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Default_credentials"></span><span id="default_credentials"></span><span id="DEFAULT_CREDENTIALS"></span>Credenciais padrão<br/> | As credenciais obtidas quando o usuário faz logon pela primeira vez no Windows.<br/>                   |
| <span id="Fresh_credentials"></span><span id="fresh_credentials"></span><span id="FRESH_CREDENTIALS"></span>Novas credenciais<br/>         | As credenciais para as quais o usuário é solicitado ao executar um aplicativo.<br/>       |
| <span id="Saved_credentials"></span><span id="saved_credentials"></span><span id="SAVED_CREDENTIALS"></span>Credenciais salvas<br/>         | As credenciais que são salvas usando o [Gerenciador de credenciais](credential-manager.md).<br/> |



 

Para incluir um servidor na categoria associada a uma determinada configuração de diretiva de grupo, adicione o [*nome da entidade de serviço*](/windows/desktop/SecGloss/s-gly) (SPN) desse servidor à lista de servidores para essa configuração de política de grupo. O SPN pode conter um único caractere curinga.

 

