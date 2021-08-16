---
description: Qualquer linguagem de script, como VBScript, que funcione com ActiveX objetos pode acessar dados WMI. Os aplicativos podem acessar o WMI no C++, usando a API COM para WMI ou no Visual Basic, usando a biblioteca de tipos Wbemdisp.tlb e a API de Script para WMI. .
ms.assetid: c0d18827-6b36-4817-8cd9-06cd0f267b28
ms.tgt_platform: multiple
title: Criando um aplicativo ou script WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddde26b2a8495126b4aa26c132adb49860627230d698431df5d713e653f1d874
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412126"
---
# <a name="creating-a-wmi-application-or-script"></a>Criando um aplicativo ou script WMI

Qualquer linguagem de script, como VBScript, que funcione com ActiveX objetos pode acessar dados WMI. Os aplicativos podem acessar o WMI no C++, usando a API COM para [WMI](com-api-for-wmi.md) ou no Visual Basic, usando a biblioteca de tipos Wbemdisp.tlb [](using-the-wmi-scripting-type-library.md) e a API de Script para [WMI](scripting-api-for-wmi.md). . Você pode obter dados por meio do WMI escrevendo um script, uma ASP (página de Active Server) ou um aplicativo HTML (HTA). Você também pode usar Windows PowerShell para obter dados ou escrever scripts. Para obter mais informações, [consulte Scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script) [e Ponto de Partida com Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true). O TechNet ScriptCenter em [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) contém centenas de exemplos de script. Para obter mais informações sobre recursos de impressão e online, consulte [Mais informações.](further-information.md)

O procedimento a seguir descreve como se conectar ao serviço WMI e ao armazenamento de dados.

**Para se conectar ao serviço WMI e ao armazenamento de dados**

1.  Localize o serviço WMI em um computador específico.
2.  Conexão a um ou mais namespaces WMI.

Essas operações são diferentes em C++, Visual Basic, .NET Framework idiomas ou ao usar um script. Scripts e Visual Basic aplicativos devem acessar classes cujas instâncias são fornecidas com dados por provedores existentes. Mas os aplicativos escritos em C++ podem fazer mais. Por exemplo, um aplicativo escrito em C++ pode enviar eventos, mas um script WMI só pode assinar para receber eventos.

Um provedor WMI pode ser escrito somente em C++ ou usando o .NET Framework. Para obter mais informações sobre como escrever aplicativos em C# ou Visual Basic .NET, consulte Visão geral do [WMI .NET](/previous-versions/bb404655(v=vs.90)).

Para obter mais informações sobre como criar aplicativos e scripts para WMI, consulte:

-   [Criando um aplicativo WMI usando C++](creating-a-wmi-application-using-c-.md)
-   [Criando um script WMI](creating-a-wmi-script.md)
-   [Criando um cliente WMI gerenciado](creating-a-managed-wmi-client.md)

Para executar a maioria das tarefas, use as classes [WMI pré-instaladas.](wmi-classes.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o WMI](using-wmi.md)
</dt> </dl>

 

 
