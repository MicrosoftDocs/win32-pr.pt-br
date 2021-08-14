---
description: Habilitando a autenticação para um aplicativo de biblioteca
ms.assetid: 80c80c14-ceef-4a74-810d-6aa3cc320cef
title: Habilitando a autenticação para um aplicativo de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bceb3d5799ee8fac1d8eb266e6513c4d2a759adb10b78b2117424b08f8c5d6ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736415"
---
# <a name="enabling-authentication-for-a-library-application"></a>Habilitando a autenticação para um aplicativo de biblioteca

Como os aplicativos de biblioteca COM+ são hospedados por outros processos, seus requisitos de segurança podem ser diferentes daqueles de aplicativos de servidor. Se o aplicativo de biblioteca for hospedado por um navegador, talvez seja necessário receber retornos de chamada não autenticados.

Para atender a essa necessidade, você pode desabilitar a autenticação para que o processo de hospedagem não execute verificações de segurança para chamadores do aplicativo de biblioteca. Quando você desabilita a autenticação, as chamadas para o aplicativo de biblioteca efetivamente não são autenticadas– todas as chamadas para ele terão êxito. Para obter mais informações, consulte [Segurança do aplicativo de biblioteca.](library-application-security.md)

**Para habilitar (ou desabilitar) a autenticação para um aplicativo de biblioteca**

1.  Clique com o botão direito do mouse no aplicativo COM+ para o qual você está habilitando ou desabilitando a autenticação e clique em **Propriedades**.

2.  Na caixa de diálogo propriedades do aplicativo, clique na **guia** Segurança.

3.  Em **Autenticação**, marque a caixa de seleção **Habilitar** autenticação para habilitar a autenticação; desempurar a caixa de seleção desabilitará a autenticação.

4.  Clique em **OK**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo um nível de autenticação para um aplicativo de servidor](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 



