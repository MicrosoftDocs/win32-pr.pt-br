---
description: As operações privilegiadas exigem privilégios de segurança como SeLoadDriverPrivilege (wbemPrivilegeLoadDriver nas constantes da API de script), um privilégio que deve ser habilitado para uma conta que esteja carregando um driver de dispositivo.
ms.assetid: 11bb8723-f329-4083-8219-2256ce44a5e3
ms.tgt_platform: multiple
title: Executando operações privilegiadas
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37abba9d774025825611e311f08414b50e660f65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797674"
---
# <a name="executing-privileged-operations"></a>Executando operações privilegiadas

As operações privilegiadas exigem privilégios de segurança como **SeLoadDriverPrivilege** (**wbemPrivilegeLoadDriver** nas [constantes da API de script](scripting-api-constants.md)), um privilégio que deve ser habilitado para uma conta que esteja carregando um driver de dispositivo. Você não pode adicionar privilégios a um administrador ou usuário por meio do WMI, só pode habilitar os privilégios que a conta já tem. Para obter uma lista de privilégios, [**consulte \_ constantes de privilégio**](privilege-constants.md).

Por padrão, um usuário local em um computador pode ler dados estáticos do [*repositório do WMI*](gloss-w.md), gravar em instâncias fornecidas por provedores e executar métodos de provedor, a menos que o provedor aplique requisitos de segurança especiais próprios. Somente os administradores podem [se conectar a um computador remoto](connecting-to-wmi-on-a-remote-computer.md), alterar descritores de segurança ou alterar dados estáticos do repositório WMI, como uma definição de classe WMI. Todos os privilégios estão habilitados para uma conexão remota. Para obter mais informações, consulte [protegendo uma conexão WMI remota](securing-a-remote-wmi-connection.md).

As constantes de privilégio para C++ diferem das que são usadas por linguagens de automação, como Visual Basic. Os scripts devem usar o valor da constante em vez do nome. Para obter mais informações, consulte [executando operações privilegiadas usando C++](executing-privileged-operations-using-c-.md) ou [executando operações privilegiadas usando o VBScript](executing-privileged-operations-using-vbscript.md).

Uma causa comum de erros de acesso negado ao usar o WMI é a falta de um privilégio habilitado para operações, como obter todas as instâncias do [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)). Sem habilitar o privilégio **SeSecurity** , você não pode acessar o arquivo de log de segurança.

O exemplo de código VBScript a seguir mostra como definir o privilégio **SeSecurity** na cadeia de caracteres do moniker. Quando usado no moniker, o nome do privilégio entre parênteses descarta o "se" inicial. Para obter mais informações, consulte [construindo uma cadeia de caracteres de moniker](constructing-a-moniker-string.md).


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate,(Security)}!\\" _
    & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery _
    ("Select * from Win32_NTEventLogFile " _
    & "Where LogFileName='Security'")
For Each LogFile in colFiles
Wscript.Echo LogFile.NumberOfRecords
Next
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Constantes de privilégio**](privilege-constants.md)
</dt> </dl>

 

 
