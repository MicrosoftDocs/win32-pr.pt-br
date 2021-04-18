---
title: Plataforma de filtragem do Windows
description: A WFP (Windows Filtering Platform) é um conjunto de API e serviços do sistema que fornecem uma plataforma para a criação de aplicativos de filtragem de rede.
ms.assetid: 0436f559-20e6-4199-8391-10eb7d85df23
keywords:
- Plataforma de filtragem do Windows
- Página inicial da plataforma de filtragem do Windows, página inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cf63f995b44be607977dd0c70c6c91eed024e81
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "105766917"
---
# <a name="windows-filtering-platform"></a>Plataforma de filtragem do Windows

## <a name="purpose"></a>Finalidade

A WFP (Windows Filtering Platform) é um conjunto de API e serviços do sistema que fornecem uma plataforma para a criação de aplicativos de filtragem de rede. A API da WFP permite aos desenvolvedores escrever código que interaja com o processamento de pacote que acontece em diversos níveis na pilha de rede do sistema operacional. Os dados de rede podem ser filtrados e também modificados antes de atingirem seu destino.

Ao fornecer uma plataforma de desenvolvimento mais simples, a WFP foi projetada para substituir as tecnologias de filtragem de pacotes anteriores, como filtros interface do driver de transporte (TDI), filtros de NDIS (especificação de interface de driver de rede) e LSP (provedores de serviço em camadas) do Winsock. A partir do Windows Server 2008 e do Windows Vista, o cabo de firewall e os drivers de conexão de filtro não estão disponíveis; em vez disso, os aplicativos que estavam usando esses drivers devem usar a WFP.

Com a API WFP, os desenvolvedores podem implementar firewalls, sistemas de detecção de intrusão, programas antivírus, ferramentas de monitoramento de rede e controles dos pais. A WFP integra-se ao e fornece suporte para recursos de firewall, como comunicação autenticada e configuração dinâmica de firewall com base no uso dos aplicativos da API de soquetes (política baseada em aplicativo). A WFP também fornece infraestrutura para gerenciamento de política IPsec, notificações de alteração, diagnóstico de rede e filtragem com monitoração de estado.

A plataforma de filtragem do Windows é uma plataforma de desenvolvimento e não um firewall em si. O aplicativo de firewall criado no Windows Vista, no Windows Server 2008 e em sistemas operacionais posteriores do firewall do Windows com segurança avançada (WFAS) é implementado usando o WFP. Portanto, os aplicativos desenvolvidos com a API WFP ou a [API do WFAS](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) usam a lógica de arbitragem de filtragem comum que é incorporada à WFP.

A API WFP consiste em uma API do modo de usuário e uma API do modo kernel. Esta seção fornece uma visão geral de toda a WFP e descreve em detalhes apenas a parte do modo de usuário da API WFP. Para obter uma descrição detalhada da API WFP do modo kernel, consulte a ajuda online do [Windows Driver Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) .

## <a name="developer-audience"></a>Público de desenvolvedores

A API da plataforma de filtragem do Windows foi projetada para uso por programadores que usam o software de desenvolvimento C/C++. Os programadores devem estar familiarizados com os conceitos de rede e o design de sistemas usando componentes de modo de usuário e de modo kernel.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

A plataforma de filtragem do Windows tem suporte em clientes que executam o Windows Vista e posterior e em servidores que executam o Windows Server 2008 e posterior. Para obter informações sobre os requisitos de tempo de execução para um elemento de programação específico, consulte a seção requisitos da página de referência para esse elemento.





 

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                               | Descrição                                                                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [O que há de novo na plataforma de filtragem do Windows](what-s-new-in-windows-filtering-platform.md)<br/> | Informações sobre novos recursos e APIs na plataforma de filtragem do Windows.<br/>                    |
| [Sobre a plataforma de filtragem do Windows](about-windows-filtering-platform.md)<br/>                 | Uma visão geral da plataforma de filtragem do Windows.<br/>                                             |
| [Usando a plataforma de filtragem do Windows](using-windows-filtering-platform.md)<br/>                 | Código de exemplo usando a API da plataforma de filtragem do Windows. <br/>                                |
| [Referência da API da plataforma de filtragem do Windows](fwp-reference.md)<br/>                            | Documentação para as funções, estruturas e constantes da plataforma de filtragem do Windows.<br/> |



 

## <a name="additional-resources"></a>Recursos adicionais

Para fazer perguntas e ter discussões sobre como usar a API WFP, visite o [Fórum da plataforma de filtragem do Windows](https://social.msdn.microsoft.com/forums/wfp/threads/).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[API da plataforma de filtragem do Windows no modo kernel-guia de design](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[API da plataforma de filtragem do Windows no modo kernel-referência](/windows-hardware/drivers/ddi/_netvista/)
</dt> <dt>

[Firewall do Windows com Advanced Security](/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page)
</dt> <dt>

[Classe auxiliar extensível do diagnóstico WFP](/windows/desktop/NDF/windows-filtering-platform-extensible-helper-class)
</dt> <dt>

[Extensões do Winsock Secure Socket](/windows/desktop/WinSock/winsock-secure-socket-extensions)
</dt> </dl>

 

