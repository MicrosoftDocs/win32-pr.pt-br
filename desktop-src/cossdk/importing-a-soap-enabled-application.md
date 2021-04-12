---
description: Quando um aplicativo habilitado para SOAP é exportado de um servidor no modo proxy, os clientes que o importam podem acessar automaticamente os métodos dos componentes que ele contém, remotamente, como serviços Web oferecidos pelo servidor no modo CAO (objeto ativado pelo cliente). Isso permite que você implante com facilidade a funcionalidade de um aplicativo COM+ em uma rede como um serviço Web XML.
ms.assetid: 7f4783f7-4f53-4f0b-bb64-ae7903097d6c
title: Importando um aplicativo SOAP-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9faca91a726caea765d4b2ca227ddba0ff3a2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501087"
---
# <a name="importing-a-soap-enabled-application"></a>Importando um aplicativo SOAP-Enabled

Quando um aplicativo habilitado para SOAP é [exportado](exporting-a-soap-enabled-application.md) de um servidor no modo proxy, os clientes que o importam podem acessar automaticamente os métodos dos componentes que ele contém, remotamente, como serviços Web oferecidos pelo servidor no modo Cao (objeto ativado pelo cliente). Isso permite que você implante com facilidade a funcionalidade de um aplicativo COM+ em uma rede como um serviço Web XML.

Quando os componentes de um aplicativo importados dessa maneira são usados no cliente, eles não são executados no cliente, mas, em vez disso, são acessados remotamente usando o serviço Web XML fornecido pelo servidor do qual o aplicativo foi exportado. Para obter detalhes sobre como usar os componentes de um aplicativo importado dessa forma, consulte [acessando serviços Web XML no modo Cao](accessing-xml-web-services-in-cao-mode.md).

## <a name="component-services-administrative-tool"></a>Ferramenta administrativa serviços de componentes

Para importar um aplicativo habilitado para SOAP em um cliente, use as seguintes etapas:

1.  Na árvore de console da ferramenta administrativa serviços de componentes, em **serviços de componentes**, abra a pasta associada ao computador cliente no qual você deseja instalar o aplicativo.

2.  Clique com o botão direito do mouse na pasta **aplicativos com+** do cliente e escolha **novo**. O **Assistente de instalação do aplicativo com+** é exibido.

3.  No **Assistente de instalação de aplicativo com+**, clique em **instalar aplicativos pré-criados**.

4.  Procure a rede para localizar ou especificar o caminho de rede do arquivo MSI no servidor do qual você deseja instalar o aplicativo.

## <a name="visual-basic"></a>Visual Basic

Não se aplica.

## <a name="cc"></a>C/C++

Não se aplica.

## <a name="remarks"></a>Comentários

Os componentes COM são identificados por um GUID, que altera se os componentes são recompilados. Se um componente COM configurado que é exposto como um serviço Web XML for recompilado, os aplicativos cliente que o utilizam serão interrompidos. Portanto, quando um componente exposto como um serviço Web XML é recompilado, os clientes devem importar novamente os aplicativos que usam o componente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral do serviço SOAP COM+](com--soap-service-overview.md)
</dt> <dt>

[Criando Serviços Web XML](creating-xml-web-services.md)
</dt> <dt>

[Exportando um aplicativo SOAP-Enabled](exporting-a-soap-enabled-application.md)
</dt> </dl>

 

 



