---
description: Windows a instrumentação de gerenciamento (WMI) é a infraestrutura para dados de gerenciamento e operações em sistemas operacionais baseados em Windows.
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

Windows a instrumentação de gerenciamento (WMI) é a infraestrutura para dados de gerenciamento e operações em sistemas operacionais baseados em Windows. você pode gravar scripts ou aplicativos WMI para automatizar tarefas administrativas em computadores remotos, mas o WMI também fornece dados de gerenciamento para outras partes do sistema operacional e produtos, por exemplo System Center Operations Manager, anteriormente Microsoft Operations Manager (MOM) ou Gerenciamento Remoto do Windows ([WinRM](/windows/desktop/WinRM/portal)).

> [!Note]  
> A documentação a seguir destina-se a desenvolvedores e administradores de ti. Se você for um usuário final que recebeu uma mensagem de erro relacionada ao WMI, vá para [suporte da Microsoft](https://support.microsoft.com/) e procure o código de erro que você vê na mensagem de erro. Para obter mais informações sobre como solucionar problemas com scripts WMI e o serviço WMI, consulte o [WMI não está funcionando!](/previous-versions/tn-archive/ff406382(v=msdn.10))

 

> [!Note]  
> O WMI tem suporte total da Microsoft; no entanto, a versão mais recente do controle e script administrativo está disponível por meio da MI (infraestrutura de gerenciamento de Windows). MI é totalmente compatível com as versões anteriores do WMI e fornece um host de recursos e benefícios que facilitam ainda mais o projeto e o desenvolvimento de provedores e clientes. para obter mais informações, consulte [Windows Management Infrastructure (MI)](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure).

 

## <a name="where-applicable"></a>Quando aplicável

o WMI pode ser usado em todos os aplicativos baseados em Windows e é mais útil em aplicativos empresariais e scripts administrativos.

Os administradores do sistema podem encontrar informações sobre como usar o WMI no TechNet [ScriptCenter](https://www.microsoft.com/technet/scriptcenter/default.mspx)e em vários livros sobre o WMI. Para obter mais informações, consulte [mais informações](further-information.md).

## <a name="developer-audience"></a>Público de desenvolvedores

o WMI foi projetado para programadores que usam o C/C++, o aplicativo Microsoft Visual Basic ou uma linguagem de script que tem um mecanismo no Windows e manipula objetos do microsoft ActiveX. Embora alguma familiaridade com a programação COM seja útil, os desenvolvedores de C++ que estão escrevendo aplicativos podem encontrar bons exemplos de introdução à [criação de um aplicativo WMI usando C++](creating-a-wmi-application-using-c-.md).

para desenvolver provedores de código gerenciado ou aplicativos em C# ou Visual Basic .net usando o .NET Framework, consulte [WMI no .NET Framework](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).

Muitos administradores e profissionais de ti acessam o WMI por meio do PowerShell. O cmdlet Get-WMI para o PowerShell permite que você recupere informações para um repositório WMI local ou remoto. Assim, vários tópicos e classes, especialmente na seção [criando clientes WMI](creating-wmi-clients.md) , contêm exemplos do PowerShell. para obter informações adicionais sobre como usar o PowerShell, consulte [Windows PowerShell](https://msdn.microsoft.com/library/dd835506.aspx) e [scripts com Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx).

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

Para obter mais informações sobre qual sistema operacional é necessário para usar um elemento de API específico ou uma classe WMI, consulte a seção requisitos de cada tópico na documentação do WMI.

Se um componente esperado parece estar ausente, consulte [disponibilidade do sistema operacional de componentes WMI](operating-system-availability-of-wmi-components.md).

Você não precisa baixar ou instalar um SDK (desenvolvimento de software) específico para criar scripts ou aplicativos para o WMI. No entanto, há algumas ferramentas administrativas do WMI que os desenvolvedores consideram úteis. Para obter mais informações, consulte a seção downloads em [mais informações](further-information.md).

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

Documentação sobre as classes WMI, as classes WMI C++, a API COM do WMI, a API de script e outros materiais de referência do WMI.

</dd> </dl>

 

 
