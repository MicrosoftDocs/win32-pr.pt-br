---
description: Quando você define um nível de representação para um aplicativo, determina o grau de autoridade que o aplicativo concede a outros aplicativos para usar sua identidade quando ele os chama.
ms.assetid: 5b5b2c2d-dc3d-4edd-9e13-e6cb13022ceb
title: Definindo um nível de representação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1075ac3b10380892cdfdf770543a2dcbb32d56c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089303"
---
# <a name="setting-an-impersonation-level"></a>Definindo um nível de representação

Quando você define um nível de representação para um aplicativo, determina o grau de autoridade que o aplicativo concede a outros aplicativos para usar sua identidade quando ele os chama. Você pode definir isso somente para aplicativos de servidor COM+ — os aplicativos de biblioteca são executados sob a identidade do processo de hospedagem e usam o nível de representação que ele especifica. Para obter mais detalhes, consulte [níveis de representação](/windows/desktop/com/impersonation-levels).

**Para selecionar um nível de representação**

1.  Clique com o botão direito do mouse no aplicativo COM+ para o qual você está definindo a representação e clique em **Propriedades**.

2.  Na caixa de diálogo Propriedades do aplicativo, clique na guia **segurança** .

3.  Na caixa **nível de representação** , selecione o nível apropriado. Os níveis são os seguintes, ordenados da concessão de menos para a maior autoridade:

    -   **Anônimo**. O cliente é anônimo ao servidor. O servidor pode representar o cliente, mas o token de representação (uma credencial local) não contém nenhuma informação sobre o cliente.
    -   **Identificar**. O servidor pode obter a identidade do cliente e pode representar o cliente para fazer verificações de ACL.
    -   **Representar**. O servidor pode representar o cliente enquanto atua em seu nome, embora com restrições. O servidor pode acessar recursos no mesmo computador que o cliente. Se o servidor estiver no mesmo computador que o cliente, ele poderá acessar os recursos de rede como o cliente. Se o servidor estiver em um computador diferente do cliente, ele poderá acessar apenas os recursos que estão no mesmo computador que o servidor. Essa é a configuração padrão para aplicativos de servidor COM+.
    -   **Delegar**. O servidor pode representar o cliente ao atuar em seu nome, seja no mesmo computador que o cliente. Durante a representação, as credenciais do cliente (ambas com local e aquelas com a validade da rede) podem ser passadas para qualquer número de computadores.

4.  Clique em **OK**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando a segurança do Role-Based](configuring-role-based-security.md)
</dt> <dt>

[Configurando a política de restrição de software](configuring-the-software-restriction-policy.md)
</dt> <dt>

[Habilitando a autenticação para um aplicativo de biblioteca](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[Definindo um nível de autenticação para um aplicativo de servidor](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 
