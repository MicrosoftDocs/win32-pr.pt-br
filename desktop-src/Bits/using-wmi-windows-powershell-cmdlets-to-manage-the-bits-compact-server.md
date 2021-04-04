---
title: Usando os cmdlets WMI do Windows PowerShell para gerenciar o BITS Compact Server
description: O Windows PowerShell fornece um mecanismo simples para se conectar ao Instrumentação de Gerenciamento do Windows (WMI) em um computador remoto e gerenciar o Serviço de Transferência Inteligente em Segundo Plano (BITS) Compact Server.
ms.assetid: fe174d2f-4ca0-431e-b1b8-1893ec54147a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c3c942672c147ec5daa0caa2a370e487be80809
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917473"
---
# <a name="using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server"></a><span data-ttu-id="07c58-103">Usando os cmdlets WMI do Windows PowerShell para gerenciar o BITS Compact Server</span><span class="sxs-lookup"><span data-stu-id="07c58-103">Using WMI Windows PowerShell Cmdlets to Manage the BITS Compact Server</span></span>

<span data-ttu-id="07c58-104">O Windows PowerShell fornece um mecanismo simples para se conectar ao Instrumentação de Gerenciamento do Windows (WMI) em um computador remoto e gerenciar o Serviço de Transferência Inteligente em Segundo Plano (BITS) Compact Server.</span><span class="sxs-lookup"><span data-stu-id="07c58-104">Windows PowerShell provides a simple mechanism to connect to Windows Management Instrumentation (WMI) on a remote computer and manage the Background Intelligent Transfer Service (BITS) Compact Server.</span></span> <span data-ttu-id="07c58-105">O BITS Compact Server é um componente de servidor opcional que deve ser instalado separadamente.</span><span class="sxs-lookup"><span data-stu-id="07c58-105">The BITS Compact Server is an optional server component that must be installed separately.</span></span> <span data-ttu-id="07c58-106">Para obter informações sobre como instalar o Compact Server, consulte a documentação do [bits Compact Server](bits-compact-server.md) .</span><span class="sxs-lookup"><span data-stu-id="07c58-106">For information about installing the Compact Server, see the [BITS Compact Server](bits-compact-server.md) documentation.</span></span>

1.  <span data-ttu-id="07c58-107">Conecte-se ao provedor do BITS.</span><span class="sxs-lookup"><span data-stu-id="07c58-107">Connect to the BITS provider.</span></span>

    ```PowerShell
    $cred = Get-Credential
    $bcs = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" `
    -List -ComputerName Server1 -Credential $cred
    ```

    

    <span data-ttu-id="07c58-108">O cmdlet [Get-Credential](/previous-versions//dd315327(v=technet.10)) solicita as credenciais do usuário para se conectar ao computador remoto e atribui as credenciais ao objeto $cred.</span><span class="sxs-lookup"><span data-stu-id="07c58-108">The [Get-Credential](/previous-versions//dd315327(v=technet.10)) cmdlet requests the user's credentials to connect to the remote computer and assigns the credentials to the $cred object.</span></span>

    <span data-ttu-id="07c58-109">Os objetos retornados pelo cmdlet [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) são atribuídos à variável $BCS.</span><span class="sxs-lookup"><span data-stu-id="07c58-109">The objects returned by the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet are assigned to the $bcs variable.</span></span> <span data-ttu-id="07c58-110">No exemplo anterior, o cmdlet [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) recupera a classe [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) no \\ namespace raiz \\ bits da Microsoft de server1.</span><span class="sxs-lookup"><span data-stu-id="07c58-110">In the preceding example, the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet retrieves the [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) class in the root\\Microsoft\\BITS namespace of Server1.</span></span> <span data-ttu-id="07c58-111">Os métodos estáticos expostos pela classe [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) podem ser chamados no objeto $BCS.</span><span class="sxs-lookup"><span data-stu-id="07c58-111">Static methods exposed by the [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) class can be called on the $bcs object.</span></span> <span data-ttu-id="07c58-112">Para obter mais informações sobre gerenciamento remoto de BITS, consulte [provedor de bits](/previous-versions/windows/desktop/bitsprov/bits-provider) e [classes de provedor bits]( /previous-versions//dd904507(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="07c58-112">For more information about BITS remote management, see [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider) and [BITS provider classes]( /previous-versions//dd904507(v=vs.85)).</span></span>

    > [!Note]  
    > <span data-ttu-id="07c58-113">O caractere de acento grave ( \` ) é usado para indicar uma quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="07c58-113">The grave-accent character (\`) is used to indicate a line break.</span></span>

     

2.  <span data-ttu-id="07c58-114">Crie um grupo de URLs no servidor.</span><span class="sxs-lookup"><span data-stu-id="07c58-114">Create a URL group on the server.</span></span>

    ```PowerShell
    $URLGroup = "https://Server1:80/testurlgroup" 
    $bcs.CreateUrlGroup($URLGroup)
    ```

    

    <span data-ttu-id="07c58-115">A https://Server1:80/testurlgroup cadeia de caracteres de prefixo de URL "" é atribuída à variável de $URLGroup.</span><span class="sxs-lookup"><span data-stu-id="07c58-115">The "https://Server1:80/testurlgroup" URL prefix string is assigned to the $URLGroup variable.</span></span> <span data-ttu-id="07c58-116">A variável $URLGroup é passada para o método [CreateUrlGroup](/previous-versions/windows/desktop/bitsprov/createurlgroup-bitslightweightserverurlgroup) , que cria o grupo de URLs no Server1.</span><span class="sxs-lookup"><span data-stu-id="07c58-116">The $URLGroup variable is passed to the [CreateUrlGroup](/previous-versions/windows/desktop/bitsprov/createurlgroup-bitslightweightserverurlgroup) method, which creates the URL group on Server1.</span></span>

    <span data-ttu-id="07c58-117">Você pode especificar um grupo de URLs diferente.</span><span class="sxs-lookup"><span data-stu-id="07c58-117">You can specify a different URL group.</span></span> <span data-ttu-id="07c58-118">O grupo de URLs deve estar em conformidade com uma cadeia de caracteres de prefixo de URL válida.</span><span class="sxs-lookup"><span data-stu-id="07c58-118">The URL group must conform to a valid URL prefix string.</span></span> <span data-ttu-id="07c58-119">Para obter mais informações sobre prefixos de URL, consulte [cadeias de caracteres URLPrefix](../http/urlprefix-strings.md).</span><span class="sxs-lookup"><span data-stu-id="07c58-119">For more information about URL prefixes, see [UrlPrefix Strings](../http/urlprefix-strings.md).</span></span>

3.  <span data-ttu-id="07c58-120">Hospede um arquivo no grupo de URLs.</span><span class="sxs-lookup"><span data-stu-id="07c58-120">Host a file on the URL group.</span></span>

    ```PowerShell
    $bcsObj = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" -filter ("UrlGroup='" + $URLGroup + "'") -ComputerName Server1 -Credential $cred
    $bcsObj.CreateURL("url.txt", "c:\\temp\\1.txt", "") -ComputerName Server1 -Credential $cred
    ```

    

    <span data-ttu-id="07c58-121">A instância de BITSCompactServerUrlGroup retornada pelo cmdlet [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) é atribuída à variável $bcsObj.</span><span class="sxs-lookup"><span data-stu-id="07c58-121">The BITSCompactServerUrlGroup instance returned by the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet is assigned to the $bcsObj variable.</span></span> <span data-ttu-id="07c58-122">O método [CreateUrl](/previous-versions/windows/desktop/bitsprov/createurl-bitslightweightserverurlgroup) é chamado para o $bcsObj com o sufixo de URL "url.txt", o caminho de origem "c: \\ \\ temp \\ \\1.txt" para o arquivo e uma cadeia de caracteres de descritor de segurança vazia como parâmetros.</span><span class="sxs-lookup"><span data-stu-id="07c58-122">The [CreateUrl](/previous-versions/windows/desktop/bitsprov/createurl-bitslightweightserverurlgroup) method is called for the $bcsObj with the "url.txt" URL suffix, the "c:\\\\temp\\\\1.txt" source path for the file, and an empty security descriptor string as parameters.</span></span> <span data-ttu-id="07c58-123">O sufixo "url.txt" é adicionado ao prefixo do grupo de URLs.</span><span class="sxs-lookup"><span data-stu-id="07c58-123">The "url.txt" suffix is added to the URL group prefix.</span></span> <span data-ttu-id="07c58-124">Os clientes podem baixar o arquivo do seguinte endereço: https://Server1:80/testurlgroup/url.txt .</span><span class="sxs-lookup"><span data-stu-id="07c58-124">Clients can download the file from the following address: https://Server1:80/testurlgroup/url.txt.</span></span>

4.  <span data-ttu-id="07c58-125">Limpe a URL e o grupo de URLs.</span><span class="sxs-lookup"><span data-stu-id="07c58-125">Clean up the URL and the URL group.</span></span>

    ```PowerShell
    $bcsObj.Delete()
    ```

    

    <span data-ttu-id="07c58-126">O método **System. Object Delete** exclui o objeto $bcsObj.</span><span class="sxs-lookup"><span data-stu-id="07c58-126">The **system.object Delete** method deletes the $bcsObj object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07c58-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="07c58-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07c58-128">BITS Compact Server</span><span class="sxs-lookup"><span data-stu-id="07c58-128">BITS Compact Server</span></span>](./bits-compact-server.md)
</dt> <dt>

[<span data-ttu-id="07c58-129">Provedor de BITS</span><span class="sxs-lookup"><span data-stu-id="07c58-129">BITS provider</span></span>](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> <dt>

<span data-ttu-id="07c58-130">[Classes de provedor BITS]( /previous-versions//dd904507(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="07c58-130">[BITS provider classes]( /previous-versions//dd904507(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="07c58-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="07c58-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span></span>
</dt> <dt>

<span data-ttu-id="07c58-132">[Get-WmiObject](/previous-versions//dd315295(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="07c58-132">[Get-WmiObject](/previous-versions//dd315295(v=technet.10))</span></span>
</dt> </dl>

 

 