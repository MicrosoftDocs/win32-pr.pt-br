---
description: Depois de habilitar as verificações de acesso, para seu aplicativo COM+, você deve selecionar o nível no qual deseja que as verificações de acesso sejam executadas.
ms.assetid: 9c044add-7761-4378-b7eb-bf4e84e913b3
title: Configurando um nível de segurança para verificações de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e912f671a27d35b51939376fa14af3b693c368e3375680913693d364ddf638
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120366"
---
# <a name="setting-a-security-level-for-access-checks"></a>Configurando um nível de segurança para verificações de acesso

Depois de habilitar as [verificações de acesso](enabling-access-checks-for-an-application.md), para seu aplicativo com+, você deve selecionar o nível no qual deseja que as verificações de acesso sejam executadas.

**Para selecionar um nível de segurança**

1.  Na árvore de console da ferramenta administrativa serviços de componentes, clique com o botão direito do mouse no aplicativo COM+ para o qual você deseja habilitar as verificações de acesso e clique em **Propriedades**.

2.  Na caixa de diálogo Propriedades do aplicativo, clique na guia **segurança** .

3.  Em **nível de segurança**, selecione uma das seguintes opções:

    -   **Executar verificações de acesso somente no nível do processo**– essa configuração indica que os usuários em funções atribuídas ao aplicativo serão adicionados ao descritor de segurança do processo. Isso tem os seguintes efeitos e implicações:

        A verificação de função refinada é desativada nos níveis de componente, método e interface. As verificações de segurança são executadas somente no nível do aplicativo.

        A propriedade de segurança não está incluída no contexto de todos os objetos em execução no aplicativo. Isso pode afetar potencialmente o modo como os objetos são ativados. Consulte [propriedade de contexto de segurança](security-context-property.md).

        O contexto de chamada de segurança não será disponibilizado. A segurança programática que se baseia em informações de contexto de chamada de segurança não funcionará. Consulte [informações de contexto de chamada de segurança](security-call-context-information.md).

    -   **Executar verificações de acesso no nível do processo e do componente**– essa configuração indica que as verificações do descritor de segurança em nível de processo e verificações completas de segurança baseadas em função serão executadas. Isso tem os seguintes efeitos e implicações:

        Para habilitar a verificação de função para componentes específicos, você deve [habilitar as verificações de acesso no nível do componente](enabling-access-checks-at-the-component-level.md).

        A propriedade de segurança é incluída no contexto de todos os objetos em execução no aplicativo. Isso pode afetar potencialmente o modo como os objetos são ativados. Consulte [propriedade de contexto de segurança](security-context-property.md).

        O contexto de chamada de segurança está disponível. A segurança baseada em função programática está habilitada. Consulte [informações de contexto de chamada de segurança](security-call-context-information.md).

        > [!Note]  
        > Para aplicativos de biblioteca COM+, você deve optar por verificar tanto no processo quanto em níveis de componente para qualquer verificação de acesso significativa para funcionar. Os aplicativos de biblioteca dependem do processo de host para segurança em nível de processo. Você pode determinar como o aplicativo de biblioteca interage com a autenticação executada pelo processo de host [definindo a autenticação](enabling-authentication-for-a-library-application.md). Para obter mais informações, consulte [segurança do aplicativo de biblioteca](library-application-security.md).

         

4.  Clique em **OK**.

Na próxima vez em que o aplicativo for iniciado, a segurança será verificada automaticamente no nível especificado. Somente os usuários atribuídos às funções atribuídas ao aplicativo receberão acesso ao aplicativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atribuindo funções a componentes, interfaces ou métodos](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Configurando a segurança do Role-Based](configuring-role-based-security.md)
</dt> <dt>

[Definindo funções para um aplicativo](defining-roles-for-an-application.md)
</dt> <dt>

[Habilitando verificações de acesso para um aplicativo](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Habilitando verificações de acesso no nível do componente](enabling-access-checks-at-the-component-level.md)
</dt> </dl>

 

 



