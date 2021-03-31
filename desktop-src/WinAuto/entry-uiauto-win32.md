---
title: Automação da Interface de Usuário
description: A automação da interface do usuário da Microsoft é uma estrutura de acessibilidade que permite que os aplicativos do Windows forneçam e consumam informações programáticas sobre interfaces do usuário.
ms.assetid: 700ca38d-ff40-472b-a95a-11fa94c3bc1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8006c79299cc1f736dc43555968443f634d4a51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823891"
---
# <a name="ui-automation"></a>Automação da Interface de Usuário

A automação da interface do usuário da Microsoft é uma estrutura de acessibilidade que permite que os aplicativos do Windows forneçam e consumam informações programáticas sobre interfaces do usuário. Ele fornece acesso programático à maioria dos elementos da interface do usuário na área de trabalho. Ele permite que produtos de tecnologia assistencial, como leitores de tela, forneçam informações sobre a interface do usuário aos usuários finais e manipulem a interface do usuário por meio de entrada padrão. A automação da interface do usuário também permite que scripts de teste automatizados interajam com a interface do usuário

-   [Quando aplicável](#where-applicable)
-   [Público do desenvolvedor](#developer-audience)
-   [Requisitos de tempo de execução](#run-time-requirements)
-   [Suporte para sistemas operacionais de nível inferior](#support-for-down-level-operating-systems)

## <a name="where-applicable"></a>Quando aplicável

Usando a automação da interface do usuário e as práticas de design acessíveis a seguir, os desenvolvedores podem fazer com que os aplicativos em execução no Windows sejam mais acessíveis para muitas pessoas com deficiências visuais, auditivas ou motoras. Além disso, a automação da interface do usuário foi projetada especificamente para fornecer uma funcionalidade robusta para cenários de teste automatizados.

## <a name="developer-audience"></a>Público do desenvolvedor

A automação da interface do usuário foi projetada para desenvolvedores experientes de C/C++. Em geral, os desenvolvedores precisam de um nível moderado de compreensão sobre objetos de Component Object Model (COM) e interfaces, Unicode e programação de API do Windows.

Para obter informações sobre automação de interface do usuário para código gerenciado, consulte [acessibilidade](/dotnet/framework/ui-automation/) na seção Guia do desenvolvedor .NET Framework do MSDN.

## <a name="run-time-requirements"></a>Requisitos de Run-Time

A automação da interface do usuário tem suporte nos seguintes sistemas operacionais: Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows 10, Windows Server 2008, Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2, Windows Server 2016 e Windows Server 2019.

> [!Note]  
> O Windows XP e o Windows Server 2003 também exigem Microsoft .NET Framework 3,0.

 

## <a name="support-for-down-level-operating-systems"></a>Suporte para sistemas operacionais de nível inferior

A atualização de plataforma para o Windows Vista é um conjunto de bibliotecas de tempo de execução que permite aos desenvolvedores direcionar aplicativos para os sistemas operacionais Windows 7 e de nível inferior. A atualização de plataforma para o Windows Server 2008 é um conjunto de bibliotecas de tempo de execução que permite aos desenvolvedores direcionar aplicativos para o Windows Server 2008 R2 e versões anteriores do Windows Server. A atualização da plataforma para Windows Vista e a atualização da plataforma para Windows Server 2008 estarão disponíveis para todos os clientes do Windows Vista e do Windows Server 2008 por meio de Windows Update. Aplicativos de terceiros que exigem atualização de plataforma para Windows Vista ou atualização de plataforma para Windows Server 2008 podem ter Windows Update detectar se estão instalados; Se não estiver, Windows Update será baixado e instalado em segundo plano.

A atualização de plataforma para o Windows Vista e a atualização de plataforma para Windows Server 2008 oferecem suporte a todo o conjunto de recursos da API de automação do Windows 3,0 nos seguintes sistemas operacionais.

-   Windows XP (inglês) <dl> Windows XP Home SP3 x86  
    Windows XP Professional SP3 x86  
    </dl>
-   Windows Server 2003 (English) <dl> Windows Server 2003 SP2 (x86 e x64)  
    </dl>
-   Windows Vista (inglês) <dl> Starter SP2 (x86 e x64)  
    Home Premium SP2 (x86 e x64)  
    Business SP2 (x86 e x64)  
    Enterprise SP2 (x86 e x64)  
    Ultimate SP2 (x86 e x64)  
    </dl>
-   Windows Server 2008 (inglês) <dl> Windows Server 2008 SP2 (x86 e x64)  
    </dl>

Para obter mais informações sobre as duas atualizações, consulte [atualização de plataforma para Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).

## <a name="in-this-section"></a>Nesta seção

-   [Conceitos básicos de automação da interface do usuário](entry-uiautocore-overview.md)
-   [Guia do programador do provedor de automação de interface do usuário](uiauto-providerportal.md)
-   [Guia do programador do cliente de automação da interface do usuário](uiauto-clientportal.md)
-   [Referência](entry-uiautocore-ref.md)
-   [Amostras](samples-entry.md)
-   [Apêndices](appendix-entry.md)

 

 