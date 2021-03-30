---
title: Manuais de telefones RAS
description: Os catálogos telefônicos fornecem uma maneira padrão de coletar e especificar as informações que o Gerenciador de conexões de acesso remoto precisa para estabelecer uma conexão remota.
ms.assetid: db6d076c-c683-4e27-ace1-d2c0cd0931f6
keywords:
- Catálogos telefônicos, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bbdfe7d2293f87e01fe33f3a078f861a35a732d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005617"
---
# <a name="ras-phone-books"></a>Manuais de telefones RAS

Os catálogos telefônicos fornecem uma maneira padrão de coletar e especificar as informações que o Gerenciador de conexões de acesso remoto precisa para estabelecer uma conexão remota. Os catálogos telefônicos associam nomes de entrada com informações como números de telefone, portas COM e configurações de modem. Cada entrada do catálogo telefônico contém as informações necessárias para estabelecer uma conexão RAS.

Os catálogos telefônicos são armazenados em arquivos de catálogo telefônico, que são arquivos de texto que contêm os nomes de entrada e as informações associadas. O RAS cria um arquivo de catálogo telefônico chamado RASPHONE. PBK. O usuário pode usar a caixa de diálogo **rede dial-up** principal para criar arquivos de catálogo telefônico pessoal. Atualmente, a API RAS não oferece suporte para a criação de um arquivo de catálogo telefônico. Algumas funções de RAS, como a função [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) , têm um parâmetro que especifica um arquivo de catálogo telefônico. Se o chamador não especificar um arquivo de catálogo telefônico, a função usará o arquivo de catálogo telefônico padrão, que é aquele selecionado pelo usuário na folha de propriedades **preferências do usuário** da caixa de diálogo **rede dial-up** .

O Windows NT 4,0 fornece as funções [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) e [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) que exibem a interface do usuário RAS interna que permite que os usuários trabalhem com catálogos telefônicos e entradas de catálogo telefônico.

**Windows 95:** A rede dial-up armazena entradas de catálogo telefônico no registro em vez de em um arquivo de catálogo telefônico. O Windows 95 não oferece suporte a arquivos de catálogo telefônico pessoais ou funções que exibem as caixas de diálogo internas de RAS.

 

 




