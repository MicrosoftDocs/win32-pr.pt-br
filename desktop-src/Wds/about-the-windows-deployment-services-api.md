---
title: sobre a API dos serviços de implantação Windows
description: Windows o WDS (serviços de implantação) é um conjunto de componentes que habilitam a implantação de sistemas operacionais Windows, particularmente Windows Vista e posterior e Windows Server 2008 e posterior.
ms.assetid: 5742e51a-70e3-4607-bfb7-181362dfb168
keywords:
- Windows serviços de implantação Windows serviços de implantação, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dd65f18c1628236358d61656c8c3b414d180e43166daa86dfa6562024252a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098676"
---
# <a name="about-the-windows-deployment-services-api"></a>sobre a API dos serviços de implantação Windows

Windows o WDS (serviços de implantação) é um conjunto de componentes que habilitam a implantação de sistemas operacionais Windows, particularmente Windows Vista e posterior e Windows Server 2008 e posterior. Você pode usá-lo para configurar novos computadores usando instalações baseadas em rede.

OEMs, integradores de sistemas e profissionais de ti corporativos que procuram informações sobre como implantar Windows em novos computadores, devem ver as informações sobre a solução WDS padrão no [guia passo a passo de atualização dos serviços de implantação Windows](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) e o [WAIK (Kit de instalação automatizada) do Windows](https://www.microsoft.com/download/details.aspx?id=10333).

Em ambientes em que a solução WDS padrão não pode ser usada, a API do WDS permite o acesso programático a alguns componentes do WDS.

-   o [Windows funções de servidor dos serviços de implantação](windows-deployment-services-server-functions.md) fornecem acesso programático ao servidor WDS Pre-Boot Execution Environment (PXE). Os componentes do servidor do WDS incluem um servidor PXE e o trivial protocolo FTP (TFTP) para a inicialização da rede de um computador para carregar e instalar um sistema operacional.
-   o [Windows funções de cliente dos serviços de implantação](windows-deployment-services-client-functions.md) fornecem acesso programático ao cliente WDS. os componentes do cliente do WDS incluem uma interface gráfica do usuário que é executada dentro do ambiente de pré-instalação do Windows (Windows PE) e se comunica com os componentes do servidor para selecionar e instalar uma imagem do sistema operacional.
-   Não há API para os componentes de gerenciamento do WDS. Esses componentes são um conjunto de ferramentas que você usa para gerenciar o servidor, as imagens do sistema operacional e as contas de computador cliente. para obter mais informações sobre os componentes de gerenciamento do WDS, consulte [o guia passo a passo de atualização dos serviços de implantação do Windows](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)).

O servidor PXE do WDS consiste em um servidor PXE e um provedor PXE. O servidor PXE contém o recurso de rede principal. O servidor PXE dá suporte a interfaces de plug-in que são conhecidas como provedores PXE. Esse modelo de provedor permite o desenvolvimento de soluções PXE personalizadas enquanto continua a usar a base de código de rede do servidor PXE principal.

-   os desenvolvedores podem usar as [funções de servidor de serviços de implantação Windows](windows-deployment-services-server-functions.md) para gravar uma DLL para que um provedor personalizado substitua ou execute em conjunto com a camada de negociação de informações de inicialização (BINL) padrão em um servidor WDS. Por exemplo, o provedor personalizado pode usar um arquivo de texto como seu armazenamento de dados em vez de Active Directory.
-   os desenvolvedores podem usar as [funções de servidor de serviços de implantação Windows](windows-deployment-services-server-functions.md) para gravar um provedor de filtro que é sequenciado antes de BINL, ou qualquer outro provedor PXE, na lista ordenada de provedores registrados. O segundo provedor, em seguida, apenas solicita solicitações PXE selecionadas, enquanto o primeiro provedor lida com outras solicitações. Por exemplo, isso pode habilitar o segundo provedor registrado na lista ordenada para oferecer nova funcionalidade sem interromper a solução de WDS existente implementada no primeiro provedor.

o cliente do WDS inclui uma interface gráfica do usuário que é executada dentro do ambiente de pré-instalação do Windows (Windows PE) e se comunica com os componentes do servidor para selecionar e instalar uma imagem do sistema operacional. A biblioteca de cliente do WDS dá suporte ao desenvolvimento de aplicativos cliente personalizados que podem usar um servidor WDS.

-   os desenvolvedores podem usar as [funções de cliente de serviços de implantação Windows](windows-deployment-services-client-functions.md) para gravar seu próprio aplicativo cliente personalizado que substitui o cliente WDS. Por exemplo, o aplicativo personalizado pode enumerar as imagens armazenadas em um servidor do WDS e enviar mensagens de progresso da instalação para o log de eventos do servidor PXE.

## <a name="windows-deployment-services-samples"></a>Windows Exemplos de serviços de implantação

um exemplo de provedor PXE personalizado, provedor de filtro e aplicativo cliente WDS está disponível no microsoft Windows software development kit (sdk), consulte [microsoft Windows software development kit](https://developer.microsoft.com/windows/downloads/windows-10-sdk/).

Você pode baixar os seguintes exemplos do WDS online na [Galeria de códigos da área de trabalho](https://github.com/microsoft/Windows-classic-samples).

<dl>

[Windows Exemplo de provedor de filtro de serviços de implantação](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/FilterProvider)  
[Windows Exemplo de enumeração de imagem dos serviços de implantação](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/ImageEnumeration)  
[Windows Exemplo de consumidor multicast dos serviços de implantação](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Multicast/WdsProvider)  
[Windows Exemplo de provedor multicast dos serviços de implantação](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Multicast/WdsProvider)  
[Windows Exemplo de provedor de serviços de implantação](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/FilterProvider)  
[Windows Exemplo de Gerenciador de transporte dos serviços de implantação](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Management/WDSTransportManager)  
</dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Uso da API de servidor de Serviços de Implantação do Windows](using-the-windows-deployment-services-server-api.md)
</dt> <dt>

[Uso da API de cliente de Serviços de Implantação do Windows](using-the-windows-deployment-services-client-api.md)
</dt> </dl>

 

 