---
description: Um manifesto de aplicativo é um arquivo XML que descreve e identifica os assemblies lado a lado particulares e compartilhados aos quais um aplicativo deve se associar em tempo de execução.
ms.assetid: c5016251-db7a-4edc-9be9-3acb03d495f8
title: Manifestos do aplicativo
ms.topic: article
ms.date: 10/08/2020
ms.custom: 19H1
ms.openlocfilehash: 2fb7297310102134dfcacf0e5f0d907fbf3a3e0b
ms.sourcegitcommit: 7eadd92b1da5eb4eab7d516a5a768e7f7fc02d4c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/16/2021
ms.locfileid: "112230237"
---
# <a name="application-manifests"></a>Manifestos do aplicativo

Um manifesto de aplicativo é um arquivo XML que descreve e identifica os assemblies lado a lado particulares e compartilhados aos quais um aplicativo deve se associar em tempo de execução. Elas devem ser as mesmas versões de assembly que foram usadas para testar o aplicativo. Os manifestos de aplicativo também podem descrever metadados para arquivos que são particulares ao aplicativo.

Para obter uma lista completa do esquema XML, consulte [manifest File Schema](manifest-file-schema.md).

Os manifestos do aplicativo têm os seguintes elementos e atributos.

| Elemento                               | Atributos                | Obrigatório |
|---------------------------------------|---------------------------|----------|
| **)**                          |                           | Sim      |
|                                       | **manifestVersion**       | Sim      |
| **NoInherit**                         |                           | Não       |
| **assemblyIdentity**                  |                           | Sim      |
|                                       | **tipo**                  | Sim      |
|                                       | **name**                  | Sim      |
|                                       | **linguagem**              | Não       |
|                                       | **processorArchitecture** | Não       |
|                                       | **version**               | Sim      |
|                                       | **publicKeyToken**        | Não       |
| **compatibilidade**                     |                           | Não       |
| **aplicativo**                       |                           | Não       |
| **supportedOS**                       | **Id**                    | Não       |
| **maxversiontested**                  | **Id**                    | Não       |
| **Estados**                        |                           | Não       |
| **dependentAssembly**                 |                           | Não       |
| **file**                              |                           | Não       |
|                                       | **name**                  | Não       |
|                                       | **hashalg**               | Não       |
|                                       | **hash**                  | Não       |
| **activeCodePage**                    |                           | Não       |
| **Elevação de autoelevação**                       |                           | Não       |
| **disableTheming**                    |                           | Não       |
| **disableWindowFiltering**            |                           | Não       |
| **dpiAware**                          |                           | Não       |
| **dpiAwareness**                      |                           | Não       |
| **gdiScaling**                        |                           | Não       |
| **highResolutionScrollingAware**      |                           | Não       |
| **longPathAware**                     |                           | Não       |
| **printerDriverIsolation**            |                           | Não       |
| **ultraHighResolutionScrollingAware** |                           | Não       |
| **msix**                              |                           | Não       |
| **heaptype**                          |                           | Não       |

## <a name="file-location"></a>Local do arquivo

Os manifestos do aplicativo devem ser incluídos como um recurso no arquivo EXE ou DLL do aplicativo.

Para obter mais informações, consulte [instalando assemblies lado a lado](installing-side-by-side-assemblies.md).

## <a name="file-name-syntax"></a>Sintaxe de nome de arquivo

O nome de um arquivo de manifesto do aplicativo é o nome do executável do aplicativo seguido por. manifest.

Por exemplo, um manifesto de aplicativo que se refere a example.exe ou example.dll usaria a seguinte sintaxe de nome de arquivo. Você pode omitir o campo <*ID de recurso*> se a ID do recurso for 1.

**example.exe. <*ID do recurso*>. manifest**

**example.dll. <*ID do recurso*>. manifest**

## <a name="elements"></a>Elementos

Os nomes de elementos e atributos diferenciam maiúsculas de minúsculas. Os valores de elementos e atributos não diferenciam maiúsculas de minúsculas, exceto para o valor do atributo de tipo.

<span id="assembly"></span><span id="ASSEMBLY"></span>

### <a name="assembly"></a>assembly

Um elemento de contêiner. Seu primeiro subelemento deve ser um elemento **NoInherit** ou **AssemblyIdentity** . Obrigatórios.

O elemento **assembly** deve estar no namespace "urn: schemas-microsoft-com: asm. v1". Os elementos filho do assembly também devem estar nesse namespace, por herança ou por marcação.

O elemento **assembly** tem os atributos a seguir.



| Atributo           | Descrição                                           |
|---------------------|-------------------------------------------------------|
| **manifestVersion** | O **atributo manifestVersion** deve ser definido como 1.0. |


<span id="noInherit"></span><span id="noinherit"></span><span id="NOINHERIT"></span>

### <a name="noinherit"></a>Noinherit

Inclua esse elemento em um manifesto do aplicativo para definir os [contextos de ativação gerados](activation-contexts.md) do manifesto com o sinalizador "no inherit". Quando esse sinalizador não é definido em um contexto de ativação e o contexto de ativação está ativo, ele é herdado por novos threads no mesmo processo, janelas, procedimentos de janela e Chamadas [de](/windows/desktop/Sync/asynchronous-procedure-calls)Procedimento Assíncrono . Definir esse sinalizador impede que o novo objeto herde o contexto ativo.

O **elemento noInherit** é opcional e normalmente omitido. A maioria dos assemblies não funciona corretamente usando um contexto de ativação não herdado porque o assembly deve ser projetado explicitamente para gerenciar a propagação de seu próprio contexto de ativação. O uso do **elemento noInherit** requer que todos os assemblies dependentes referenciados pelo manifesto do aplicativo tenham um elemento **noInherit** em seu [manifesto do assembly](assembly-manifests.md).

Se **noInherit** for usado em um manifesto, ele deverá ser o primeiro subelemento do elemento **assembly.** O **elemento assemblyIdentity** deve vir imediatamente após **o elemento noInherit.** Se **noInherit** não for usado, **assemblyIdentity** deverá ser o primeiro subelemento do elemento **assembly.** O **elemento noInherit** não tem elementos filho. Não é um elemento válido nos [manifestos do assembly.](assembly-manifests.md)

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a>assemblyIdentity

Como o primeiro subelemento de um elemento **de assembly,** **assemblyIdentity** descreve e identifica exclusivamente o aplicativo que possui esse manifesto do aplicativo. Como o primeiro subelemento de um elemento **dependentAssembly,** **assemblyIdentity** descreve um assembly lado a lado exigido pelo aplicativo. Observe que cada assembly referenciado no manifesto do aplicativo requer uma **assemblyIdentity** que corresponde exatamente à **assemblyIdentity** no manifesto de assembly próprio do assembly referenciado.

O **elemento assemblyIdentity** tem os seguintes atributos. Ele não tem subelementos.

| Atributo                 | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **tipo**                  | Especifica o tipo de aplicativo ou assembly. O valor deve ser Win32 e todos em menor caso. Obrigatórios.                                                                                                                                                                                                                                                                                                                              |
| **name**                  | Nomeia exclusivamente o aplicativo ou assembly. Use o seguinte formato para o nome: Organization.Division.Name. Por exemplo, Microsoft.Windows.mysampleApp. Obrigatórios.                                                                                                                                                                                                                                                               |
| **linguagem**              | Identifica o idioma do aplicativo ou assembly. Opcional. Se o aplicativo ou assembly for específico do idioma, especifique o código de linguagem DHTML. Na **assemblyIdentidade de um** aplicativo destinado ao uso mundial (idioma neutro) omite o atributo de idioma.<br/> Em um **assemblyIdentidade de** um assembly destinado ao uso mundial (neutro na linguagem), de definido o valor da linguagem como " \* ".<br/> |
| **processorArchitecture** | Especifica o processador. Os valores válidos incluem `x86`, `amd64`, `arm` e `arm64`. Opcional.                                                                                                                                                                                                                                                                                                                       |
| **version**               | Especifica a versão do aplicativo ou assembly. Use o formato de versão de quatro partes: mmmmm.nnnnn.ooooo.ppppp. Cada uma das partes separadas por períodos pode ser de 0 a 65535, inclusive. Para obter mais informações, consulte [Versões do assembly](assembly-versions.md). Obrigatórios.                                                                                                                                                                        |
| **Publickeytoken**        | Uma cadeia de caracteres hexadecimal de 16 caracteres que representa os últimos 8 bytes do hash SHA-1 da chave pública na qual o aplicativo ou assembly está assinado. A chave pública usada para assinar o catálogo deve ter 2.048 bits ou mais. Necessário para todos os assemblies compartilhados lado a lado.                                                                                                                                                     |

<span id="compatibility"></span><span id="COMPATIBILITY"></span>

### <a name="compatibility"></a>compatibilidade

Contém pelo menos um **aplicativo**. Ele não tem atributos. Opcional. Manifestos de aplicativo sem um elemento de compatibilidade padrão para a compatibilidade do Windows Vista no Windows 7.

<span id="application"></span><span id="APPLICATION"></span>

### <a name="application"></a>aplicativo

Contém pelo menos um **elemento DOOS** com suporte. A partir Windows 10, versão 1903, ele também pode conter um **elemento maxversiontested** opcional. Ele não tem atributos. Opcional.

<span id="supportedOS"></span><span id="supportedos"></span><span id="SUPPORTEDOS"></span>

### <a name="supportedos"></a>supportedOS

O **elemento supportedOS** tem o atributo a seguir. Ele não tem subelementos.

| Atributo | Descrição   |
|-----------|-----------------------|
| **Id**    | De definir o atributo Id como **{e2011457-1546-43c5-a5fe-008deee3d3f0}** para executar o aplicativo usando a funcionalidade vista. Isso pode permitir que um aplicativo projetado para o Windows Vista seja executado em um sistema operacional posterior. <br/> De definir o atributo Id como **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** para executar o aplicativo usando a funcionalidade do Windows 7.<br/> Os aplicativos que suportam o Windows Vista, o Windows 7 e Windows 8 funcionalidade não exigem manifestos separados. Nesse caso, adicione os GUIDs para todos os sistemas operacionais Windows.<br/> Para obter informações sobre o comportamento do atributo **de ID** no Windows, consulte o guia Windows 8 e o Guia de Compatibilidade do [Windows Server 2012.](https://www.microsoft.com/download/details.aspx?id=27416)<br/> Os seguintes GUIDs correspondem aos sistemas operacionais indicados:<br/> **{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** -> Windows 10, Windows Server 2016 e Windows Server 2019<br/> **{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 e Windows Server 2012 R2<br/> **{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 e Windows Server 2012<br/> **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 e Windows Server 2008 R2<br/> **{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> Windows Vista e Windows Server 2008<br/> Você pode testar isso no Windows 7 ou Windows 8.x executando Monitor de Recursos (resmon), indo para a guia CPU, clicando com o botão direito do mouse nos rótulos de coluna, "Selecionar Coluna..." e marque "Contexto do Sistema Operacional". No Windows 8.x, você também pode encontrar essa coluna disponível no Gerenciador de Tarefas (taskmgr). O conteúdo da coluna mostra o valor mais alto encontrado ou "Windows Vista" como o padrão. <br/> |

<span id="maxVersionTested"></span><span id="maxversiontested"></span><span id="MAXVERSIONTESTED"></span>

### <a name="maxversiontested"></a>maxversiontested

O **elemento maxversiontested** especifica as versões do Windows em que o aplicativo foi testado a partir da versão mínima do sistema operacional que o aplicativo dá suporte até a versão máxima. O conjunto completo de versões pode ser encontrado [aqui.](https://developer.microsoft.com/windows/downloads/sdk-archive/) Isso destina-se a ser usado por aplicativos da área de trabalho que usam Ilhas [XAML](/windows/apps/desktop/modernize/xaml-islands) e que não são implantados em um pacote MSIX. Esse elemento tem suporte no Windows 10, versão 1903 e versões posteriores.

O **elemento maxversiontested** tem o atributo a seguir. Ele não tem subelementos.

| Atributo | Descrição    |
|-----------|----------------|
| **Id**    | De definir o atributo Id como uma cadeia de caracteres de versão de 4 partes que especifica a versão máxima do Windows em que o aplicativo foi testado. Por exemplo, "10.0.18226.0". |

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a>dependência

Contém pelo menos um **dependentAssembly.** Ele não tem atributos. Opcional.

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a>dependentAssembly

O primeiro subelemento de **dependentAssembly** deve ser um **elemento assemblyIdentity** que descreve um assembly lado a lado exigido pelo aplicativo. Cada **dependentAssembly** deve estar dentro de exatamente uma **dependência**. Ele não tem atributos.

<span id="file"></span><span id="FILE"></span>

### <a name="file"></a>file

Especifica arquivos que são privados para o aplicativo. Opcional.

O **elemento** file tem os atributos mostrados na tabela a seguir.



| Atributo   | Descrição                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **name**    | Nome do arquivo. Por exemplo, Comctl32.dll.                                                            |
| **Hashalg** | Algoritmo usado para criar um hash do arquivo. Esse valor deve ser SHA1.                                 |
| **hash**    | Um hash do arquivo referenciado pelo nome. Uma cadeia de caracteres hexadecimal de comprimento, dependendo do algoritmo de hash. |

<span id="activeCodePage"></span><span id="activecodepage"></span><span id="ACTIVECODEPAGE"></span>

### <a name="activecodepage"></a>activeCodePage

Force um processo a usar UTF-8 como a página de código do processo.

**activeCodePage** foi adicionado na versão 1903 do Windows (atualização de maio de 2019). Você pode declarar essa propriedade e o destino/executar em builds anteriores do Windows, mas deve lidar com a detecção e a conversão de página de código herddas como de costume. Consulte [Usar a página de código UTF-8](/windows/uwp/design/globalizing/use-utf8-code-page) para obter detalhes.

Esse elemento não tem atributos. **UTF-8 é** apenas um valor válido para **o elemento activeCodePage.**

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2019/WindowsSettings"> 
      <activeCodePage>UTF-8</activeCodePage> 
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="autoElevate"></span><span id="autoelevate"></span><span id="AUTOELEVATE"></span>

### <a name="autoelevate"></a>autoElevate

Especifica se a elevação automática está habilitada. **TRUE** indica que ele está habilitado. Ele não tem atributos.

<span id="disableTheming"></span><span id="disabletheming"></span><span id="DISABLETHEMING"></span>

### <a name="disabletheming"></a>disableTheming

Especifica se a entrega de elementos da interface do usuário a um tema está desabilitada. **TRUE** indica desabilitado. Ele não tem atributos.

<span id="disableWindowFiltering"></span><span id="disablewindowfiltering"></span><span id="DISABLEWINDOWFILTERING"></span>

### <a name="disablewindowfiltering"></a>disableWindowFiltering

Especifica se a filtragem de janelas deve ser desabilitada. **TRUE** desabilita a filtragem de janelas para que você possa enumerar janelas imersivas da área de trabalho. **disableWindowFiltering** foi adicionado Windows 8 e não tem atributos.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <disableWindowFiltering>true</disableWindowFiltering>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAware"></span><span id="dpiaware"></span><span id="DPIAWARE"></span>

### <a name="dpiaware"></a>dpiAware

Especifica se o processo atual está ciente de pontos por polegada (dpi).

**Windows 10, versão 1607:** O **elemento dpiAware** será ignorado se **o elemento dpiAwareness** estiver presente. Você pode incluir ambos os elementos em um manifesto se quiser especificar um comportamento diferente para Windows 10, versão 1607 do que para uma versão anterior do sistema operacional.

A tabela a seguir descreve o comportamento que resulta com base na presença do **elemento dpiAware** e no texto que ele contém. O texto dentro do elemento não é sensível a minúsculas.

| Estado do **elemento dpiAware** | Descrição     |
|-----------------------------------|---------|
| Absent                            | O processo atual não tem conhecimento de dpi por padrão. Você pode alterar essa configuração programaticamente chamando a [**função SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) [**ou SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)                                                                                                                                                            |
| Contém "true"                   | O processo atual reconhece o dpi do sistema.                                                                                                                                                                                                                                                                                                                                                          |
| Contém "false"                  | **Windows Vista, Windows 7 e Windows 8:** O comportamento é o mesmo de quando **o dpiAware** está ausente.<br/> **Windows 8.1 e Windows 10:** O processo atual não tem conhecimento de dpi e você não pode alterar essa configuração programaticamente chamando a função [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) ou [**SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)<br/> |
| Contém "true/pm"                | **Windows Vista, Windows 7 e Windows 8:** O processo atual reconhece o dpi do sistema.<br/> **Windows 8.1 e Windows 10:** O processo atual reconhece dpi por monitor.<br/>                                                                                                                                                                                                          |
| Contém "por monitor"            | **Windows Vista, Windows 7 e Windows 8:** O comportamento é o mesmo de quando **o dpiAware** está ausente.<br/> **Windows 8.1 e Windows 10:** O processo atual reconhece dpi por monitor.<br/>                                                                                                                                                                                      |
| Contém qualquer outra cadeia de caracteres         | **Windows Vista, Windows 7 e Windows 8:** O comportamento é o mesmo de quando **o dpiAware** está ausente.<br/> **Windows 8.1 e Windows 10:** O processo atual não tem conhecimento de dpi e você não pode alterar essa configuração programaticamente chamando a função [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) ou [**SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)<br/> |

Para obter mais informações sobre as configurações de reconhecimento de dpi, consulte [Comparação de níveis de reconhecimento de DPI](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).

**dpiAware** não tem atributos.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAwareness"></span><span id="dpiawareness"></span><span id="DPIAWARENESS"></span>

### <a name="dpiawareness"></a>dpiAwareness

Especifica se o processo atual está ciente de pontos por polegada (dpi).

A versão mínima do sistema operacional que dá suporte ao **elemento dpiAwareness** é Windows 10 versão 1607. Para versões que suportam **o elemento dpiAwareness,** **o dpiAwareness** substitui o **elemento dpiAware.** Você pode incluir ambos os elementos em um manifesto se quiser especificar um comportamento diferente para Windows 10, versão 1607 do que para uma versão anterior do sistema operacional.

O **elemento dpiAwareness** pode conter um único item ou uma lista de itens separados por vírgulas. No último caso, o primeiro item (mais à esquerda) na lista reconhecido pelo sistema operacional é usado. Dessa forma, você pode especificar diferentes comportamentos com suporte em versões futuras do sistema operacional Windows.

A tabela a seguir descreve o comportamento que resulta com base na presença do elemento **dpiAwareness** e no texto que ele contém em seu item reconhecido mais à esquerda. O texto dentro do elemento não é sensível a minúsculas.

| **Status do elemento dpiAwareness:**        | Descrição                          |
|-----------------------------------------|-------------------------------------------|
| O elemento está ausente                       | O **elemento dpiAware** especifica se o processo está ciente de dpi.                                                                                                                                                                   |
| Não contém nenhum item reconhecido            | O processo atual não tem conhecimento de dpi por padrão. Você pode alterar essa configuração programaticamente chamando a [**função SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) [**ou SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) |
| O primeiro item reconhecido é "system"       | O processo atual reconhece o dpi do sistema.                                                                                                                                                                                               |
| O primeiro item reconhecido é "permonitor"   | O processo atual reconhece dpi por monitor.                                                                                                                                                                                          |
| O primeiro item reconhecido é "permonitorv2" | O processo atual usa o contexto de reconhecimento de dpi por monitor-v2. Esse item só será reconhecido no Windows 10 versão 1703 ou posterior.                                                                                              |
| O primeiro item reconhecido é "não ciente"      | O processo atual não tem conhecimento de dpi. Você **não pode** alterar essa configuração programaticamente chamando a função [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) ou [**SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)      |

Para obter mais informações sobre as configurações de reconhecimento de dpi com suporte por esse elemento, consulte [RECONHECIMENTO de DPI \_ ](/windows/desktop/api/windef/ne-windef-dpi_awareness) e CONTEXTO DE RECONHECIMENTO [de DPI \_ \_ ](/windows/desktop/hidpi/dpi-awareness-context).

**dpiAwareness** não tem atributos.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <dpiAwareness>PerMonitorV2, unaware</dpiAwareness>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="gdiScaling"></span><span id="gdiscaling"></span><span id="GDISCALING"></span>

### <a name="gdiscaling"></a>gdiScaling

Especifica se o dimensionamento GDI está habilitado. A versão mínima do sistema operacional que dá suporte ao **elemento gdiScaling** é Windows 10 versão 1703.

A estrutura GDI (interface do dispositivo gráfico) pode aplicar o dimensionamento de DPI a primitivos e texto por monitor sem atualizações para o próprio aplicativo. Isso pode ser útil para que os aplicativos GDI não sejam mais atualizados ativamente.

Gráficos não vetoriais (como bitmaps, ícones ou barras de ferramentas) não podem ser dimensionados por esse elemento. Além disso, elementos gráficos e textos que aparecem em bitmaps construídos dinamicamente por aplicativos também não podem ser dimensionados por esse elemento.

**TRUE** indica que esse elemento está habilitado. Ele não tem atributos.


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2017/WindowsSettings">
      <gdiScaling>true</gdiScaling>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="highResolutionScrollingAware"></span><span id="highresolutionscrollingaware"></span><span id="HIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="highresolutionscrollingaware"></a>highResolutionScrollingAware

Especifica se o com conhecimento de rolagem de alta resolução está habilitado. **TRUE** indica que ele está habilitado. Ele não tem atributos.

<span id="longPathAware"></span><span id="longpathaware"></span><span id="LONGPATHAWARE"></span>

### <a name="longpathaware"></a>longPathAware

Habilita caminhos longos que **excedem MAX_PATH** comprimento. Esse elemento tem suporte no Windows 10, versão 1607 e posterior. Para obter mais informações, consulte [este artigo](../fileio/maximum-file-path-limitation.md).

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <ws2:longPathAware>true</ws2:longPathAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="printerDriverIsolation"></span><span id="printerdriverisolation"></span><span id="PRINTERDRIVERISOLATION"></span>

### <a name="printerdriverisolation"></a>printerDriverIsolation

Especifica se o isolamento do driver de impressora está habilitado. **TRUE** indica que ele está habilitado. Ele não tem atributos. O isolamento do driver de impressora melhora a confiabilidade do serviço de impressão do Windows, permitindo que os drivers de impressora sejam executados em processos separados do processo no qual o spooler de impressão é executado. Suporte para isolamento de driver de impressora iniciado no Windows 7 e Windows Server 2008 R2. Um aplicativo pode declarar o isolamento do driver de impressora em seu manifesto do aplicativo para isolar-se do driver de impressora e melhorar sua confiabilidade. Ou seja, o aplicativo não falhará se o driver da impressora tiver um erro.


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <printerDriverIsolation>true</printerDriverIsolation>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="ultraHighResolutionScrollingAware"></span><span id="ultrahighresolutionscrollingaware"></span><span id="ULTRAHIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="ultrahighresolutionscrollingaware"></a>ultraHighResolutionScrollingAware

Especifica se o ultra-high-resolution-scrolling aware está habilitado. **TRUE** indica que ele está habilitado. Ele não tem atributos.

<span id="msix"></span><span id="MSIX"></span>

### <a name="msix"></a>MSIX

Especifica as informações de identidade de um [pacote MSIX esparso](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) para o aplicativo atual. Esse elemento tem suporte no Windows 10, versão 2004 e versões posteriores.

O **elemento msix** deve estar no namespace `urn:schemas-microsoft-com:msix.v1` . Ele tem os atributos mostrados na tabela a seguir.

| Atributo   | Descrição                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **Editor**    | Descreve as informações do editor. Esse valor deve corresponder ao **atributo Publicador** no [elemento Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) no manifesto do pacote esparso. |
| **packageName** | Descreve o conteúdo do pacote. Esse valor deve corresponder ao **atributo Name** no [elemento Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) no manifesto do pacote esparso.    |
| **applicationId**    | O identificador exclusivo do aplicativo. Esse valor deve corresponder ao **atributo ID** no [elemento Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) no manifesto do pacote esparso.  |

```xml
<?xml version="1.0" encoding="utf-8"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1">
  <assemblyIdentity version="1.0.0.0" name="Contoso.PhotoStoreApp"/>
  <msix xmlns="urn:schemas-microsoft-com:msix.v1"
          publisher="CN=Contoso"
          packageName="ContosoPhotoStore"
          applicationId="ContosoPhotoStore"
        />
</assembly>
```

### <a name="heaptype"></a>heapType

Substitui a implementação de heap padrão para as [APIs de heap do Win32](../Memory/heap-functions.md) a usar.

* O valor **SegmentHeap** indica que o heap de segmento será usado. O heap de segmento é uma implementação de heap moderna que geralmente reduzirá o uso geral de memória. Esse elemento tem suporte no Windows 10, versão 2004 (build 19041) e posterior.
* Todos os outros valores são ignorados.

Esse elemento não tem atributos.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2020/WindowsSettings">
      <heapType>SegmentHeap</heapType>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

## <a name="example"></a>Exemplo

A seguir está um exemplo de um manifesto do aplicativo para um aplicativo chamado MySampleApp.exe. O aplicativo consome o assembly lado a lado SampleAssembly.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">

  <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--This Id value indicates the application supports Windows Vista functionality -->
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--This Id value indicates the application supports Windows 7 functionality-->
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--This Id value indicates the application supports Windows 8 functionality-->
          <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
        <!--This Id value indicates the application supports Windows 8.1 functionality-->
          <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
      </application> 
  </compatibility>

  <assemblyIdentity type="win32" 
                    name="myOrganization.myDivision.mySampleApp" 
                    version="6.0.0.0" 
                    processorArchitecture="x86" 
                    publicKeyToken="0000000000000000"
  />
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" 
                        name="Proseware.Research.SampleAssembly" 
                        version="6.0.0.0" 
                        processorArchitecture="X86" 
                        publicKeyToken="0000000000000000" 
                        language="*"
      />
    </dependentAssembly>
  </dependency>
</assembly>
```
