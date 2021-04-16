---
description: Quando você define um nível de autenticação para um aplicativo, determina qual grau de autenticação é executado quando os clientes chamam o aplicativo.
ms.assetid: a59935de-6b8f-4c0a-8479-e30bc0509698
title: Definindo um nível de autenticação para um aplicativo de servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83450b3f8d1939d08cc3d16a21f438c8da6f8fc1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761075"
---
# <a name="setting-an-authentication-level-for-a-server-application"></a>Definindo um nível de autenticação para um aplicativo de servidor

Quando você define um nível de autenticação para um aplicativo, determina qual grau de autenticação é executado quando os clientes chamam o aplicativo. Níveis de autenticação mais altos fornecem maior segurança e integridade dos dados, embora geralmente com alguma degradação do desempenho. Para obter mais informações, consulte [autenticação de cliente](client-authentication.md).

**Para selecionar um nível de autenticação para um aplicativo de servidor**

1.  Clique com o botão direito do mouse no aplicativo COM+ para o qual você está definindo autenticação e clique em **Propriedades**.

2.  Na caixa de diálogo Propriedades do aplicativo, clique na guia **segurança** .

3.  Na caixa **nível de autenticação para chamadas** , selecione o nível apropriado. Os níveis são os seguintes, ordenados da mais baixa para a mais alta segurança:

    -   **None**. Nenhuma autenticação ocorre.
    -   **Conecte-se**. Autentica as credenciais somente quando a conexão é feita.
    -   **Chame**. Autentica as credenciais no início de cada chamada.
    -   **Pacote**. Autentica as credenciais e verifica se todos os dados de chamada foram recebidos. Essa é a configuração padrão para aplicativos de servidor COM+.
    -   **Integridade do pacote**. Autentica as credenciais e verifica se nenhum dado de chamada foi modificado em trânsito.
    -   **Privacidade do pacote**. Autentica as credenciais e criptografa o pacote, incluindo os dados, a identidade e a assinatura do remetente.

4.  Clique em **OK**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Habilitando a autenticação para um aplicativo de biblioteca](enabling-authentication-for-a-library-application.md)
</dt> </dl>

 

 



