---
description: Lojas de pessoas ao meu redor
ms.assetid: 3f2aa9bd-49ca-4fa6-b718-7cbeeef857c7
title: Lojas de pessoas ao meu redor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d18bf60e43aba278862fbd19f3c8909e344bc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829177"
---
# <a name="people-near-me-stores"></a>Lojas de pessoas ao meu redor

Aplicativos capazes de [pessoas ao meu redor](about-people-near-me.md) (PNM) podem usar os seguintes armazenamentos de dados:

### <a name="windows-address-book"></a>Catálogo de endereços do Windows

O catálogo de endereços do Windows armazena informações sobre contatos e seus certificados digitais. O contato '**me**', que representa o usuário conectado no momento, também é armazenado no catálogo de endereços do Windows.

### <a name="certificate-store"></a>Repositório de certificados

O repositório de certificados contém o certificado autoassinado para o contato '**me**'.

### <a name="application-store"></a>Repositório de aplicativos

Um instalador de aplicativo registra um aplicativo com o PNM durante o processo de instalação. Esses são os objetos que podem ser pesquisados por outros usuários ao tentar se conectar a um usuário com um aplicativo comum, como um jogo de computador. Para cada aplicativo, a loja de aplicativos contém o nome do aplicativo, um GUID (identificador global exclusivo), um escopo do aplicativo, uma descrição e um caminho para o arquivo executável do programa. O escopo de um aplicativo pode ser definido como nenhum (não anunciado), pessoas ao meu redor (anunciados na sub-rede local), contatos (anunciados apenas para contatos) ou todos (anunciados na sub-rede local e para contatos). A loja de aplicativos está localizada no registro do Windows Vista.

 

 



