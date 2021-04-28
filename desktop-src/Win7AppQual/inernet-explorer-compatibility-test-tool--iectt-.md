---
description: IECTT (Internet Explorer Compatibility Test Tool)
ms.assetid: 11169540-555A-48A9-A4CD-535D5765C005
title: IECTT (Internet Explorer Compatibility Test Tool)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3a35b3120e95c668f2808c9c525d0c1d4f89f8f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088280"
---
# <a name="internet-explorer-compatibility-test-tool-iectt"></a>IECTT (Internet Explorer Compatibility Test Tool)

A ferramenta de teste de compatibilidade do Internet Explorer (IECTT) é um componente do [Kit de ferramentas de compatibilidade de aplicativos da Microsoft](/windows-hardware/get-started/adk-install). Essa ferramenta pode ajudá-lo a diagnosticar problemas em seus aplicativos Web exibindo problemas em tempo real e, opcionalmente, carregando os resultados em um banco de dados ACT. Os resultados incluem detalhes sobre possíveis problemas de compatibilidade e links para obter mais informações sobre cada problema de compatibilidade. O IECTT também permite que você exclua problemas e modifique os atributos disponíveis.

## <a name="to-open-iectt"></a>Para abrir o IECTT

1.  Instale o [Kit de ferramentas de compatibilidade de aplicativos da Microsoft](/windows-hardware/get-started/adk-install).
2.  Clique em **Iniciar**, aponte para **programas**, aponte para kit de ferramentas de compatibilidade de **aplicativos da Microsoft 5,6**, aponte para ferramentas para **desenvolvedores e testadores** e clique em **ferramenta de teste de compatibilidade do Internet Explorer**.

As seções a seguir descrevem cenários comuns de IECTT.

## <a name="view-issues-in-real-time"></a>Exibir problemas em tempo real

Você pode localizar e exibir seus problemas baseados na Web em tempo real, enquanto testa seus sites e aplicativos Web no Windows Internet Explorer 7 e no Windows Internet Explorer 8. Depois de concluir o teste, você poderá exibir os resultados na tela de **dados ao vivo** do IECTT.

## <a name="upload-issues-to-your-act-database"></a>Carregar problemas em seu banco de dados ACT

Você pode carregar seus problemas baseados na Web no banco de dados ACT, que processa as informações e permite que você exiba seus resultados na tela **analisar** do Gerenciador de compatibilidade de aplicativos.

## <a name="collect-your-compatibility-data"></a>Coletar seus dados de compatibilidade

Você pode coletar os dados de compatibilidade relacionados ao seu site e ao aplicativo Web usando a ferramenta IECTT com o Internet Explorer 7 ou o Internet Explorer 7.

**Para coletar os dados de compatibilidade**

1.  Feche todas as janelas ativas do Internet Explorer do Windows.
2.  No IECTT, na barra de ferramentas da **ferramenta de teste de compatibilidade do Internet Explorer** , clique em **habilitar**.
3.  Abra uma janela do Internet Explorer 7 ou do Internet Explorer 8.

    Uma mensagem é exibida e indica que o log de avaliação de compatibilidade está ativado.

4.  Visite os sites ou aplicativos Web que são necessários para uso por sua organização. À medida que você visita cada site, a ferramenta IECTT exibe, em tempo real, os possíveis problemas de compatibilidade.
5.  Na barra de ferramentas da **ferramenta de teste de compatibilidade do Internet Explorer** , clique em **desabilitar** quando terminar.

    O processo de log de compatibilidade é concluído e interrompido.

## <a name="filter-your-issue-results"></a>Filtrar os resultados do problema

Você pode filtrar qualquer um dos resultados do IECTT por nome de objeto, por tipo de problema ou por ambos.

**Para filtrar os resultados do problema**

1.  Na tela da **ferramenta de teste de compatibilidade do Internet Explorer** , clique em **Filtrar**.

    A caixa de diálogo **filtro de problemas** é exibida.

2.  Insira o nome do objeto que você pretende exibir na caixa **digite o nome do objeto para o qual exibir os problemas** .

Para obter mais informações sobre essa ferramenta e outras ferramentas de desenvolvedores, consulte o [que é a ferramenta de teste de compatibilidade do Internet Explorer?](/previous-versions/windows/it-pro/windows-7/cc721989(v=ws.10)) na biblioteca MSDN e a postagem [no blog log de compatibilidade de aplicativos no IE8](/archive/blogs/ie/application-compatibility-logging-in-ie8) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ferramentas para depuração de aplicativos Web e Complementos](tools-for-debugging-web-applications-and-add-ons.md)
</dt> </dl>

 

 
