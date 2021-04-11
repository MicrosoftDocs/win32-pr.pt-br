---
description: .
ms.assetid: 87331C1D-F468-4CA4-92BD-D4E5D4E930BC
title: Segurança (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bbaaa6b34463e04f5870082e5c693462f4e19fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172314"
---
# <a name="security-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Segurança (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)

A partir do Windows Internet Explorer 7, o Windows Internet Explorer é executado em um contexto de segurança chamado *modo protegido* quando os usuários o executam no sistema operacional Windows Vista ou em uma versão posterior. Esse modo executa o Internet Explorer em uma configuração de privilégio inferior a de um aplicativo de usuário padrão, de modo que determinadas funcionalidades sejam limitadas, especialmente controles ActiveX e certos tipos de plug-ins. Para obter mais informações sobre o modo protegido no Internet Explorer e seu impacto na compatibilidade, consulte [compreendendo e trabalhando no modo protegido do Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) na biblioteca MSDN.

Por padrão, o Windows Internet Explorer 8 também permite o DEP (prevenção de execução de dados), que ajuda os aplicativos a evitar a execução de código arbitrário em ataques online. No entanto, alguns complementos podem não usar esse recurso de segurança (por exemplo, quaisquer complementos que não foram projetados para executar apenas o código localizado na memória que foi especificamente marcado como executável, como aplicativos que são criados usando uma versão mais antiga da estrutura da ATL (ActiveX Template Library).

O Internet Explorer 8 também protege os usuários contra possíveis vulnerabilidades de segurança que usam scripts. Por exemplo, você não pode navegar de uma URL em uma zona menos confiável para uma URL em uma zona mais confiável, exceto pela interação explícita do usuário. Você também não pode ocultar determinados elementos da interface do usuário do navegador (como a barra de endereços) em uma zona não confiável (Internet).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atualizações de design que afetam a compatibilidade entre navegadores](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 
