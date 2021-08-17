---
description: O VDS (serviço de disco virtual) gerencia uma ampla gama de configurações de armazenamento, desde desktops de disco único até matrizes de armazenamento externo. O serviço expõe uma API (interface de programação de aplicativo).
ms.assetid: 536aafd2-cc04-48cc-8ee7-920efbba2a5f
title: Serviço de Disco Virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c84217b1ca63debe3e117e33b2358e4b0e55697c02ce8e00ce7f764c1fbf692
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137129"
---
# <a name="virtual-disk-service"></a>Serviço de Disco Virtual

\[a partir do Windows 8 e Windows Server 2012, a interface COM do serviço de disco Virtual é substituída pela [API de gerenciamento de Armazenamento Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

## <a name="purpose"></a>Finalidade

O VDS (serviço de disco virtual) gerencia uma ampla gama de configurações de armazenamento, desde desktops de disco único até matrizes de armazenamento externo. O serviço expõe uma API (interface de programação de aplicativo).

## <a name="where-applicable"></a>Quando aplicável

a partir do Windows 8 e do Windows Server 8, a interface COM do serviço de disco Virtual é substituída pela API de gerenciamento do Armazenamento, uma interface de programação baseada em WMI. para gerenciar subsistemas de armazenamento, (Windows) discos, partições e volumes, é altamente recomendável usar a API de gerenciamento de Armazenamento. para obter mais informações, consulte a [API de gerenciamento de Armazenamento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).

Para todos os usos, exceto volumes de inicialização espelho (usando um volume espelhado para hospedar o sistema operacional), discos dinâmicos são preteridos. para dados que exigem resiliência contra falhas de unidade, use Espaços de Armazenamento, uma solução de virtualização de armazenamento resiliente. para obter mais informações, consulte a [visualização técnica do Espaços de Armazenamento](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).

Os desenvolvedores de aplicativos que usam as interfaces descritas neste guia podem consultar e configurar um conjunto heterogêneo de armazenamento gerenciado internamente e fornecido pelo fornecedor. O VDS oculta de aplicativos as complexidades associadas ao armazenamento, tornando o serviço diferente do fornecedor e da tecnologia neutro.

## <a name="developer-audience"></a>Público de desenvolvedores

esta documentação destina-se a desenvolvedores de aplicativos que estão familiarizados com os recursos de armazenamento das plataformas Microsoft Windows e que são conhecimentos sobre o desenvolvimento com.

O guia também destina-se a fabricantes de subsistema de hardware que desenvolvem e dão suporte a programas de provedor de hardware VDS.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

o VDS tem suporte no Windows Server 2003, Windows Vista e posterior. Para obter informações sobre os requisitos de tempo de execução para um determinado elemento de programação, consulte a seção requisitos da documentação para esse elemento.

há suporte para a execução de aplicativos vds de 32 bits no WOW64, mas os provedores de vds de 64 bits devem ser executados como aplicativos nativos em versões de Windows bits de 64.

o VDS está disponível no SDK (Software Development Kit) do Microsoft Windows. você pode instalar o SDK para Windows 7 e Windows Server 2008 R2 no [centro de Download Windows](https://www.microsoft.com/download/details.aspx?id=8279). esta versão do SDK do Windows pode ser usada para desenvolver aplicativos VDS para o Windows Server 2003, Windows Vista e posterior. você também pode baixar a [versão ISO](https://www.microsoft.com/download/details.aspx?id=8442) do SDK no centro de download Windows.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                         | Descrição                                                                                            |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Sobre o VDS](about-vds.md)<br/>         | Descreve o modelo de objeto VDS, estratégias de configuração de armazenamento e notificações de VDS.<br/>    |
| [Usando VDS](using-vds.md)<br/>         | Descreve como usar o VDS para consultar e configurar dispositivos de armazenamento.<br/>                            |
| [Referência do VDS](vds-reference.md)<br/> | Descreve constantes do VDS, tipos de dados, enumerações, interfaces, estruturas e códigos de erro.<br/> |



 

 

