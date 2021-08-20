---
description: Windows A Instrumentação de Gerenciamento (WMI) é a infraestrutura para dados de gerenciamento e operações em Windows operacionais baseados em sistemas operacionais.
ms.assetid: 4804152f-2042-4c6a-83c6-75c5e1ab7a04
ms.tgt_platform: multiple
title: Instrumentação de Gerenciamento do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0b08c0301881b57c8132be9eead2e5b52cb64d4d3c4278985a573d5bff94f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553130"
---
# <a name="windows-management-instrumentation"></a>Instrumentação de Gerenciamento do Windows

## <a name="purpose"></a>Finalidade

Windows A Instrumentação de Gerenciamento (WMI) é a infraestrutura para dados de gerenciamento e operações em Windows operacionais baseados em sistemas operacionais. Você pode escrever scripts WMI ou aplicativos para automatizar tarefas administrativas em computadores remotos, mas o WMI também fornece dados de gerenciamento para outras partes do sistema operacional e produtos, por exemplo, System Center Operations Manager, anteriormente Microsoft Operations Manager (MOM) ou[WinRM](/windows/desktop/WinRM/portal)(Gerenciamento Remoto do Windows).

> [!Note]  
> A documentação a seguir é destinada a desenvolvedores e administradores de IT. Se você for um usuário final que passou por uma mensagem [](https://support.microsoft.com/) de erro referente ao WMI, vá para o Suporte da Microsoft e pesquise o código de erro que você vê na mensagem de erro. Para obter mais informações sobre como solucionar problemas com scripts WMI e o serviço WMI, consulte [WMI não está funcionando!](/previous-versions/tn-archive/ff406382(v=msdn.10))

 

> [!Note]  
> O WMI é totalmente suportado pela Microsoft; no entanto, a versão mais recente do controle e script administrativo está disponível por meio da MI (infraestrutura de gerenciamento Windows) do Windows. A MI é totalmente compatível com versões anteriores do WMI e fornece uma série de recursos e benefícios que facilitam o design e o desenvolvimento de provedores e clientes. Para obter mais informações, [consulte Windows mi (infraestrutura](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)de gerenciamento) .

 

## <a name="where-applicable"></a>Quando aplicável

O WMI pode ser usado em Windows aplicativos baseados em dados e é mais útil em aplicativos empresariais e scripts administrativos.

Os administradores do sistema podem encontrar informações sobre como usar o WMI no TechNet [ScriptCenter](https://www.microsoft.com/technet/scriptcenter/default.mspx)e em vários livros sobre o WMI. Para obter mais informações, consulte [Mais informações.](further-information.md)

## <a name="developer-audience"></a>Público de desenvolvedores

O WMI foi projetado para programadores que usam C/C++, o aplicativo Microsoft Visual Basic ou uma linguagem de script que tem um mecanismo no Windows e lida com objetos ActiveX Microsoft. Embora alguma familiaridade com a programação COM seja útil, os desenvolvedores do C++ que estão escrevendo aplicativos podem encontrar bons exemplos para começar a criar um aplicativo WMI usando [C++.](creating-a-wmi-application-using-c-.md)

Para desenvolver provedores de código gerenciado ou aplicativos em C# ou Visual Basic .NET usando o .NET Framework, consulte [WMI no .NET Framework](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).

Muitos administradores e profissionais de TI acessam o WMI por meio do PowerShell. O cmdlet Get-WMI para PowerShell permite que você recupere informações para um repositório WMI local ou remoto. Assim, vários tópicos e classes, especialmente na seção Criando clientes [WMI,](creating-wmi-clients.md) contêm exemplos do PowerShell. Para obter informações adicionais sobre como usar o PowerShell, [consulte Windows PowerShell](https://msdn.microsoft.com/library/dd835506.aspx) [scripts com Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx).

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

Para obter mais informações sobre qual sistema operacional é necessário para usar um elemento de API específico ou classe WMI, consulte a seção Requisitos de cada tópico na documentação do WMI.

Se um componente esperado parecer estar ausente, consulte Disponibilidade do sistema operacional [de componentes WMI](operating-system-availability-of-wmi-components.md).

Você não precisa baixar nem instalar um SDK (desenvolvimento de software) específico para criar scripts ou aplicativos para WMI. No entanto, há algumas ferramentas administrativas WMI que os desenvolvedores acham úteis. Para obter mais informações, consulte a seção Downloads em [Informações Adicionais](further-information.md).

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[Sobre o WMI](about-wmi.md)
</dt> <dd>

Informações gerais sobre o WMI.

</dd> <dt>

[Usando o WMI](using-wmi.md)
</dt> <dd>

Informações sobre como desenvolver aplicativos para usar o WMI, que inclui informações sobre ferramentas.

</dd> <dt>

[Referência de WMI](wmi-reference.md)
</dt> <dd>

Documentação sobre as classes WMI, as classes WMI C++, a API COM do WMI, a API de Script e outros materiais de referência do WMI.

</dd> </dl>

 

 
