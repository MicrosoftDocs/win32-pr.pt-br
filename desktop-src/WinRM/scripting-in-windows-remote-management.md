---
title: Scripts no Windows Gerenciamento Remoto
description: A API de Script no WinRM e a API COM para C++ que o acompanha foram projetadas para refletir de perto as operações do protocolo WS-Management.
ms.assetid: fda2042a-8fca-4cd8-bb55-fd1c3591921e
ms.tgt_platform: multiple
keywords:
- Scripts no Windows Gerenciamento Remoto
- Windows Gerenciamento Remoto, script no
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c10d36420b2826162a6ed5e3fb6bf69408a74032faafac75c84c25a754cf534
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795426"
---
# <a name="scripting-in-windows-remote-management"></a>Scripts no Windows Gerenciamento Remoto

A [API de Script no WinRM](winrm-scripting-api.md) e a API COM para C++ que o acompanha foram projetadas para refletir de perto as operações do protocolo WS-Management.

A API de Script WinRM no Windows Remote Management dá suporte a todas as WS-Management de protocolo, exceto uma. Ele não permite assinaturas para eventos. Para assinar eventos do Log de Eventos do Sistema BMC, você deve usar as ferramentas de linha de comando Wecutil ou Wevtutil. Para obter mais informações, consulte [Eventos](events.md).

A API de Script WinRM é chamada por Winrm.vbs, uma ferramenta de linha de comando, que é escrita em Visual Basic Scripting Edition (VBScript). Winrm.vbs fornece exemplos de como usar a [API de Script WinRM](winrm-scripting-api.md).

## <a name="using-wsman-compared-to-using-wmi-scripting"></a>Usando o WSman em comparação com o uso de scripts WMI

O WMI se conecta a computadores remotos por meio do DCOM, o que requer a configuração descrita em Conectando-se [ao WMI em um computador remoto.](/windows/desktop/WmiSdk/connecting-to-wmi-on-a-remote-computer) O WinRM não usa o DCOM para se conectar a um computador remoto. Em vez disso, WS-Management protocolo envia mensagens SOAP e o serviço usa uma única porta para HTTP e uma porta para transporte HTTPS.

Ao contrário da ferramenta de linha de comando **winrm,** os scripts devem fornecer o XML necessário para passar para as mensagens WS-Management protocolo. Eles também devem fornecer URIs. Para obter mais informações, consulte [URIs de](resource-uris.md) recurso [e Windows Gerenciamento Remoto Remoto e WMI](windows-remote-management-and-wmi.md).

A API de Script WMI funciona com objetos, como instâncias do [**\_ LogicalDisk do Win32,**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)que representam recursos em um computador. Essa classe WMI é definida [*em arquivos Managed Object Format (MOF),*](/windows/desktop/WmiSdk/gloss-m) que são armazenados em formato binário no repositório WMI. No WMI, uma operação Get para um único recurso ou uma consulta para várias instâncias retorna objetos WMI.

Um script WinRM não retorna objetos, mas sim fluxos de texto XML. Para obter mais informações, [consulte Windows Gerenciamento Remoto e WMI.](windows-remote-management-and-wmi.md)

## <a name="displaying-xml-output-from-winrm-scripts"></a>Exibindo a saída XML de scripts WinRM

A API de Script WinRM obtém e recebe cadeias de caracteres XML que descrevem recursos. O XML resultante está na forma de um fluxo de texto e requer que uma transformação XML seja exibida de alguma outra maneira.

O script WinRM a seguir produz uma saída XML bruta.


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set xmlFile = CreateObject( "MSxml.DOMDocument")
Set Session = Wsman.CreateSession
Response = Session.Get("http://schemas.microsoft.com/wbem/wsman/" _
    & "1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(Response)
xmlFile.Save( "c:\RawOutput.xml")
```



O bloco de texto a seguir mostra a saída XML do script WinRM.


```XML
<p:Win32_Service xmlns:xsi="https://www.w3.org/2001/XMLSchema-
instance" xmlns:p="http://schemas.microsoft.com/wbem/wsman/1
/wmi/root/cimv2/Win32_Service" xmlns:cim="https://schemas.dmtf
.org/wbem/wsman/1/base" cim:Class="Win32_Service"><p:AcceptP
ause>false</p:AcceptPause><p:AcceptStop>true</p:AcceptStop>
<p:Caption>Print Spooler</p:Caption><p:CheckPoint>0</p:CheckP
oint><p:CreationClassName>Win32_Service</p:CreationClassName>
<p:Description>Loads files to memory for later printing</p:De
scription><p:DesktopInteract>true</p:DesktopInteract><p:Displ
ayName>Print Spooler</p:DisplayName><p:ErrorControl>Normal</p
:ErrorControl><p:ExitCode>0</p:ExitCode><p:InstallDate xsi:ni
l="true"/><p:Name>spooler</p:Name><p:PathName>C:\Windows\Syst
em32\spoolsv.exe</p:PathName><p:ProcessId>1720</p:ProcessId><
p:ServiceSpecificExitCode>0</p:ServiceSpecificExitCode><p:Ser
viceType>Own Process</p:ServiceType><p:Started>true</p:Starte
d><p:StartMode>Auto</p:StartMode><p:StartName>LocalSystem</p:
StartName><p:State>Running</p:State><p:Status>OK</p:Status><p
:SystemCreationClassName>Win32_ComputerSystem</p:SystemCreati
onClassName><p:SystemName>wsplab6-4</p:SystemName><p:TagId>0<
/p:TagId><p:WaitHint>0</p:WaitHint><cim:Location xmlns:cim="h
ttp://schemas.dmtf.org/wbem/wsman/1/base" xmlns:a="https://sc
hemas.xmlsoap.org/ws/2004/08/addressing" xmlns:w="https://sche
mas.dmtf.org/wbem/wsman/1/wsman"><a:Address>https://schemas.xm
lsoap.org/ws/2004/08/addressing/role/anonymous</a:Address><a:
ReferenceParameters><w:ResourceURI>https://schemas.microsoft.c
om/wbem/wsman/1/wmi/root/cimv2/Win32_Service</w:ResourceURI><
w:SelectorSet><w:Selector Name="Name">spooler</w:Selector></w
:SelectorSet></a:ReferenceParameters></cim:Location></p:Win32
_Service>
```



Seus scripts podem usar uma transformação XML para tornar essa saída mais acessível. Para obter mais informações, [consulte Exibindo a saída XML de scripts WinRM.](displaying-xml-output-from-winrm-scripts.md)

A versão a seguir do script formatará o XML em uma saída acessível por humanos.


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set xmlFile = CreateObject( "MSXml.DOMDocument" )
Set xslFile = CreateObject( "MSXml.DOMDocument" )

Set Session = Wsman.CreateSession
Response = Session.Get("http://schemas.microsoft.com/wbem/wsman/" _
    & "1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(Response)
xslFile.Load( "WsmTxt.xsl" )
Wscript.Echo xmlFile.TransformNode( xslFile )
```



A transformação XSL cria a saída a seguir.


```XML
Win32_Service
    AcceptPause = false
    AcceptStop = true
    Caption = Print Spooler
    CheckPoint = 0
    CreationClassName = Win32_Service
    Description = Loads files to memory for later printing
    DesktopInteract = true
    DisplayName = Print Spooler
    ErrorControl = Normal
    ExitCode = 0
    InstallDate = null
    Name = Spooler
    PathName = C:\Windows\System32\spoolsv.exe
    ProcessId = 1720
    ServiceSpecificExitCode = 0
    ServiceType = Own Process
    Started = true
    StartMode = Auto
    StartName = LocalSystem
    State = Running
    Status = OK
    SystemCreationClassName = Win32_ComputerSystem
    SystemName = wsplab6-4
    TagId = 0
    WaitHint = 0
```



## <a name="winrm-script-and-winrmcmd-output"></a>Saída do WinRM Script e Winrm.cmd

A saída de um script WinRM é codificada em Unicode. Se você criar um [FileSystemObject](/previous-versions//6kxy1a51(v=vs.85)) e gravar um arquivo do script, o arquivo resultante será Unicode. No entanto, se você redirecionar a saída para um arquivo, a codificação será ANSI. Se você redirecionar a saída para um arquivo XML e houver caracteres Unicode na saída, o XML será inválido. Esteja ciente de que a ferramenta de linha de **comando Winrm** saída ANSI.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre Windows gerenciamento remoto](about-windows-remote-management.md)
</dt> <dt>

[Usando Windows gerenciamento remoto](using-windows-remote-management.md)
</dt> <dt>

[Msxsl](/previous-versions/windows/desktop/ms763742(v=vs.85))
</dt> <dt>

[Referência dom](/previous-versions/windows/desktop/ms764730(v=vs.85))
</dt> </dl>

 

 