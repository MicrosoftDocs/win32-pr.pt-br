---
title: .NET Framework configurações padrão
description: .NET Framework 4.5 é padrão e .NET Framework 3.5 é opcional
ms.assetid: 19B53C82-812A-49AC-87C6-C08E7C199208
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b45aef294e035f5fb7e647c49b22206ac8aadd
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883130"
---
# <a name="net-framework-45-is-default-and-net-framework-35-is-optional"></a>.NET Framework 4.5 é padrão e .NET Framework 3.5 é opcional

## <a name="platforms"></a>Plataformas

**Clientes** Windows 8     
**Servidores** Windows Server 2012     

## <a name="description"></a>Description

.NET Framework 4.5 está habilitado por padrão no Windows 8. Windows 8 não inclui o .NET 3.5 por padrão, mas os arquivos do .NET 3.5 estão disponíveis na mídia de instalação do Windows 8 como um recurso opcional.

Se o usuário estiver atualizando do Windows 7 para o Windows 8, o .NET Framework 3.5 será totalmente habilitado para garantir que todos os aplicativos no computador continuem a funcionar corretamente.

## <a name="manifestation"></a>Manifestação

Se o usuário executar uma instalação limpa do Windows 8 e, em seguida, instalar aplicativos que exigem o .NET Framework 3.5 (ou 2.0), ele disparará uma solicitação para os arquivos .NET 3.5 necessários. Normalmente, os arquivos ausentes serão baixados da atualização do Windows (depois de pedir permissão ao usuário), mas se o acesso à atualização do Windows não for possível, a habilitação do .NET Framework 3.5 falhará, a menos que uma fonte alternativa para os arquivos ausentes tenha sido especificada.

## <a name="mitigation"></a>Atenuação

Para habilitar .NET Framework 3.5 somente em máquinas de teste com instalação limpa de Windows 8:

1.  Copie sxs de fontes da imagem ISO de build do sistema operacional montado \\ \\ para \\ dotnet35 ou pasta semelhante. Por exemplo:
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  Execute esta linha de comando usando privilégios de administrador:
    ```
    Dism.exe /online /enable-feature /featurename:NetFX3 /All /Source:c:\dotnet35 /LimitAccess

    ```



> [!Note]  
> A pasta SxS de origem não deve ser usada como um mecanismo \\ de redistribuição, pois esse não é um mecanismo com suporte.



## <a name="solution"></a>Solução

**Para consumidores:**

Windows 8 inclui um mecanismo que habilita automaticamente o .NET Framework 3.5 ao tentar instalar o pacote redistribuível ou quando um instalador de aplicativo que precisa do .NET 3.5 invoca o redistribuível.

**Para desenvolvedores de aplicativos (e administradores de IT):**

Os administradores de IT podem configurar aplicativos .NET 3.5 para executar no .NET 3.5 ou no .NET 4.5 (dependendo do que já está instalado). Para executar um aplicativo gerenciado na 3.5 ou 4.5, basta adicionar uma seção no arquivo de configuração do aplicativo. Isso garantirá que, se o .NET 3.5 estiver instalado, o aplicativo será executado no .NET 3.5; caso contrário, o aplicativo será executado no .NET 4.5. Um exemplo da seção adicional no arquivo de configuração é fornecido abaixo:


```
<configuration>
   <startup>
      <supportedRuntime version="v2.0.50727"/>
      <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5"/>
   </startup>
</configuration>
```



**Para OEMs empresariais:**

Para habilitar .NET Framework 3.5 para builds EEAP e para aplicativos que não têm acesso Windows Atualização:

1.  Copie sxs de fontes da imagem ISO de build do sistema operacional montado \\ \\ para a pasta \\ dotnet35 ou semelhante. Por exemplo:
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  De definir a regkey:
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]
     LocalSourcePath = c:\dotnet35
    ```



**Para empresas:**

Para máquinas que estão configuradas para usar o WSUS para manutenção, você pode definir uma entrada do Registro para permitir que o computador use a Atualização do Windows para habilenciar o .NET 3.5 em vez do WSUS (a manutenção ainda será feita no WSUS se você fizer isso).

-   De definir a regkey:
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]  RepairContentServerSource =DWORD(2)
    ```



Essa entrada do Registro também pode ser definida por meio de Política de Grupo (Política de Computador Local -> Configuração do Computador -> Modelos Administrativos -> System. Selecione a configuração Especificar configurações para instalação de componente opcional e reparo de componente .

Se você selecionar Contatar Windows Atualizar diretamente para baixar o conteúdo de reparo em vez do WSUS (Windows Server Update Services), qualquer tentativa de adicionar recursos do Windows (por exemplo, .NET Framework 3.5) ou recursos de reparo disparará downloads de arquivos do Windows Update. Os computadores de destino exigem acesso à Internet e AO WU para essa opção. As operações de manutenção normais continuarão a usar o WSUS se ele tiver sido configurado como uma origem.

**Uma observação sobre como definir o local de origem local por meio de entradas do Registro**

Os administradores de TI podem definir locais de origem para arquivos .NET 3.5 por meio de uma entrada do Registro, para que os usuários possam usar a caixa de diálogo Adicionar/Remover recursos do Windows para habilitar recursos com carga ausente sem precisar especificar um local de origem. O valor da entrada do Registro pode ser controlado por meio da política de grupo.

Há suporte para esta entrada do Registro:



<table>
<thead>
<tr class="header">
<th>Entrada</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Caminho de origem local</td>
<td>REG_EXPAND_SZ</td>
<td>Caminho(s) de origem local a ser usado por padrão. Vários caminhos podem ser especificados; eles devem ser separados por ; . Os locais serão pesquisados na ordem em que são especificados. <br/> Os locais de origem locais especificados na linha de comando do DISM têm precedência sobre os locais especificados nesta entrada do Registro. Os locais de pasta podem ser especificados nesta entrada do Registro. <br/> Os WIMs podem ser usados, mas o caminho deve ser para o arquivo WIM; não há necessidade de montá-lo, por exemplo: <br/> <dl> wim: \\ machine\share\file.wim:1<br />
</dl> Observe o 1 no final. Você deve especificar o índice numérico da imagem que deseja usar no arquivo WIM. <br/> Para um WIM montado, o caminho de origem precisa se referir ao diretório do Windows da imagem montada, em vez do ponto de montagem (por exemplo: /source: mount_point \windows em vez &lt; &gt; de /source: &lt; mount_point &gt; ). <br/></td>
</tr>
</tbody>
</table>





## <a name="resources"></a>Recursos

<dl>

[Implementando a política baseada no Registro](/previous-versions/windows/desktop/Policy/implementing-registry-based-policy)  
</dl>
