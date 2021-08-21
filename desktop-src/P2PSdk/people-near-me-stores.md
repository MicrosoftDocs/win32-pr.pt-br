---
description: Pessoas ao meu Redor armazenamentos
ms.assetid: 3f2aa9bd-49ca-4fa6-b718-7cbeeef857c7
title: Pessoas ao meu Redor armazenamentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 945a49d174f53037427aaa2f45dc0f567dc0acdba57e4a0b0231954e7e66fe90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061374"
---
# <a name="people-near-me-stores"></a>Pessoas ao meu Redor armazenamentos

Aplicativos com [Pessoas ao meu Redor](about-people-near-me.md) (PNM) podem usar os seguintes armazenamentos de dados:

### <a name="windows-address-book"></a>Windows Catálogo de Endereços

O Windows Catálogo de Endereços armazena informações sobre contatos e seus certificados digitais. O contato '**Me**', que representa o usuário conectado no momento, também é armazenado no Windows Catálogo de Endereços.

### <a name="certificate-store"></a>Repositório de certificados

O Armazenamento de Certificados contém o certificado auto-assinado para o contato '**Me**'.

### <a name="application-store"></a>Repositório de aplicativos

Um instalador de aplicativo registra um aplicativo com PNM durante o processo de instalação. Esses são os objetos que podem ser pesquisados por outros usuários ao tentar se conectar a um usuário com um aplicativo comum, como um jogo de computador. Para cada aplicativo, o Application Store contém o nome do aplicativo, um GUID (identificador global exclusivo), um escopo do aplicativo, uma descrição e um caminho para o arquivo executável do programa. O escopo de um aplicativo pode ser definido como Nenhum (não anunciado), Pessoas ao meu Redor (anunciado na sub-rede local), Contatos (anunciado apenas para contatos) ou Todos (anunciados na sub-rede local e para contatos). O Armazenamento de Aplicativos está localizado no Windows Vista.

 

 



