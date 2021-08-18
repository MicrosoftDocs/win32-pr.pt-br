---
description: Um arquivo de configuração de aplicativo é um arquivo XML usado para controlar a associação de assembly.
ms.assetid: b7453f2b-52a4-4af9-8410-ebbb430ada67
title: Arquivos de configuração de aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cf4b22d3710c0dd38e83f827a175ad591309f22ab8ac2d81e93438f27d07dc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142519"
---
# <a name="application-configuration-files"></a>Arquivos de configuração de aplicativo

Um arquivo de configuração de aplicativo é um arquivo XML usado para controlar a associação de assembly. Ele pode redirecionar um aplicativo do uso de uma versão de um assembly lado a lado para outra versão do mesmo assembly. Isso é chamado [de configuração por aplicativo.](per-application-configuration.md) Um arquivo de configuração de aplicativo se aplica somente a um manifesto de aplicativo específico e assemblies dependentes. Componentes isolados compilados com um manifesto de ID de RECURSO DE MANIFESTO ISOLATIONAWARE inserido \_ \_ \_ exigem um arquivo de configuração de aplicativo separado. Os manifestos gerenciados [**com CreateActCtx exigem**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) um arquivo de configuração de aplicativo separado.

O redirecionamento especificado por um arquivo de configuração de aplicativo pode substituir as versões de assembly [especificadas](application-manifests.md) pelos manifestos do aplicativo e pelos arquivos [de configuração do editor](publisher-configuration-files.md). Por exemplo, se um arquivo de configuração do publicador especificar que todas as referências a um assembly sejam redirecionadas da versão 1.0.0.0 para 1.1.0.0, um arquivo de configuração de aplicativo poderá ser usado para redirecionar um aplicativo específico para usar a versão 1.0.0.0. Um arquivo de configuração de aplicativo se aplica somente ao manifesto do aplicativo especificado e assemblies dependentes.

Para uma listagem completa do esquema XML, consulte Esquema de arquivo de [configuração de aplicativo.](application-configuration-file-schema.md)

Os arquivos de configuração de aplicativo têm os elementos e atributos mostrados na tabela a seguir.



| Elemento               | Atributos                | Obrigatório |
|-----------------------|---------------------------|----------|
| **configuração**     |                           | Sim      |
| **windows**           |                           | Sim      |
| **publisherPolicy**   |                           | Sim      |
|                       | **aplicar**                 | Sim      |
| **Runtime**           |                           | Não       |
| **assemblyBinding**   |                           | Sim      |
| **Sondagem**           |                           | Não       |
|                       | **Privatepath**           | Sim      |
| **Dependência**        |                           | Não       |
| **dependentAssembly** |                           | Sim      |
| **Assemblyidentity**  |                           | Sim      |
|                       | **tipo**                  | Sim      |
|                       | **name**                  | Sim      |
|                       | **linguagem**              | Não       |
|                       | **processorArchitecture** | Sim      |
|                       | **version**               | Sim      |
|                       | **Publickeytoken**        | Não       |
| **bindingRedirect**   |                           | Sim      |
|                       | **oldVersion**            | Sim      |
|                       | **newVersion**            | Sim      |



 

## <a name="file-location"></a>Localização do arquivo

Os arquivos de configuração do aplicativo devem ser instalados no mesmo local que o manifesto [do aplicativo](application-manifests.md).

## <a name="file-name-syntax"></a>Sintaxe de nome de arquivo

O nome de um arquivo de configuração de aplicativo é o nome do executável do aplicativo seguido por .config.

Por exemplo, um arquivo de configuração de aplicativo que se refere Example.exe ou Example.dll usaria a sintaxe de nome de arquivo mostrada no exemplo a seguir. Você pode omitir o campo para <*ID* do recurso> instalar o arquivo de configuração como um arquivo separado ou se a ID do recurso for 1.

**example.exe.<*ID de recurso*>.config**

**example.dll.<*ID de recurso*>.config**

## <a name="elements"></a>Elementos

Os nomes de elementos e atributos são sensíveis a minúsculas. Os valores de elementos e atributos não fazem parte de maiúsculas e minúsculas, exceto pelo valor do atributo de tipo.

<span id="configuration"></span><span id="CONFIGURATION"></span>

### <a name="configuration"></a>configuração

Um elemento de contêiner para os **elementos windows** e **runtime** de um arquivo de configuração de aplicativo. Obrigatórios.

<span id="windows"></span><span id="WINDOWS"></span>

### <a name="windows"></a>windows

Inclui as partes do arquivo de configuração de aplicativo que se aplicam ao redirecionamento de assemblies Win32.

> [!Note]  
> O autor de um aplicativo não deve incluir um arquivo de configuração com um subelemento do **Windows** como parte de seu aplicativo. Isso poderá ser permitido se a única finalidade do arquivo de configuração for habilitar a funcionalidade **privatePath** de **um elemento de investigação.** O **elemento de investigação** não está disponível em sistemas anteriores Windows Server 2008 R2 e Windows 7.

<span id="publisherPolicy"></span><span id="publisherpolicy"></span><span id="PUBLISHERPOLICY"></span>

### <a name="publisherpolicy"></a>publisherPolicy

Especifica se a política do publicador deve ser aplicada.

Esse elemento tem os atributos mostrados na tabela a seguir.



| Atributo | Descrição                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| **aplicar** | Um valor de "sim" aplica a política do editor. Essa é a configuração padrão. O valor "não" não aplica a política do editor. |

<span id="runtime"></span><span id="RUNTIME"></span>

### <a name="runtime"></a>runtime

Inclui as partes do arquivo de configuração de aplicativo que se aplicam ao redirecionamento de assemblies .Net.

<span id="assemblyBinding"></span><span id="assemblybinding"></span><span id="ASSEMBLYBINDING"></span>

### <a name="assemblybinding"></a>assemblyBinding

Inclui as informações de redirecionamento para o aplicativo e o assembly afetado por esse arquivo de configuração de aplicativo. O primeiro subelemento de **assemblyBinding** deve ser um **assemblyIdentity** que identifica o aplicativo.

A partir do Windows Server 2008 R2 e Windows 7, um **elemento assemblyBinding** pode incluir um subelemento **de** investigação.

<span id="probing"></span><span id="PROBING"></span>

### <a name="probing"></a>Sondagem

Um subelemento opcional de um **elemento assemblyBinding** que estende a pesquisa de assemblies para diretórios adicionais. Os diretórios adicionais não precisam ser subdireários do diretório do assembly.

> [!Note]  
> Esse elemento não está disponível em sistemas anteriores ao Windows Server 2008 R2 e Windows 7 e só pode ser usado em um **elemento do Windows.**

Esse elemento tem os atributos mostrados na tabela a seguir.

| Atributo       | Descrição                                                                                                                                                                                                                                   |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Privatepath** | Especifica os [caminhos relativos](/windows/desktop/FileIO/naming-a-file) de subdireários do diretório base do aplicativo que podem conter assemblies. Um máximo de nove caminhos de subdiretório pode ser especificado. Delimitar cada caminho de subdiretório com um ponto e vírgula. |

Você pode usar o especificador especial de dois pontos em um caminho para denotar o diretório pai do diretório atual. Não mais do que dois níveis acima do diretório atual podem ser especificados usando pontos duplos. Não use pontos triplos. Por exemplo, um aplicativo que usa o elemento **de investigação** a seguir verifica diretórios adicionais para um assembly.

``` XML
<probing privatePath="bin;..\bin2\subbin;bin3"/>
```

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a>dependência
Um elemento de contêiner para pelo menos **um dependentAssembly.** Cada **dependentAssembly** pode estar dentro de exatamente uma **dependência**. Esse elemento não tem atributos. Opcional.

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a>dependentAssembly

O primeiro subelemento deve ser um **elemento assemblyIdentity** que identifica o assembly lado a lado que está sendo redirecionado pelo arquivo de configuração do aplicativo. Um **dependentAssembly** não tem atributos.

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a>assemblyIdentity

Como o primeiro subelemento de um **elemento assemblyBinding,** **assemblyIdentity** descreve e identifica exclusivamente um aplicativo. O arquivo de configuração do aplicativo redireciona a associação desse aplicativo para assemblies lado a lado. Por exemplo, o **assemblyIdentity** a seguir indica que o arquivo de configuração do aplicativo afeta a associação do aplicativo mysampleApp a assemblies lado a lado. Os assemblies que estão sendo redirecionados seriam identificados em **um dependentAssembly.**

``` XML
<assemblyIdentity processorArchitecture="X86" name="Microsoft.Windows.mysampleApp" type="win32" version="1.0.0.0"/>
```

Como o primeiro subelemento de um elemento **dependentAssembly,** **assemblyIdentity** descreve um assembly lado a lado do qual o aplicativo depende. O arquivo de configuração do aplicativo reconfigura a identidade desse assembly necessário. Por exemplo, o **assemblyIdentity** e **bindingRedirect** a seguir reconfiguram uma dependência na Microsoft. Windows. SampleAssembly da versão 2.0.0.0 para a versão 2.1.0.0.

``` XML
<dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32"
          name="Microsoft.Windows.SampleAssembly"
          processorArchitecture="x86"
          publicKeyToken="0000000000000000"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.1.0.0"/>
      </dependentAssembly>
</dependency>
```

Observe que cada **assemblyIdentity** incluído em **um dependentAssembly** deve corresponder exatamente à **assemblyIdentity** no próprio manifesto [de assembly do assembly](assembly-manifests.md).

O **elemento assemblyIdentity** tem os seguintes atributos. Ele não tem subelementos.

| Atributo                 | Descrição                                                                                                                                                                                                                                                                                                          |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **tipo**                  | O valor deve ser win32 (em caso inferior). Obrigatórios.                                                                                                                                                                                                                                                                      |
| **name**                  | O atributo name identifica o aplicativo que está sendo afetado pelo arquivo de configuração do aplicativo ou pelo assembly que está sendo redirecionado. Use o seguinte formato para o nome: Organization.Division.Name. Obrigatórios. Por exemplo: Microsoft. Windows. MysampleApp ou Microsoft. Windows. MysampleAsm.<br/>            |
| **linguagem**              | Identifica o idioma. Opcional. Para um **assemblyIdentity que se** refere a um assembly, se o assembly for específico do idioma, especifique o código de linguagem DHTML. Se o assembly for para uso em todo o mundo (idioma neutro) de definir o valor como " \* ".<br/>                                                            |
| **processorArchitecture** | Especifica o processador que executa o aplicativo.                                                                                                                                                                                                                                                                     |
| **version**               | Especifica a versão do aplicativo ou assembly. Use a sintaxe de versão de quatro partes: mmmm.nnnn.oooo.pppp. Obrigatórios.                                                                                                                                                                                                   |
| **Publickeytoken**        | Para uma **assemblyIdentity** que se refere a um assembly, uma cadeia de caracteres hexadecimal de 16 caracteres que representa os últimos 8 bytes do hash SHA-1 da chave pública na qual o assembly está assinado. A chave pública usada para assinar o catálogo deve ter 2.048 bits ou mais. Necessário para todos os assemblies compartilhados lado a lado. |

<span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>

### <a name="bindingredirect"></a>bindingRedirect

O **elemento bindingRedirect** contém informações de redirecionamento para a associação do assembly. Cada **bindingRedirect** deve ser incluído em exatamente **um dependentAssembly.** A sintaxe de versão de quatro partes da nova versão e da versão antiga deve especificar as mesmas versões principais e secundárias.

Esse elemento tem os atributos mostrados na tabela a seguir.

| Atributo      | Descrição                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **oldVersion** | Especifica a versão do assembly que está sendo substituído e redirecionado. Use a sintaxe de versão de quatro partes nnnnn.nnnnn.nnnnn.nnnnn. Especifique um intervalo de versões por um traço sem espaços. Por exemplo, 2.14.3.0 ou 2.14.3.0 2.16.0.0. Obrigatórios. |
| **newVersion** | Especifica a versão do assembly de substituição. Use a sintaxe de versão de quatro partes nnnnn.nnnnn.nnnnn.nnnnn.                                                                                                                                     |

## <a name="remarks"></a>Comentários

Os arquivos de configuração do aplicativo não especificam arquivos.

## <a name="example"></a>Exemplo

``` XML
<bindingRedirect oldVersion="1.0.0.0" newVersion="1.0.10.0"/>
<bindingRedirect oldVersion="1.0.50.2011-1.0.60.65535" newVersion="1.0.70.0"/>
```
