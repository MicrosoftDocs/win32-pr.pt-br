---
description: .
ms.assetid: bcf0a534-c123-40c4-91b4-645c4912f31a
title: Cadeia de Caracteres do Agente do Usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d2d9b25863fbc89ee88e24e3f98b8facad6a59f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922970"
---
# <a name="user-agent-string"></a><span data-ttu-id="fdf7e-103">Cadeia de Caracteres do Agente do Usuário</span><span class="sxs-lookup"><span data-stu-id="fdf7e-103">User Agent String</span></span>

<span data-ttu-id="fdf7e-104">A *cadeia de caracteres do agente do usuário* contém informações sobre a identidade de um navegador.</span><span class="sxs-lookup"><span data-stu-id="fdf7e-104">The *User Agent String* contains information about a browser's identity.</span></span> <span data-ttu-id="fdf7e-105">A cadeia de caracteres do agente do usuário é relatada ao servidor Web como um cabeçalho HTTP toda vez que um navegador faz uma solicitação para um servidor Web.</span><span class="sxs-lookup"><span data-stu-id="fdf7e-105">The User Agent String is reported to the web server as an HTTP header every time that a browser makes a request to a web server.</span></span> <span data-ttu-id="fdf7e-106">Você também pode acessá-lo por meio de um script do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="fdf7e-106">You can also access it through a client-side script.</span></span> <span data-ttu-id="fdf7e-107">Por exemplo, você pode exibir a cadeia de caracteres do agente do usuário digitando a seguinte URL na barra de endereços do Windows Internet Explorer 8: "JavaScript: Alert (Navigator. UserAgent)".</span><span class="sxs-lookup"><span data-stu-id="fdf7e-107">For example, you can display the User Agent String by typing the following URL into the Windows Internet Explorer 8 address bar: "javascript:alert(navigator.userAgent)".</span></span> <span data-ttu-id="fdf7e-108">A ilustração a seguir mostra a caixa de diálogo resultante típica do Internet Explorer 8 em execução no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fdf7e-108">The following illustration shows the typical resulting dialog box from Internet Explorer 8 running on Windows 7.</span></span>

![captura de tela da caixa diaog do Internet Explorer que tem a cadeia de caracteres do agente do usuário](images/useragent-alert.png)

<span data-ttu-id="fdf7e-110">Normalmente, a cadeia de caracteres do agente do usuário é analisada especificamente para a subcadeia de caracteres MSIE.</span><span class="sxs-lookup"><span data-stu-id="fdf7e-110">Typically, the User Agent String is parsed specifically for the MSIE substring.</span></span> <span data-ttu-id="fdf7e-111">Com base na versão relatada do navegador, a lógica de programação do lado do cliente ou do servidor executa uma ação diferente.</span><span class="sxs-lookup"><span data-stu-id="fdf7e-111">Based on the reported version of the browser, the client-side or server-side programming logic takes a different action.</span></span> <span data-ttu-id="fdf7e-112">Para obter mais informações sobre a cadeia de caracteres do agente do usuário, consulte [o que será o relatório do Windows Internet Explorer como a cadeia de caracteres User-Agent?](/previous-versions/cc817582(v=msdn.10)) na biblioteca MSDN.</span><span class="sxs-lookup"><span data-stu-id="fdf7e-112">For more information about the User Agent String, see [What Will Windows Internet Explorer Report as the User-Agent String?](/previous-versions/cc817582(v=msdn.10)) in the MSDN Library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fdf7e-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fdf7e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdf7e-114">Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade</span><span class="sxs-lookup"><span data-stu-id="fdf7e-114">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



