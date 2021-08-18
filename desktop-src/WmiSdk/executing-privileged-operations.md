---
description: As operações privilegiadas exigem privilégios de segurança, como SeLoadDriverPrivilege (wbemPrivilegeLoadDriver nas Constantes de API de Script), um privilégio que deve ser habilitado para uma conta que está carregando um driver de dispositivo.
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
ms.openlocfilehash: ce87a5783462be86d6e2e2b0565e93d811b972393319a34f84be2ab3d8e34c64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050864"
---
# <a name="executing-privileged-operations"></a>Executando operações privilegiadas

As operações privilegiadas exigem privilégios de segurança, como **SeLoadDriverPrivilege** (**wbemPrivilegeLoadDriver** nas Constantes da API de [Script),](scripting-api-constants.md)um privilégio que deve ser habilitado para uma conta que está carregando um driver de dispositivo. Não é possível adicionar privilégios a um administrador ou usuário por meio do WMI, você só pode habilitar os privilégios que a conta já tem. Para ver uma lista de privilégios, consulte [**\_ Constantes de privilégio.**](privilege-constants.md)

Por padrão, um usuário local em um computador pode ler dados estáticos do repositório [*WMI,*](gloss-w.md)gravar em instâncias fornecidas por provedores e executar métodos de provedor, a menos que o provedor imputação requisitos de segurança especiais próprios. Somente os administradores podem [se conectar a](connecting-to-wmi-on-a-remote-computer.md)um computador remoto, alterar descritores de segurança ou alterar dados de repositório WMI estáticos, como uma definição de classe WMI. Todos os privilégios são habilitados para uma conexão remota. Para obter mais informações, consulte [Proteger uma conexão WMI remota.](securing-a-remote-wmi-connection.md)

As constantes de privilégio para C++ diferem daquelas usadas por linguagens de automação, como Visual Basic. Os scripts devem usar o valor da constante em vez do nome. Para obter mais informações, [consulte Executando operações privilegiadas usando C++](executing-privileged-operations-using-c-.md) ou [Executando operações privilegiadas usando o VBScript.](executing-privileged-operations-using-vbscript.md)

Uma causa comum de erros de acesso negado ao usar o WMI é a falta de um privilégio habilitado para operações, como obter todas as instâncias do [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)). Sem habilenciar **o privilégio SeSecurity,** você não pode acessar o arquivo de log de segurança.

O exemplo de código VBScript a seguir mostra como definir o privilégio **SeSecurity** na cadeia de caracteres do moniker. Quando usado no moniker, o nome do privilégio entre parênteses descarta o "Se" inicial. Para obter mais informações, consulte [Constructing a Moniker String](constructing-a-moniker-string.md).


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

 

 
