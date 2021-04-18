---
title: .NET Framework configurações padrão
description: .NET Framework 4,5 é o padrão e .NET Framework 3,5 é opcional
ms.assetid: 19B53C82-812A-49AC-87C6-C08E7C199208
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab1f91acc8739b2c660bfb1ba1392ea192511d1c
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "105784670"
---
# <a name="net-framework-45-is-default-and-net-framework-35-is-optional"></a>.NET Framework 4,5 é o padrão e .NET Framework 3,5 é opcional

## <a name="platforms"></a>Plataformas

**Clientes**   do   Windows 8  
**Servidores**   do   Windows Server 2012  

## <a name="description"></a>Descrição

O .NET Framework 4,5 está habilitado por padrão no Windows 8. O Windows 8 não inclui o .NET 3,5 por padrão, mas os arquivos para o .NET 3,5 estão disponíveis na mídia de instalação do Windows 8 como um recurso opcional.

Se o usuário estiver atualizando do Windows 7 para o Windows 8, .NET Framework 3,5 será totalmente habilitado para garantir que todos os aplicativos no computador continuem a funcionar corretamente.

## <a name="manifestation"></a>Manifestação

Se o usuário executar uma instalação limpa do Windows 8 e, em seguida, instalar aplicativos que exigem o .NET Framework 3,5 (ou 2,0), eles dispararão uma solicitação para os arquivos do .NET 3,5 necessários. Normalmente, os arquivos ausentes serão baixados de Windows Update (depois de solicitar a permissão ao usuário), mas se o acesso ao Windows Update não for possível, a habilitação .NET Framework 3,5 falhará, a menos que uma fonte alternativa para os arquivos ausentes tenha sido especificada.

## <a name="mitigation"></a>Atenuação

Para habilitar o .NET Framework 3,5 somente em máquinas de teste com instalações limpas do Windows 8:

1.  Copie \\ \\ as fontes SxS \\ da imagem ISO Build do sistema operacional montado para dotnet35 ou para uma pasta semelhante. Por exemplo:
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  Execute esta linha de comando usando privilégios de administrador:
    ```
    Dism.exe /online /enable-feature /featurename:NetFX3 /All /Source:c:\dotnet35 /LimitAccess

    ```



> [!Note]  
> A \\ pasta SxS de fontes não deve ser usada como um mecanismo de redistribuição, pois não é um mecanismo com suporte.



## <a name="solution"></a>Solução

**Para consumidores:**

O Windows 8 inclui um mecanismo que habilita automaticamente .NET Framework 3,5 ao tentar instalar o pacote redistribuível ou quando um instalador de aplicativo que precisa do .NET 3,5 invoca o redistribuível.

**Para desenvolvedores de aplicativos (e administradores de ti):**

Os administradores de ti podem configurar aplicativos .NET 3,5 para serem executados no .NET 3,5 ou no .NET 4,5 (dependendo do que já está instalado). Para executar um aplicativo gerenciado em 3,5 ou 4,5, basta adicionar uma seção no arquivo de configuração do aplicativo. Isso garantirá que, se o .NET 3,5 estiver instalado, o aplicativo será executado no .NET 3,5; caso contrário, o aplicativo será executado no .NET 4,5. Um exemplo da seção adicional no arquivo de configuração é fornecido abaixo:


```
<configuration>
   <startup>
      <supportedRuntime version="v2.0.50727"/>
      <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5"/>
   </startup>
</configuration>
```



**Para OEMs corporativos:**

Para habilitar o .NET Framework 3,5 para compilações do EEAP e para aplicativos que não têm acesso ao Windows Update:

1.  Copie \\ o \\ SxS \\ de fontes da imagem ISO de Build do sistema operacional montado para o dotnet35 ou para a pasta semelhante. Por exemplo:
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  Defina o RegKey:
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]
     LocalSourcePath = c:\dotnet35
    ```



**Para empresas:**

Para computadores configurados para usar o WSUS para manutenção, você pode definir uma entrada de registro para permitir que o computador Use Windows Update para habilitar o .NET 3,5 em vez do WSUS (a manutenção ainda será feita do WSUS se você fizer isso).

-   Defina o RegKey:
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]  RepairContentServerSource =DWORD(2)
    ```



Essa entrada de registro também pode ser definida por meio de Política de Grupo (política de computador local-> configuração do computador-> sistema Modelos Administrativos->. Selecione a configuração especificar configurações para instalação de componente opcional e reparo de componentes.

Se você selecionar contatar Windows Update diretamente para baixar conteúdo de reparo em vez de Windows Server Update Services (WSUS), quaisquer tentativas de adicionar recursos do Windows (por exemplo, .NET Framework 3,5) ou reparar recursos irão disparar downloads de arquivo do Windows Update. Os computadores de destino exigem acesso de Internet e WU para essa opção. As operações normais de manutenção continuam a usar o WSUS se ele tiver sido configurado como uma origem.

**Uma observação sobre como definir o local de origem local por meio de entradas do registro**

Os administradores de ti podem definir locais de origem local para arquivos .NET 3,5 por meio de uma entrada de registro, para que os usuários possam usar a caixa de diálogo Adicionar/remover recursos do Windows para habilitar recursos com carga ausente sem precisar especificar um local de origem. O valor da entrada do registro pode ser controlado por meio da diretiva de grupo.

Há suporte para essa entrada de registro:



<table>
<thead>
<tr class="header">
<th>Entrada</th>
<th>Tipo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Caminho de origem local</td>
<td>REG_EXPAND_SZ</td>
<td>Caminho (s) de origem local a serem usados por padrão. Vários caminhos podem ser especificados; Eles devem ser separados por;. Os locais serão pesquisados na ordem em que são especificados. <br/> Locais de origem local que são especificados na linha de comando do DISM, têm precedência sobre os locais especificados nessa entrada de registro. Os locais de pasta podem ser especificados nessa entrada de registro. <br/> WIMs pode ser usado, mas o caminho deve ser para o arquivo WIM; Não é necessário montá-lo, por exemplo: <br/> <dl> Wim: \\ machine\share\file.wim: 1<br />
</dl> Observe o 1 no final. Você deve especificar o índice numérico da imagem que deseja usar no arquivo WIM. <br/> Para um WIM montado, o caminho de origem precisa se referir ao diretório do Windows da imagem montada, e não ao ponto de montagem (por exemplo:/Source: <mount_point> \Windows em vez de/Source: <mount_point> ). <br/></td>
</tr>
</tbody>
</table>





## <a name="resources"></a>Recursos

<dl>

[Implementando a política baseada no registro](/previous-versions/windows/desktop/Policy/implementing-registry-based-policy)  
</dl>