---
description: Os grupos de pares exigem que cada membro tenha um certificado específico, que é chamado de GMC (certificado de membro de grupo).
ms.assetid: 3966d4eb-4504-4b1e-9c9f-6eab7751d7ed
title: Como funciona a segurança de grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d272e9a0567c6edc300a52cfa206305253ec5a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828407"
---
# <a name="how-group-security-works"></a>Como funciona a segurança de grupo

Os grupos de pares exigem que cada membro tenha um certificado específico, que é chamado de GMC (certificado de membro de grupo). O certificado GMC garante que todos os registros trocados entre os pares sejam assinados digitalmente. A chave pública de um par está contida nas estruturas que são passadas como parte da comunicação entre os pares, incluindo [**\_ \_ informações de credenciais de pares**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info).

Um GMC pode ser emitido em uma cadeia. Por exemplo, um criador pode emitir um GMC para o administrador A, que pode emitir um GMC para o administrador B, que pode emitir um GMC para o membro M. A cadeia GMC resultante é: Creator->A->B->M, que tem um comprimento de 4. O comprimento da cadeia é importante, pois não pode ser maior que 24. Se o administrador do 24 em uma cadeia tentar emitir um GMC para um membro, [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) ou [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) retornará o peer E a cadeia de par \_ \_ \_ muito \_ longo.

Um GMC também pode ser emitido chamando [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials). Um GMC implica a associação de usuário no grupo para o qual o GMC é emitido e pode ter um tempo de vida finito ou infinito. A atividade do membro do grupo não pode ser maior do que o tempo de vida especificado no GMC.

> [!Note]  
> O tempo de vida de GMC infinito está definido atualmente em 1000 anos.

 

A atividade do membro do grupo é limitada pelo tempo de vida do GMC e inclui o seguinte:

-   **Operações de registro** – um par não pode publicar informações em um grupo após a associação do grupo expirar ou publicar registros que têm um tempo de vida maior do que o tempo de vida da Associação de grupo do par.
-   **Operações de associação** -um administrador de grupo não pode emitir uma associação que tem um tempo de vida além da data especificada na associação de administrador de grupo. Por exemplo, se um administrador tiver 500 horas restantes em seu tempo de vida GMC, todas as associações emitidas deverão ser inferiores a 500 horas.

Como um membro do grupo não pode ter um tempo de vida maior do que o administrador que convida esse membro do grupo, é recomendável que você defina o tempo de vida do GMC de um administrador como infinito ou um tempo de vida muito longo. Por padrão, o criador do grupo tem um tempo de vida infinito.

## <a name="renewing-group-membership"></a>Renovando a associação de grupo

Para renovar as credenciais de um administrador ou membro cujo tempo de vida GMC esteja pronto para expirar, você tem as duas opções a seguir:

-   Chame [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) e passe a identidade do membro cujo tempo de vida está pronto para expirar. Se as credenciais forem especificadas como **nulas** e as informações de associação do par estiverem disponíveis para o grupo, a hora da renovação será definida com a mesma duração especificada nas credenciais de membro publicadas anteriormente. Se um período de duração diferente precisar ser especificado, uma nova estrutura de [**\_ \_ informações de credencial de par**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) deverá ser fornecida contendo a nova duração da vida útil e, em seguida, um novo GMC será publicado para o membro.

    Opcionalmente, a função [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) usa o \_ sinalizador de credenciais de armazenamento de grupo par \_ \_ , que publica automaticamente as novas credenciais do membro no banco de dados do grupo. Quando o membro se conecta ao grupo da próxima vez, para a primeira vez ou depois de ficar offline, o membro Obtém o GMC atualizado do banco de dados.

-   Chame [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) para passar a identidade do membro cujo tempo de vida de GMC está pronto para expirar. Se a expiração especificada no convite for **nula**, a duração do tempo de vida da GMC será a mesma que a GMC do administrador que emite a associação. Se o criador especificar a expiração como **NULL**, um GMC com um tempo de vida infinito será emitido.

    Se um par receber um GMC que expira antes do valor de tempo de vida da presença, os endereços do par não estarão disponíveis nas estruturas de [**\_ membro de par**](/windows/desktop/api/P2P/ns-p2p-peer_member) retornadas na enumeração iniciada por uma chamada para [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers). Isso acontece porque as informações de presença não são publicadas nesse caso, mesmo que o \_ sinalizador de presença de desabilitação de pares \_ não esteja definido.

 

 



