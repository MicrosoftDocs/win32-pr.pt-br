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
# <a name="creating-active-server-pages-for-wmi"></a><span data-ttu-id="ff13b-103">Criando páginas de Active Server para o WMI</span><span class="sxs-lookup"><span data-stu-id="ff13b-103">Creating Active Server Pages for WMI</span></span>

<span data-ttu-id="ff13b-104">O ASP (Microsoft Active Server Pages) pode criar páginas da Web dinâmicas, incluindo scripts do lado do servidor e do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="ff13b-104">Microsoft Active Server Pages (ASP) can create dynamic webpages by including both server-side and client-side scripts.</span></span> <span data-ttu-id="ff13b-105">As páginas ASP podem ser muito mais rápidas do que as páginas HTML do cliente porque a maior parte do trabalho é feita no servidor.</span><span class="sxs-lookup"><span data-stu-id="ff13b-105">ASP pages can be much faster than client HTML pages because most of the work is done on the server.</span></span> <span data-ttu-id="ff13b-106">Você também pode usar páginas ASP para exibir informações sobre computadores remotos em outros computadores que não têm o Instrumentação de Gerenciamento do Windows (WMI) instalado.</span><span class="sxs-lookup"><span data-stu-id="ff13b-106">You can also use ASP pages to display information about remote computers to other computers that do not have Windows Management Instrumentation (WMI) installed.</span></span>

<span data-ttu-id="ff13b-107">O procedimento a seguir descreve como usar o WMI com ASP.</span><span class="sxs-lookup"><span data-stu-id="ff13b-107">The following procedure describes how to use WMI with ASP.</span></span>

<span data-ttu-id="ff13b-108">**Para usar o WMI com ASP**</span><span class="sxs-lookup"><span data-stu-id="ff13b-108">**To use WMI with ASP**</span></span>

1.  <span data-ttu-id="ff13b-109">Escreva uma página ASP (. asp) que usa o WMI e coloque-a em um diretório acessível ao seu servidor Web.</span><span class="sxs-lookup"><span data-stu-id="ff13b-109">Write an ASP page (.asp) that uses WMI, and place it in a directory accessible to your web server.</span></span>

    <span data-ttu-id="ff13b-110">Scripts ASP para WMI podem ser desenvolvidos com várias linguagens de script, incluindo o VBScript.</span><span class="sxs-lookup"><span data-stu-id="ff13b-110">ASP scripts for WMI can be developed with several scripting languages, including VBScript.</span></span> <span data-ttu-id="ff13b-111">Você pode construir a parte do script WMI de uma página ASP exatamente como construir qualquer outro script que usa o WMI, com uma restrição importante: não é possível usar métodos WMI assíncronos em páginas ASP.</span><span class="sxs-lookup"><span data-stu-id="ff13b-111">You can construct the WMI script part of an ASP page exactly as you construct any other script that uses WMI, with one important restriction: you cannot use asynchronous WMI methods within ASP pages.</span></span> <span data-ttu-id="ff13b-112">Observe também que todas as chamadas para **GetObject** ou **CreateObject** devem estar no código do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="ff13b-112">Note also that any calls to **GetObject** or **CreateObject** must be in the server-side code.</span></span> <span data-ttu-id="ff13b-113">Para obter mais informações, consulte [API de script para WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="ff13b-113">For more information, see [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

2.  <span data-ttu-id="ff13b-114">Defina a configuração de autenticação para o Serviços de Informações da Internet (IIS).</span><span class="sxs-lookup"><span data-stu-id="ff13b-114">Set up authentication configuration for Internet Information Services (IIS).</span></span> <span data-ttu-id="ff13b-115">Para obter mais informações, consulte [Configuring IIS 5 and posterior for WMI ASP scripting](configuring-iis-5-for-wmi-asp-scripting.md).</span><span class="sxs-lookup"><span data-stu-id="ff13b-115">For more information, see [Configuring IIS 5 and Later for WMI ASP Scripting](configuring-iis-5-for-wmi-asp-scripting.md).</span></span>
3.  <span data-ttu-id="ff13b-116">Desabilite o acesso anônimo e habilite a autenticação integrada do Windows para o arquivo ASP.</span><span class="sxs-lookup"><span data-stu-id="ff13b-116">Disable anonymous access, and enable Windows Integrated Authentication for the ASP file.</span></span> <span data-ttu-id="ff13b-117">Você pode definir essas configurações para sua página ASP usando o snap-in do IIS localizado na pasta **Ferramentas administrativas** do painel de **controle**.</span><span class="sxs-lookup"><span data-stu-id="ff13b-117">You can configure these settings for your ASP page by using the IIS snap-in located in the **Administrative Tools** folder of the **Control Panel**.</span></span>

## <a name="wmi-asp-page-example"></a><span data-ttu-id="ff13b-118">Exemplo de página ASP WMI</span><span class="sxs-lookup"><span data-stu-id="ff13b-118">WMI ASP Page Example</span></span>

<span data-ttu-id="ff13b-119">O exemplo a seguir usa Instrumentação de Gerenciamento do Windows (WMI) em uma página de Active Server (ASP) para exibir o endereço IP e as configurações de gateway de IP padrão para o servidor do qual esse script é executado.</span><span class="sxs-lookup"><span data-stu-id="ff13b-119">The following example uses Windows Management Instrumentation (WMI) within an Active Server Page (ASP) to display the IP address and default IP gateway settings for the server from which this script is executed.</span></span>


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



 

 



