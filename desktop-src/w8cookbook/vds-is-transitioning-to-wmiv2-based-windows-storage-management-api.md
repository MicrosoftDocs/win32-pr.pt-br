---
title: o serviço de disco Virtual está em transição para Windows API de gerenciamento de Armazenamento
description: o serviço de disco Virtual está em transição para Windows API de gerenciamento de Armazenamento
ms.assetid: AB2A7D08-03B2-4595-A8EC-805D111A0E89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a45e25452ae0b6bb20e0ca04130b7fa2fd64f2a191d504380f973f663b7931ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852033"
---
# <a name="virtual-disk-service-is-transitioning-to-windows-storage-management-api"></a>o serviço de disco Virtual está em transição para Windows API de gerenciamento de Armazenamento

## <a name="platforms"></a>Plataformas

**clientes** – Windows 8  
**servidores** – Windows Server 2012  


## <a name="description"></a>Descrição

começando com Windows 8 e Windows Server 2012, a interface COM do serviço de disco Virtual é substituída pela API de gerenciamento do Armazenamento, uma interface de programação baseada em WMI. para gerenciar subsistemas de armazenamento, (Windows) discos, partições e volumes, é altamente recomendável usar a API de gerenciamento de Armazenamento. para obter mais informações, consulte [Windows Armazenamento API de gerenciamento](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).

Para todos os usos, exceto volumes de inicialização espelho (usando um volume espelhado para hospedar o sistema operacional), discos dinâmicos são preteridos. para dados que exigem resiliência contra falhas de unidade, use Espaços de Armazenamento, uma solução de virtualização de armazenamento resiliente. para obter mais informações, consulte a [visualização técnica do Espaços de Armazenamento](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).

você pode continuar a usar o DiskPart, o DiskRAID e o gerenciamento de disco durante o período de reprovação, mas essas ferramentas não funcionarão com Espaços de Armazenamento ou com quaisquer outras APIs de gerenciamento de Armazenamento Instrumentação de Gerenciamento do Windows Windows baseadas em WMI) ou em clientes ou utilitários de gerenciamento de armazenamento in-box.


| APIs | Armazenamento Subsistemas | Discos básicos | Discos Dinâmicos | Espaços de Armazenamento |
| --- | --- | --- | --- | --- |
| VDS | Sim | Sim | Sim | Não |
| WMI | Sim | Sim | Não | Sim |
| DiskPart | n/d | Sim | Sim | Não |
| DiskRAID |  Sim | n/d | n/d | n/d |
| GUI de gerenciamento de disco | n/d | Sim | Sim | Não |
| PowerShell | Sim | Sim | Não | Sim |
| Espaços de Armazenamento Painel de controle | n/d | Não | Não | Sim |


O resultado dessa transição aumentará a resiliência do armazenamento, a disponibilidade e a escalabilidade; uma linguagem de programação e script unificada, custos de gerenciamento de armazenamento reduzidos e gerenciamento de armazenamento remoto mais fácil.

## <a name="manifestation"></a>Manifestação

os utilitários do DiskPart e do DiskRAID usados no ambiente do VDS não dão suporte à nova Espaços de Armazenamento. da mesma forma, o novo utilitário do PowerShell Armazenamento não dá suporte aos discos dinâmicos preteridos

## <a name="mitigation"></a>Atenuação

a Microsoft recomenda enfaticamente que você baseie qualquer novo aplicativo de gerenciamento de armazenamento na api de gerenciamento de Armazenamento Windows e que planeja fazer a transição de aplicativos existentes baseados na infraestrutura do VDS para a api de gerenciamento de Armazenamento Windows durante os ciclos de atualização padrão.

## <a name="resources"></a>Recursos

-   [API de Gerenciamento do Armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
-   [Cmdlets de armazenamento no Windows PowerShell](/powershell/module/storage/?view=win10-ps)
-   [Instrumentação de Gerenciamento do Windows](../wmisdk/wmi-start-page.md)
-   [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=VS.85).aspx)

 

 