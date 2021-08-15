---
description: Os aplicativos cliente e scripts que acessam provedores WMI padrão de 32 bits continuam funcionando normalmente durante a execução em um sistema operacional de 64 bits.
ms.assetid: 68819bea-a48d-4de1-a50d-f03ae04775f5
ms.tgt_platform: multiple
title: Obter e fornecer dados em um computador de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46163290d1212fd66bef48dba177034769360e8d7c6249dfdf40327ce2adc32c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118819370"
---
# <a name="getting-and-providing-data-on-a-64-bit-computer"></a>Obter e fornecer dados em um computador de 64 bits

Os aplicativos cliente e scripts que acessam provedores WMI padrão de 32 bits continuam funcionando normalmente durante a execução em um sistema operacional de 64 bits. Somente dois provedores pré-instalados, o provedor do Registro do Sistema e o provedor de exibição [,](view-provider.md)têm versões de 64 bits que são executados lado a lado com as versões de 32 bits. [](/previous-versions/windows/desktop/regprov/system-registry-provider) No entanto, um aplicativo de 3 Windows 2 bits que solicita instâncias do WDM (modelo de driver) de 32 bits recebe as instâncias padrão da classe WDM de 64 bits em um sistema operacional de 64 bits.

## <a name="accessing-default-and-nondefault-provider-data"></a>Acessando dados padrão e não padrão do provedor

Em geral, os autores de provedor não incluem versões de 32 bits e 64 bits de um provedor no mesmo sistema operacional. Se não houver nenhum provedor de 64 bits, um provedor de 32 bits poderá continuar a ser executado por meio das instalações do WOW64. Um provedor de 64 bits também pode fornecer dados para um aplicativo de 32 bits. Para obter mais informações, [consulte Fornecendo dados WMI em uma plataforma de 64 bits.](providing-wmi-data-on-a-64-bit-platform.md)

Se existirem duas versões, os aplicativos cliente e scripts poderão usar os parâmetros de contexto disponíveis na [API COM](com-api-for-wmi.md) e na API de [Script](scripting-api-for-wmi.md) para se conectar explicitamente a um provedor WMI não padrão específico, se ele estiver disponível. Para obter mais informações, consulte [Solicitando dados WMI em uma plataforma de 64 bits.](requesting-wmi-data-on-a-64-bit-platform.md)

O diagrama a seguir mostra as conexões padrão e não padrão, usando o Registro como um exemplo para o qual dois provedores podem existir lado a lado em uma plataforma de 64 bits.

![conexões padrão e não padrão em uma plataforma de 64 bits](images/32-64bit-registry.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solicitando dados WMI em uma plataforma de 64 bits](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[Fornecendo dados WMI em uma plataforma de 64 bits](providing-wmi-data-on-a-64-bit-platform.md)
</dt> </dl>

 

 
