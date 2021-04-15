---
description: Um usuário pode verificar o status da interface teredo no prompt de comando digitando netsh interface teredo show State e examinando a saída.
ms.assetid: b6ac1708-fb8a-449b-b30f-c889688a4bac
title: A infraestrutura de mesmo nível e Teredo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2550d8da46339205de60c4a537d03c10940da4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505883"
---
# <a name="the-peer-infrastructure-and-teredo"></a>A infraestrutura de mesmo nível e Teredo

Um usuário pode verificar o status da interface [Teredo](https://msdn.microsoft.com/library/ms819742.aspx) no prompt de comando digitando **netsh interface teredo show State** e examinando a saída. Se o estado for "offline", o Teredo não estará ativo, o que impede que o usuário se conecte a outros usuários por meio de seus endereços Teredo. É possível que o Teredo esteja offline porque o firewall está desabilitado ou não oferece suporte a [IPv6](/previous-versions/windows/embedded/ms898970(v=msdn.10)).

 

 
