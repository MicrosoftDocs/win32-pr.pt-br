---
description: usando o .NET Framework 4 com aplicativos criados em versões anteriores
ms.assetid: 287E25AD-A560-40DA-A4E6-C46A3123914E
title: usando o .NET Framework 4 com aplicativos criados em versões anteriores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c400f38efe93d2fc77d5de1f700b550f455f3e29db8ba96ef778771d82158c76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994566"
---
# <a name="using-net-framework-4-with-applications-built-on-earlier-versions"></a>usando o .NET Framework 4 com aplicativos criados em versões anteriores

## <a name="platform"></a>Plataforma

 **clientes** -Windows XP, Windows Vista, Windows 7  
**servidores** -Windows server 2003, Windows server 2008, Windows server 2008 R2  


## <a name="feature-impact"></a>Impacto do recurso

 **Severidade** -baixa  
**Frequência** -alta  






## <a name="description"></a>Descrição

o .NET Framework 4 é altamente compatível com aplicativos que são criados usando versões anteriores do .NET Framework. as principais alterações no .NET Framework 4 são melhorar a segurança, a conformidade dos padrões, a exatidão, a confiabilidade e o desempenho.

no entanto, .NET Framework 4 não usa automaticamente sua versão do Common Language Runtime (CLR) para executar aplicativos que são criados com o uso de versões anteriores do .NET Framework.

## <a name="manifestation"></a>Manifestação

se você tiver criado um aplicativo usando uma .NET Framework anterior e um usuário abrir esse aplicativo em um computador que tenha o .NET Framework 4 e a versão anterior do .NET Framework instalado, o aplicativo usará a versão mais antiga do CLR.

no entanto, se o .NET Framework 4 for a única versão de tempo de execução instalada no computador, o aplicativo lançará uma exceção e solicitará que o usuário instale a versão de tempo de execução na qual você criou o aplicativo.

## <a name="solution"></a>Solução

para executar aplicativos criados com versões anteriores do .NET Framework com o .NET Framework 4, você deve compilar seu aplicativo para direcionar a versão do .NET Framework 4 especificando-o nas propriedades do seu projeto no Microsoft Visual Studio, ou pode especificar .NET Framework 4 no [**<supportedRuntime> elemento**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) em um arquivo de configuração de aplicativo.

para obter mais informações sobre como migrar para o .NET Framework 4, consulte [guia de migração para o .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) e [compatibilidade de versão no .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100)).

## <a name="compatibility-tests"></a>Testes de compatibilidade

Depois de fazer as alterações, teste seu aplicativo para certificar-se de que ele seja executado corretamente. você pode testar a compatibilidade conforme descrito no tópico [.NET Framework 4 compatibilidade de aplicativos](/previous-versions/dd889541(v=msdn.10)) .

se seu aplicativo ou componente não funcionar após a instalação do .NET Framework 4, envie um bug por meio do site do [Microsoft Conexão](https://connect.microsoft.com/visualstudio) .

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [**<supportedRuntime> elementos**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))
-   [Guia de migração do .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))
-   [Compatibilidade de versão no .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))
-   **explicação da compatibilidade de aplicativos RTM do .NET Framework 4:**<https://msdn.microsoft.com/library/dd889541.aspx>
-   [Microsoft Connect](https://connect.microsoft.com/)

 

 
