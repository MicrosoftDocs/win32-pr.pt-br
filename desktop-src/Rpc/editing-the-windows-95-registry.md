---
title: Editando o registro do Windows 95
description: Você pode usar o REGEDIT para editar o registro do Windows 95 para designar um NSP.
ms.assetid: 109daf4a-722f-4a25-a778-72360ee07ad9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c622ea44a5e365ca631d6d4db34af8e939ea6487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822946"
---
# <a name="editing-the-windows-95-registry"></a>Editando o registro do Windows 95

Você pode usar o REGEDIT para editar o registro do Windows 95 para designar um NSP.

**Para designar um provedor de serviços de Microsoft Locator Name para Windows 95**

1.  Selecionar

    **HKEY \_ SOFTWARE do \_ computador local** \\  \\ **Microsoft** \\ **RPC**

2.  Criar uma nova chave chamada

    **NameService**

3.  Com a chave **NameService** selecionada, crie os novos nomes de **StringValue** e modifique-os para conter dados, conforme mostrado na tabela a seguir.

    

    | Nome                     | Dados                                                                        |
    |--------------------------|-----------------------------------------------------------------------------|
    | **Defaultsyntax**        | 3<br/>                                                                |
    | **Protocolo**             | ncacn \_ NP<br/>                                                        |
    | **Ponto de extremidade**             | \\\\localizador de pipe<br/>                                                  |
    | **NetworkAddress**       | meuservidor (em que meuservidor é o nome do computador com Windows NT)<br/> |
    | **ServerNetworkAddress** | meuservidor<br/>                                                         |

    

     

Você pode usar o REGEDIT para editar o registro do Windows 95 para designar um NSP de CDS do DCE.

**Para designar um provedor de serviços de nome de CDS DCE para Windows 95**

1.  Selecionar

    **HKEY \_ SOFTWARE do \_ computador local** \\  \\ **Microsoft** \\ **RPC**

2.  Criar uma nova chave chamada

    **NameService**

3.  Com a chave **NameService** selecionada, crie os novos nomes de **StringValue** e modifique-os para conter dados, conforme mostrado na tabela a seguir.

    

    | Nome                     | Dados                                                             |
    |--------------------------|------------------------------------------------------------------|
    | **Defaultsyntax**        | 3<br/>                                                     |
    | **Protocolo**             | \_TCP IP \_ ncacn<br/>                                        |
    | **Ponto de extremidade**             | "" (uma cadeia de caracteres vazia)<br/>                                  |
    | **NetworkAddress**       | meuservidor (o nome do computador host que executa o nsid)<br/> |
    | **ServerNetworkAddress** | meuservidor (o nome do computador host que executa o nsid)<br/> |

    

     

    > [!Note]  
    > Você deve ter o produto serviço de diretório de célula do DCE do Digital Equipment Corporation para configurar os CDS do DCE como seu provedor de serviços de nome. Consulte a documentação fornecida pela Digital Equipment Corporation para obter informações sobre os CDS da DCE.

     

 

 





