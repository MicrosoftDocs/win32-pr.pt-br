---
description: Descreve as configurações de política de energia que comem um esquema de energia.
ms.assetid: cd515cd6-67f4-45d0-b769-3abc7a56faa8
title: Power Policy Configurações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f8c0dbd4c7f2a27b6e6b96528c689c6609c175eded58a1de625af71e965f37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674306"
---
# <a name="power-policy-settings"></a>Power Policy Configurações

Planos de energia e esquemas consistem em preferências e configurações de política.

Um plano de energia consiste em um grupo de preferências de configuração de energia. Essas preferências consistem em um valor AC e DC para cada uma das configurações de energia. Cada plano de energia é identificado por meio de **um GUID** exclusivo, bem como um nome amigável. Windows O Vista tem três planos de energia padrão: Economia de Energia, Balanceado e Alto Desempenho. Esses planos podem ser personalizados e planos adicionais podem ser criados. Todos os planos de energia têm um atributo de personalidade que indica o comportamento geral de economia de energia do plano.

A tabela a seguir mostra as três personalidades do plano de energia. 

| Nome de exibição     | Descrição                                                                   | **GUID**                             |
|------------------|-------------------------------------------------------------------------------|--------------------------------------|
| Economia de energia      | Oferece desempenho reduzido, o que pode aumentar a economia de energia.                | a1841308-3541-4fab-bc81-f71556f20b4a |
| Balanced         | Balanceia automaticamente o desempenho e o consumo de energia de acordo com a demanda. | 381b4222-f694-41f0-9685-ff5bb260df2e |
| Alto Desempenho | Fornece desempenho máximo às custas de um maior consumo de energia.      | 8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c |



 

> [!Note]  
> Os dispositivos que são [compatíveis com o modo De espera](/windows-hardware/design/device-experiences/modern-standby) moderno permitem apenas o plano **de** energia balanceado. **O Modo de Espera Moderno** é a solução mais nova e simplificada para o gerenciamento de configurações de energia.

 

Cada computador tem um plano de energia único e ativo. Por padrão, os usuários não privilegiados podem acessar as configurações de energia do sistema. O acesso a todas as configurações de energia ou individuais pode ser controlado por meio de ACLs nas configurações de energia ou por meio Política de Grupo. Os aplicativos [**devem chamar PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) para determinar se o usuário tem acesso à configuração de energia.

Cada configuração de energia é identificada por um **GUID** exclusivo e inclui um nome amigável, uma descrição, valores acessíveis e valores padrão para AC e DC. As configurações de energia personalizadas podem ser criadas usando a [**função PowerCreateSetting.**](/windows/desktop/api/PowrProf/nf-powrprof-powercreatesetting)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Esquemas de energia](power-schemes.md)
</dt> </dl>

 

 
