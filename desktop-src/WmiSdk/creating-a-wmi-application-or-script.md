---
description: Qualquer linguagem de script, como o VBScript, que funciona com objetos ActiveX pode acessar dados do WMI. Os aplicativos podem acessar o WMI em C++, usando a API COM para WMI ou no Visual Basic, usando a biblioteca de tipos Wbemdisp. tlb e a API de script para WMI. .
ms.assetid: c0d18827-6b36-4817-8cd9-06cd0f267b28
ms.tgt_platform: multiple
title: Criando um script ou aplicativo WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b27e3cffd7e4d9bea4ce36e7c0da77ae5d72cdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810778"
---
# <a name="creating-a-wmi-application-or-script"></a>Criando um script ou aplicativo WMI

Qualquer linguagem de script, como o VBScript, que funciona com objetos ActiveX pode acessar dados do WMI. Os aplicativos podem acessar o WMI em C++, usando a [API com para WMI](com-api-for-wmi.md) ou no Visual Basic, usando a [biblioteca de tipos](using-the-wmi-scripting-type-library.md) Wbemdisp. tlb e a [API de script para WMI](scripting-api-for-wmi.md). . Você pode obter dados por meio do WMI escrevendo um script, uma página de Active Server (ASP) ou um aplicativo HTML (HTA). Você também pode usar o Windows PowerShell para obter dados ou gravar scripts. Para obter mais informações, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script) e [introdução com o Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true). O TechNet ScriptCenter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) contém centenas de exemplos de script. Para obter mais informações sobre recursos de impressão e online, consulte [mais informações](further-information.md).

O procedimento a seguir descreve como se conectar ao serviço WMI e ao armazenamento de dados.

**Para se conectar ao serviço WMI e ao armazenamento de dados**

1.  Localize o serviço WMI em um computador específico.
2.  Conecte-se a um ou mais namespaces do WMI.

Essas operações são diferentes em C++, Visual Basic, .NET Framework linguagens ou ao usar um script. Scripts e Visual Basic aplicativos devem acessar classes cujas instâncias são fornecidas com os dados por provedores existentes. Mas os aplicativos escritos em C++ podem fazer mais. Por exemplo, um aplicativo escrito em C++ pode enviar eventos, mas um script WMI só pode assinar eventos de recebimento.

Um provedor WMI só pode ser escrito em C++ ou usando o .NET Framework. Para obter mais informações sobre como escrever aplicativos em C# ou Visual Basic .NET, consulte [visão geral do WMI .net](/previous-versions/bb404655(v=vs.90)).

Para obter mais informações sobre como criar aplicativos e scripts para o WMI, consulte:

-   [Criando um aplicativo WMI usando C++](creating-a-wmi-application-using-c-.md)
-   [Criando um script WMI](creating-a-wmi-script.md)
-   [Criando um cliente WMI gerenciado](creating-a-managed-wmi-client.md)

Para executar a maioria das tarefas, use as [classes do WMI](wmi-classes.md)pré-instalado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o WMI](using-wmi.md)
</dt> </dl>

 

 
