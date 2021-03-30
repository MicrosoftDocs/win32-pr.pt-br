---
title: Problemas de segurança para publicação de serviço
description: O sistema restringe a capacidade de criar, modificar ou excluir objetos de ponto de conexão. Esteja atento e manipule essas restrições ao publicar um serviço.
ms.assetid: 38e20a47-738d-4951-ad74-249039afeb52
ms.tgt_platform: multiple
keywords:
- Problemas de segurança para o AD de publicação de serviço
- Active Directory, usando, segurança, problemas de segurança da publicação de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fee5be89c490fa938cdc9c7cf3d7d72434a3dffa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634919"
---
# <a name="security-issues-for-service-publication"></a>Problemas de segurança para publicação de serviço

O sistema restringe a capacidade de criar, modificar ou excluir objetos de ponto de conexão. Esteja atento e manipule essas restrições ao publicar um serviço.

Os clientes devem ser capazes de confiar nos dados publicados em um objeto de ponto de conexão no diretório. Por esse motivo, a permissão para criar um objeto de ponto de conexão normalmente é restrita a usuários privilegiados, como administradores de domínio. Isso impede que usuários não autorizados de clientes decepcionante criem pontos de conexão inválidos para serviços bem conhecidos.

Os serviços não devem ser executados com privilégios de administrador de domínio. Isso significa que um serviço normalmente não pode criar seu próprio ponto de conexão. Em vez disso, você fornece um aplicativo de instalação ou configuração de serviço que cria o ponto de conexão. Esse instalador deve ser executado por um usuário com os privilégios necessários.

Embora um serviço normalmente não possa criar seu ponto de conexão, ele deve ser capaz de atualizar as propriedades do ponto de conexão em tempo de execução. As propriedades do ponto de conexão contêm os dados de associação usados pelos clientes para se conectarem ao serviço. Se os dados de associação forem alterados, o serviço deverá atualizar o ponto de conexão; caso contrário, os clientes não poderão usar o serviço. Isso significa que o instalador também deve modificar o descritor de segurança no objeto de ponto de conexão para permitir que o serviço leia e grave as propriedades apropriadas em tempo de execução. Para obter mais informações e um exemplo de código, consulte [habilitando a conta de serviço para acessar as propriedades do SCP](enabling-service-account-to-access-scp-properties.md).

Um serviço em execução na conta LocalSystem pode criar um ponto de conexão como um objeto filho em seu próprio objeto de computador no diretório. Esse serviço é uma exceção à regra de serviços que não cria seus próprios pontos de conexão. Um serviço LocalSystem também tem permissão para modificar as propriedades de objetos de ponto de conexão em seu próprio objeto de computador. Lembre-se de que um serviço deve ser executado na conta LocalSystem somente se for absolutamente necessário. Para obter mais informações, consulte [diretrizes para selecionar uma conta de logon de serviço](guidelines-for-selecting-a-service-logon-account.md).

O aplicativo que cria um objeto de ponto de conexão ou qualquer objeto deve ter permissões criar filho para a classe de objeto a ser criada no contêiner em que o objeto será criado. Para remover um objeto, o processo que executa a operação deve ter permissões de excluir filho para a classe de objeto a ser excluída no contêiner que contém o objeto ou ter permissões de exclusão no próprio objeto. Para atualizar um ponto de conexão, o processo que executa a operação deve ter acesso de gravação às propriedades a serem atualizadas no objeto.

 

 




