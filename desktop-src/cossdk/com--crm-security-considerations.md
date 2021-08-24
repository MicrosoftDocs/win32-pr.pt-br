---
description: Considerações sobre segurança do COM+ CRM
ms.assetid: e212c847-b43b-43be-b089-82336551b89a
title: Considerações sobre segurança do COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1052f9e8cf4f23dd80e2b4706b7e13c0f39a2aedd9b9a985da2d41101118467d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638726"
---
# <a name="com-crm-security-considerations"></a>Considerações sobre segurança do COM+ CRM

Um arquivo de log crm pode conter informações confidenciais que devem ser protegidas. Por esse motivo, se o aplicativo de servidor estiver em execução em qualquer identidade diferente de Usuário Interativo quando o arquivo de log do CRM for criado pela primeira vez, o arquivo de log do CRM será protegido somente para esse usuário. Esse recurso está disponível apenas no sistema de arquivos NTFS. Se a identidade do aplicativo de servidor for alterada posteriormente, as informações de segurança do arquivo de log do CRM não serão alteradas automaticamente. Ele pode ser alterado manualmente usando ferramentas de administração Windows existentes. A alternativa é simplesmente excluir o arquivo de log do CRM quando ele estiver em um estado limpo (o que é esperado após um desligamento controlado do aplicativo de servidor).

Em operação normal, o COM+ cria o componente compensador crm e chama a interface [**ICrmCompensator.**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) No entanto, um usuário com privilégios para criar o CRM Compensator pode chamar a interface **ICrmCompensator** em momentos inadequados, possivelmente causando problemas de segurança do sistema. Para ajudar a proteger contra esses problemas de segurança, o administrador do sistema pode usar a segurança baseada em função para restringir o componente crm compensator somente às identidades dos aplicativos de servidor nos quais ele é executado. Se o componente estiver em execução em um aplicativo de biblioteca, isso incluirá todas as identidades dos aplicativos de servidor.

> [!Note]  
> A partir do Windows Server 2003, para ajudar a evitar a ativação de fora do aplicativo de servidor, é possível garantir ainda mais um sistema mais seguro marcando o componente crm compensator como privado.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos de Resource Manager compensação COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



