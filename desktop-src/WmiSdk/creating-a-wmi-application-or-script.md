---
description: qualquer linguagem de script, como o VBScript, que funciona com ActiveX objetos pode acessar dados do WMI. os aplicativos podem acessar o wmi em C++, usando a api COM para wmi ou no Visual Basic, usando a biblioteca de tipos Wbemdisp. tlb e a API de script para WMI. .
ms.assetid: c0d18827-6b36-4817-8cd9-06cd0f267b28
ms.tgt_platform: multiple
title: Criando um script ou aplicativo WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddde26b2a8495126b4aa26c132adb49860627230d698431df5d713e653f1d874
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412126"
---
# <a name="creating-a-wmi-application-or-script"></a>Criando um script ou aplicativo WMI

qualquer linguagem de script, como o VBScript, que funciona com ActiveX objetos pode acessar dados do WMI. os aplicativos podem acessar o wmi em C++, usando a [api COM para wmi](com-api-for-wmi.md) ou no Visual Basic, usando a [biblioteca de tipos](using-the-wmi-scripting-type-library.md) Wbemdisp. tlb e a [API de script para WMI](scripting-api-for-wmi.md). . Você pode obter dados por meio do WMI escrevendo um script, uma página de Active Server (ASP) ou um aplicativo HTML (HTA). você também pode usar Windows PowerShell para obter dados ou gravar scripts. Para obter mais informações, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script) e [introdução com Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true). O TechNet ScriptCenter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) contém centenas de exemplos de script. Para obter mais informações sobre recursos de impressão e online, consulte [mais informações](further-information.md).

O procedimento a seguir descreve como se conectar ao serviço WMI e ao armazenamento de dados.

**Para se conectar ao serviço WMI e ao armazenamento de dados**

1.  Localize o serviço WMI em um computador específico.
2.  Conexão a um ou mais namespaces do WMI.

essas operações são diferentes em C++, Visual Basic, .NET Framework linguagens ou ao usar um script. Scripts e Visual Basic aplicativos devem acessar classes cujas instâncias são fornecidas com os dados por provedores existentes. Mas os aplicativos escritos em C++ podem fazer mais. Por exemplo, um aplicativo escrito em C++ pode enviar eventos, mas um script WMI só pode assinar eventos de recebimento.

Um provedor WMI só pode ser escrito em C++ ou usando o .NET Framework. para obter mais informações sobre como escrever aplicativos em C# ou Visual Basic .net, consulte [visão geral do WMI .net](/previous-versions/bb404655(v=vs.90)).

Para obter mais informações sobre como criar aplicativos e scripts para o WMI, consulte:

-   [Criando um aplicativo WMI usando C++](creating-a-wmi-application-using-c-.md)
-   [Criando um script WMI](creating-a-wmi-script.md)
-   [Criando um cliente WMI gerenciado](creating-a-managed-wmi-client.md)

Para executar a maioria das tarefas, use as [classes do WMI](wmi-classes.md)pré-instalado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o WMI](using-wmi.md)
</dt> </dl>

 

 
