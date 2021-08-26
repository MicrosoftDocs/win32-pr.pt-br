---
description: IECTT (Internet Explorer Compatibility Test Tool)
ms.assetid: 11169540-555A-48A9-A4CD-535D5765C005
title: IECTT (Internet Explorer Compatibility Test Tool)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12209664dc5aca037b30d938f9c25c9a0e25d02d84019c1a3cb43056a3af06df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998936"
---
# <a name="internet-explorer-compatibility-test-tool-iectt"></a>IECTT (Internet Explorer Compatibility Test Tool)

A IECTT (Internet Explorer de Teste de Compatibilidade) é um componente do Microsoft [Application Compatibility Toolkit](/windows-hardware/get-started/adk-install). Essa ferramenta pode ajudá-lo a diagnosticar problemas em seus aplicativos Web exibindo problemas em tempo real e, opcionalmente, carregando os resultados em um banco de dados ACT. Os resultados incluem detalhes sobre possíveis problemas de compatibilidade e links para obter mais informações sobre cada problema de compatibilidade. O IECTT também permite que você exclua problemas e modifique os atributos disponíveis.

## <a name="to-open-iectt"></a>Para abrir o IECTT

1.  Instale o [microsoft application compatibility Toolkit](/windows-hardware/get-started/adk-install).
2.  Clique em Iniciar , aponte para Programas **,** aponte para Microsoft **Application Compatibility Toolkit 5.6**, aponte para Ferramentas de Desenvolvedor e **Testador** e clique em Internet Explorer Ferramenta de Teste de **Compatibilidade**.

As seções a seguir descrevem cenários comuns de IECTT.

## <a name="view-issues-in-real-time"></a>Exibir problemas em tempo real

Você pode localizar e exibir seus problemas baseados na Web em tempo real, enquanto está testando seus sites e aplicativos Web no Windows Internet Explorer 7 e Windows Internet Explorer 8. Depois de concluir o teste, você poderá exibir os resultados na tela **Dados Ao** Vivo do IECTT.

## <a name="upload-issues-to-your-act-database"></a>Upload Problemas com o banco de dados ACT

Você pode carregar seus problemas baseados na Web no banco de dados ACT,  que processa as informações e permite exibir os resultados na tela Analisar do Gerenciador de Compatibilidade de Aplicativos.

## <a name="collect-your-compatibility-data"></a>Coletar seus dados de compatibilidade

Você pode coletar seus dados de compatibilidade relacionados ao site e ao aplicativo Web usando a ferramenta IECTT com Internet Explorer 7 ou Internet Explorer 7.

**Para coletar seus dados de compatibilidade**

1.  Feche todas as janelas de Windows Internet Explorer ativa.
2.  No IECTT, na barra de ferramentas **Internet Explorer ferramenta de** teste de compatibilidade, clique em **Habilitar**.
3.  Abra uma Internet Explorer 7 ou Internet Explorer 8.

    Uma mensagem é exibida e indica que o log de avaliação de compatibilidade está ligado.

4.  Visite os sites ou aplicativos Web que são necessários para uso pela sua organização. Conforme você visita cada site, a ferramenta IECTT exibe, em tempo real, seus possíveis problemas de compatibilidade.
5.  Na barra **de ferramentas Internet Explorer Ferramenta de Teste** de Compatibilidade, clique em **Desabilitar** quando terminar.

    O processo de registro em log de compatibilidade termina e é interrompido.

## <a name="filter-your-issue-results"></a>Filtrar os resultados do problema

Você pode filtrar qualquer um dos resultados de IECTT por nome de objeto, por tipo de problema ou por ambos.

**Para filtrar os resultados do problema**

1.  Na tela **Internet Explorer ferramenta de teste de compatibilidade,** clique em **Filtrar**.

    A **caixa de diálogo Filtro** de Problemas é exibida.

2.  Insira o nome do objeto que você pretende exibir na caixa Inserir o nome do objeto **para exibir problemas.**

Para obter mais informações sobre essa ferramenta e outras ferramentas de desenvolvedores, consulte O que é a ferramenta de teste de compatibilidade do [Internet Explorer?](/previous-versions/windows/it-pro/windows-7/cc721989(v=ws.10)) na postagem de blog Biblioteca MSDN e Registro em log de compatibilidade de aplicativos [no IE8.](/archive/blogs/ie/application-compatibility-logging-in-ie8)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ferramentas para depurar aplicativos Web e complementos](tools-for-debugging-web-applications-and-add-ons.md)
</dt> </dl>

 

 
