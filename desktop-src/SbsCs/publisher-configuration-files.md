---
description: Um arquivo de configuração do Publicador é um arquivo XML que redireciona globalmente os aplicativos e assemblies do usando uma versão de um assembly lado a lado para outra versão do mesmo assembly.
ms.assetid: b10752af-80a7-4027-b525-90333d0d010a
title: Arquivos de configuração do Publicador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cc5d7d7b7ffdad3d1179a7f8c66a347d91e0a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829774"
---
# <a name="publisher-configuration-files"></a>Arquivos de configuração do Publicador

Um arquivo de configuração do Publicador é um arquivo XML que redireciona globalmente os aplicativos e assemblies do usando uma versão de um assembly lado a lado para outra versão do mesmo assembly. Normalmente, o editor do assembly emite uma correção de atualização ou de segurança compatível por assembly, emitindo um arquivo de configuração de editor para ser instalado junto com uma atualização de service pack. Isso é conhecido como [configuração do Publicador](publisher-configuration.md). Para obter mais informações sobre esse tipo de [configuração](configuration.md) , consulte configuração do editor.

Os arquivos de configuração do Publicador têm os seguintes elementos e atributos. Para obter uma lista completa do esquema XML, consulte [esquema do arquivo de configuração do Publicador](publisher-configuration-file-schema.md).



| Elemento               | Atributos                | Obrigatório |
|-----------------------|---------------------------|----------|
| **)**          |                           | Yes      |
|                       | **manifestVersion**       | Yes      |
| **assemblyIdentity**  |                           | Yes      |
|                       | **tipo**                  | Sim      |
|                       | **name**                  | Sim      |
|                       | **linguagem**              | No       |
|                       | **processorArchitecture** | No       |
|                       | **version**               | Yes      |
|                       | **publicKeyToken**        | No       |
| **Estados**        |                           | No       |
| **dependentAssembly** |                           | No       |
| **bindingRedirect**   |                           | Yes      |
|                       | **oldVersion**            | Yes      |
|                       | **newVersion**            | Yes      |



 

## <a name="file-location"></a>Local do arquivo

Os arquivos de configuração do Publicador devem ser instalados na pasta WinSxS. Normalmente, eles são instalados como um arquivo separado, mas os arquivos de configuração do Publicador também podem ser incluídos como um recurso em uma DLL. Um arquivo de configuração do Publicador não pode ser incluído como um recurso em um arquivo EXE. Um arquivo EXE pode incluir um [manifesto do aplicativo](application-manifests.md) como um recurso.

## <a name="file-name-syntax"></a>Sintaxe de nome de arquivo

O nome de arquivo de um arquivo de configuração do Publicador tem a *política* de formulário. *principal*. *secundária*. *AssemblyName* onde *Major* e *Minor* referem-se às partes principais e secundárias da [versão do assembly](assembly-versions.md) que está sendo afetada. O *AssemblyName* refere-se ao nome do assembly.

Por exemplo, um arquivo de configuração de Publicador para a versão 6,0 do assembly Microsoft. Windows. Common-Controls teria o seguinte nome:

<dl> Policy. 6.0. Microsoft. Windows. Common – Controls  
</dl>

Não use arquivos de configuração de política para incrementar a versão principal ou secundária de um assembly. Por exemplo, não redirecione a versão 6.0.0.0 para 7.0.0.0 ou 6.1.0.0. Quando um aplicativo faz referência a uma versão de assembly, como 6.0.0.0, o lado a lado verifica a presença de quaisquer arquivos de configuração de política com as versões primárias e secundárias especificadas, por exemplo, 6,0. O aplicativo é então Redirecionado para outra versão do assembly, por exemplo, 6.0.1.0. Se um arquivo de configuração do Publicador incrementar a versão principal ou secundária de um assembly, o redirecionamento subsequente do assembly poderá exigir a emissão de vários arquivos de configuração de política.

## <a name="elements"></a>Elementos

<dl> <dt>

<span id="assembly"></span><span id="ASSEMBLY"></span>**)**
</dt> <dd>

Um elemento de contêiner. Seu primeiro subelemento deve ser um **AssemblyIdentity**. Obrigatórios.

O elemento assembly deve estar no namespace **urn: schemas-microsoft-com: asm. v1**. Os elementos filho do assembly também devem estar nesse namespace, por herança ou por marcação.

O elemento **assembly** tem os atributos a seguir.



| Atributo           | Descrição                                           |
|---------------------|-------------------------------------------------------|
| **manifestVersion** | O atributo **manifestVersion** deve ser definido como 1,0. |



 

</dd> <dt>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**assemblyIdentity**
</dt> <dd>

Descreve e identifica exclusivamente um assembly lado a lado.

Como o primeiro subelemento de um elemento de **assembly** , o **AssemblyIdentity** descreve o assembly lado a lado que está tendo uma ou mais de suas dependências de assembly alteradas. O arquivo de configuração do Publicador redireciona as dependências do assembly identificado. Por exemplo, o **AssemblyIdentity** a seguir indica que o arquivo de configuração do Publicador afeta as dependências do assembly x86 Microsoft. Windows. pop 6.0.0.0.

``` syntax
<assemblyIdentity 
     type="win32-policy" 
     publicKeyToken="0000000000000000" 
     name="policy.6.0.Microsoft.Windows.Pop" 
     version="2.1.0.0" 
     processorArchitecture="x86"/>
```

Como o primeiro subelemento de um elemento **dependentAssembly** , **AssemblyIdentity** descreve uma dependência de assembly lado a lado. O arquivo de configuração do Publicador reconfigura a identidade desse assembly lado a lado necessário. A alteração é especificada em um **bindingRedirect**. Por exemplo, o **AssemblyIdentity** a seguir altera qualquer dependência em Microsoft. Windows. SampleAssembly versão 2.0.0.0 para uma dependência em Microsoft. Windows. SampleAssembly versão 2.0.1.0.

``` syntax
<dependency>
      <dependentAssembly>
         <assemblyIdentity 
type="win32" 
name="Microsoft.Windows.SampleAssembly"  
processorArchitecture="x86"
publicKeyToken="0000000000000000"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
      </dependentAssembly>
</dependency>
```

O elemento **AssemblyIdentity** tem os atributos a seguir. Ele não tem subelementos.



| Atributo                 | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **tipo**                  | Especifica o tipo de assembly. Obrigatórios. No **AssemblyIdentity** para o assembly que está sendo afetado, o valor do atributo **Type** deve ser definido como Win32-Policy. O valor Win32-Policy deve estar em todas as letras minúsculas.<br/> No **AssemblyIdentity** para a dependência de alteração do assembly, o valor do atributo **Type** deve ser definido como Win32. O valor Win32 deve estar em todas as letras minúsculas.<br/>                                                                                                                                                                                                             |
| **name**                  | Nomeia exclusivamente um assembly. Obrigatórios. No **AssemblyIdentity** para o assembly que está sendo afetado, Name tem a *política* de formulário. *principal*. *secundária*. *AssemblyName* em que *Major* e *Minor* se referem às partes principal e secundária da [versão do assembly](assembly-versions.md).<br/> No **AssemblyIdentity** para a dependência de alteração de assembly, Name tem o formato Organization.Division.Name. Por exemplo, Microsoft. Windows. MysampleApp.<br/>                                                                                                                                                                                 |
| **linguagem**              | Identifica o idioma do assembly. Opcional. No **AssemblyIdentity** para o assembly que está sendo afetado, se o assembly for específico a um idioma, especifique o código de linguagem DHTML. Se o assembly for para uso mundial (neutro à linguagem), omita esse atributo.<br/> No **AssemblyIdentity** para a dependência de alteração de assembly, se o assembly for específico de idioma, especifique o código de linguagem DHTML. Se o assembly for para uso mundial (com neutralidade de idioma), defina o valor como " \* ".<br/>                                                                                                                            |
| **processorArchitecture** | Especifica o processador que executa o aplicativo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **version**               | Especifica a versão do assembly. Use a sintaxe de versão de quatro partes: mmmm. nnnn. Oooo. PPPP Necessário somente no **AssemblyIdentity** de contexto def. Não especifique o atributo Version no **AssemblyIdentity** de contexto de referência.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **publicKeyToken**        | Uma cadeia de caracteres hexadecimal de 16 caracteres que representa os últimos 8 bytes do hash SHA-1 da chave pública sob a qual o assembly está assinado. A chave pública usada para assinar o catálogo deve ter 2048 bits ou mais. Um publicKeyToken é necessário para todos os assemblies compartilhados lado a lado. O publicKeyToken usado para o arquivo de configuração do Publicador deve ser a mesma chave usada para o assembly assinado. Os arquivos de configuração do Publicador podem ser assinados usando as mesmas ferramentas usadas com assemblies, consulte [exemplo de assinatura de assembly](assembly-signing-example.md) e [criando arquivos e catálogos assinados](creating-signed-files-and-catalogs.md). |



 

</dd> <dt>

<span id="dependency"></span><span id="DEPENDENCY"></span>**Estados**
</dt> <dd>

Um elemento de contêiner opcional para pelo menos um **dependentAssembly**. Ele não tem atributos.

</dd> <dt>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**dependentAssembly**
</dt> <dd>

Cada **dependentAssembly** deve estar dentro de exatamente uma **dependência**. Um **dependentAssembly** não tem atributos. O primeiro subelemento de **dependentAssembly** deve ser um **AssemblyIdentity** para o assembly lado a lado que está sendo reconfigurado pela configuração do Publicador.

</dd> <dt>

<span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>**bindingRedirect**
</dt> <dd>

O elemento **bindingRedirect** contém informações de redirecionamento para a associação do assembly.

Esse elemento tem os atributos mostrados na tabela a seguir.



| Atributo      | Descrição                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **oldVersion** | Especifica a versão do assembly que está sendo substituída e redirecionada. Use a sintaxe de versão de quatro partes nnnnn. NNNNN. NNNNN. NNNNN. Especifique um intervalo de versões por um traço sem espaços. Por exemplo, 2.14.3.0 ou 2.14.3.0 2.16.0.0. Obrigatórios. |
| **newVersion** | Especifica a versão do assembly de substituição. Use a sintaxe de versão de quatro partes nnnnn. NNNNN. NNNNN. NNNNN.                                                                                                                                     |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Os arquivos de configuração do Publicador não especificam arquivos. Observe que os arquivos de política específicos do idioma são separados do arquivo de configuração do Publicador.

## <a name="example"></a>Exemplo

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.6.0.Proseware.Research.SampleAssembly" version="1.0.1.0" language="en-us" processorArchitecture="x86"/>
<dependency>
<dependentAssembly>
<assemblyIdentity type="win32" publicKeyToken="0000000000000000" name="Proseware.Research.SampleAssembly" language="en-us" processorArchitecture="x86"/>
<bindingRedirect oldVersion="1.0.0.0" newVersion="1.0.1.0"/>
</dependentAssembly>
</dependency>
</assembly>
```

 

 




