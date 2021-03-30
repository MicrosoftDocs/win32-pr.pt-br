---
title: Ativação de sessão para sessão com um moniker de sessão
description: A ativação de sessão para sessão (também chamada de ativação entre sessões) permite que um processo de cliente inicie (ative) um processo de servidor local em uma sessão especificada.
ms.assetid: d405c276-040b-4cde-aeb2-482a25e2867f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2714f3dbe7b23c8b7f04d4271018891960b87f76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641679"
---
# <a name="session-to-session-activation-with-a-session-moniker"></a>Ativação de sessão para sessão com um moniker de sessão

A ativação de sessão para sessão (também chamada de ativação entre sessões) permite que um processo de cliente inicie (ative) um processo de servidor local em uma sessão especificada. Esse recurso está disponível para aplicativos que são configurados para execução no contexto de segurança do usuário interativo, também conhecido como o modo de ativação de objeto "RunAs Interactive User". Para obter mais informações sobre contextos de segurança, consulte [o contexto de segurança do cliente](/windows/desktop/SecAuthZ/the-client-security-context).

O COM distribuído (DCOM) permite a ativação de objeto por sessão usando um [moniker de sessão](session-monikers.md)fornecido pelo sistema. Outros monikers fornecidos pelo sistema incluem [identificadores de arquivo](../com/file-monikers.md), [monikers de item](../com/item-monikers.md), [monikers compostos](../com/composite-monikers.md)genéricos, [antimonikers](../com/anti-monikers.md), [monikers de ponteiro](../com/pointer-monikers.md)e [identificadores de URL](../com/url-monikers.md).

Para poder usar o moniker da sessão, o aplicativo DCOM deve ser definido para ser executado como usuário interativo. Isso pode ser definido usando a ferramenta administrativa serviços de componentes, exibindo as propriedades do aplicativo DCOM e selecionando **o usuário interativo** na guia **identidade** . Para obter mais informações sobre os possíveis riscos de segurança associados à definição de um aplicativo DCOM para ser executado como usuário interativo em um ambiente de Serviços de Área de Trabalho Remota, consulte a seção "identidade do aplicativo (COM)" da documentação COM do SDK (Software Development Kit) da plataforma.

Se qualquer outro tipo de usuário for selecionado para executar o aplicativo, o moniker da sessão será ignorado pelo aplicativo. O moniker da sessão também é ignorado por aplicativos do servidor COM+. Para obter mais informações sobre outros métodos para selecionar o tipo de usuário para executar o aplicativo, consulte a documentação COM no SDK da plataforma.

Para criar um moniker de sessão, você deve compor a ID de sessão da sessão de Serviços de Área de Trabalho Remota com um moniker de classe que especifica a ID de classe do servidor de processo.

**Para criar um moniker de sessão**

1.  Prefixe o nome de exibição do moniker da classe com o nome de exibição do moniker da sessão usando a seguinte sintaxe:

    ``` syntax
    "Session:[digits]!clsid:[class id]"
    ```

    em que *dígitos* representa a ID da sessão na qual o processo do servidor será iniciado e onde ID da *classe* representa a ID de classe do servidor. Observe que a ID de sessão é um número de base 10.

    Para computadores que executam o Windows XP ou posterior, usar a seguinte sintaxe resultará em COM enviando a ativação para a sessão de console físico ativa atualmente, independentemente de sua ID de sessão:

    ``` syntax
    "Session:Console!clsid:[class id]"
    ```

2.  Depois de criar o moniker da sessão, você pode passar o resultado para a função [**MkParseDisplayName**](/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname) ou para a função [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) .

Você pode usar um moniker de sessão da mesma maneira que usaria qualquer outro moniker.

Para obter um exemplo de código que demonstra como ativar um processo de servidor local em uma sessão especificada, consulte [usando um moniker de sessão](using-a-session-moniker.md).

Para obter mais informações sobre a ativação de objeto, identificadores de classe e identificadores de classes fornecidos pelo sistema, consulte a documentação COM no SDK da plataforma.

> [!Note]  
> Os processos criados entre as sessões têm um limite superior ao tamanho do bloco de ambiente. Esse limite é de cerca de 4 KB, mas pode ser maior ou menor dependendo de quais outras informações são necessárias para criar o processo (por exemplo, nomes de arquivo, diretórios e parâmetros para o novo processo).

 

 

 