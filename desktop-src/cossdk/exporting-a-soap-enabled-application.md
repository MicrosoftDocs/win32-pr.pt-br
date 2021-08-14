---
description: Quando você usa COM+ para criar um serviço Web XML, esse serviço pode ser usado por qualquer cliente autorizado, incluindo aqueles que não usam COM+ ou até mesmo o Microsoft Windows.
ms.assetid: c40031a6-f3de-4ef4-b9aa-3f49e57da5b4
title: Exportando um aplicativo SOAP-Enabled aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce79bbc5dca59feb23ba9e976575b3b33570ecd27cf1e6a68560b02e073f48bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307283"
---
# <a name="exporting-a-soap-enabled-application"></a>Exportando um aplicativo SOAP-Enabled aplicativo

Quando você usa COM+ para criar um serviço Web XML, esse serviço pode ser usado por qualquer cliente autorizado, incluindo aqueles que não usam COM+ ou até mesmo o Microsoft Windows. No entanto, usar um serviço Web COM+ no modo de OBJETO ativado pelo cliente (OBJECT) de um aplicativo cliente COM+ é especialmente fácil. Basta exportar o aplicativo habilitado para SOAP [](importing-a-soap-enabled-application.md) no modo proxy e importá-lo para o cliente para o qual você deseja acessar o serviço Web XML correspondente.

## <a name="component-services-administrative-tool"></a>Ferramenta Administrativa dos Serviços de Componentes

Para exportar um aplicativo habilitado para SOAP de um servidor, use as seguintes etapas:

1.  Na árvore de console da ferramenta administrativa serviços de componentes, em **Serviços** de Componentes, abra a pasta Aplicativos **COM+** associada ao computador que você deseja gerenciar.

2.  Clique com o botão direito do mouse no componente que você deseja expor como um serviço Web XML e escolha **Exportar**. O **Assistente de Exportação de Aplicativos COM+** é exibido.

3.  Na caixa de texto rotulada Insira o caminho completo e o nome do arquivo de aplicativo a ser **criado,** insira o  caminho completo e o nome de arquivo para o arquivo MSI que conterá o aplicativo exportado ou clique em Procurar para selecionar o caminho completo e o nome do arquivo usando uma caixa de diálogo.

4.  Em **Exportar como**, selecione o botão Proxy de Aplicativo – Instalar em outros computador para **habilitar o acesso a esse** computador.

## <a name="visual-basic"></a>Visual Basic

Não se aplica.

## <a name="cc"></a>C/C++

Não se aplica.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral do serviço COM+ SOAP](com--soap-service-overview.md)
</dt> <dt>

[Criando serviços Web XML](creating-xml-web-services.md)
</dt> <dt>

[Importando um SOAP-Enabled aplicativo](importing-a-soap-enabled-application.md)
</dt> </dl>

 

 



