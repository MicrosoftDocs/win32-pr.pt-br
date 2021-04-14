---
description: Quando você executa um script em um sistema local que obtém dados de um sistema remoto, o WMI fornece suas credenciais para o provedor de dados no sistema remoto.
ms.assetid: e27ff207-b067-47df-9706-e8af51646d28
ms.tgt_platform: multiple
title: Delegando com WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8a624f3d437d977ff73b3854a59cfd634350e7
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104370824"
---
# <a name="delegating-with-wmi"></a>Delegando com WMI

Quando você executa um script em um sistema local que obtém dados de um sistema remoto, o WMI fornece suas credenciais para o provedor de dados no sistema remoto. Isso requer apenas um nível de representação de **Impersonate**, pois apenas um salto de rede é necessário. No entanto, se o script se conectar ao WMI no sistema remoto e tentar abrir um arquivo de log em um sistema remoto adicional, o script falhará, a menos que o nível de representação seja **delegado**. O nível de representação de **delegado** é exigido por qualquer operação que envolva mais de um salto de rede. Para obter mais informações sobre segurança DCOM no WMI, consulte [definindo a segurança do processo do aplicativo cliente](setting-client-application-process-security.md). Para obter mais informações sobre uma conexão de salto de uma rede entre dois computadores, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).

**Para usar a delegação para se conectar a um computador por meio de outro computador**

1.  Habilite a delegação no Active Directory (**Active Directory usuários e computadores** em **tarefas administrativas** do **painel de controle** ) no controlador de domínio. A conta no sistema remoto deve ser marcada como **confiável para delegação** e a conta no sistema local não deve ser marcada, pois a **conta é confidencial e não pode ser delegada**. o sistema local, o sistema remoto e o controlador de domínio devem ser membros do mesmo domínio ou em domínios confiáveis.

    **Observação**  Usar a delegação é um risco de segurança, pois fornece aos processos fora do seu controle direto a capacidade de usar suas credenciais.

2.  Modifique seu código da maneira a seguir para indicar que você deseja usar a delegação.

    <dl> <dt>

    <span id="PowerShell"></span><span id="powershell"></span><span id="POWERSHELL"></span>PowerShell
    </dt> <dd>

    Defina o parâmetro *-Impersonation* no cmdlet do WMI como **delegado**.

    </dd> <dt>

    <span id="VBScript"></span><span id="vbscript"></span><span id="VBSCRIPT"></span>VBScript
    </dt> <dd>

    Defina o parâmetro *ImpersonationLevel* para **delegar** na chamada para [SWbemLocator. ConnectServer](swbemlocator-connectserver.md) ou **delegado** na cadeia de caracteres do [moniker](constructing-a-moniker-string.md) . Você também pode definir a representação em um objeto [**SWbemSecurity**](swbemsecurity.md).

    </dd> <dt>

    <span id="C__"></span><span id="c__"></span>C++
    </dt> <dd>

    Defina o parâmetro de nível de representação para o **delegado de nível de imp do RPC \_ C \_ \_ \_** na chamada para [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ou [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket). Para obter mais informações sobre quando fazer essas chamadas, consulte [Inicializando com para um aplicativo WMI](initializing-com-for-a-wmi-application.md).

    Para passar a identidade do cliente para servidores COM remotos em C++, defina o encobrimento na chamada para [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket). Para obter mais informações, consulte [encobrindo](../com/cloaking.md).

    </dd> </dl>

## <a name="examples"></a>Exemplos

O exemplo de código a seguir mostra uma cadeia de caracteres do moniker que define a representação a ser **delegada**. Lembre-se de que a autoridade deve ser definida como Kerberos.


```vb
set objWMIServices = Getobject("winmgmts:{impersonationLevel=Delegate,authority=kerberos:MyDomain\Computer_B}!\\ComputerB\Root\CIMv2")
```



O exemplo de código a seguir mostra como definir a representação para **delegar** (um valor de 4) usando [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).


```vb
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objWMIService = objLocator.ConnectServer(Computer_B, _
                                             "Root\CIMv2", _
                                             AdminAccount, _
                                             MyPassword, _
                                             "kerberos:Domain\Computer_B")
objWMIService.Security_.ImpersonationLevel = 4
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Protegendo uma conexão WMI remota](securing-a-remote-wmi-connection.md)
</dt> <dt>

[Criando processos remotamente com o WMI](creating-processes-remotely.md)
</dt> </dl>

 

 
