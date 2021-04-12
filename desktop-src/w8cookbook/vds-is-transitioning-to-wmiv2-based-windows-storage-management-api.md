---
title: O serviço de disco virtual está em transição para a API de gerenciamento de armazenamento do Windows
description: O serviço de disco virtual está em transição para a API de gerenciamento de armazenamento do Windows
ms.assetid: AB2A7D08-03B2-4595-A8EC-805D111A0E89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceea3ffe82358737ca8f39e9ef6db0bdb1f116ef
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104366800"
---
# <a name="virtual-disk-service-is-transitioning-to-windows-storage-management-api"></a>O serviço de disco virtual está em transição para a API de gerenciamento de armazenamento do Windows

## <a name="platforms"></a>Plataformas

**Clientes** – Windows 8  
**Servidores** – Windows Server 2012  


## <a name="description"></a>Descrição

A partir do Windows 8 e do Windows Server 2012, a interface COM do serviço de disco virtual é substituída pela API de gerenciamento de armazenamento, uma interface de programação baseada em WMI. Para gerenciar subsistemas de armazenamento, discos, partições e volumes do (Windows), é altamente recomendável usar a API de gerenciamento de armazenamento. Para obter mais informações, consulte [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).

Para todos os usos, exceto volumes de inicialização espelho (usando um volume espelhado para hospedar o sistema operacional), discos dinâmicos são preteridos. Para dados que exigem resiliência contra falha de unidade, use espaços de armazenamento, uma solução de virtualização de armazenamento resiliente. Para obter mais informações, consulte [Visualização técnica de espaços de armazenamento](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).

Você pode continuar a usar o DiskPart, o DiskRAID e o gerenciamento de disco durante o período de reprovação, mas essas ferramentas não funcionarão com espaços de armazenamento ou com outras APIs de gerenciamento de armazenamento do Windows baseadas em Instrumentação de Gerenciamento do Windows (WMI) ou utilitários de gerenciamento de armazenamento in-box ou clientes.


| APIs | Subsistemas de armazenamento | Discos básicos | Discos Dinâmicos | Espaços de Armazenamento |
| --- | --- | --- | --- | --- |
| VDS | Sim | Sim | Sim | Não |
| WMI | Sim | Sim | Não | Sim |
| DiskPart | N/D | Sim | Sim | Não |
| DiskRAID |  Sim | n/d | N/D | N/D |
| GUI de gerenciamento de disco | N/D | Sim | Sim | Não |
| PowerShell | Sim | Sim | Não | Sim |
| Painel de controle de espaços de armazenamento | N/D | Não | Não | Sim |


O resultado dessa transição aumentará a resiliência do armazenamento, a disponibilidade e a escalabilidade; uma linguagem de programação e script unificada, custos de gerenciamento de armazenamento reduzidos e gerenciamento de armazenamento remoto mais fácil.

## <a name="manifestation"></a>Manifestação

Os utilitários do DiskPart e do DiskRAID usados no ambiente do VDS não dão suporte aos novos espaços de armazenamento. Da mesma forma, o novo utilitário de armazenamento do PowerShell não dá suporte aos discos dinâmicos preteridos

## <a name="mitigation"></a>Atenuação

A Microsoft recomenda enfaticamente que você baseie qualquer novo aplicativo de gerenciamento de armazenamento na API de gerenciamento de armazenamento do Windows e que planeja fazer a transição de aplicativos existentes baseados na infraestrutura do VDS para a API de gerenciamento de armazenamento do Windows durante os ciclos de atualização padrão.

## <a name="resources"></a>Recursos

-   [API de Gerenciamento do Armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
-   [Cmdlets de armazenamento no Windows PowerShell](/powershell/module/storage/?view=win10-ps)
-   [Instrumentação de Gerenciamento do Windows](../wmisdk/wmi-start-page.md)
-   [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=VS.85).aspx)

 

 