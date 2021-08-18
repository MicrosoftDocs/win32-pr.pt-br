---
title: Usando cmdlets de Windows PowerShell WMI para gerenciar o bits compact server
description: Windows PowerShell fornece um mecanismo simples para se conectar ao WMI (Instrumentação de Gerenciamento Windows) em um computador remoto e gerenciar o servidor compacto Serviço de Transferência Inteligente em Segundo Plano (BITS).
ms.assetid: fe174d2f-4ca0-431e-b1b8-1893ec54147a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e82401e80b5e49b7d2b964ec910d15d70aea7ce9c782a0173bef97aa8b3a5c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021074"
---
# <a name="using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server"></a>Usando cmdlets de Windows PowerShell WMI para gerenciar o bits compact server

Windows PowerShell fornece um mecanismo simples para se conectar ao WMI (Instrumentação de Gerenciamento Windows) em um computador remoto e gerenciar o servidor compacto Serviço de Transferência Inteligente em Segundo Plano (BITS). O BITS Compact Server é um componente de servidor opcional que deve ser instalado separadamente. Para obter informações sobre como instalar o Compact Server, consulte a [documentação do BITS Compact Server.](bits-compact-server.md)

1.  Conexão para o provedor BITS.

    ```PowerShell
    $cred = Get-Credential
    $bcs = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" `
    -List -ComputerName Server1 -Credential $cred
    ```

    

    O cmdlet [Get-Credential](/previous-versions//dd315327(v=technet.10)) solicita as credenciais do usuário para se conectar ao computador remoto e atribui as credenciais ao objeto $cred usuário.

    Os objetos retornados pelo cmdlet [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) são atribuídos à variável $bcs dados. No exemplo anterior, o cmdlet [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) recupera a [classe BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) no namespace raiz \\ do Microsoft BITS de \\ Server1. Métodos estáticos expostos pela [classe BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) podem ser chamados no $bcs objeto . Para obter mais informações sobre o gerenciamento remoto do BITS, consulte [Provedor bits e](/previous-versions/windows/desktop/bitsprov/bits-provider) classes de provedor [BITS]( /previous-versions//dd904507(v=vs.85)).

    > [!Note]  
    > O caractere de acento grave ( \` ) é usado para indicar uma quebra de linha.

     

2.  Crie um grupo de URL no servidor.

    ```PowerShell
    $URLGroup = "https://Server1:80/testurlgroup" 
    $bcs.CreateUrlGroup($URLGroup)
    ```

    

    A cadeia https://Server1:80/testurlgroup de caracteres de prefixo de URL " é atribuída à variável $URLGroup dados. A $URLGroup variável é passada para o [método CreateUrlGroup,](/previous-versions/windows/desktop/bitsprov/createurlgroup-bitslightweightserverurlgroup) que cria o grupo de URL no Server1.

    Você pode especificar um grupo de URL diferente. O grupo de URL deve estar em conformidade com uma cadeia de caracteres de prefixo de URL válida. Para obter mais informações sobre prefixos de URL, consulte [UrlPrefix Strings](../http/urlprefix-strings.md).

3.  Hospede um arquivo no grupo de URL.

    ```PowerShell
    $bcsObj = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" -filter ("UrlGroup='" + $URLGroup + "'") -ComputerName Server1 -Credential $cred
    $bcsObj.CreateURL("url.txt", "c:\\temp\\1.txt", "") -ComputerName Server1 -Credential $cred
    ```

    

    A instância BITSCompactServerUrlGroup retornada pelo cmdlet [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) é atribuída à variável $bcsObj. O [método CreateUrl](/previous-versions/windows/desktop/bitsprov/createurl-bitslightweightserverurlgroup) é chamado para o $bcsObj com o sufixo de URL "url.txt", o caminho de origem "c: temp1.txt" para o arquivo e uma cadeia de caracteres de descritor de segurança vazia como \\ \\ \\ \\ parâmetros. O sufixo "url.txt" é adicionado ao prefixo do grupo de URL. Os clientes podem baixar o arquivo do seguinte endereço: https://Server1:80/testurlgroup/url.txt .

4.  Limpe a URL e o grupo de URL.

    ```PowerShell
    $bcsObj.Delete()
    ```

    

    O **método system.object Delete** exclui o objeto $bcsObj objeto .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[BITS Compact Server](./bits-compact-server.md)
</dt> <dt>

[Provedor BITS](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> <dt>

[Classes de provedor BITS]( /previous-versions//dd904507(v=vs.85))
</dt> <dt>

[Get-Credential](/previous-versions//dd315327(v=technet.10))
</dt> <dt>

[Get-WmiObject](/previous-versions//dd315295(v=technet.10))
</dt> </dl>

 

 