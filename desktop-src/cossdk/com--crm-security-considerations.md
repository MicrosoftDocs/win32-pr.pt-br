---
description: Considerações de segurança do CRM do COM+
ms.assetid: e212c847-b43b-43be-b089-82336551b89a
title: Considerações de segurança do CRM do COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ababde9f31c0c2655fbf4f0c46b216ca0cbfee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089057"
---
# <a name="com-crm-security-considerations"></a>Considerações de segurança do CRM do COM+

Um arquivo de log do CRM pode conter informações confidenciais que devem ser protegidas. Por esse motivo, se o aplicativo de servidor estiver sendo executado sob qualquer identidade diferente de usuário interativo quando o arquivo de log do CRM for criado, o arquivo de log do CRM será protegido somente para esse usuário. Esse recurso está disponível apenas no sistema de arquivos NTFS. Se a identidade do aplicativo do servidor for alterada posteriormente, as informações de segurança do arquivo de log do CRM não serão alteradas automaticamente. Ele pode ser alterado manualmente usando as ferramentas de administração existentes do Windows. A alternativa é simplesmente excluir o arquivo de log do CRM quando ele estiver em um estado limpo (que é esperado após um desligamento controlado do aplicativo de servidor).

Na operação normal, o COM+ cria o componente compensador de CRM e chama a interface [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) . No entanto, um usuário com privilégios para criar o compensador de CRM pode chamar a interface **ICrmCompensator** em momentos inadequados, possivelmente causando problemas de segurança do sistema. Para ajudar a proteger contra esses problemas de segurança, o administrador do sistema pode usar a segurança baseada em função para restringir o componente compensador de CRM somente a essas identidades dos aplicativos de servidor em que ele é executado. Se o componente estiver sendo executado em um aplicativo de biblioteca, isso incluirá todas as identidades dos aplicativos de servidor.

> [!Note]  
> A partir do Windows Server 2003, para ajudar a impedir a ativação de fora do aplicativo de servidor, é possível garantir um sistema mais seguro marcando o componente compensador de CRM como particular.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do Gerenciador de recursos de compensação COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



