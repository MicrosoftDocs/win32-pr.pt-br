---
description: Quando um aplicativo habilitado para SOAP tiver sido exportado de um servidor no modo proxy, os clientes que o importarem poderão acessar automaticamente os métodos dos componentes que ele contém, remotamente, como serviços Web oferecidos pelo servidor no modo OBJECT ativado pelo cliente (OBJECT). Isso permite que você implante facilmente a funcionalidade de um aplicativo COM+ em uma rede como um serviço Web XML.
ms.assetid: 7f4783f7-4f53-4f0b-bb64-ae7903097d6c
title: Importando um SOAP-Enabled aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a41a60c2b5ca69197582a684920e9e935f28631779bc632810049f1a7d03945
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858916"
---
# <a name="importing-a-soap-enabled-application"></a>Importando um SOAP-Enabled aplicativo

Quando um aplicativo habilitado para SOAP tiver sido [exportado](exporting-a-soap-enabled-application.md) de um servidor no modo proxy, os clientes que o importarem poderão acessar automaticamente os métodos dos componentes que ele contém, remotamente, como serviços Web oferecidos pelo servidor no modo OBJECT ativado pelo cliente (OBJECT). Isso permite que você implante facilmente a funcionalidade de um aplicativo COM+ em uma rede como um serviço Web XML.

Quando os componentes de um aplicativo importado dessa maneira são usados no cliente, eles não são executados no cliente, mas são acessados remotamente usando o serviço Web XML fornecido pelo servidor do qual o aplicativo foi exportado. Para obter detalhes sobre como usar os componentes de um aplicativo importado dessa maneira, consulte [Acessando serviços Web XML no modo XML](accessing-xml-web-services-in-cao-mode.md).

## <a name="component-services-administrative-tool"></a>Ferramenta Administrativa dos Serviços de Componentes

Para importar um aplicativo habilitado para SOAP para um cliente, use as seguintes etapas:

1.  Na árvore de console da ferramenta administrativa serviços de componentes, em **Serviços** de Componentes, abra a pasta associada ao computador cliente no qual você deseja instalar o aplicativo.

2.  Clique com o botão direito do mouse na pasta **Aplicativos COM+** do cliente e escolha **Novo.** O **Assistente de Instalação de Aplicativo COM+ é** exibido.

3.  No Assistente **de Instalação do Aplicativo COM+,** clique em Instalar **aplicativos pré-construídos.**

4.  Procure a rede para localizar ou especificar o caminho de rede do arquivo MSI no servidor do qual você deseja instalar o aplicativo.

## <a name="visual-basic"></a>Visual Basic

Não se aplica.

## <a name="cc"></a>C/C++

Não se aplica.

## <a name="remarks"></a>Comentários

Os componentes COM são identificados por um GUID, que muda se os componentes são recompilados. Se um componente COM configurado que é exposto como um serviço Web XML for recompilado, os aplicativos cliente que o usam serão descompilados. Portanto, quando um componente exposto como um serviço Web XML é recompilado, os clientes devem importar os aplicativos que usam o componente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral do serviço COM+ SOAP](com--soap-service-overview.md)
</dt> <dt>

[Criando serviços Web XML](creating-xml-web-services.md)
</dt> <dt>

[Exportando um aplicativo SOAP-Enabled aplicativo](exporting-a-soap-enabled-application.md)
</dt> </dl>

 

 



