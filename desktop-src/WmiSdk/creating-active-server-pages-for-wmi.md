---
description: Descreve como criar ASP (Microsoft Active Server Pages) que exibem informações sobre computadores remotos para computadores que não têm o WMI instalado.
ms.assetid: add08566-6408-43e4-9d0d-4c0851540602
ms.tgt_platform: multiple
title: Criando Active Server páginas para WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee7b31a5f4874e0ae4431ac452ea604da9c154bbb78e8debb91aad7ea892fa09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030606"
---
# <a name="creating-active-server-pages-for-wmi"></a>Criando Active Server páginas para WMI

O ASP (Microsoft Active Server Pages) pode criar páginas da Web dinâmicas incluindo scripts do lado do servidor e do lado do cliente. As páginas ASP podem ser muito mais rápidas do que as páginas HTML do cliente porque a maior parte do trabalho é feita no servidor. Você também pode usar páginas ASP para exibir informações sobre computadores remotos para outros computadores que não têm a WMI (Instrumentação de Gerenciamento de Windows) instalada.

O procedimento a seguir descreve como usar o WMI com o ASP.

**Para usar o WMI com o ASP**

1.  Escreva uma página ASP (.asp) que usa o WMI e coloque-a em um diretório acessível ao servidor Web.

    Scripts ASP para WMI podem ser desenvolvidos com várias linguagens de script, incluindo VBScript. Você pode construir a parte de script WMI de uma página ASP exatamente como constrói qualquer outro script que usa WMI, com uma restrição importante: você não pode usar métodos WMI assíncronos em páginas ASP. Observe também que todas as chamadas **para GetObject** ou **CreateObject** devem estar no código do lado do servidor. Para obter mais informações, consulte [API de script para WMI](scripting-api-for-wmi.md).

2.  Configurar a configuração de autenticação para Serviços de Informações da Internet (IIS). Para obter mais informações, [consulte Configuring IIS 5 and Later for WMI ASP Scripting](configuring-iis-5-for-wmi-asp-scripting.md).
3.  Desabilite o acesso anônimo e habilita Windows Autenticação Integrada para o arquivo ASP. Você pode definir essas configurações para sua página do ASP  usando o snap-in do IIS localizado na pasta Ferramentas Administrativas do **Painel de Controle**.

## <a name="wmi-asp-page-example"></a>Exemplo de página ASP do WMI

O exemplo a seguir usa Windows WMI (Instrumentação de Gerenciamento) em uma ASP (página de Active Server) para exibir as configurações de endereço IP e gateway IP padrão para o servidor do qual esse script é executado.


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



 

 



