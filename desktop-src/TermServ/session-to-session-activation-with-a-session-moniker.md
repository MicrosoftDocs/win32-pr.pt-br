---
title: Ativação de sessão para sessão com um Moniker de sessão
description: A ativação de sessão para sessão (também chamada de ativação entre sessões) permite que um processo do cliente inicie (ative) um processo de servidor local em uma sessão especificada.
ms.assetid: d405c276-040b-4cde-aeb2-482a25e2867f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213627facdd2dee9e4ba7cc698d2be5455424b4394d295448a07aeb52788dd42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988126"
---
# <a name="session-to-session-activation-with-a-session-moniker"></a>Ativação de sessão para sessão com um Moniker de sessão

A ativação de sessão para sessão (também chamada de ativação entre sessões) permite que um processo do cliente inicie (ative) um processo de servidor local em uma sessão especificada. Esse recurso está disponível para aplicativos configurados para executar no contexto de segurança do usuário interativo, também conhecido como modo de ativação de objeto "Usuário Interativo RunAs". Para obter mais informações sobre contextos de segurança, consulte [Contexto de segurança do cliente.](/windows/desktop/SecAuthZ/the-client-security-context)

O COM distribuído (DCOM) habilita a ativação de objeto por sessão usando um [Moniker](session-monikers.md)de Sessão fornecido pelo sistema. Outros [monikers](../com/composite-monikers.md)fornecidos pelo sistema incluem monikers de arquivo , [monikers](../com/file-monikers.md)de [item,](../com/item-monikers.md)monikers de composição genéricos, [anti-monikers](../com/anti-monikers.md), [monikers](../com/pointer-monikers.md)de ponteiro e [monikers de URL](../com/url-monikers.md).

Para poder usar o moniker de sessão, o aplicativo DCOM deve ser definido para ser executado como o usuário interativo. Isso pode ser definido usando a ferramenta Administrativa dos Serviços de Componentes, exibindo as Propriedades do aplicativo DCOM e selecionando O usuário **interativo** na **guia** Identidade. Para obter mais informações sobre os possíveis riscos de segurança associados à configuração de um aplicativo DCOM para ser executado como o usuário interativo em um ambiente Serviços de Área de Trabalho Remota, consulte a seção "Identidade do Aplicativo (COM)" da documentação COM no SDK (Kit de Desenvolvimento de Software de Plataforma).

Se qualquer outro tipo de usuário for selecionado para executar o aplicativo, o moniker de sessão será ignorado pelo aplicativo. O moniker de sessão também é ignorado por aplicativos de servidor COM+. Para obter mais informações sobre outros métodos para selecionar o tipo de usuário para executar o aplicativo, consulte a documentação COM no SDK da Plataforma.

Para criar um moniker de sessão, você deve compor a ID de sessão da sessão Serviços de Área de Trabalho Remota com um moniker de classe que especifica a ID de classe do servidor de processo.

**Para criar um moniker de sessão**

1.  Prefixe o nome de exibição do moniker de classe com o nome de exibição do moniker de sessão usando a seguinte sintaxe:

    ``` syntax
    "Session:[digits]!clsid:[class id]"
    ```

    em *que dígitos* representam a ID de sessão da sessão na qual o processo do servidor será iniciado e onde a *ID* da classe representa a ID de classe do servidor. Observe que a ID da sessão é um número de base 10.

    Para computadores que estão executando o Windows XP ou posterior, o uso da sintaxe a seguir resultará no envio com a ativação para a sessão de console físico ativa no momento, seja qual for sua ID de sessão:

    ``` syntax
    "Session:Console!clsid:[class id]"
    ```

2.  Depois de criar o moniker de sessão, você pode passar o resultado para a função [**MkParseDisplayName**](/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname) ou para a [função MkParseDisplayNameEx.](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85))

Você pode usar um moniker de sessão da mesma maneira que usaria qualquer outro moniker.

Para um exemplo de código que demonstra como ativar um processo de servidor local em uma sessão especificada, consulte [Usando um Moniker de sessão](using-a-session-moniker.md).

Para obter mais informações sobre a ativação de objeto, monikers fornecidos pelo sistema e monikers de classe, consulte a documentação com no SDK da plataforma.

> [!Note]  
> Os processos criados entre sessões têm um limite superior no tamanho do bloco de ambiente. Esse limite é de cerca de 4 KB, mas pode ser maior ou menor dependendo de quais outras informações são necessárias para criar o processo (por exemplo, nomes de arquivo, diretórios e parâmetros para o novo processo).

 

 

 