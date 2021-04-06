---
description: Quando você usa o COM+ para criar um serviço Web XML, esse serviço pode ser usado por qualquer cliente autorizado, incluindo aqueles que não usam COM+ ou mesmo Microsoft Windows.
ms.assetid: c40031a6-f3de-4ef4-b9aa-3f49e57da5b4
title: Exportando um aplicativo SOAP-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d5c92029f431fc06964f233c5746c283821d11c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826516"
---
# <a name="exporting-a-soap-enabled-application"></a>Exportando um aplicativo SOAP-Enabled

Quando você usa o COM+ para criar um serviço Web XML, esse serviço pode ser usado por qualquer cliente autorizado, incluindo aqueles que não usam COM+ ou mesmo Microsoft Windows. No entanto, usar um serviço Web COM+ no modo CAO (objeto ativado pelo cliente) de um aplicativo cliente do COM+ é especialmente fácil. Basta exportar o aplicativo habilitado para SOAP no modo proxy e, em seguida, [importá](importing-a-soap-enabled-application.md) -lo para o cliente para o qual você deseja acessar o Web Service XML correspondente.

## <a name="component-services-administrative-tool"></a>Ferramenta administrativa serviços de componentes

Para exportar um aplicativo habilitado para SOAP de um servidor, use as seguintes etapas:

1.  Na árvore de console da ferramenta administrativa serviços de componentes, em **serviços de componentes**, abra a pasta **aplicativos com+** associada ao computador que você deseja gerenciar.

2.  Clique com o botão direito do mouse no componente que você deseja expor como um serviço Web XML e escolha **Exportar**. O **Assistente para exportação de aplicativos com+** é exibido.

3.  Na caixa de texto rotulada, **Insira o caminho completo e o nome do arquivo do aplicativo a ser criado**, insira o caminho completo e o nome do arquivo do MSI que conterá o aplicativo exportado ou clique em **procurar** para selecionar o caminho completo e o nome do arquivo usando uma caixa de diálogo.

4.  Em **exportar como**, selecione o botão de opção **proxy de aplicativo – instalar em outros computadores para habilitar o acesso a este computador** .

## <a name="visual-basic"></a>Visual Basic

Não se aplica.

## <a name="cc"></a>C/C++

Não se aplica.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral do serviço SOAP COM+](com--soap-service-overview.md)
</dt> <dt>

[Criando Serviços Web XML](creating-xml-web-services.md)
</dt> <dt>

[Importando um aplicativo SOAP-Enabled](importing-a-soap-enabled-application.md)
</dt> </dl>

 

 



