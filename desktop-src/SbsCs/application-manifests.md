---
description: Um manifesto de aplicativo é um arquivo XML que descreve e identifica os assemblies lado a lado particulares e compartilhados aos quais um aplicativo deve se associar em tempo de execução.
ms.assetid: c5016251-db7a-4edc-9be9-3acb03d495f8
title: Manifestos do aplicativo
ms.topic: article
ms.date: 10/08/2020
ms.custom: 19H1
ms.openlocfilehash: cb065bc4d6d29f4142c23cdd91c83769e2fb9b87
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "105751169"
---
# <a name="application-manifests"></a>Manifestos do aplicativo

Um manifesto de aplicativo é um arquivo XML que descreve e identifica os assemblies lado a lado particulares e compartilhados aos quais um aplicativo deve se associar em tempo de execução. Elas devem ser as mesmas versões de assembly que foram usadas para testar o aplicativo. Os manifestos de aplicativo também podem descrever metadados para arquivos que são particulares ao aplicativo.

Para obter uma lista completa do esquema XML, consulte [manifest File Schema](manifest-file-schema.md).

Os manifestos do aplicativo têm os seguintes elementos e atributos.

| Elemento                               | Atributos                | Obrigatório |
|---------------------------------------|---------------------------|----------|
| **)**                          |                           | Yes      |
|                                       | **manifestVersion**       | Yes      |
| **NoInherit**                         |                           | No       |
| **assemblyIdentity**                  |                           | Yes      |
|                                       | **tipo**                  | Sim      |
|                                       | **name**                  | Sim      |
|                                       | **linguagem**              | No       |
|                                       | **processorArchitecture** | No       |
|                                       | **version**               | Yes      |
|                                       | **publicKeyToken**        | No       |
| **compatibilidade**                     |                           | No       |
| **aplicativo**                       |                           | No       |
| **supportedOS**                       | **Id**                    | No       |
| **maxversiontested**                  | **Id**                    | No       |
| **Estados**                        |                           | No       |
| **dependentAssembly**                 |                           | No       |
| **file**                              |                           | No       |
|                                       | **name**                  | No       |
|                                       | **hashalg**               | No       |
|                                       | **hash**                  | No       |
| **activeCodePage**                    |                           | No       |
| **Elevação de autoelevação**                       |                           | No       |
| **disableTheming**                    |                           | No       |
| **disableWindowFiltering**            |                           | No       |
| **dpiAware**                          |                           | No       |
| **dpiAwareness**                      |                           | No       |
| **gdiScaling**                        |                           | No       |
| **highResolutionScrollingAware**      |                           | No       |
| **longPathAware**                     |                           | No       |
| **printerDriverIsolation**            |                           | No       |
| **ultraHighResolutionScrollingAware** |                           | No       |
| **MSIX**                              |                           | No       |
| **heaptype**                          |                           | No       |

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
| **manifestVersion** | O atributo **manifestVersion** deve ser definido como 1,0. |


<span id="noInherit"></span><span id="noinherit"></span><span id="NOINHERIT"></span>

### <a name="noinherit"></a>NoInherit

Inclua esse elemento em um manifesto de aplicativo para definir os [contextos de ativação](activation-contexts.md) gerados do manifesto com o sinalizador "sem herança". Quando esse sinalizador não é definido em um contexto de ativação e o contexto de ativação está ativo, ele é herdado por novos threads no mesmo processo, janelas, procedimentos de janela e [chamadas de procedimento assíncronos](/windows/desktop/Sync/asynchronous-procedure-calls). Definir esse sinalizador impede que o novo objeto herde o contexto ativo.

O elemento **NoInherit** é opcional e normalmente é omitido. A maioria dos assemblies não funciona corretamente usando um contexto de ativação sem herança porque o assembly deve ser explicitamente projetado para gerenciar a propagação de seu próprio contexto de ativação. O uso do elemento **NoInherit** requer que quaisquer assemblies dependentes referenciados pelo manifesto do aplicativo tenham um elemento **NoInherit** em seu [manifesto do assembly](assembly-manifests.md).

Se **NoInherit** for usado em um manifesto, ele deverá ser o primeiro subelemento do elemento **assembly** . O elemento **AssemblyIdentity** deve vir imediatamente após o elemento **NoInherit** . Se **NoInherit** não for usado, **AssemblyIdentity** deverá ser o primeiro subelemento do elemento **assembly** . O elemento **NoInherit** não tem nenhum elemento filho. Não é um elemento válido em [manifestos de assembly](assembly-manifests.md).

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a>assemblyIdentity

Como o primeiro subelemento de um elemento de **assembly** , **AssemblyIdentity** descreve e identifica exclusivamente o aplicativo proprietário deste manifesto do aplicativo. Como o primeiro subelemento de um elemento **dependentAssembly** , **AssemblyIdentity** descreve um assembly lado a lado exigido pelo aplicativo. Observe que cada assembly referenciado no manifesto do aplicativo requer um **AssemblyIdentity** que corresponda exatamente ao **AssemblyIdentity** no manifesto do assembly do assembly referenciado.

O elemento **AssemblyIdentity** tem os atributos a seguir. Ele não tem subelementos.

| Atributo                 | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **tipo**                  | Especifica o tipo de aplicativo ou assembly. O valor deve ser Win32 e todos em letras minúsculas. Obrigatórios.                                                                                                                                                                                                                                                                                                                              |
| **name**                  | Nomeia exclusivamente o aplicativo ou o assembly. Use o seguinte formato para o nome: Organization.Division.Name. Por exemplo, Microsoft. Windows. mysampleApp. Obrigatórios.                                                                                                                                                                                                                                                               |
| **linguagem**              | Identifica o idioma do aplicativo ou assembly. Opcional. Se o aplicativo ou o assembly for específico a um idioma, especifique o código de linguagem DHTML. No **AssemblyIdentity** de um aplicativo destinado para uso mundial (neutro à linguagem), omita o atributo language.<br/> Em um **AssemblyIdentity** de um assembly destinado para uso mundial (neutro à linguagem), defina o valor de idioma como " \* ".<br/> |
| **processorArchitecture** | Especifica o processador. Os valores válidos incluem `x86`, `amd64`, `arm` e `arm64`. Opcional.                                                                                                                                                                                                                                                                                                                       |
| **version**               | Especifica a versão do aplicativo ou do assembly. Use o formato de versão de quatro partes: mmmmm. NNNNN. Ooooo. ppppp. Cada uma das partes separadas por períodos pode ser de 0-65535 inclusive. Para obter mais informações, consulte [versões de assembly](assembly-versions.md). Obrigatórios.                                                                                                                                                                        |
| **publicKeyToken**        | Uma cadeia de caracteres hexadecimal de 16 caracteres que representa os últimos 8 bytes do hash SHA-1 da chave pública sob a qual o aplicativo ou assembly é assinado. A chave pública usada para assinar o catálogo deve ter 2048 bits ou mais. Necessário para todos os assemblies compartilhados lado a lado.                                                                                                                                                     |

<span id="compatibility"></span><span id="COMPATIBILITY"></span>

### <a name="compatibility"></a>compatibilidade

Contém pelo menos um **aplicativo**. Ele não tem atributos. Opcional. Manifestos do aplicativo sem um elemento de compatibilidade padrão para compatibilidade com o Windows Vista no Windows 7.

<span id="application"></span><span id="APPLICATION"></span>

### <a name="application"></a>aplicativo

Contém pelo menos um elemento **supportedOS** . A partir do Windows 10, versão 1903, ele também pode conter um elemento **maxversiontested** opcional. Ele não tem atributos. Opcional.

<span id="supportedOS"></span><span id="supportedos"></span><span id="SUPPORTEDOS"></span>

### <a name="supportedos"></a>supportedOS

O elemento **supportedOS** tem o atributo a seguir. Ele não tem subelementos.

| Atributo | Descrição   |
|-----------|-----------------------|
| **Id**    | Defina o atributo ID como **{e2011457-1546-43c5-a5fe-008deee3d3f0}** para executar o aplicativo usando a funcionalidade do vista. Isso pode permitir que um aplicativo projetado para o Windows Vista seja executado em um sistema operacional posterior. <br/> Defina o atributo ID como **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** para executar o aplicativo usando a funcionalidade do Windows 7.<br/> Os aplicativos que dão suporte à funcionalidade do Windows Vista, do Windows 7 e do Windows 8 não exigem manifestos separados. Nesse caso, adicione os GUIDs para todos os sistemas operacionais Windows.<br/> Para obter informações sobre o comportamento de atributo de **ID** no Windows, consulte o manual de compatibilidade do Windows [8 e do Windows Server 2012](https://www.microsoft.com/download/details.aspx?id=27416).<br/> Os GUIDs a seguir correspondem aos sistemas operacionais Indicados:<br/> **{8e0f7a12-bfb3-4FE8-B9A5-48fd50a15a9a}** -> Windows 10, windows Server 2016 e windows Server 2019<br/> **{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 e Windows Server 2012 R2<br/> **{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 e windows Server 2012<br/> **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 e windows Server 2008 R2<br/> **{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> o Windows Vista e o windows Server 2008<br/> Você pode testar isso no Windows 7 ou no Windows 8. x executando Monitor de Recursos (resmon), acessando a guia CPU, clicando com o botão direito do mouse nos rótulos de coluna, "Selecionar coluna..." e confira "contexto do sistema operacional". No Windows 8. x, você também pode encontrar essa coluna disponível no Gerenciador de tarefas (taskmgr). O conteúdo da coluna mostra o valor mais alto encontrado ou "Windows Vista" como o padrão. <br/> |

<span id="maxVersionTested"></span><span id="maxversiontested"></span><span id="MAXVERSIONTESTED"></span>

### <a name="maxversiontested"></a>maxversiontested

O elemento **maxversiontested** especifica a versão máxima do Windows para a qual o aplicativo foi testado. Isso se destina a ser usado por aplicativos de área de trabalho que usam [ilhas XAML](/windows/apps/desktop/modernize/xaml-islands) e que não são implantados em um pacote MSIX. Esse elemento tem suporte no Windows 10, versão 1903 e versões posteriores.

O elemento **maxversiontested** tem o atributo a seguir. Ele não tem subelementos.

| Atributo | Descrição    |
|-----------|----------------|
| **Id**    | Defina o atributo ID como uma cadeia de caracteres de versão de 4 partes que especifica a versão máxima do Windows para a qual o aplicativo foi testado. Por exemplo, "10.0.18226.0". |

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a>dependência

Contém pelo menos um **dependentAssembly**. Ele não tem atributos. Opcional.

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a>dependentAssembly

O primeiro subelemento de **dependentAssembly** deve ser um elemento **AssemblyIdentity** que descreve um assembly lado a lado exigido pelo aplicativo. Cada **dependentAssembly** deve estar dentro de exatamente uma **dependência**. Ele não tem atributos.

<span id="file"></span><span id="FILE"></span>

### <a name="file"></a>arquivo

Especifica os arquivos que são privados para o aplicativo. Opcional.

O elemento **File** tem os atributos mostrados na tabela a seguir.



| Atributo   | Descrição                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **name**    | Nome do arquivo. Por exemplo, Comctl32.dll.                                                            |
| **hashalg** | Algoritmo usado para criar um hash do arquivo. Esse valor deve ser SHA1.                                 |
| **hash**    | Um hash do arquivo referido pelo nome. Uma cadeia de caracteres hexadecimal de comprimento, dependendo do algoritmo de hash. |

<span id="activeCodePage"></span><span id="activecodepage"></span><span id="ACTIVECODEPAGE"></span>

### <a name="activecodepage"></a>activeCodePage

Force um processo a usar UTF-8 como a página de código do processo.

o **activeCodePage** foi adicionado na versão 1903 do Windows (maio de 2019 atualização). Você pode declarar essa propriedade e o destino/executar em compilações anteriores do Windows, mas você deve manipular a detecção de página de código herdada e a conversão como de costume. Consulte [usar a página de código UTF-8](/windows/uwp/design/globalizing/use-utf8-code-page) para obter detalhes.

Esse elemento não tem atributos. **UTF-8** é apenas um valor válido para o elemento **activeCodePage** .

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

### <a name="autoelevate"></a>Elevação de autoelevação

Especifica se a elevação automática está habilitada. **Verdadeiro** indica que está habilitado. Ele não tem atributos.

<span id="disableTheming"></span><span id="disabletheming"></span><span id="DISABLETHEMING"></span>

### <a name="disabletheming"></a>disableTheming

Especifica se a concessão de elementos da interface do usuário um tema está desabilitado. **Verdadeiro** indica desabilitado. Ele não tem atributos.

<span id="disableWindowFiltering"></span><span id="disablewindowfiltering"></span><span id="DISABLEWINDOWFILTERING"></span>

### <a name="disablewindowfiltering"></a>disableWindowFiltering

Especifica se a filtragem de janela deve ser desabilitada. **Verdadeiro** desabilita a filtragem de janela para que você possa enumerar janelas de imersão da área de trabalho. **disableWindowFiltering** foi adicionado ao Windows 8 e não tem nenhum atributo.

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

Especifica se o processo atual tem reconhecimento de pontos por polegada (DPI).

**Windows 10, versão 1607:** O elemento **dpiAware** será ignorado se o elemento **dpiAwareness** estiver presente. Você pode incluir os dois elementos em um manifesto se quiser especificar um comportamento diferente para o Windows 10, versão 1607 do que para uma versão anterior do sistema operacional.

A tabela a seguir descreve o comportamento que resulta com base na presença do elemento **dpiAware** e no texto que ele contém. O texto dentro do elemento não diferencia maiúsculas de minúsculas.

| Estado do elemento **dpiAware** | Descrição     |
|-----------------------------------|---------|
| Absent                            | O processo atual é DPI sem reconhecimento por padrão. Você pode alterar programaticamente essa configuração chamando a função [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) ou [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .                                                                                                                                                            |
| Contém "true"                   | O processo atual reconhece o DPI do sistema.                                                                                                                                                                                                                                                                                                                                                          |
| Contém "false"                  | **Windows Vista, Windows 7 e Windows 8:** O comportamento é o mesmo que quando o **dpiAware** está ausente.<br/> **Windows 8.1 e Windows 10:** O processo atual é de reconhecimento de dpi e não é possível alterar programaticamente essa configuração chamando a função [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) ou [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .<br/> |
| Contém "true/PM"                | **Windows Vista, Windows 7 e Windows 8:** O processo atual reconhece o DPI do sistema.<br/> **Windows 8.1 e Windows 10:** O processo atual tem reconhecimento de DPI por monitor.<br/>                                                                                                                                                                                                          |
| Contém "por monitor"            | **Windows Vista, Windows 7 e Windows 8:** O comportamento é o mesmo que quando o **dpiAware** está ausente.<br/> **Windows 8.1 e Windows 10:** O processo atual tem reconhecimento de DPI por monitor.<br/>                                                                                                                                                                                      |
| Contém qualquer outra cadeia de caracteres         | **Windows Vista, Windows 7 e Windows 8:** O comportamento é o mesmo que quando o **dpiAware** está ausente.<br/> **Windows 8.1 e Windows 10:** O processo atual é de reconhecimento de dpi e não é possível alterar programaticamente essa configuração chamando a função [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) ou [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .<br/> |

Para obter mais informações sobre configurações de reconhecimento de DPI, consulte [comparação de níveis de reconhecimento de DPI](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).

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

Especifica se o processo atual tem reconhecimento de pontos por polegada (DPI).

A versão mínima do sistema operacional que dá suporte ao elemento **dpiAwareness** é Windows 10, versão 1607. Para versões que dão suporte ao elemento **dpiAwareness** , o **dpiAwareness** substitui o elemento **dpiAware** . Você pode incluir os dois elementos em um manifesto se quiser especificar um comportamento diferente para o Windows 10, versão 1607 do que para uma versão anterior do sistema operacional.

O elemento **dpiAwareness** pode conter um único item ou uma lista de itens separados por vírgula. No último caso, o primeiro item (mais à esquerda) na lista reconhecida pelo sistema operacional é usado. Dessa forma, você pode especificar diferentes comportamentos com suporte em versões futuras do sistema operacional Windows.

A tabela a seguir descreve o comportamento que resulta com base na presença do elemento **dpiAwareness** e no texto que ele contém em seu item reconhecido mais à esquerda. O texto dentro do elemento não diferencia maiúsculas de minúsculas.

| status do elemento **dpiAwareness** :        | Descrição                          |
|-----------------------------------------|-------------------------------------------|
| Elemento ausente                       | O elemento **dpiAware** especifica se o processo tem reconhecimento de DPI.                                                                                                                                                                   |
| Não contém itens reconhecidos            | O processo atual é DPI sem reconhecimento por padrão. Você pode alterar programaticamente essa configuração chamando a função [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) ou [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) . |
| O primeiro item reconhecido é "System"       | O processo atual reconhece o DPI do sistema.                                                                                                                                                                                               |
| O primeiro item reconhecido é "permonitor"   | O processo atual tem reconhecimento de DPI por monitor.                                                                                                                                                                                          |
| O primeiro item reconhecido é "permonitorv2" | O processo atual usa o contexto de reconhecimento de DPI por monitor v2. Este item só será reconhecido no Windows 10 versão 1703 ou posterior.                                                                                              |
| O primeiro item reconhecido é "sem reconhecimento"      | O processo atual não reconhece dpi. Você **não pode** alterar essa configuração programaticamente chamando a função [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) ou [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .      |

Para obter mais informações sobre configurações de reconhecimento de DPI com suporte neste elemento, consulte [ \_ reconhecimento de DPI](/windows/desktop/api/windef/ne-windef-dpi_awareness) e [contexto de \_ reconhecimento \_ de DPI](/windows/desktop/hidpi/dpi-awareness-context).

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

Especifica se o dimensionamento GDI está habilitado. A versão mínima do sistema operacional que dá suporte ao elemento **gdiScaling** é Windows 10 versão 1703.

A estrutura GDI (Graphics Device Interface) pode aplicar o dimensionamento de DPI a primitivos e texto por monitor sem atualizações para o próprio aplicativo. Isso pode ser útil para aplicativos GDI que não estão mais sendo atualizados ativamente.

Elementos gráficos não vetoriais (como bitmaps, ícones ou barras de ferramentas) não podem ser dimensionados por este elemento. Além disso, elementos gráficos e texto que aparecem em bitmaps construídos dinamicamente por aplicativos também não podem ser dimensionados por esse elemento.

**Verdadeiro** indica que esse elemento está habilitado. Ele não tem atributos.


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

Especifica se o reconhecimento da rolagem de alta resolução está habilitado. **Verdadeiro** indica que está habilitado. Ele não tem atributos.

<span id="longPathAware"></span><span id="longpathaware"></span><span id="LONGPATHAWARE"></span>

### <a name="longpathaware"></a>longPathAware

Habilita caminhos longos que excedem **MAX_PATH** de comprimento. Esse elemento tem suporte no Windows 10, versão 1607 e posterior. Para obter mais informações, consulte [este artigo](../fileio/maximum-file-path-limitation.md).

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

Especifica se o isolamento de driver de impressora está habilitado. **Verdadeiro** indica que está habilitado. Ele não tem atributos. O isolamento do driver de impressora melhora a confiabilidade do serviço de impressão do Windows permitindo que os drivers de impressora sejam executados em processos separados do processo no qual o spooler de impressão é executado. Suporte para isolamento de driver de impressora iniciado no Windows 7 e no Windows Server 2008 R2. Um aplicativo pode declarar o isolamento do driver de impressora em seu manifesto de aplicativo para se isolar do driver de impressora e melhorar sua confiabilidade. Ou seja, o aplicativo não falhará se o driver de impressora tiver um erro.


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

Especifica se o reconhecimento de rolagem de resolução extremamente alta está habilitado. **Verdadeiro** indica que está habilitado. Ele não tem atributos.

<span id="msix"></span><span id="MSIX"></span>

### <a name="msix"></a>MSIX

Especifica as informações de identidade de um [pacote MSIX esparso](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) para o aplicativo atual. Esse elemento tem suporte no Windows 10, versão 2004 e versões posteriores.

O elemento **msix** deve estar no namespace `urn:schemas-microsoft-com:msix.v1` . Ele tem os atributos mostrados na tabela a seguir.

| Atributo   | Descrição                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **programa**    | Descreve as informações do Publicador. Esse valor deve corresponder ao atributo **Publisher** no elemento [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) em seu manifesto de pacote esparso. |
| **packageName** | Descreve o conteúdo do pacote. Esse valor deve corresponder ao atributo **Name** no elemento [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) em seu manifesto de pacote esparso.    |
| **applicationId**    | O identificador exclusivo do aplicativo. Esse valor deve corresponder ao atributo **ID** no elemento [Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) em seu manifesto de pacote esparso.  |

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

### <a name="heaptype"></a>heaptype

Substitui a implementação de heap padrão para as [APIs de heap do Win32](../Memory/heap-functions.md) a serem usadas.

* O valor **SegmentHeap** indica que o heap de segmento será usado. O heap de segmento é uma implementação de heap moderna que geralmente reduzirá o uso geral da memória. Esse elemento tem suporte no Windows 10, versão 2004 (Build 19041) e posterior.
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

Veja a seguir um exemplo de um manifesto de aplicativo para um aplicativo chamado MySampleApp.exe. O aplicativo consome o assembly lado a lado do SampleAssembly.

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
