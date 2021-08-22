---
title: BITS Compact Server
description: O Serviço de Transferência Inteligente em Segundo Plano (BITS) Compact Server é um servidor de arquivos HTTP/HTTPS autônomo que fornece a capacidade de transferir um número limitado de arquivos grandes de forma assíncrona entre computadores.
ms.assetid: ab4cf901-6d93-433c-b1b2-ffa54d10725c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41cfbc18a8dc06bb474ab8df9df85fb7b8a96838db14bbc18aee4d94881985d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529186"
---
# <a name="bits-compact-server"></a>BITS Compact Server

O Serviço de Transferência Inteligente em Segundo Plano (BITS) Compact Server é um servidor de arquivos HTTP/HTTPS autônomo que fornece a capacidade de transferir um número limitado de arquivos grandes de forma assíncrona entre computadores. O servidor Compact é criado como um serviço NT e usa HTTP.SYS.

O BITS Compact Server destina-se a ser usado por clientes empresariais e de pequenas empresas sob as seguintes condições:

-   O uso antecipado é de, no máximo, 25 grupos de URLs, e cada grupo de URLs dá suporte a três transferências de arquivo simultâneas.
-   As transferências de arquivos ocorrem entre computadores no mesmo domínio ou domínios mutuamente confiáveis.
-   As transferências de arquivo não são destinadas a clientes voltados para a Internet.

## <a name="installing-the-bits-compact-server"></a>Instalando o BITS Compact Server

O BITS Compact Server é um componente de servidor opcional. Você pode usar uma das seguintes opções para instalar o BITS Compact Server:

-   Gerenciador do Servidor

-   Usando o Windows PowerShell

-   Gerenciador de Pacotes

**Para instalar o BITS Compact Server usando Gerenciador do Servidor**

1.  Na seção **Resumo de recursos** do **Gerenciador do servidor**, clique em **Adicionar recursos**.
2.  No Assistente para adicionar recursos, selecione **serviço de transferência inteligente em segundo plano (bits)** e o **Compact Server**.
3.  Siga as instruções do assistente, incluindo a instalação do software necessário, se indicado.

Para obter mais informações, consulte a ajuda online do **Gerenciador do servidor** .

**Para instalar o BITS Compact Server usando Windows PowerShell**

1.  em um prompt de comando Windows PowerShell, digite o seguinte comando: **Import-Module servermanager**. Em seguida, pressione Enter.
2.  Digite o seguinte comando: **Add-WINDOWSFEATURE bits-Compact-Server**. Em seguida, pressione Enter.

o exemplo de baseado em texto a seguir demonstra como instalar o BITS Compact Server usando cmdlets Windows PowerShell.

``` syntax
PS C:\> Import-Module ServerManager
PS C:\> Add-WindowsFeature BITS-Compact-Server

Success Restart Needed Exit Code Feature Result
------- -------------- --------- --------------
True    No             Success   {Compact Server}


PS C:\>
```

para obter informações sobre como usar cmdlets, consulte a documentação do [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) .

Para obter mais informações sobre o cmdlet Import-Module, consulte [Import-Module](/previous-versions//dd347701(v=technet.10)) na biblioteca do Microsoft TechNet. Para obter ajuda na linha de comando, digite **Get-Help Import-Module**.

Para obter mais informações sobre o cmdlet Add-WindowsFeature, consulte [Add-WindowsFeature](/previous-versions//dd347701(v=technet.10)) na biblioteca do Microsoft TechNet. Para obter ajuda na linha de comando, digite **Get-Help Add-WindowsFeature**.

**para instalar o BITS Compact Server usando Gerenciador de Pacotes**

-   Digite o seguinte comando: **PkgMgr.exe/IU: LightweightServer**.

> [!Note]  
> As configurações serão perdidas se o serviço do Compact Server for reiniciado ou se o computador for reinicializado.

 

## <a name="bits-compact-server-remote-management"></a>Gerenciamento remoto do BITS Compact Server

O BITS Compact Server com gerenciamento remoto de BITS permite transferências de arquivos remotas mais seguras. o gerenciamento remoto de bits usa um provedor de Instrumentação de Gerenciamento do Windows (WMI) para permitir que um administrador de sistema ou um aplicativo de controlador crie remotamente trabalhos de transferência de BITS nos clientes e publique arquivos para hospedagem no BITS Compact Server. O provedor BITS também pode ser usado para permitir que um aplicativo use remotamente o cliente BITS em conjunto com o BITS Compact Server para transferir arquivos de um computador remoto para outro computador remoto.

Para obter mais informações, consulte a documentação do [provedor bits](/previous-versions/windows/desktop/bitsprov/bits-provider) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Provedor de BITS](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> </dl>

 

 