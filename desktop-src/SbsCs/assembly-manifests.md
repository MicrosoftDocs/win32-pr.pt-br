---
description: Um manifesto do assembly é um arquivo XML que descreve um assembly lado a lado.
ms.assetid: f7973019-0a80-498e-adf1-c66267c813f4
title: Manifestos de assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d7c6739bc83e56a42a926ca6aecb739fc41bbf39225cc531afc7afc6706ccc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142509"
---
# <a name="assembly-manifests"></a>Manifestos de assembly

Um manifesto do assembly é um arquivo XML que descreve um assembly lado a lado. Os manifestos do assembly descrevem os nomes e as versões de assemblies, arquivos e recursos lado a lado do assembly, bem como a dependência do assembly em outros assemblies lado a lado. A instalação, a ativação e a execução corretas de assemblies lado a lado exigem que o manifesto do assembly sempre acompanhe um assembly no sistema.

Para obter uma lista completa do esquema XML, consulte [manifest File Schema](manifest-file-schema.md).

Os manifestos de assembly têm os seguintes elementos e atributos.



| Elemento                           | Atributos                | Obrigatório |
|-----------------------------------|---------------------------|----------|
| **)**                      |                           | Sim      |
|                                   | **manifestVersion**       | Sim      |
| **não herdado**                 |                           | Não       |
| **assemblyIdentity**              |                           | Sim      |
|                                   | **tipo**                  | Sim      |
|                                   | **name**                  | Sim      |
|                                   | **linguagem**              | Não       |
|                                   | **processorArchitecture** | Não       |
|                                   | **version**               | Sim      |
|                                   | **publicKeyToken**        | Não       |
| **Estados**                    |                           | Não       |
| **dependentAssembly**             |                           | Não       |
| **file**                          |                           | Não       |
|                                   | **name**                  | Sim      |
|                                   | **hashalg**               | Não       |
|                                   | **hash**                  | Não       |
| **comClass**                      |                           | Não       |
|                                   | **descrição**           | Não       |
|                                   | **CLSID**                 | Sim      |
|                                   | **threadingModel**        | Não       |
|                                   | **tlbid**                 | Não       |
|                                   | **ProgID**                | Não       |
|                                   | **miscStatus**            | Não       |
|                                   | **miscStatusIcon**        | Não       |
|                                   | **miscStatusContent**     | Não       |
|                                   | **miscStatusDocPrint**    | Não       |
|                                   | **miscStatusDocPrint**    | Não       |
| **importação**                       |                           | Não       |
|                                   | **tlbid**                 | Sim      |
|                                   | **version**               | Sim      |
|                                   | **helpdir**               | Sim      |
|                                   | **identificação**            | Não       |
|                                   | **sinalizadores**                 | Não       |
| **comInterfaceExternalProxyStub** |                           | Não       |
|                                   | **IID**                   | Sim      |
|                                   | **baseInterface**         | Não       |
|                                   | **numMethods**            | Não       |
|                                   | **name**                  | Não       |
|                                   | **tlbid**                 | Não       |
|                                   | **proxyStubClsid32**      | Não       |
| **comInterfaceProxyStub**         |                           | Não       |
|                                   | **IID**                   | Sim      |
|                                   | **name**                  | Sim      |
|                                   | **tlbid**                 | Não       |
|                                   | **baseInterface**         | Não       |
|                                   | **numMethods**            | Não       |
|                                   | **proxyStubClsid32**      | Não       |
|                                   | **threadingModel**        | Não       |
| **windowClass**                   |                           | Não       |
|                                   | **versão**             | Não       |



 

## <a name="file-location"></a>Localização do arquivo

Os manifestos de assembly podem ser instalados em três locais:

-   Como manifestos que acompanham [assemblies compartilhados](/windows/desktop/Msi/shared-assemblies), os manifestos de assembly devem ser instalados como um arquivo separado no cache de assembly lado a lado. normalmente, essa é a pasta WinSxS no diretório Windows.
-   Como manifestos que acompanham [assemblies privados](/windows/desktop/Msi/private-assemblies), os manifestos de assembly devem ser instalados na estrutura de diretório do aplicativo. Normalmente, esse é um arquivo separado na mesma pasta que o arquivo executável do aplicativo.
-   Como um recurso em uma DLL, o assembly está disponível para o uso particular da DLL. Um manifesto do assembly não pode ser incluído como um recurso em um EXE. Um arquivo EXE pode incluir um [manifesto do aplicativo](application-manifests.md) como um recurso.

## <a name="file-name-syntax"></a>Sintaxe de nome de arquivo

O nome de um manifesto do assembly é qualquer nome de arquivo válido seguido por. manifest.

Por exemplo, um manifesto do assembly que se refere a myAssembly usaria a seguinte sintaxe de nome de arquivo. Você pode omitir o campo <*ID de recurso*> se o manifesto do assembly estiver sendo instalado como um arquivo separado ou se a ID do recurso for 1.

<dl> myAssembly. <resource ID> . manifesto
</dl>

> [!Note]  
> Por causa da maneira como pesquisas lado a lado para assemblies particulares, as seguintes restrições de nomenclatura se aplicam ao empacotar uma DLL como um assembly privado. Uma maneira recomendada de fazer isso é colocar o manifesto do assembly na DLL como um recurso. Nesse caso, a ID do recurso deve ser igual a 1 e o nome do assembly privado pode ser o mesmo que o nome da DLL. Por exemplo, se o nome da DLL for Microsoft.Windows.mysample.dll, o valor do atributo name usado no elemento **AssemblyIdentity** do manifesto também poderá ser Microsoft. Windows. mysample. Uma maneira alternativa é colocar o manifesto do assembly em um arquivo separado. Nesse caso, o nome do assembly e seu manifesto devem ser diferentes do nome da DLL. Por exemplo, Microsoft. Windows. mysampleAsm, Microsoft. Windows. mysampleAsm. manifest e Microsoft.Windows.Mysample.dll. Para obter mais informações sobre como as pesquisas lado a lado de assemblies particulares, consulte [sequência de pesquisa de assembly](assembly-searching-sequence.md).

 

## <a name="elements"></a>Elementos

Os nomes de elementos e atributos diferenciam maiúsculas de minúsculas. Os valores de elementos e atributos não diferenciam maiúsculas de minúsculas, exceto para o valor do atributo de tipo.

<dl> <dt>

<span id="assembly"></span><span id="ASSEMBLY"></span>**)**
</dt> <dd>

Um elemento de contêiner. Seu primeiro subelemento deve ser um elemento **AssemblyIdentity** ou não **herdável** . O manifesto do assembly descreve exclusivamente o assembly lado a lado identificado pelo **AssemblyIdentity**. Obrigatórios.

O elemento assembly deve estar no namespace "urn: schemas-microsoft-com: asm. v1". Os elementos filho do assembly também devem estar nesse namespace, por herança ou por marcação.

O elemento **assembly** tem o atributo a seguir.



| Atributo           | Descrição                                           |
|---------------------|-------------------------------------------------------|
| **manifestVersion** | O atributo **manifestVersion** deve ser definido como 1,0. |



 

</dd> <dt>

<span id="noInheritable"></span><span id="noinheritable"></span><span id="NOINHERITABLE"></span>**não herdado**
</dt> <dd>

Inclua esse elemento em um manifesto do assembly para indicar que o assembly gerencia os [contextos de ativação](activation-contexts.md) e seus objetos. O elemento **noInheritable** deve ser um subelemento de um elemento de **assembly** . O elemento **AssemblyIdentity** deve vir após qualquer elemento **noInheritable** . O elemento **Noherdável** será necessário no manifesto do assembly se o assembly for usado por qualquer [manifesto do aplicativo](application-manifests.md) que inclua o elemento **NoInherit** . Um elemento não **herdável** em um manifesto de aplicativo não tem efeito. Um elemento não **herdável** não tem nenhum elemento filho.

</dd> <dt>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**assemblyIdentity**
</dt> <dd>

Descreve e identifica exclusivamente um assembly lado a lado.

Como o primeiro subelemento de um elemento de **assembly** , **AssemblyIdentity** descreve e identifica exclusivamente o assembly lado a lado que possui esse manifesto do assembly. Isso é chamado de **AssemblyIdentity** de contexto def do manifesto do assembly.

Como o primeiro subelemento de um elemento **dependentAssembly** , **AssemblyIdentity** descreve e identifica exclusivamente um assembly lado a lado que é usado pelo **AssemblyIdentity** de contexto def. Isso é chamado de **AssemblyIdentity** de contexto de referência do manifesto do assembly. O assembly de contexto DEF requer que o assembly de contexto de referência funcione corretamente. Observe que cada **AssemblyIdentity** de contexto de referência deve corresponder exatamente a um **ASSEMBLYIDENTITY** de contexto def correspondente no manifesto do assembly do assembly referenciado.

Este elemento não tem subelementos. O elemento **AssemblyIdentity** tem os seguintes atributos.



| Atributo                 | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **tipo**                  | Especifica o tipo de assembly. O valor deve ser Win32 e em letras minúsculas. Obrigatórios.                                                                                                                                                                                                                                                                                                                                                         |
| **name**                  | Nomeia exclusivamente o assembly. Use o seguinte formato para o nome do assembly: Organization.Division.Name. Por exemplo, Microsoft. Windows. mysampleAsm. Obrigatórios. Observe que, no caso de uma DLL empacotada como um assembly privado com um arquivo de manifesto separado, o nome do assembly deve ser diferente do nome da DLL e do manifesto.<br/>                                                                              |
| **linguagem**              | Identifica o idioma do assembly. Opcional. Se o assembly for específico a um idioma, especifique o código de linguagem DHTML. No **AssemblyIdentity** de contexto def de um manifesto de assembly destinado para uso mundial (neutro à linguagem), omita o atributo language.<br/> Em um **AssemblyIdentity** de contexto de referência de um manifesto de assembly destinado para uso mundial (neutro à linguagem), defina o valor de idioma como " \* ".<br/> |
| **processorArchitecture** | Especifica o processador. os valores válidos são x86 para 32 bits Windows e ia64 para Windows de 64 bits. Opcional.                                                                                                                                                                                                                                                                                                                               |
| **version**               | Especifica a versão do assembly. Use o formato de versão de quatro partes: mmmmm. NNNNN. Ooooo. ppppp. Cada uma das partes separadas por períodos pode ser de 0-65535 inclusive. Para obter mais informações, consulte [versões de assembly](assembly-versions.md). Obrigatórios.                                                                                                                                                                                               |
| **publicKeyToken**        | Uma cadeia de caracteres hexadecimal de 16 caracteres que representa os últimos 8 bytes do hash SHA-1 da chave pública sob a qual o assembly está assinado. A chave pública usada para assinar o catálogo deve ter 2048 bits ou mais. Necessário para assemblies compartilhados lado a lado.                                                                                                                                                                                |



 

</dd> <dt>

<span id="dependency"></span><span id="DEPENDENCY"></span>**Estados**
</dt> <dd>

Um elemento de contêiner incluindo pelo menos um **dependentAssembly**. O primeiro subelemento deve ser um elemento **dependentAssembly** . Uma **dependência** não tem atributos. Opcional.

</dd> <dt>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**dependentAssembly**
</dt> <dd>

O primeiro subelemento deve ser um elemento **AssemblyIdentity** que descreve e identifica exclusivamente um assembly lado a lado que é usado pelo assembly lado a lado que possui esse manifesto do assembly. Cada **dependentAssembly** deve estar dentro de exatamente uma **dependência**. Opcional.

</dd> <dt>

<span id="file"></span><span id="FILE"></span>**Grupo**
</dt> <dd>

Contém arquivos usados por um assembly lado a lado. Contém os subelementos **ComClass**, **TypeLib**, **WindowClass**, **comInterfaceProxyStub** . Opcional.

O elemento **File** tem os atributos a seguir.



| Atributo   | Descrição                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **name**    | Nome do arquivo, por exemplo, Conctl32.dll.                                                            |
| **hashalg** | Algoritmo usado para criar um hash do arquivo. Esse valor deve ser SHA1.                                 |
| **hash**    | Um hash do arquivo referido pelo nome. Uma cadeia de caracteres hexadecimal de comprimento, dependendo do algoritmo de hash. |



 

</dd> <dt>

<span id="comClass"></span><span id="comclass"></span><span id="COMCLASS"></span>**comClass**
</dt> <dd>

Um subelemento de um elemento **File** . Opcional.

O elemento **ComClass** tem os atributos a seguir.



| Atributo               | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **descrição**         | Nome da classe.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **CLSID**               | O GUID que identifica exclusivamente a classe. Obrigatórios. O valor deve estar no formato de um GUID válido.                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **threadingModel**      | O modelo de Threading usado por classes COM em processo. Se essa propriedade for nula, nenhum modelo de Threading será usado. O componente é criado no thread principal do cliente e as chamadas de outros threads são empacotadas para esse thread. Opcional. Os valores válidos são: "Apartment", "Free", "both" e "neutral".                                                                                                                                                                                                                         |
| **tlbid**               | GUID da biblioteca de tipos para este componente COM. O valor deve estar no formato de um GUID. Opcional.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **ProgID**              | Identificador programático dependente de versão associado ao componente COM. O formato de um ProgID é <> do *fornecedor* . <*componente*>. <*versão*>.                                                                                                                                                                                                                                                                                                                                                                      |
| **miscStatus**          | Duplicatas no manifesto do assembly as informações fornecidas pela chave do registro MiscStatus. Se os valores dos atributos **miscStatusIcon**, **miscStatusContent**, **miscStatusDocprint** ou **miscStatusThumbnail** não forem encontrados, o valor padrão correspondente listado em **MiscStatus** será usado para os atributos ausentes. O valor pode ser uma lista delimitada por vírgula dos valores de atributo da tabela a seguir. Você pode usar esse atributo se a classe COM for uma classe OCX que requer valores de chave do registro MiscStatus. |
| **miscStatusIcon**      | Duplicatas no manifesto do assembly as informações fornecidas pelo ícone do DVASPECT \_ . Ele pode fornecer um ícone de um objeto. O valor pode ser uma lista delimitada por vírgula dos valores de atributo da tabela a seguir. Você pode usar esse atributo se a classe COM for uma classe OCX que requer valores de chave do registro MiscStatus.                                                                                                                                                                                                                |
| **miscStatusContent**   | Duplicatas no manifesto do assembly as informações fornecidas pelo conteúdo do DVASPECT \_ . Ele pode fornecer uma exibição de documento composto para uma tela ou impressora. O valor pode ser uma lista delimitada por vírgula dos valores de atributo da tabela a seguir. Você pode usar esse atributo se a classe COM for uma classe OCX que requer valores de chave do registro MiscStatus.                                                                                                                                                                          |
| **miscStatusDocprint**  | Duplicatas no manifesto do assembly as informações fornecidas por DVASPECT \_ DOCPRINT. Ele pode fornecer uma representação de objeto que possa ser exibida na tela como se fosse impressa em uma impressora. O valor pode ser uma lista delimitada por vírgula dos valores de atributo da tabela a seguir. Você pode usar esse atributo se a classe COM for uma classe OCX que requer valores de chave do registro MiscStatus.                                                                                                                                               |
| **miscStatusThumbnail** | Duplicatas em um manifesto de assembly as informações fornecidas pela \_ miniatura DVASPECT. Ele pode fornecer uma miniatura de um objeto exibível em uma ferramenta de navegação. O valor pode ser uma lista delimitada por vírgula dos valores de atributo da tabela a seguir. Você pode usar esse atributo se a classe COM for uma classe OCX que requer valores de chave do registro MiscStatus.                                                                                                                                                                         |



 

O elemento **ComClass** pode ter elementos <progid>...</progid> como filhos, que listam os PROGIDs dependentes da versão.

O exemplo a seguir mostra um elemento **ComClass** incluído em um elemento **File** .

``` syntax
<file name="sampleu.dll">
        <comClass description="Font Property Page"
    clsid="{0BE35200-8F91-11CE-9DE3-00AA004BB851}"
          threadingModel = "Both"
             tlbid = "{44EC0535-400F-11D0-9DCD-00A0C90391D3}"/>
        <comClass description="Color Property Page"
    clsid="{0BE35201-8F91-11CE-9DE3-00AA004BB851}" 
    progid="ABC.Registrar"/>
    </file>
```

Se sua classe COM é uma classe OCX que requer a subchave do registro MiscStatus para especificar como criar e exibir um objeto, você pode habilitar o objeto duplicando essas informações no manifesto do assembly. Especifique as características do objeto usando os atributos **MiscStatus**, **miscStatusIcon**, **miscStatusContent**, **miscStatusDocprint** e **miscStatusThumbnail** do elemento **ComClass** . Defina esses atributos como uma lista separada por vírgulas de valores de atributo da tabela a seguir. Esses atributos duplicam as informações que seriam fornecidas por uma enumeração DVASPECT. Se nenhum valor for encontrado para **miscStatusIcon**, **miscStatusContent**, **miscStatusDocprint** ou **MiscStatusThumbnail**, os valores padrão especificados em **MiscStatus** serão usados. Use os valores de atributo da tabela a seguir. Elas correspondem aos sinalizadores de bit de uma enumeração [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) .



| Valor do atributo              | Constante OLEMISC                      |
|------------------------------|---------------------------------------|
| recomposeonresize            | OLEMISC \_ RECOMPOSEONRESIZE            |
| onlyiconic                   | OLEMISC \_ ONLYICONIC                   |
| insertnotreplace             | OLEMISC \_ INSERTNOTREPLACE             |
| static                       | OLEMISC \_ estático                       |
| cantlinkinside               | OLEMISC \_ CANTLINKINSIDE               |
| canlinkbyole1                | OLEMISC \_ CANLINKBYOLE1                |
| islinkobject                 | islinkobject do OLEMISC \_                 |
| inverso                    | OLEMISC \_                    |
| activatewhenvisible          | OLEMISC \_ ACTIVATEWHENVISIBLE          |
| renderingisdeviceindependent | RENDERIZAÇÃO \_ OLEMISCISDEVICEINDEPENDENT |
| invisibleatruntime           | OLEMISC \_ INVISIBLEATRUNTIME           |
| alwaysrun                    | OLEMISC \_ ALWAYSRUN                    |
| actslikebutton               | OLEMISC \_ ACTSLIKEBUTTON               |
| actslikelabel                | OLEMISC \_ ACTSLIKELABEL                |
| nouiactivate                 | OLEMISC \_ NOUIACTIVATE                 |
| alinhável                    | OLEMISC \_ ALIGNABLE                    |
| simpleframe                  | OLEMISC \_ SIMPLEFRAME                  |
| setclientsitefirst           | OLEMISC \_ SETCLIENTSITEFIRST           |
| Imemode                      | TOLEMISC \_ IMEMODE                     |
| ignoreativatewhenvisible     | OLEMISC \_ IGNOREACTIVATEWHENVISIBLE    |
| wantstomenumerge             | OLEMISC \_ WANTSTOMENUMERGE             |
| supportsmultilevelundo       | OLEMISC \_ SUPPORTSMULTILEVELUNDO       |



 

</dd> <dt>

<span id="typelib"></span><span id="TYPELIB"></span>**Typelib**
</dt> <dd>

Um subelemento de um **elemento de** arquivo. Opcional.

O **elemento typelib** tem os atributos mostrados na tabela a seguir.



| Atributo      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **tlbid**      | A ID exclusiva da biblioteca de tipos. Obrigatórios.                                                                                                                                                                                                                                                                                                                                                                                    |
| **version**    | O número de versão de duas partes da biblioteca de tipos. Se apenas o número de versão secundária aumentar, todos os recursos da biblioteca de tipos anteriores serão compatíveis. Se o número de versão principal mudar, o código compilado na biblioteca de tipos deverá ser recompilado. O número de versão da biblioteca de tipos pode ser diferente do número de versão do aplicativo. Obrigatórios.                                      |
| **helpdir**    | O diretório em que o arquivo de Ajuda para os tipos na biblioteca de tipos está localizado. Se o aplicativo for compatível com bibliotecas de tipos para vários idiomas, as bibliotecas poderão se referir a nomes de arquivo diferentes no diretório arquivo de Ajuda. Se nenhum valor, especifique "". Obrigatórios.                                                                                                                                                          |
| **Resourceid** | A representação de cadeia de caracteres hexadecimal do LCID (identificador de localidade). São de um a quatro dígitos hexadecimais sem prefixo 0x e sem zeros à esquerda. O LCID pode ter um identificador de sublânguo neutro. Para obter mais informações, consulte [Identificadores de localidade](/windows/desktop/Intl/locale-identifiers). Opcional.                                                                                                                                      |
| **sinalizadores**      | A representação de cadeia de caracteres dos sinalizadores de biblioteca de tipos para essa biblioteca de tipos. Especificamente, ele deve ser um de "RESTRICTED", "CONTROL", "HIDDEN" e "HASDISKIMAGE". Esses são os valores da enumeração [**LIBFLAGS**](/windows/win32/api/oaidl/ne-oaidl-libflags) e são os mesmos sinalizadores especificados no parâmetro *uLibFlags* do [**método ICreateTypeLib::SetLibFlags.**](/windows/win32/api/oaidl/nf-oaidl-icreatetypelib-setlibflags) Opcional. |



 

O exemplo a seguir mostra um **elemento typelib** incluído em um **elemento de** arquivo.

``` syntax
<file name="sampleu.dll">
       <typelib tlbid="{44EC0535-400F-11D0-9DCD-00A0C90391D3}"
       version="1.0" helpdir=""/>
</file>
```

</dd> <dt>

<span id="comInterfaceExternalProxyStub"></span><span id="cominterfaceexternalproxystub"></span><span id="COMINTERFACEEXTERNALPROXYSTUB"></span>**comInterfaceExternalProxyStub**
</dt> <dd>

O **comInterfaceExternalProxyStub** é um subelemento de um elemento **assembly** e é usado para interfaces de automação. Por exemplo, [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) e suas interfaces derivadas. Opcional.

A implementação de proxy-stub padrão é adequada para a maioria das interfaces de automação, como interfaces derivadas de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch). O stub de proxy de interface e todas as outras implementações de interface proxy-stub externos devem estar listados no **comInterfaceExternalProxyStub**. O **elemento comInterfaceExternalProxyStub** tem os atributos mostrados na tabela a seguir.



| Atributo         | Descrição                                                                                                                                                                                 |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Iid**           | O IID da interface para a qual o proxy está sendo declarado. Obrigatórios. O valor deve estar no formato: "{iid}".                                                                         |
| **Baseinterface** | O IID da interface da qual o descrito pelo atributo **iid** é derivado. Esse atributo é opcional. O valor deve estar no formato: "{iid}".                            |
| **numMethods**    | O número de métodos implementados pela interface . Esse atributo é opcional. O valor deve estar no formato: "n".                                                                       |
| **name**          | Nome da interface como ela seria exibida no código. Por exemplo, "IViewObject". Isso não deve ser uma cadeia de caracteres descritiva. Esse atributo é opcional. O valor deve estar no formato: "name". |
| **tlbid**         | A biblioteca de tipos que contém a descrição da interface especificada pelo atributo **iid.** Esse atributo é opcional. O valor deve estar no formato: "{tlbid}".                |
| proxyStubClsid32  | Mapas um IID para um CLSID em DLLs de proxy de 32 bits.                                                                                                                                                |



 

O exemplo a seguir mostra **um elemento comInterfaceExternalProxyStub.**

``` syntax
<comInterfaceExternalProxyStub 
  name="IAxWinAmbientDispatch" 
    iid="{B6EA2051-048A-11D1-82B9-00C04FB9942E}" 
    numMethods="35" 
  baseInterface="{00000000-0000-0000-C000-000000000046}"/>
```

</dd> <dt>

<span id="comInterfaceProxyStub"></span><span id="cominterfaceproxystub"></span><span id="COMINTERFACEPROXYSTUB"></span>**comInterfaceProxyStub**
</dt> <dd>

Um subelemento de um **elemento de** arquivo. Opcional.

Se um arquivo no assembly implementar um stub de proxy, a marca de arquivo correspondente deverá incluir um subelemento **comInterfaceProxyStub** com atributos idênticos a um **elemento comInterfaceProxyStub.** O marshaling de interfaces entre processos e threads pode não funcionar conforme o esperado se você omitir algumas das dependências **comInterfaceProxyStub** para seu componente.

O **elemento comInterfaceProxyStub** tem os seguintes atributos.



| Atributo            | Descrição                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IID**              | Dos. IID da interface para a qual o proxy está sendo declarado. Obrigatórios. O valor deve estar no formato: "{IID}".                                                                                                                                                                                        |
| **name**             | Nome da interface como apareceria no código. Por exemplo, "IViewObject". Essa não deve ser uma cadeia de caracteres descritiva. Esse atributo é opcional. O valor deve estar no formato: "nome".                                                                                                                 |
| **tlbid**            | A biblioteca de tipos que contém a descrição da interface especificada pelo atributo **IID** . Esse atributo é opcional. O valor deve estar no formato: "{TLBID}".                                                                                                                                 |
| **baseInterface**    | O IID da interface da qual o descrito pelo atributo **IID** é derivado. Esse atributo é opcional. O valor deve estar no formato: "{IID}".                                                                                                                                            |
| **numMethods**       | O número de métodos implementados pela interface. Esse atributo é opcional. O valor deve estar no formato: "n".                                                                                                                                                                                       |
| **proxyStubClsid32** | Mapas um IID a um CLSID em DLLs de proxy de 32 bits.                                                                                                                                                                                                                                                                |
| **threadingModel**   | O modelo de Threading usado por classes COM em processo. Se essa propriedade for nula, nenhum modelo de Threading será usado. O componente é criado no thread principal do cliente e as chamadas de outros threads são empacotadas para esse thread. Opcional. Os valores válidos são: "Apartment", "Free", "both" e "neutral". |



 

</dd> <dt>

<span id="windowclass"></span><span id="WINDOWCLASS"></span>**windowclass**
</dt> <dd>

O nome de uma classe do Windows com controle de versão. O elemento **WindowClass** tem o atributo a seguir.



| Atributo     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **versão** | Esse atributo controla se o nome da classe de janela interna usado no registro contém a versão do assembly que contém a classe de janela. O valor desse atributo pode ser "Sim" ou "não". O padrão é "Sim". O valor "no" só deve ser usado se a mesma classe de janela for definida por um componente lado a lado e um componente equivalente não lado a lado e você desejar tratá-los como a mesma classe de janela. Observe que as regras usuais sobre o registro de classe de janela aplicam-se somente ao primeiro componente que registra a classe Window será capaz de registrá-la, já que ela não tem controle de versão. |



 

O exemplo a seguir mostra um elemento **WindowClass** incluído em um elemento **File** .

``` syntax
<file name="comctl32.dll">
        <windowClass versioned="no">ToolbarWindow32</windowClass>
</file>
```

</dd> </dl>

## <a name="example"></a>Exemplo

Veja a seguir um exemplo de um manifesto do assembly.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" 
manifestVersion="1.0">
    <assemblyIdentity type="win32" name="Microsoft.Tools.SampleAssembly" version="6.0.0.0" processorArchitecture="x86" publicKeyToken="0000000000000000"/>
    <file name="sampleu.dll" hash="3eab067f82504bf271ed38112a4ccdf46094eb5a" hashalg="SHA1">
        <comClass description="Font Property Page" clsid="{0BE35200-8F91-11CE-9DE3-00AA004BB851}"/>
        <comClass description="Color Property Page" clsid="{0BE35201-8F91-11CE-9DE3-00AA004BB851}"/>
        <comClass description="Picture Property Page" clsid="{0BE35202-8F91-11CE-9DE3-00AA004BB851}"/>
    </file>
    <file name="bar.dll" hash="ac72753e5bb20446d88a48c8f0aaae769a962338" hashalg="SHA1"/>
    <file name="foo.dll" hash="a7312a1f6cfb46433001e0540458de60adcd5ec5" hashalg="SHA1">
        <comClass description="Registrar Class" clsid="{44EC053A-400F-11D0-9DCD-00A0C90391D3}" progid="ATL.Registrar"/>
    <comInterfaceProxyStub iid="{B6EA2051-048A-11D1-82B9-00C04FB9942E}" name=" IAxWinAmbientDispatch " tlbid="{34EC053A-400F-11D0-9DCD-00A0C90391D3}"/>
        <typelib tlbid="{44EC0535-400F-11D0-9DCD-00A0C90391D3}" version="1.0" helpdir=""/>
    </file>
    <file name="sampledll.dll" hash="ba62960ceb15073d2598379307aad84f3a73dfcb" hashalg="SHA1"/>
<windowClass>ToolbarWindow32</windowClass>
        <windowClass>ComboBoxEx32</windowClass>
        <windowClass>sample_trackbar32</windowClass>
        <windowClass>sample_updown32</windowClass>
</assembly>
```

 

