---
description: Descreve como criar páginas do Microsoft Active Server (ASP) que exibem informações sobre computadores remotos em computadores que não têm o WMI instalado.
ms.assetid: add08566-6408-43e4-9d0d-4c0851540602
ms.tgt_platform: multiple
title: Criando páginas de Active Server para o WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 52143284be54868d36b55a6dd86e0b49c82d863d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811666"
---
# <a name="creating-active-server-pages-for-wmi"></a>Criando páginas de Active Server para o WMI

O ASP (Microsoft Active Server Pages) pode criar páginas da Web dinâmicas, incluindo scripts do lado do servidor e do lado do cliente. As páginas ASP podem ser muito mais rápidas do que as páginas HTML do cliente porque a maior parte do trabalho é feita no servidor. Você também pode usar páginas ASP para exibir informações sobre computadores remotos em outros computadores que não têm o Instrumentação de Gerenciamento do Windows (WMI) instalado.

O procedimento a seguir descreve como usar o WMI com ASP.

**Para usar o WMI com ASP**

1.  Escreva uma página ASP (. asp) que usa o WMI e coloque-a em um diretório acessível ao seu servidor Web.

    Scripts ASP para WMI podem ser desenvolvidos com várias linguagens de script, incluindo o VBScript. Você pode construir a parte do script WMI de uma página ASP exatamente como construir qualquer outro script que usa o WMI, com uma restrição importante: não é possível usar métodos WMI assíncronos em páginas ASP. Observe também que todas as chamadas para **GetObject** ou **CreateObject** devem estar no código do lado do servidor. Para obter mais informações, consulte [API de script para WMI](scripting-api-for-wmi.md).

2.  Defina a configuração de autenticação para o Serviços de Informações da Internet (IIS). Para obter mais informações, consulte [Configuring IIS 5 and posterior for WMI ASP scripting](configuring-iis-5-for-wmi-asp-scripting.md).
3.  Desabilite o acesso anônimo e habilite a autenticação integrada do Windows para o arquivo ASP. Você pode definir essas configurações para sua página ASP usando o snap-in do IIS localizado na pasta **Ferramentas administrativas** do painel de **controle**.

## <a name="wmi-asp-page-example"></a>Exemplo de página ASP WMI

O exemplo a seguir usa Instrumentação de Gerenciamento do Windows (WMI) em uma página de Active Server (ASP) para exibir o endereço IP e as configurações de gateway de IP padrão para o servidor do qual esse script é executado.


```VB
<%@ LANGUAGE="VBSCRIPT"%>
<HTML>
<HEAD>
<TITLE>WMI ASP Example:
    Read Default Gateway and IP Address information </TITLE>
</HEAD>

<BODY>

<%
On Error Resume Next
set IPConfigSet = GetObject("winmgmts:" _
   & "{impersonationLevel=impersonate}!root\cimv2").ExecQuery" _
    & "("SELECT IPAddress, DefaultIPGateway "" _ 
    & " FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled=TRUE")
%>

<%If Err <> 0 Then %>
    <%if err.number = -2147217405 then%>
        <p>Error 0x80041003: Access Denied: 
           Check permissions and file security for this ASP file.</p>
    <%else%>
        <p>Error description: <%=Err.description%> 
           error number <%=Err.number%></p>
    <%end if%>

<%end if %>

<%for each IPConfig in IPConfigSet%>

    <%if Not IsNull(IPConfig.IPAddress) then %>
        <%for i=LBound(IPConfig.IPAddress) 
            to UBound(IPConfig.IPAddress)%>
            <p>IP Address: <%=IPConfig.IPAddress(i)%></p>
        <%next%>
    <%end if%>
    

    <%if Not IsNull(IPConfig.DefaultIPGateway) then %>
        <%for i=LBound(IPConfig.DefaultIPGateway) 
            to UBound(IPConfig.DefaultIPGateway)%>
            <p>Default IP Gateway: 
                <%=IPConfig.DefaultIPGateway(i)%></p>
        <%next%>
    <%end if%>
<%next%>

<%If Err <> 0 Then %>
    <p>error description: <%=Err.description%> 
       error number <%=Err.number%></p>
<%end if %>

</BODY>
</HTML>
```



 

 



