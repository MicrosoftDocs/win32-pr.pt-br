---
title: Phone-Book arquivos e informações de conexão
description: Uma chamada de RasDial deve especificar as informações que o Gerenciador de conexão de acesso remoto precisa para estabelecer a conexão.
ms.assetid: bc3885a4-3c1e-47bc-b622-072b33ac3b51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d352772eec057edd6ab8c9f53640c50ea0fc73
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084791"
---
# <a name="phone-book-files-and-connection-information"></a>Phone-Book arquivos e informações de conexão

Uma chamada de [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) deve especificar as informações que o Gerenciador de conexão de acesso remoto precisa para estabelecer a conexão. Normalmente, a chamada **RasDial** fornece as informações de conexão especificando uma entrada de catálogo telefônico. As informações de conexão em uma entrada de catálogo telefônico incluem números de telefone, taxas de bps, [informações de autenticação de usuário](user-authentication-information.md)e [outras informações de conexão](other-connection-information.md).

Um cliente RAS usa os parâmetros da função [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para especificar um arquivo de catálogo telefônico e uma entrada nesse arquivo. O parâmetro *lpszPhonebookPath* pode especificar o nome de um arquivo de catálogo telefônico ou pode ser **nulo** para indicar que o arquivo de catálogo telefônico padrão deve ser usado. O parâmetro *lpRasDialParams* aponta para uma estrutura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) que especifica o nome da entrada do catálogo telefônico a ser usada.

Para exibir uma lista de entradas de catálogo telefônico da qual o usuário pode selecionar uma conexão, um cliente RAS pode chamar a função [**RasEnumEntries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa) para enumerar as entradas em um arquivo de catálogo telefônico.

Para fazer uma conexão sem usar uma entrada de catálogo telefônico, a chamada [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) pode especificar uma cadeia de caracteres vazia para o membro **SzEntryName** da estrutura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) . O membro **RASDIALPARAMS. szPhoneNumber** deve conter o número a ser chamado. Nesse caso, o Gerenciador de conexão de acesso remoto usa a primeira porta de modem disponível e os valores padrão para todas as outras configurações.

 

 