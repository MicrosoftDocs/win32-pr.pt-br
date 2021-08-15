---
title: Windows Deployment Services
description: implantar sistemas operacionais Windows. Configure novos clientes com uma instalação baseada em rede sem exigir que os administradores visitem cada computador ou instalem diretamente da mídia de CD ou DVD.
ms.assetid: 790abc27-03cc-4f93-bf04-a4eb37e614bb
keywords:
- Windows serviços de implantação Windows serviços de implantação
- Windows serviços de implantação Windows serviços de implantação home page
- serviços de implantação Windows serviços de implantação
- serviços de implantação do WDS Windows consulte Windows serviços de implantação
- serviços de instalação remota Windows serviços de implantação consulte Windows serviços de implantação
- serviços de implantação do Windows RIS consulte Windows serviços de implantação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100483541420015ed84a95543f2f94bafb2d509d44e6b321b53729caa94588cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999506"
---
# <a name="windows-deployment-services"></a>Windows Deployment Services

## <a name="purpose"></a>Finalidade

Windows O WDS (serviços de implantação) é a versão revisada do RIS (serviços de instalação remota). o WDS permite a implantação de sistemas operacionais Windows. Você pode usar o WDS para configurar novos clientes com uma instalação baseada em rede sem exigir que os administradores visitem cada computador ou instalem diretamente da mídia de CD ou DVD.

## <a name="developer-audience"></a>Público de desenvolvedores

O público-alvo principal da API do WDS é para grupos que desenvolvem ferramentas e processos personalizados para ti e outros grupos de administração do computador. em ambientes em que a solução de WDS (serviços de implantação de Windows padrão) não pode ser usada, a API do wds permite o acesso programático a alguns componentes do WDS.

OEMs (fabricantes originais de equipamento), integradores de sistemas e profissionais de ti corporativos que procuram informações sobre como implantar Windows em novos computadores, devem ver as informações sobre a solução de WDS (serviços de implantação de Windows) padrão no [guia passo a passo de atualização dos serviços de implantação do Windows](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) e o [WAIK (Kit de instalação automatizada) do Windows](https://www.microsoft.com/download/details.aspx?id=10333).

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

o WDS está disponível como um complemento do Windows server 2003 com service pack 1 (SP1) e está incluído no sistema operacional a partir do Windows server 2003 com service pack 2 (SP2) e Windows server 2008. A API do servidor PXE do WDS requer a função de servidor WDS no servidor para implementar provedores PXE personalizados. a API do cliente do WDS requer a fase Microsoft Ambiente de Pré-Instalação do Windows (Windows PE 2,0) do processamento da instalação. uma imagem inicializável de RAMDISK do Windows PE 2,0 no. O formato WIM deve ser baixado como parte do processo de inicialização de rede para implementar clientes WDS personalizados.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                 | Descrição                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [sobre a API dos serviços de implantação Windows](about-the-windows-deployment-services-api.md)<br/> | Informações gerais sobre a API do servidor WDS e a API do cliente WDS.<br/>    |
| [Windows Referência de serviços de implantação](windows-deployment-services-reference.md)<br/>         | descreve os Windows as funções e estruturas dos serviços de implantação.<br/> |



 

 

