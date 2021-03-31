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
# <a name="using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server"></a>Usando os cmdlets WMI do Windows PowerShell para gerenciar o BITS Compact Server

O Windows PowerShell fornece um mecanismo simples para se conectar ao Instrumentação de Gerenciamento do Windows (WMI) em um computador remoto e gerenciar o Serviço de Transferência Inteligente em Segundo Plano (BITS) Compact Server. O BITS Compact Server é um componente de servidor opcional que deve ser instalado separadamente. Para obter informações sobre como instalar o Compact Server, consulte a documentação do [bits Compact Server](bits-compact-server.md) .

1.  Conecte-se ao provedor do BITS.

    ```PowerShell
    $cred = Get-Credential
    $bcs = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" `
    -List -ComputerName Server1 -Credential $cred
    ```

    

    O cmdlet [Get-Credential](/previous-versions//dd315327(v=technet.10)) solicita as credenciais do usuário para se conectar ao computador remoto e atribui as credenciais ao objeto $cred.

    Os objetos retornados pelo cmdlet [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) são atribuídos à variável $BCS. No exemplo anterior, o cmdlet [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) recupera a classe [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) no \\ namespace raiz \\ bits da Microsoft de server1. Os métodos estáticos expostos pela classe [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) podem ser chamados no objeto $BCS. Para obter mais informações sobre gerenciamento remoto de BITS, consulte [provedor de bits](/previous-versions/windows/desktop/bitsprov/bits-provider) e [classes de provedor bits]( /previous-versions//dd904507(v=vs.85)).

    > [!Note]  
    > O caractere de acento grave ( \` ) é usado para indicar uma quebra de linha.

     

2.  Crie um grupo de URLs no servidor.

    ```PowerShell
    $URLGroup = "https://Server1:80/testurlgroup" 
    $bcs.CreateUrlGroup($URLGroup)
    ```

    

    A https://Server1:80/testurlgroup cadeia de caracteres de prefixo de URL "" é atribuída à variável de $URLGroup. A variável $URLGroup é passada para o método [CreateUrlGroup](/previous-versions/windows/desktop/bitsprov/createurlgroup-bitslightweightserverurlgroup) , que cria o grupo de URLs no Server1.

    Você pode especificar um grupo de URLs diferente. O grupo de URLs deve estar em conformidade com uma cadeia de caracteres de prefixo de URL válida. Para obter mais informações sobre prefixos de URL, consulte [cadeias de caracteres URLPrefix](../http/urlprefix-strings.md).

3.  Hospede um arquivo no grupo de URLs.

    ```PowerShell
    $bcsObj = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" -filter ("UrlGroup='" + $URLGroup + "'") -ComputerName Server1 -Credential $cred
    $bcsObj.CreateURL("url.txt", "c:\\temp\\1.txt", "") -ComputerName Server1 -Credential $cred
    ```

    

    A instância de BITSCompactServerUrlGroup retornada pelo cmdlet [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) é atribuída à variável $bcsObj. O método [CreateUrl](/previous-versions/windows/desktop/bitsprov/createurl-bitslightweightserverurlgroup) é chamado para o $bcsObj com o sufixo de URL "url.txt", o caminho de origem "c: \\ \\ temp \\ \\1.txt" para o arquivo e uma cadeia de caracteres de descritor de segurança vazia como parâmetros. O sufixo "url.txt" é adicionado ao prefixo do grupo de URLs. Os clientes podem baixar o arquivo do seguinte endereço: https://Server1:80/testurlgroup/url.txt .

4.  Limpe a URL e o grupo de URLs.

    ```PowerShell
    $bcsObj.Delete()
    ```

    

    O método **System. Object Delete** exclui o objeto $bcsObj.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[BITS Compact Server](./bits-compact-server.md)
</dt> <dt>

[Provedor de BITS](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> <dt>

[Classes de provedor BITS]( /previous-versions//dd904507(v=vs.85))
</dt> <dt>

[Get-Credential](/previous-versions//dd315327(v=technet.10))
</dt> <dt>

[Get-WmiObject](/previous-versions//dd315295(v=technet.10))
</dt> </dl>

 

 