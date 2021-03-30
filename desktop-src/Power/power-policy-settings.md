---
description: Descreve as configurações de política de energia que compõem um esquema de energia.
ms.assetid: cd515cd6-67f4-45d0-b769-3abc7a56faa8
title: Configurações de política de energia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f490c758a890faf314be1ddffe9ac7a503bd473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662179"
---
# <a name="power-policy-settings"></a>Configurações de política de energia

Planos de energia e esquemas consistem em preferências e configurações de política.

Um plano de energia consiste em um grupo de preferências de configuração de energia. Essas preferências consistem em um valor AC e DC para cada uma das configurações de energia. Cada plano de energia é identificado por meio de um **GUID** exclusivo, bem como um nome amigável. O Windows Vista tem três planos de energia padrão: economia de energia, equilibrado e alto desempenho. Esses planos podem ser personalizados e planos adicionais podem ser criados. Todos os planos de energia têm um atributo de personalidade que indica o comportamento de economia de energia geral do plano.

A tabela a seguir mostra os três personalidades do plano de energia. 

| Nome de exibição     | Description                                                                   | **GUID**                             |
|------------------|-------------------------------------------------------------------------------|--------------------------------------|
| Economia de energia      | Oferece um desempenho reduzido que pode aumentar a economia de energia.                | a1841308-3541-4fab-bc81-f71556f20b4a |
| Balanced         | Balanceia automaticamente o consumo de energia e de desempenho de acordo com a demanda. | 381b4222-f694-41f0-9685-ff5bb260df2e |
| Alto Desempenho | Oferece desempenho máximo às custas de maior consumo de energia.      | 8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c |



 

> [!Note]  
> Os dispositivos que dão suporte ao modo de [espera moderno](/windows-hardware/design/device-experiences/modern-standby) só permitem o plano de energia **equilibrado** . O **modo de espera moderno** é a solução mais recente e mais simplificada para o gerenciamento de configurações de energia.

 

Cada computador tem um plano de energia único e ativo. Por padrão, os usuários sem privilégios são capazes de acessar as configurações de energia do sistema. O acesso a todas as configurações de energia individuais pode ser controlado por meio de ACLs nas configurações de energia ou por meio de Política de Grupo. Os aplicativos devem chamar [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) para determinar se o usuário tem acesso à configuração de energia.

Cada configuração de energia é identificada por um **GUID** exclusivo e inclui um nome amigável, descrição, valores permitidos e valores padrão para AC e DC. As configurações de energia personalizadas podem ser criadas usando a função [**PowerCreateSetting**](/windows/desktop/api/PowrProf/nf-powrprof-powercreatesetting) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Esquemas de energia](power-schemes.md)
</dt> </dl>

 

 
