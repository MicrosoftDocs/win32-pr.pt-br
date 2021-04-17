---
description: O VDS (serviço de disco virtual) gerencia uma ampla gama de configurações de armazenamento, desde desktops de disco único até matrizes de armazenamento externo. O serviço expõe uma API (interface de programação de aplicativo).
ms.assetid: 536aafd2-cc04-48cc-8ee7-920efbba2a5f
title: Serviço de Disco Virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcfef0c5a73fcb2e6911395c829380c4bdfe56ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789998"
---
# <a name="virtual-disk-service"></a>Serviço de Disco Virtual

\[A partir do Windows 8 e do Windows Server 2012, a interface COM do serviço de disco virtual é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

## <a name="purpose"></a>Finalidade

O VDS (serviço de disco virtual) gerencia uma ampla gama de configurações de armazenamento, desde desktops de disco único até matrizes de armazenamento externo. O serviço expõe uma API (interface de programação de aplicativo).

## <a name="where-applicable"></a>Quando aplicável

A partir do Windows 8 e do Windows Server 8, a interface COM do serviço de disco virtual é substituída pela API de gerenciamento de armazenamento, uma interface de programação baseada em WMI. Para gerenciar subsistemas de armazenamento, discos, partições e volumes do (Windows), é altamente recomendável usar a API de gerenciamento de armazenamento. Para obter mais informações, consulte a [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).

Para todos os usos, exceto volumes de inicialização espelho (usando um volume espelhado para hospedar o sistema operacional), discos dinâmicos são preteridos. Para dados que exigem resiliência contra falha de unidade, use espaços de armazenamento, uma solução de virtualização de armazenamento resiliente. Para obter mais informações, consulte [Visualização técnica de espaços de armazenamento](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).

Os desenvolvedores de aplicativos que usam as interfaces descritas neste guia podem consultar e configurar um conjunto heterogêneo de armazenamento gerenciado internamente e fornecido pelo fornecedor. O VDS oculta de aplicativos as complexidades associadas ao armazenamento, tornando o serviço diferente do fornecedor e da tecnologia neutro.

## <a name="developer-audience"></a>Público de desenvolvedores

Esta documentação é destinada a desenvolvedores de aplicativos que estão familiarizados com os recursos de armazenamento das plataformas Microsoft Windows e que são mais experientes em relação ao desenvolvimento COM.

O guia também destina-se a fabricantes de subsistema de hardware que desenvolvem e dão suporte a programas de provedor de hardware VDS.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

O VDS tem suporte no Windows Server 2003, Windows Vista e posterior. Para obter informações sobre os requisitos de tempo de execução para um determinado elemento de programação, consulte a seção requisitos da documentação para esse elemento.

Há suporte para a execução de aplicativos VDS de 32 bits no WOW64, mas os provedores VDS de 64 bits devem ser executados como aplicativos nativos em versões do Windows de bits 64.

O VDS está disponível no SDK (Software Development Kit) do Microsoft Windows. Você pode instalar o SDK para Windows 7 e Windows Server 2008 R2 no [centro de download do Windows](https://www.microsoft.com/download/details.aspx?id=8279). Esta versão do SDK do Windows pode ser usada para desenvolver aplicativos VDS para o Windows Server 2003, o Windows Vista e versões posteriores. Você também pode baixar a [versão ISO](https://www.microsoft.com/download/details.aspx?id=8442) do SDK no centro de download do Windows.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                         | Descrição                                                                                            |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Sobre o VDS](about-vds.md)<br/>         | Descreve o modelo de objeto VDS, estratégias de configuração de armazenamento e notificações de VDS.<br/>    |
| [Usando VDS](using-vds.md)<br/>         | Descreve como usar o VDS para consultar e configurar dispositivos de armazenamento.<br/>                            |
| [Referência do VDS](vds-reference.md)<br/> | Descreve constantes do VDS, tipos de dados, enumerações, interfaces, estruturas e códigos de erro.<br/> |



 

 

