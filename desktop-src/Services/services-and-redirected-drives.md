---
description: Um serviço (ou qualquer processo em execução em um contexto de segurança diferente) que deve acessar um recurso remoto deve usar o nome UNC (Convenção de nomenclatura universal) para acessar o recurso.
ms.assetid: 2582259d-077c-4089-9a87-1a377994f0bd
title: Serviços e unidades redirecionadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3b1435e69ded3bf13a0869a0b9ad2b90bb4682c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922609"
---
# <a name="services-and-redirected-drives"></a>Serviços e unidades redirecionadas

Um serviço (ou qualquer processo em execução em um contexto de segurança diferente) que deve acessar um recurso remoto deve usar o nome UNC (Convenção de nomenclatura universal) para acessar o recurso. O serviço deve ter os privilégios apropriados para acessar o recurso. Se um serviço do lado do servidor usar uma conexão RPC, a delegação deverá ser habilitada no servidor remoto.

As letras das unidades não são globais para o sistema. Cada sessão de logon recebe seu próprio conjunto de letras de unidade de A a Z. Portanto, as unidades redirecionadas não podem ser compartilhadas entre processos em execução em contas de usuário diferentes. Além disso, um serviço (ou qualquer processo em execução em sua própria sessão de logon) não pode acessar as letras da unidade que foram estabelecidas em uma sessão de logon diferente.

Um serviço não deve acessar diretamente os recursos locais ou de rede por meio de letras de unidade mapeadas, nem chamar o comando **net use** para mapear letras de unidade em tempo de execução. O comando **net use** não é recomendado por vários motivos:

-   Os mapeamentos de unidade existem em contextos de logon. portanto, se um aplicativo estiver sendo executado no contexto da [conta LocalService](localservice-account.md), qualquer outro serviço em execução nesse contexto poderá ter acesso à unidade mapeada.
-   Se o serviço fornecer credenciais explícitas para um comando **net use** , essas credenciais poderão ser compartilhadas inadvertidamente fora dos limites de serviço. Em vez disso, o serviço deve usar a [representação do cliente](/windows/desktop/SecAuthZ/client-impersonation) para representar o usuário.
-   Vários serviços em execução no mesmo contexto podem interferir entre si. Se ambos os serviços executarem um **uso líquido** explícito e fornecerem as mesmas credenciais ao mesmo tempo, um serviço falhará com um erro "já conectado".

Além disso, um serviço não deve usar as [funções de rede do Windows](/windows/desktop/WNet/windows-networking-functions) para gerenciar as letras de unidade mapeadas. Embora as funções WNet possam retornar com êxito, o comportamento resultante não é o esperado. Quando o sistema estabelece uma unidade redirecionada, ele é armazenado em uma base por usuário. Somente o usuário é capaz de gerenciar a unidade redirecionada. O sistema mantém o controle de unidades redirecionadas com base no SID (identificador de segurança) de logon do usuário. O SID de logon é um identificador exclusivo para a sessão de logon do usuário. Um único usuário pode ter várias sessões de logon simultâneas no sistema.

Se um serviço estiver configurado para ser executado em uma conta de usuário, o sistema sempre criará uma nova sessão de logon para o usuário e iniciará o serviço nessa nova sessão de logon. Portanto, um serviço não pode gerenciar os mapeamentos de unidade estabelecidos nas outras sessões do usuário.

**Windows Server 2003:** Em um computador que tem várias interfaces de rede (ou seja, um computador de hospedagem múltipla), os atrasos de até 60 segundos podem ocorrer ao usar caminhos UNC para acessar arquivos armazenados em um servidor remoto de protocolo SMB. Para obter mais informações, consulte o [artigo 890553](https://support.microsoft.com/kb/890553) na base de dados de conhecimento de ajuda e suporte.

 

 
