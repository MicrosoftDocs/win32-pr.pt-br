---
description: O sistema cria um perfil de usuário na primeira vez que um usuário faz logon em um computador. Em logons subsequentes, o sistema carrega o perfil do usuário e, em seguida, outros componentes do sistema configuram o ambiente do usuário de acordo com as informações no perfil.
title: Sobre perfis de usuário
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 333f1861-91fe-4796-af13-dd300a5c6ec3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: cc6715a63c86913d5a525805e6178b3230505d0b
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879532"
---
# <a name="about-user-profiles"></a>Sobre perfis de usuário

O sistema cria um perfil de usuário na primeira vez que um usuário faz logon em um computador. Em logons subsequentes, o sistema carrega o perfil do usuário e, em seguida, outros componentes do sistema configuram o ambiente do usuário de acordo com as informações no perfil.

## <a name="types-of-user-profiles"></a>Tipos de perfis de usuário

-   [Perfis de usuário local](local-user-profiles.md). Um perfil de usuário local é criado na primeira vez que um usuário faz logon em um computador. O perfil é armazenado no disco rígido local do computador. As alterações feitas no perfil de usuário local são específicas para o usuário e para o computador no qual as alterações são feitas.
-   [Perfis de usuário de roaming](roaming-user-profiles.md). Um perfil de usuário móvel é uma cópia do perfil local que é copiado para o e armazenado em um compartilhamento de servidor. Esse perfil é baixado em qualquer computador em que um usuário faz logon em uma rede. As alterações feitas em um perfil de usuário móvel são sincronizadas com a cópia do perfil do servidor quando o usuário faz logoff. A vantagem dos perfis de usuário de roaming é que os usuários não precisam criar um perfil em cada computador que usam em uma rede.
-   [Perfis de usuário obrigatórios](mandatory-user-profiles.md). Um perfil de usuário obrigatório é um tipo de perfil que os administradores podem usar para especificar as configurações para os usuários. Somente administradores do sistema podem fazer alterações em perfis de usuário obrigatórios. As alterações feitas por usuários nas configurações da área de trabalho são perdidas quando o usuário faz logoff.
-   [Perfis de usuário temporários](temporary-user-profiles.md). Um perfil temporário é emitido cada vez que uma condição de erro impede que o perfil do usuário seja carregado. Os perfis temporários são excluídos no final de cada sessão e as alterações feitas pelo usuário nas configurações e arquivos da área de trabalho são perdidas quando o usuário faz logoff. os perfis temporários só estão disponíveis em computadores que executam o Windows 2000 e posterior.

Um perfil de usuário consiste nos seguintes elementos:

-   Um hive do registro. O hive do registro é o arquivo NTuser. dat. O hive é carregado pelo sistema no logon do usuário e é mapeado para a chave de registro **HKEY \_ Current \_ User** . O hive do registro do usuário mantém as preferências e a configuração com base no registro do usuário.
-   Um conjunto de pastas de perfil armazenadas no sistema de arquivos. Os arquivos de perfil do usuário são armazenados no diretório de **perfis** , em uma base de pasta por usuário. A pasta de perfil do usuário é um contêiner para aplicativos e outros componentes do sistema para popular com subpastas e dados por usuário, como documentos e arquivos de configuração. Windows O Explorer usa as pastas de perfil do usuário extensivamente para itens como a área de trabalho do usuário, o menu **Iniciar** e a pasta **documentos** .

Os perfis de usuário oferecem as seguintes vantagens:

-   Quando o usuário faz logon em um computador, o sistema usa as mesmas configurações que estavam em uso quando o usuário fez logoff pela última vez.
-   Ao compartilhar um computador com outros usuários, cada usuário recebe sua área de trabalho personalizada após o logon.
-   Configurações no perfil do usuário são exclusivos para cada usuário. As configurações não podem ser acessadas por outros usuários. As alterações feitas no perfil de um usuário não afetam outros perfis de usuários ou de outros usuários.

## <a name="user-profile-tiles-in-windows-7-and-later"></a>blocos de perfil do usuário no Windows 7 e posterior

no Windows 7 ou posterior, cada perfil de usuário tem uma imagem associada apresentada como um bloco de usuário. Esses blocos aparecem para os usuários no item do painel de controle **contas de usuário** e sua subpágina **gerenciar contas** . Os arquivos de imagem para o convidado padrão e as contas de usuário padrão também aparecerão aqui se você tiver direitos de acesso de administrador.

> [!Note]  
> A subpágina **gerenciar contas** é acessada por meio do link **gerenciar outra conta** no item do painel de controle de **contas de usuário** .

 

-   % ProgramData% \\ de \\ imagens da conta de usuário da Microsoft \\Guest.bmp
-   % ProgramData% \\ de \\ imagens da conta de usuário da Microsoft \\User.bmp

A imagem do bloco do usuário é armazenada na pasta Temp local de usuários do% SystemDrive% \\ Users \\ &lt; &gt; \\ AppData \\ \\ como &lt; nome de usuário &gt;.bmp. Quaisquer caracteres de barra ( \\ ) são convertidos em caracteres de sinal de adição (+). Por exemplo, o domínio \\ usuário é convertido em domínio + usuário.

O arquivo de imagem aparece na pasta **Temp** do usuário:

-   Depois que o usuário concluir a configuração inicial do sistema (OOBE).
-   Quando o usuário inicia pela primeira vez o item do painel de controle de **contas de usuário** .
-   Quando o usuário vai para a subpágina **gerenciar contas** do item do painel de controle de **contas de usuário** . Além disso, os blocos para todos os outros usuários no computador são mostrados.

Essas instâncias são as únicas vezes que as imagens são criadas ou atualizadas. Portanto, há várias limitações a serem consideradas ao usar o local da pasta **Temp** programaticamente:

1.  Não há garantia de que o bloco do usuário esteja presente. Se o usuário excluir o arquivo de .bmp, por exemplo manualmente ou por meio de um utilitário que exclui arquivos temporários, esse bloco do usuário não será recriado automaticamente até que o usuário inicie o item do painel de controle de **contas de usuário** ou **gerenciar contas** .

2.  Os blocos de usuário para outros usuários no computador podem não estar presentes na pasta **temporária** do usuário conectado no momento. por exemplo, se o usuário A cria o usuário B por meio do item do painel de controle de **contas de usuário** , o bloco do usuário b é criado na pasta **Temp** do usuário a quando Windows envia o usuário a para a subpágina **gerenciar contas** . Como a estrutura de diretório não é criada para o usuário B até que ele faça logon, a pasta **temporária** do usuário a é o único local em que o bloco do usuário B está armazenado. Quando o usuário B faz logon, a única imagem armazenada na pasta **temporária** do usuário b é sua própria.

    1.  Para obter todos os blocos de usuário para usuários em um sistema, talvez os aplicativos precisem Pesquisar no diretório **temporário** de cada usuário.
    2.  Como a ACL (lista de controle de acesso) desses diretórios **temporários** permite o acesso ao sistema, ao administrador e ao usuário atual, os aplicativos precisam elevar o acesso para outros usuários.

3.  Não há garantia de que os blocos de outros usuários estejam atualizados em suas pastas **temporárias** . Se o usuário B atualizar seu bloco de usuário, o usuário A não verá a alteração até que o usuário A acesse a subpágina **gerenciar contas** . Portanto, se os aplicativos usarem a pasta **Temp** do usuário para obter o bloco do usuário B, esses aplicativos poderão obter um arquivo de imagem desatualizado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Perfis de usuário local](local-user-profiles.md)
</dt> <dt>

[Perfis de usuário em roaming](roaming-user-profiles.md)
</dt> <dt>

[Perfis de usuário obrigatórios](mandatory-user-profiles.md)
</dt> <dt>

[Perfis de usuário temporários](temporary-user-profiles.md)
</dt> <dt>

[Diretório de perfis](profiles-directory.md)
</dt> <dt>

[Variáveis de ambiente do usuário](user-environment-variables.md)
</dt> <dt>

[Troca rápida de usuário](fast-user-switching.md)
</dt> </dl>

 

 



