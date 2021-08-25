---
title: livros de Telefone RAS
description: os livros de Telefone fornecem uma maneira padrão de coletar e especificar as informações que o gerenciador de conexões de acesso remoto precisa para estabelecer uma conexão remota.
ms.assetid: db6d076c-c683-4e27-ace1-d2c0cd0931f6
keywords:
- livros de Telefone, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba80b11696df220a904a13685855818b945794c17b9bd4233e9f897592ee7b7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868416"
---
# <a name="ras-phone-books"></a>livros de Telefone RAS

os livros de Telefone fornecem uma maneira padrão de coletar e especificar as informações que o gerenciador de conexões de acesso remoto precisa para estabelecer uma conexão remota. Telefone livros associam nomes de entrada com informações como números de telefone, portas COM e configurações de modem. Cada entrada do catálogo telefônico contém as informações necessárias para estabelecer uma conexão RAS.

os livros de Telefone são armazenados em arquivos de catálogo telefônico, que são arquivos de texto que contêm os nomes de entrada e as informações associadas. O RAS cria um arquivo de catálogo telefônico chamado RASPHONE. PBK. O usuário pode usar a caixa de diálogo **rede dial-up** principal para criar arquivos de catálogo telefônico pessoal. Atualmente, a API RAS não oferece suporte para a criação de um arquivo de catálogo telefônico. Algumas funções de RAS, como a função [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) , têm um parâmetro que especifica um arquivo de catálogo telefônico. Se o chamador não especificar um arquivo de catálogo telefônico, a função usará o arquivo de catálogo telefônico padrão, que é aquele selecionado pelo usuário na folha de propriedades **preferências do usuário** da caixa de diálogo **rede dial-up** .

Windows NT 4,0 fornece as funções [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) e [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) que exibem a interface do usuário RAS interna que permite que os usuários trabalhem com catálogos telefônicos e entradas de catálogo telefônico.

**Windows 95:** A rede dial-up armazena entradas de catálogo telefônico no registro em vez de em um arquivo de catálogo telefônico. Windows 95 não oferece suporte a arquivos de catálogo telefônico pessoais ou funções que exibem as caixas de diálogo internas de RAS.

 

 




