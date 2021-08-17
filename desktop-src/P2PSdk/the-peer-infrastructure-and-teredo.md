---
description: Um usuário pode verificar o status da interface Teredo no prompt de comando digitando netsh interface teredo show state e examinando a saída.
ms.assetid: b6ac1708-fb8a-449b-b30f-c889688a4bac
title: A infraestrutura par e Teredo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18dfa3fe075d0829358849b3783272aac74e60545c1e58e1d9bf1663738e3721
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794233"
---
# <a name="the-peer-infrastructure-and-teredo"></a>A infraestrutura par e Teredo

Um usuário pode verificar o status da interface [Teredo](https://msdn.microsoft.com/library/ms819742.aspx) no prompt de comando digitando **netsh interface teredo show state** e examinando a saída. Se o estado estiver "offline", o Teredo não está ativo, o que impede que o usuário se conecte a outros usuários por meio de seus endereços Teredo. É possível que o Teredo possa estar offline porque o firewall está desabilitado ou não dá suporte a [IPv6.](/previous-versions/windows/embedded/ms898970(v=msdn.10))

 

 
