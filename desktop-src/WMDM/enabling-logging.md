---
title: Habilitando o registro em log
description: Habilitando o registro em log
ms.assetid: 50fc1d71-b650-4ba5-a6e1-631c0b9fe8ad
keywords:
- Windows Gerenciador de Dispositivos de mídia, registro em log
- Gerenciador de Dispositivos, registro em log
- aplicativos de área de trabalho, registro em log
- provedores de serviços, registro em log
- Guia de programação, registro em log
- registro em log
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff937b2a3abd16f7319c3abb73a3a2159350049fff8c89d343cc5545f8a21ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585114"
---
# <a name="enabling-logging"></a>Habilitando o registro em log

Windows A mídia Gerenciador de Dispositivos fornece um objeto de log que pode salvar informações em um arquivo de texto em tempo de execução. Os desenvolvedores de aplicativos e provedores de serviços podem usar esse objeto para armazenar mensagens em um arquivo de log enquanto seu aplicativo ou provedor de serviços está em execução. esse objeto é especialmente útil ao manipular arquivos protegidos por drm, porque Windows mídia Gerenciador de Dispositivos não permitirá que você anexe um depurador a um processo que esteja manipulando arquivos protegidos por DRM.

O agente é um objeto com com a ID de classe CLSID \_ WMDMLogger que expõe uma interface, [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger). Os componentes não precisam de um certificado para usar o objeto de log.

por padrão, Windows mídia Gerenciador de Dispositivos mantém um arquivo de log, independentemente se um aplicativo usa **IWMDMLogger**. Esse arquivo de log é um arquivo de texto simples, e cada entrada inclui uma entrada precedida por um carimbo de data/hora no formato AAAAMMDDHHMMSS, usando a hora local de 24 horas. Windows A mídia Gerenciador de Dispositivos registra todas as chamadas à API, juntamente com as entradas que você adicionar chamando mensagens **IWMDMLogger** . Todas as entradas do arquivo de log são anexadas ao arquivo até que a [**redefinição**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-reset) seja chamada ou o arquivo exceda seu tamanho máximo. O arquivo é fechado automaticamente após cada operação de log. O mesmo arquivo de log é usado para entradas de aplicativo e de sistema.

As etapas a seguir mostram como usar o objeto de log:

1.  Inclua wmdmlog. h em seu projeto.
2.  Crie um objeto de log chamando **CoCreateInstance**(CLSID \_ WMDMLogger) e solicitando a interface **IWMDMLogger** . Atribua o ponteiro de interface a uma variável global.
3.  Verifique se o log está habilitado chamando [**IWMDMLogger:: IsEnabled**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-isenabled); Se não estiver, habilite-a chamando [**IWMDMLogger:: Enable**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-enable).
4.  Especifique um nome e um tamanho de arquivo de log personalizados. Isso é feito chamando [**IWMDMLogger:: Setlogfilename**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setlogfilename) e [**IWMDMLogger:: SetSizeParams**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setsizeparams).
5.  Em pontos no código em que você deseja fazer uma entrada no log, chame [**IWMDMLogger:: LogDword**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logdword) para cadeias de caracteres de log que contêm variáveis (esse método é semelhante a **wsprintf** da maneira que permite formatar uma cadeia de caracteres contendo um valor de variável) ou chamar [**IWMDMLogger:: LogString**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logstring) para registrar cadeias de caracteres constantes.

Para obter um exemplo de código, consulte as páginas de referência para os métodos de [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Tarefas comuns a aplicativos e provedores de serviços**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




