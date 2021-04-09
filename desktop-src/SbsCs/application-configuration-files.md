---
description: Um arquivo de configuração de aplicativo é um arquivo XML usado para controlar a associação de assembly.
ms.assetid: b7453f2b-52a4-4af9-8410-ebbb430ada67
title: Arquivos de configuração de aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b1a2e0f6b493c217aded9e11507f660d517b400
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090213"
---
# <a name="application-configuration-files"></a>Arquivos de configuração de aplicativo

Um arquivo de configuração de aplicativo é um arquivo XML usado para controlar a associação de assembly. Ele pode redirecionar um aplicativo do usando uma versão de um assembly lado a lado para outra versão do mesmo assembly. Isso é chamado [de configuração por aplicativo](per-application-configuration.md). Um arquivo de configuração de aplicativo se aplica somente a um manifesto de aplicativo específico e a assemblies dependentes. Componentes isolados compilados com um manifesto de ID de recurso de manifesto ISOLATIONAWARE inserido \_ \_ \_ exigem um arquivo de configuração de aplicativo separado. Os manifestos gerenciados com [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) exigem um arquivo de configuração de aplicativo separado.

O redirecionamento especificado por um arquivo de configuração de aplicativo pode substituir as versões de assembly especificadas por [manifestos de aplicativo](application-manifests.md) e [arquivos de configuração de Publicador](publisher-configuration-files.md). Por exemplo, se um arquivo de configuração de Publicador especificar que todas as referências a um assembly sejam redirecionadas da versão 1.0.0.0 para 1.1.0.0, um arquivo de configuração de aplicativo poderá ser usado para redirecionar um aplicativo específico para usar a versão 1.0.0.0. Um arquivo de configuração de aplicativo aplica-se somente ao manifesto do aplicativo e aos assemblies dependentes especificados.

Para obter uma lista completa do esquema XML, consulte [esquema de arquivo de configuração de aplicativo](application-configuration-file-schema.md).

Os arquivos de configuração do aplicativo têm os elementos e atributos mostrados na tabela a seguir.



| Elemento               | Atributos                | Obrigatório |
|-----------------------|---------------------------|----------|
| **configuração**     |                           | Yes      |
| **windows**           |                           | Yes      |
| **publisherPolicy Apply**   |                           | Yes      |
|                       | **usar**                 | Yes      |
| **appmodel**           |                           | No       |
| **Elemento assemblyBinding**   |                           | Yes      |
| **investigação**           |                           | No       |
|                       | **privatePath**           | Yes      |
| **Estados**        |                           | No       |
| **dependentAssembly** |                           | Yes      |
| **assemblyIdentity**  |                           | Yes      |
|                       | **tipo**                  | Sim      |
|                       | **name**                  | Sim      |
|                       | **linguagem**              | No       |
|                       | **processorArchitecture** | Yes      |
|                       | **version**               | Yes      |
|                       | **publicKeyToken**        | No       |
| **bindingRedirect**   |                           | Yes      |
|                       | **oldVersion**            | Yes      |
|                       | **newVersion**            | Yes      |



 

## <a name="file-location"></a>Local do arquivo

Os arquivos de configuração do aplicativo devem ser instalados no mesmo local que o [manifesto do aplicativo](application-manifests.md)do aplicativo.

## <a name="file-name-syntax"></a>Sintaxe de nome de arquivo

O nome de um arquivo de configuração de aplicativo é o nome do executável do aplicativo seguido por. config.

Por exemplo, um arquivo de configuração de aplicativo que se refere a Example.exe ou Example.dll usaria a sintaxe de nome de arquivo mostrada no exemplo a seguir. Você pode omitir o campo para <*ID de recurso*> se estiver instalando o arquivo de configuração como um arquivo separado ou se a ID do recurso for 1.

**example.exe. <*ID do recurso* C1.config**

**example.dll. <*ID do recurso* C1.config**

## <a name="elements"></a>Elementos

Os nomes de elementos e atributos diferenciam maiúsculas de minúsculas. Os valores de elementos e atributos não diferenciam maiúsculas de minúsculas, exceto para o valor do atributo Type.

<span id="configuration"></span><span id="CONFIGURATION"></span>

### <a name="configuration"></a>configuração

Um elemento de contêiner para os elementos de **tempo de execução** e do **Windows** de um arquivo de configuração de aplicativo. Obrigatórios.

<span id="windows"></span><span id="WINDOWS"></span>

### <a name="windows"></a>windows

Inclui as partes do arquivo de configuração do aplicativo que se aplicam ao redirecionamento de assemblies do Win32.

> [!Note]  
> O autor de um aplicativo não deve incluir um arquivo de configuração com um subelemento do **Windows** como parte de seu aplicativo. Isso pode ser permitido se a única finalidade do arquivo de configuração é habilitar a funcionalidade **privatePath** de um elemento de **investigação** . O elemento de **investigação** não está disponível em sistemas anteriores ao windows Server 2008 R2 e ao Windows 7.

<span id="publisherPolicy"></span><span id="publisherpolicy"></span><span id="PUBLISHERPOLICY"></span>

### <a name="publisherpolicy"></a>publisherPolicy Apply

Especifica se a política do Publicador deve ser aplicada.

Esse elemento tem os atributos mostrados na tabela a seguir.



| Atributo | Descrição                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| **usar** | Um valor de "Sim" aplica a política do Publicador. Essa é a configuração padrão. O valor "no" não aplica a política do Publicador. |

<span id="runtime"></span><span id="RUNTIME"></span>

### <a name="runtime"></a>runtime

Inclui as partes do arquivo de configuração do aplicativo que se aplicam ao redirecionamento de assemblies do .net.

<span id="assemblyBinding"></span><span id="assemblybinding"></span><span id="ASSEMBLYBINDING"></span>

### <a name="assemblybinding"></a>Elemento assemblyBinding

Inclui as informações de redirecionamento para o aplicativo e o assembly afetado por esse arquivo de configuração de aplicativo. O primeiro subelemento de **assemblyBinding** deve ser um **AssemblyIdentity** que identifica o aplicativo.

A partir do Windows Server 2008 R2 e do Windows 7, um elemento **assemblyBinding** pode incluir um subelemento de **investigação** .

<span id="probing"></span><span id="PROBING"></span>

### <a name="probing"></a>investigação

Um subelemento opcional de um elemento **assemblyBinding** que estende a pesquisa de assemblies em diretórios adicionais. Os diretórios adicionais não precisam ser subdiretórios do diretório do assembly.

> [!Note]  
> Esse elemento não está disponível em sistemas anteriores ao Windows Server 2008 R2 e ao Windows 7 e só pode ser usado dentro de um elemento do **Windows** .

Esse elemento tem os atributos mostrados na tabela a seguir.

| Atributo       | Descrição                                                                                                                                                                                                                                   |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **privatePath** | Especifica os [caminhos relativos](/windows/desktop/FileIO/naming-a-file) de subdiretórios do diretório base do aplicativo que podem conter assemblies. Um máximo de nove caminhos de subdiretórios podem ser especificados. Delimite cada caminho de subdiretório com um ponto e vírgula. |

Você pode usar o especificador especial de pontos duplos em um caminho para denotar o diretório pai do diretório atual. Não é possível especificar mais de dois níveis acima do diretório atual usando dois pontos. Não use pontos triplos. Por exemplo, um aplicativo que usa o seguinte elemento de **investigação** verifica diretórios adicionais para um assembly.

``` XML
<probing privatePath="bin;..\bin2\subbin;bin3"/>
```

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a>dependência
Um elemento de contêiner para pelo menos um **dependentAssembly**. Cada **dependentAssembly** pode estar dentro de exatamente uma **dependência**. Esse elemento não tem atributos. Opcional.

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a>dependentAssembly

O primeiro subelemento deve ser um elemento **AssemblyIdentity** que identifica o assembly lado a lado sendo redirecionado pelo arquivo de configuração do aplicativo. Um **dependentAssembly** não tem atributos.

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a>assemblyIdentity

Como o primeiro subelemento de um elemento **assemblyBinding** , **AssemblyIdentity** descreve e identifica exclusivamente um aplicativo. O arquivo de configuração de aplicativo redireciona a associação desse aplicativo para assemblies lado a lado. Por exemplo, o **AssemblyIdentity** a seguir indica que o arquivo de configuração do aplicativo afeta a associação do aplicativo mysampleApp a assemblies lado a lado. Os assemblies sendo redirecionados seriam identificados em um **dependentAssembly**.

``` XML
<assemblyIdentity processorArchitecture="X86" name="Microsoft.Windows.mysampleApp" type="win32" version="1.0.0.0"/>
```

Como o primeiro subelemento de um elemento **dependentAssembly** , **AssemblyIdentity** descreve um assembly lado a lado no qual o aplicativo depende. O arquivo de configuração do aplicativo reconfigura a identidade desse assembly necessário. Por exemplo, o **AssemblyIdentity** e o **bindingRedirect** a seguir reconfigura uma dependência em Microsoft. Windows. SampleAssembly da versão 2.0.0.0 para a versão 2.1.0.0.

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

Observe que cada **AssemblyIdentity** incluído em um **dependentAssembly** deve corresponder exatamente ao **AssemblyIdentity** no [manifesto do assembly](assembly-manifests.md)próprio do assembly.

O elemento **AssemblyIdentity** tem os atributos a seguir. Ele não tem subelementos.

| Atributo                 | Descrição                                                                                                                                                                                                                                                                                                          |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **tipo**                  | O valor deve ser Win32 (em letras minúsculas). Obrigatórios.                                                                                                                                                                                                                                                                      |
| **name**                  | O atributo Name identifica o aplicativo que está sendo afetado pelo arquivo de configuração do aplicativo ou o assembly que está sendo redirecionado. Use o seguinte formato para o nome: Organization.Division.Name. Obrigatórios. Por exemplo: Microsoft. Windows. MysampleApp ou Microsoft. Windows. MysampleAsm.<br/>            |
| **linguagem**              | Identifica o idioma. Opcional. Para um **AssemblyIdentity** se referir a um assembly, se o assembly for específico a um idioma, especifique o código de linguagem DHTML. Se o assembly for para uso mundial (com neutralidade de idioma), defina o valor como " \* ".<br/>                                                            |
| **processorArchitecture** | Especifica o processador que executa o aplicativo.                                                                                                                                                                                                                                                                     |
| **version**               | Especifica a versão do aplicativo ou assembly. Use a sintaxe de versão de quatro partes: mmmm. nnnn. Oooo. PPPP. Obrigatórios.                                                                                                                                                                                                   |
| **publicKeyToken**        | Para um **AssemblyIdentity** se referir a um assembly, uma cadeia de caracteres hexadecimal de 16 caracteres que representa os últimos 8 bytes do hash SHA-1 da chave pública sob a qual o assembly está assinado. A chave pública usada para assinar o catálogo deve ter 2048 bits ou mais. Necessário para todos os assemblies compartilhados lado a lado. |

<span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>

### <a name="bindingredirect"></a>bindingRedirect

O elemento **bindingRedirect** contém informações de redirecionamento para a associação do assembly. Cada **bindingRedirect** deve ser incluído em exatamente um **dependentAssembly**. A sintaxe de versão de quatro partes da nova versão e da versão antiga deve especificar as mesmas versões principais e secundárias.

Esse elemento tem os atributos mostrados na tabela a seguir.

| Atributo      | Descrição                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **oldVersion** | Especifica a versão do assembly que está sendo substituída e redirecionada. Use a sintaxe de versão de quatro partes nnnnn. NNNNN. NNNNN. NNNNN. Especifique um intervalo de versões por um traço sem espaços. Por exemplo, 2.14.3.0 ou 2.14.3.0 2.16.0.0. Obrigatórios. |
| **newVersion** | Especifica a versão do assembly de substituição. Use a sintaxe de versão de quatro partes nnnnn. NNNNN. NNNNN. NNNNN.                                                                                                                                     |

## <a name="remarks"></a>Comentários

Os arquivos de configuração do aplicativo não especificam arquivos.

## <a name="example"></a>Exemplo

``` XML
<bindingRedirect oldVersion="1.0.0.0" newVersion="1.0.10.0"/>
<bindingRedirect oldVersion="1.0.50.2011-1.0.60.65535" newVersion="1.0.70.0"/>
```
