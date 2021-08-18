---
description: Security (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.assetid: 87331C1D-F468-4CA4-92BD-D4E5D4E930BC
title: Security (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d392f5bf14997962173b9054baba861003877d851d6bd62a947b15757feec23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994656"
---
# <a name="security-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Security (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)

A partir do Windows Internet Explorer 7, o Windows Internet Explorer é executado  em um contexto de segurança chamado Modo Protegido quando os usuários o executam no sistema operacional Windows Vista ou em uma versão posterior. Esse modo é Internet Explorer em uma configuração de privilégio inferior ao de um aplicativo de usuário padrão, de modo que determinada funcionalidade seja limitada, especialmente ActiveX controles e determinados tipos de plug-ins. Para obter mais informações sobre o Modo Protegido no Internet Explorer e seu impacto sobre a compatibilidade, consulte Understanding [and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) in the Biblioteca MSDN.

Por padrão, o Windows Internet Explorer 8 também habilita a DEP (Prevenção de Execução de Dados), que ajuda os aplicativos a evitar a execução de código arbitrário em ataques online. No entanto, alguns complementos podem não usar esse recurso de segurança (por exemplo, quaisquer complementos que não foram projetados para executar apenas o código localizado na memória que foi especificamente marcado como executável, como aplicativos criados usando uma versão mais antiga da estrutura da ATL (Biblioteca de Modelos do ActiveX).

Internet Explorer 8 também protege os usuários contra possíveis vulnerabilidades de segurança que usam scripts. Por exemplo, você não pode navegar de uma URL em uma zona menos confiável para uma URL em uma zona mais confiável, exceto pela interação explícita do usuário. Você também não pode ocultar determinados elementos da interface do usuário do navegador (como a barra de endereços) em uma zona não confiável (Internet).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criar atualizações que impactam a compatibilidade entre navegadores](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 
