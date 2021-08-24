---
description: Conectando-se remotamente ao WMI com o PowerShell
ms.assetid: 9a06f0c3-2845-48aa-9988-79cc4607ce19
ms.tgt_platform: multiple
title: Conectando-se remotamente ao WMI com o PowerShell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d499c59ee6774b1e972e192dfc2c0d1228469196c66e8f3feb80d1c9d6339c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679866"
---
# <a name="connecting-to-wmi-remotely-with-powershell"></a>Conectando-se remotamente ao WMI com o PowerShell

Windows PowerShell fornece um mecanismo simples para se conectar Windows WMI (Instrumentação de Gerenciamento) em um computador remoto. As conexões remotas no WMI são afetadas [pelo Firewall do Windows,](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11))pelas configurações do DCOM e pelo [UAC (Controle](/previous-versions/aa905108(v=msdn.10))de Conta de Usuário). Para obter mais informações sobre como configurar conexões remotas, consulte [Conectando-se ao WMI remotamente começando com Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md).

Os exemplos neste tópico se baseiam nos VBScripts de [Conectando-se ao WMI em um computador remoto.](connecting-to-wmi-on-a-remote-computer.md) Todos os exemplos neste tópico usam o cmdlet [Get-WmiObject.](/previous-versions//dd315295(v=technet.10)) Para obter mais informações, [consulte Get-WmiObject](/previous-versions//dd315295(v=technet.10)).

## <a name="windows-powershell-examples"></a>Windows PowerShell exemplos

Ao criar uma conexão com um computador remoto, um usuário pode especificar as informações de conexão, como o nome do computador remoto, as credenciais e o nível de autenticação para a conexão. Os exemplos a seguir ilustram como se conectar a um computador remoto usando diferentes conjuntos de credenciais e como acessar informações do WMI.

O exemplo Windows PowerShell a seguir mostra como definir o nível de representação:


```PowerShell

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -ComputerName Computer_B
```



No exemplo anterior, o usuário se conecta a um computador remoto usando as mesmas credenciais (domínio e nome de usuário) com as mesmas credenciais com as que fez logout. O usuário também solicitou o uso da representação. Ao contrário do exemplo de VBScript original, uma cadeia de caracteres de moniker não é necessária porque o nível de representação é definido pela propriedade "Impersonation". Por padrão, o nível de representação é definido como 3 (Representar).

O exemplo lista todas as instâncias da classe [**Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process) que estão em execução no computador remoto.

> [!Note]  
> Você deve especificar o namespace WMI ao qual se conectar no computador remoto, pois é possível que o namespace padrão não seja o mesmo em computadores diferentes.

 

O exemplo Windows PowerShell a seguir mostra como se conectar a um computador remoto com credenciais diferentes e definir o nível de representação como 3, que é Representar:


```PowerShell

$Computer = "atl-dc-01"

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -Credential `
FABRIKAM\administrator -ComputerName $Computer
```



No exemplo anterior, o nome do computador foi atribuído à variável $Computer dados. O usuário se conecta a um computador remoto usando credenciais específicas (domínio e nome de usuário) e solicita a representação para o nível de autenticação.

> [!Note]  
> O caractere de acento grave ( \` ) é usado para indicar uma quebra de linha. É equivalente ao caractere de sublinhado ( \_ ) no VBScript.

 

O exemplo Windows PowerShell a seguir se conecta a um grupo de computadores remotos no mesmo domínio criando uma matriz de nomes de computador remotos e, em seguida, exibindo nomes dos dispositivos Plug and Play — instâncias do [**Win32 \_ PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)— em cada computador:


```PowerShell
$ArrComputers = "Computer1", "Computer2", "Computer3"
foreach ($Computer in $ArrComputers) 
{
write-host ""
write-host "===================================="
write-host "Computer: $Computer"
write-host "===================================="

write-host "-----------------------------------"
write-host "Win32_PnPEntity instance"
write-host "-----------------------------------"

$ColItems = Get-WmiObject -Class Win32_PnPEntity -Namespace "root\cimv2" -Computer $Computer
$ColItems[0..47] | Format-List Name, Status
}
```



> [!Note]  
> Para executar o script Windows PowerShell anterior, você deve ser um administrador nos computadores remotos. Além disso, em relação ao exemplo anterior, observe o seguinte:

 

-   Os nomes de computador na matriz devem ser entre aspas porque são cadeias de caracteres.
-   Os objetos retornados pelo [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) são atribuídos à variável $ColItems dados.
-   O operador range \[ \] limitou a lista de Plug and Play dispositivos a 48 instâncias. Para obter mais informações, consulte [Sobre \_ operadores](/previous-versions//dd347588(v=technet.10)).
-   O " \| " é o caractere de pipeline. O objeto retornado por ColItems é enviado para o cmdlet [Format-List.]( /previous-versions//dd347700(v=technet.10))

O exemplo Windows PowerShell a seguir permite que você se conecte a um computador remoto em um domínio diferente. Este exemplo também exibe os nomes de processo para instâncias do [**Processo Win32 \_**](/windows/desktop/CIMWin32Prov/win32-process) no computador remoto.


```PowerShell
$Computer = "FullComputerName" 
$Domain = "DOMAIN"
$Credential = Get-Credential
$ColItems = Get-WmiObject -Class Win32_Process -Authority "ntlmdomain:$Domain" `
-Credential $Credential -Locale "MS_409" -Namespace "root\cimv2"  -ComputerName $Computer

foreach ($ObjItem in $colItems) 
{
write-host "Process Name:" $ObjItem.name
}
```



> [!Note]  
> Para executar o script Windows PowerShell anterior, você deve ser um administrador no computador remoto.

 

No exemplo anterior, o usuário se conecta a um computador remoto em um domínio diferente e especifica uma localidade preferencial. O [comando Get-Credential](/previous-versions//dd315327(v=technet.10)) solicita as credenciais do usuário e atribui as credenciais a um objeto . O exemplo também lista os nomes de instâncias da [**classe Processo \_ Win32**](/windows/desktop/CIMWin32Prov/win32-process) que estão em execução no computador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
