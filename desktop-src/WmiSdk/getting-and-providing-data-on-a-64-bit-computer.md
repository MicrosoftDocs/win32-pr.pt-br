---
description: Os aplicativos cliente e scripts que acessam provedores de 32 bits WMI padrão continuam a operar normalmente quando executados em um sistema operacional de 64 bits.
ms.assetid: 68819bea-a48d-4de1-a50d-f03ae04775f5
ms.tgt_platform: multiple
title: Obter e fornecer dados em um computador de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7d8ff5430a7c47b652bfbcca05d2f53ba857d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564093"
---
# <a name="getting-and-providing-data-on-a-64-bit-computer"></a>Obter e fornecer dados em um computador de 64 bits

Os aplicativos cliente e scripts que acessam provedores de 32 bits WMI padrão continuam a operar normalmente quando executados em um sistema operacional de 64 bits. Somente dois provedores pré-instalados, o provedor de [registro do sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) e o [provedor de exibição](view-provider.md)têm versões de 64 bits que são executadas lado a lado com as versões de 32 bits. No entanto, um aplicativo de 32 bits que solicita instâncias de Windows Driver Model de 32 bits (WDM) recebe as instâncias de classe WDM de 64 bits padrão em um sistema operacional de 64 bits.

## <a name="accessing-default-and-nondefault-provider-data"></a>Acessando dados de provedor padrão e não padrão

Em geral, os gravadores de provedor não incluem versões de 32 bits e 64 bits de um provedor no mesmo sistema operacional. Se nenhum provedor de 64 bits existir, um provedor de 32 bits poderá continuar executando os recursos do WOW64. O provedor de 64 bits pode, da mesma forma, fornecer dados para um aplicativo de 32 bits. Para obter mais informações, consulte [fornecendo dados do WMI em uma plataforma de 64 bits](providing-wmi-data-on-a-64-bit-platform.md).

Se existirem duas versões, os aplicativos e scripts cliente poderão usar os parâmetros de contexto disponíveis na [API com](com-api-for-wmi.md) e a [API de script](scripting-api-for-wmi.md) para se conectar explicitamente a um provedor WMI não padrão específico, se estiver disponível. Para obter mais informações, consulte [solicitando dados WMI em uma plataforma de 64 bits](requesting-wmi-data-on-a-64-bit-platform.md).

O diagrama a seguir mostra as conexões padrão e não padrão, usando o registro como um exemplo para o qual dois provedores podem existir lado a lado em uma plataforma de 64 bits.

![conexões padrão e não padrão em uma plataforma de 64 bits](images/32-64bit-registry.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solicitando dados WMI em uma plataforma de 64 bits](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[Fornecendo dados do WMI em uma plataforma de 64 bits](providing-wmi-data-on-a-64-bit-platform.md)
</dt> </dl>

 

 
