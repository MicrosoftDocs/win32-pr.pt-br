---
description: Windows pacotes de autenticação fornecem serviços de autenticação implementando a funcionalidade específica do pacote para as funções LsaLogonUser e LsaCallAuthenticationPackage fornecidas pela LSA.
ms.assetid: 71f7eccd-694d-475f-b6d0-1eaf9ac468f5
title: Windows Pacotes de autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8288e54398702994938627b13c745a67f96fbc44dc710e2e5a7ac65a8620685
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915075"
---
# <a name="windows-authentication-packages"></a>Windows Pacotes de autenticação

Windows pacotes de autenticação fornecem serviços de autenticação implementando a funcionalidade específica do pacote para as funções [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) e [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) fornecidas pela LSA.

MSV1 \_ 0 é um exemplo de um [*pacote de autenticação*](../secgloss/a-gly.md)Windows. O \_ pacote MSV1 0 aceita um nome de usuário e uma senha de [*hash*](../secgloss/h-gly.md) , que é pesquisada no banco de dados Sam (Gerenciador de [*contas de segurança*](../secgloss/s-gly.md) ). Dependendo dos resultados da pesquisa, o pacote de autenticação MSV1 \_ 0 aceita ou rejeita a tentativa de autenticação.

para obter uma lista das funções de suporte que o LSA fornece para uso por Windows pacotes de autenticação que exigem serviços do sistema, consulte [funções de LSA chamadas por pacotes de autenticação](authentication-functions.md).

Windows pacotes de autenticação devem implementar um conjunto de funções que são chamadas pelo LSA. Para obter a lista completa de funções, consulte [funções implementadas por pacotes de autenticação](authentication-functions.md).

 

 
