---
description: Habilitando a autenticação para um aplicativo de biblioteca
ms.assetid: 80c80c14-ceef-4a74-810d-6aa3cc320cef
title: Habilitando a autenticação para um aplicativo de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cfa9f2a6a5e3c1312fa13e0aff1e9f4ea17e4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788147"
---
# <a name="enabling-authentication-for-a-library-application"></a>Habilitando a autenticação para um aplicativo de biblioteca

Como os aplicativos de biblioteca COM+ são hospedados por outros processos, seus requisitos de segurança podem ser diferentes dos aplicativos de servidor. Se o aplicativo de biblioteca for hospedado por um navegador, talvez seja necessário receber retornos de chamada não autenticados.

Para atender a essa necessidade, você pode desabilitar a autenticação para que o processo de hospedagem não execute verificações de segurança para os chamadores do aplicativo de biblioteca. Quando você desabilita a autenticação, as chamadas para o aplicativo de biblioteca efetivamente não são autenticadas – todas as chamadas para ela serão realizadas com sucesso. Para obter mais informações, consulte [segurança do aplicativo de biblioteca](library-application-security.md).

**Para habilitar (ou desabilitar) a autenticação para um aplicativo de biblioteca**

1.  Clique com o botão direito do mouse no aplicativo COM+ para o qual você está habilitando ou desabilitando a autenticação e clique em **Propriedades**.

2.  Na caixa de diálogo Propriedades do aplicativo, clique na guia **segurança** .

3.  Em **autenticação**, marque a caixa de seleção **habilitar autenticação** para habilitar a autenticação; desmarcar a caixa de seleção desativará a autenticação.

4.  Clique em **OK**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo um nível de autenticação para um aplicativo de servidor](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 



