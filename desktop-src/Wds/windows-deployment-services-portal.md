---
title: Windows Deployment Services
description: Implantar sistemas operacionais Windows. Configure novos clientes com uma instalação baseada em rede sem exigir que os administradores visitem cada computador ou instalem diretamente da mídia de CD ou DVD.
ms.assetid: 790abc27-03cc-4f93-bf04-a4eb37e614bb
keywords:
- Serviço de implantação do Windows serviços de implantação do Windows
- Serviços de implantação do Windows serviços de implantação do Windows, home page
- serviços de implantação serviços de implantação do Windows
- Serviços de implantação do Windows WDS consulte serviços de implantação do Windows
- Serviços de instalação remota serviços de implantação do Windows consulte serviços de implantação do Windows
- Serviços de implantação do Windows RIS consulte serviços de implantação do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b35bebb000b383552f12d259ca17552165e9247f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105772993"
---
# <a name="windows-deployment-services"></a>Windows Deployment Services

## <a name="purpose"></a>Finalidade

O WDS (serviços de implantação do Windows) é a versão revisada do RIS (serviços de instalação remota). O WDS permite a implantação de sistemas operacionais Windows. Você pode usar o WDS para configurar novos clientes com uma instalação baseada em rede sem exigir que os administradores visitem cada computador ou instalem diretamente da mídia de CD ou DVD.

## <a name="developer-audience"></a>Público de desenvolvedores

O público-alvo principal da API do WDS é para grupos que desenvolvem ferramentas e processos personalizados para ti e outros grupos de administração do computador. Em ambientes em que a solução padrão WDS (serviços de implantação do Windows) não pode ser usada, a API do WDS permite o acesso programático a alguns componentes do WDS.

Os OEMs (fabricantes originais do equipamento), os integradores de sistemas e os profissionais de ti corporativos que procuram informações sobre como implantar o Windows em novos computadores, devem ver as informações sobre a solução padrão do WDS (serviços de implantação do Windows) no [guia passo a passo da atualização dos serviços de implantação do Windows](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) e o [WAIK (Kit de instalação automatizada do Windows)](https://www.microsoft.com/download/details.aspx?id=10333).

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

O WDS está disponível como um complemento para o Windows Server 2003 com Service Pack 1 (SP1) e está incluído no sistema operacional a partir do Windows Server 2003 com Service Pack 2 (SP2) e Windows Server 2008. A API do servidor PXE do WDS requer a função de servidor WDS no servidor para implementar provedores PXE personalizados. A API do cliente do WDS requer a fase Microsoft Ambiente de Pré-Instalação do Windows (Windows PE 2,0) do processamento da instalação. Uma imagem inicializável de RAMDISK do Windows PE 2,0 no. O formato WIM deve ser baixado como parte do processo de inicialização de rede para implementar clientes WDS personalizados.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                 | Descrição                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Sobre a API dos serviços de implantação do Windows](about-the-windows-deployment-services-api.md)<br/> | Informações gerais sobre a API do servidor WDS e a API do cliente WDS.<br/>    |
| [Referência dos serviços de implantação do Windows](windows-deployment-services-reference.md)<br/>         | Descreve as funções e estruturas dos serviços de implantação do Windows.<br/> |



 

 

