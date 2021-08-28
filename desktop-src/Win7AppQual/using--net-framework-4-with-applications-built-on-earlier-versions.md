---
description: Usando .NET Framework 4 com aplicativos com base em versões anteriores
ms.assetid: 287E25AD-A560-40DA-A4E6-C46A3123914E
title: Usando .NET Framework 4 com aplicativos com base em versões anteriores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a12eb34b00cfe14a18e83e7726f1ffa962ba03f8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884749"
---
# <a name="using-net-framework-4-with-applications-built-on-earlier-versions"></a>Usando .NET Framework 4 com aplicativos com base em versões anteriores

## <a name="platform"></a>Plataforma

 **Clientes** – Windows XP, Windows Vista, Windows 7  
**Servidores** – Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  


## <a name="feature-impact"></a>Impacto do recurso

 **Gravidade –** Baixa  
**Frequência** – Alta  






## <a name="description"></a>Description

O .NET Framework 4 é altamente compatível com aplicativos que são construídos usando versões .NET Framework anteriores. As principais alterações no .NET Framework 4 são melhorar a segurança, a conformidade de padrões, a correção, a confiabilidade e o desempenho.

No entanto, .NET Framework 4 não usa automaticamente sua versão do CLR (Common Language Runtime) para executar aplicativos que são construídos usando versões anteriores do .NET Framework.

## <a name="manifestation"></a>Manifestação

Se você criou um aplicativo usando um .NET Framework anterior e um usuário abrir esse aplicativo em um computador que tenha o .NET Framework 4 e a versão anterior do .NET Framework instalados, o aplicativo usará a versão anterior do CLR.

No entanto, se o .NET Framework 4 for a única versão de runtime instalada no computador, o aplicativo lançará uma exceção e pedirá que o usuário instale a versão de runtime em que você criou o aplicativo.

## <a name="solution"></a>Solução

Para executar aplicativos que são compilados com versões anteriores do .NET Framework com o .NET Framework 4, você deve compilar seu aplicativo para direcionar a versão do .NET Framework 4 especificando-a nas propriedades do seu projeto no Microsoft Visual Studio ou você pode especificar .NET Framework 4 no elemento [**&lt; supportedRuntime &gt;**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) em um arquivo de configuração de aplicativo.

Para obter mais informações sobre como migrar para o .NET Framework 4, consulte Guia de migração para o [.NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) e Compatibilidade de versão [no .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100)).

## <a name="compatibility-tests"></a>Testes de compatibilidade

Depois de fazer as alterações, teste seu aplicativo para garantir que ele seja executado corretamente. Você pode testar a compatibilidade conforme descrito no [tópico .NET Framework Compatibilidade de Aplicativos 4.](/previous-versions/dd889541(v=msdn.10))

Se seu aplicativo ou componente não funcionar após .NET Framework 4 estiver instalado, envie um bug por meio do site [do Microsoft Conexão.](https://connect.microsoft.com/visualstudio)

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [**&lt;Elemento &gt; supportedRuntime**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))
-   [Guia de migração do .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))
-   [Compatibilidade de versão no .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))
-   **.NET Framework passo a passo de compatibilidade do aplicativo RTM 4:**<https://msdn.microsoft.com/library/dd889541.aspx>
-   [Microsoft Connect](https://connect.microsoft.com/)

 

 
