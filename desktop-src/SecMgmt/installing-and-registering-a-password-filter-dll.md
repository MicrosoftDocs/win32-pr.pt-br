---
description: A DLL de filtro de senha do Windows, Passfilt.dll, é executada no contexto de segurança da conta do sistema local e ajuda você a filtrar senhas de conta local ou de domínio.
ms.assetid: 12a6fe6d-5b37-4fcf-bd04-0a22d84ba323
title: Instalando e registrando uma DLL de filtro de senha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cd911c1a527384e48a2ae4567f6d85862e184cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828552"
---
# <a name="installing-and-registering-a-password-filter-dll"></a>Instalando e registrando uma DLL de filtro de senha

Você pode usar o filtro de senha do Windows para filtrar as senhas de conta local ou de domínio. Para usar o filtro de senha para contas de domínio, instale e registre a DLL em cada controlador de domínio no domínio.

Execute as etapas a seguir para instalar o filtro de senha. Você pode executar essas etapas manualmente ou pode escrever um instalador para executar essas etapas. Você precisa ser um administrador ou pertencer ao grupo de administradores para executar essas etapas.

**Para instalar e registrar uma DLL de filtro de senha do Windows**

1.  Copie a DLL para o diretório de instalação do Windows no controlador de domínio ou no computador local. Em instalações padrão, a pasta padrão é \\ Windows \\ System32. Certifique-se de criar uma DLL de filtro de senha de 32 bits para computadores de 32 bits e uma DLL de filtro de senha de 64 bits para computadores de 64 bits e, em seguida, copie-os para o local apropriado.
2.  Para registrar o filtro de senha, atualize a seguinte chave do registro do sistema:

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Control
                Lsa
    ```

    Se a subchave **pacotes de notificação** existir, adicione o nome da sua dll aos dados do valor existente. Não substitua os valores existentes e não inclua a extensão. dll.

    Se a subchave **pacotes de notificação** não existir, adicione-a e, em seguida, especifique o nome da dll para os dados do valor. Não inclua a extensão. dll.

    A subchave **pacotes de notificação** pode adicionar vários pacotes.

3.  Localize a configuração de complexidade da senha.

    No painel de controle, clique em **desempenho e manutenção**, clique em **Ferramentas administrativas**, clique duas vezes em **política de segurança local**, clique duas vezes em **políticas de conta** e clique duas vezes em **política de senha**.

4.  Para impor o filtro de senha padrão do Windows e o filtro de senha personalizada, verifique se a configuração de política **senhas devem atender aos requisitos de complexidade** está habilitada. Caso contrário, desabilite a configuração de política as **senhas devem atender aos requisitos de complexidade** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Considerações sobre programação de filtro de senha](password-filter-programming-considerations.md)
</dt> <dt>

[Imposição de senha forte e Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)
</dt> <dt>

[Funções de filtro de senha](management-functions.md)
</dt> </dl>

 

 



