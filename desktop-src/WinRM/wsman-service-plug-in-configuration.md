---
title: Configuração de plug-in do serviço WinRM
description: Um plug-in winRM (gerenciamento remoto) do Windows deve ser registrado no catálogo do WinRM para permitir que a infraestrutura determine dinamicamente o conjunto de plug-ins disponíveis e os URIs de recurso aos quais eles são suportados.
ms.assetid: d71cd244-3f10-40e3-a756-36cdf41b9cad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b82b24b8631cd6a47a879a6fa0684b9b2ac9c542699396d0f0997afe14cac8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323714"
---
# <a name="winrm-service-plug-in-configuration"></a>Configuração de plug-in do serviço WinRM

Um plug-in winRM (gerenciamento remoto) do Windows deve ser registrado no catálogo do WinRM para permitir que a infraestrutura determine dinamicamente o conjunto de plug-ins disponíveis e os [*URIs*](windows-remote-management-glossary.md) de recurso aos quais eles são suportados. Todos [*os URIs de*](windows-remote-management-glossary.md) recurso para plug-ins winRM devem estar em conformidade com o formato definido no RFC 3986 ( [https://www.ietf.org/rfc/rfc3986.txt](https://www.ietf.org/rfc/rfc3986.txt) ). A configuração é feita por meio do serviço WinRM principal.

O comando a seguir registra uma configuração de plug-in com o serviço WinRM:

```console
winrm create http://schemas.microsoft.com/wbem/wsman/1/config/plugin?name=MyPlugIn -file:myplugin.xml
```

> [!NOTE]
> O serviço WinRM precisa ser reiniciado para expor os plug-ins recém-registrados.

A configuração de plug-in é especificada em XML. A seguir, é mostrado um exemplo.

```XML
<PlugInConfiguration xmlns="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
                     Name="MyPlugIn"
                     Filename="%systemroot%\system32\myplugin.dll" 
                     SDKVersion="1"
                     XmlRenderingType="text"
                     Architecture="64"
                     Enabled="true">

 <InitializationParameters>
  <Param Name="myParam1" Value="myValue1"/>
  <Param Name="myParam2" Value="myValue2"/>
 </InitializationParameters>

 <Resources>
  <Resource ResourceUri="https://schemas.MyCompany.com/MyUri1" SupportsOptions="true" ExactMatch="false">
   <Capability Type="Get" SupportsFragment="true"/>
   <Capability Type="Put" SupportsFragment="true"/>
   <Capability Type="Create"/>
   <Capability Type="Delete"/>
   <Capability Type="Invoke"/>
   <Capability Type="Enumerate" SupportsFiltering="true"/>
  </Resource>

  <Resource ResourceUri="https://schemas.MyCompany.com/MyUri2" SupportsOptions="false" ExactMatch="true">
   <Security Uri="https://schemas.MyCompany.com/MyUri2" Sddl="O:NSG:BAD:P(A;;GA;;;BA)"/>
   <Security Uri="https://schemas.MyCompany.com/MyUri2/MoreSpecific" Sddl="O:NSG:BAD:P(A;;GR;;;BA)" ExactMatch="true"/>
   <Capability Type="Shell"/>
  </Resource>
 </Resources>
</PlugInConfiguration>
```



A lista a seguir descreve os elementos XML mais detalhadamente e é seguida pelo esquema de configuração especificado como um XSD.

<dl> <dt>

<span id="PlugInConfiguration_OperationsConfiguration"></span><span id="pluginconfiguration_operationsconfiguration"></span><span id="PLUGINCONFIGURATION_OPERATIONSCONFIGURATION"></span>**PlugInConfiguration** / **OperationsConfiguration**
</dt> <dd>

Especifica o nome do arquivo do plug-in de operações. Todas as variáveis de ambiente que são colocadas nessa entrada serão expandidas no contexto dos usuários quando uma solicitação entrar. Cada usuário pode ter uma versão diferente da mesma variável de ambiente, para que cada usuário possa acabar com um plug-in diferente. Essa entrada não pode estar em branco e deve apontar para um plug-in válido.

</dd> <dt>

<span id="PlugInConfiguration_Name"></span><span id="pluginconfiguration_name"></span><span id="PLUGINCONFIGURATION_NAME"></span>**PlugInConfiguration** / **Nome**
</dt> <dd>

Especifica o nome de exibição a ser usado para o plug-in. Se um erro for retornado do plug-in, esse nome será colocado no XML de erro retornado ao aplicativo cliente. O nome não é específico da localidade.

</dd> <dt>

<span id="PlugInConfiguration_Architecture"></span><span id="pluginconfiguration_architecture"></span><span id="PLUGINCONFIGURATION_ARCHITECTURE"></span>**PlugInConfiguration** / **Arquitetura**
</dt> <dd>

Especifica se o plug-in de operações é de 32 bits ou 64 bits. Se esse elemento não for especificado, o valor será padrão para "32" em sistemas x86 e para "64" em sistemas de 64 bits. Para sistemas x86, o único valor válido é "32". Se o valor for "32" em um sistema de 64 bits, o redirecionamento wow64 precisará ser levado em conta ao inserir as informações **de Nome de** arquivo. O sistema de arquivos subjacente usará o redirecionamento wow64 para converter o sistema32 em syswow64. Por exemplo, se **Filename** for \\ "%windir% system32myplugin.dll" e Architecture for "32", o arquivo de plug-in real será localizado em \\  "%windir% \\ syswow64 \\myplugin.dll".

</dd> <dt>

<span id="PlugInConfiguration_XmlRenderingType"></span><span id="pluginconfiguration_xmlrenderingtype"></span><span id="PLUGINCONFIGURATION_XMLRENDERINGTYPE"></span>**PlugInConfiguration** / **XmlRenderingType**
</dt> <dd>

Configura o formato no qual XML é passado para plug-ins por meio do [**objeto WSMAN \_ DATA.**](/windows/desktop/api/Wsman/ns-wsman-wsman_data) Os seguintes tipos estão disponíveis:

<dl> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Texto
</dt> <dd>

Os dados XML de entrada estão contidos em uma estrutura TEXT de TIPO DE DADOS WSMAN, que representa o \_ XML como um buffer de memória \_ \_ **PCWSTR.**

</dd> <dt>

<span id="XMLReader"></span><span id="xmlreader"></span><span id="XMLREADER"></span>Xmlreader
</dt> <dd>

Os dados XML de entrada estão contidos em uma estrutura WSMAN DATA TYPE WS XML READER, que representa o XML como um objeto XmlReader, que é definido no arquivo de título \_ \_ \_ \_ \_ WebServices.h. 

</dd> </dl> </dd> <dt>

<span id="PlugInConfiguration_InitializationXml"></span><span id="pluginconfiguration_initializationxml"></span><span id="PLUGINCONFIGURATION_INITIALIZATIONXML"></span>**PlugInConfiguration** / **InitializationXml**
</dt> <dd>

Esse nó é opcional e permite que um plug-in configure XML extra que será passado para o [**método WSManPluginStartup.**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup) A maioria dos plug-ins não precisará dessa informação extra, mas se um plug-in precisar ser usado em mais de um cenário que exija semântica de tempo de run time diferente, esse XML dará ao plug-in a flexibilidade para fazer isso.

</dd> <dt>

<span id="PlugInConfiguration_Resources"></span><span id="pluginconfiguration_resources"></span><span id="PLUGINCONFIGURATION_RESOURCES"></span>**PlugInConfiguration** / **Recursos**
</dt> <dd>

Especifica uma lista de [*URIs de recurso compatíveis*](windows-remote-management-glossary.md)com esse plug-in. Pelo menos uma **entrada ResourceUri** deve ser especificada; caso contrário, o XML será rejeitado.

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource"></span><span id="pluginconfiguration_resources_resource"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE"></span>**PlugInConfiguration** / **Recursos** / **Recurso**
</dt> <dd>

Representa uma configuração [*de URI de recurso*](windows-remote-management-glossary.md)único.

> [!Note]  
> O **atributo SupportsOptions** pode ser definido como false. Se **SupportsOptions for** definido como false, esse atributo não será listado quando o recurso for enumerado.

 

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_ResourceUri"></span><span id="pluginconfiguration_resources_resource_resourceuri"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_RESOURCEURI"></span>**PlugInConfiguration** / **Recursos** / **Recurso** / **ResourceUri**
</dt> <dd>

Especifica um único [*URI de recurso*](windows-remote-management-glossary.md) completo ou como uma cadeia de caracteres de combinação parcial com base no **atributo ExactMatch.** Se **ExactMatch** não estiver presente, o padrão será **False,** o que significa que o processador SOAP do WinRM fará uma corresponder parcial ao início do *URI* do recurso e, se houver uma combinação, passe-o para o plug-in. O **atributo SupportsOptions** poderá ser especificado se esse *URI* de recurso tiver permissão para ter todas as opções passadas. Por padrão, não há suporte para opções e, se alguma estiver presente na solicitação do cliente, um erro será retornado. Se as opções são suportadas pelo plug-in, é importante que o plug-in retorne o erro correto se uma opção estiver presente que o plug-in não entenda quando o sinalizador **mustUnderstand** está definido como **True.**

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_Capability"></span><span id="pluginconfiguration_resources_resource_capability"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_CAPABILITY"></span>**PlugInConfiguration** / **Recursos** / **Recurso** / **Funcionalidade**
</dt> <dd>

Especifica uma funcionalidade que está disponível neste [*URI de recurso.*](windows-remote-management-glossary.md) Haverá uma entrada para cada tipo de operação compatível. As seguintes opções estão disponíveis:

<dl> <dt>

<span id="Get"></span><span id="get"></span><span id="GET"></span>Obter
</dt> <dd>

Há suporte para operações Get no [*URI do recurso.*](windows-remote-management-glossary.md) O **atributo SupportFragment** será usado se a operação get for compatível com o conceito. O **atributo SupportFiltering** não é válido e deve ser definido como false. Essa funcionalidade não será válida para um *URI de* recurso se também há suporte para operações de shell.

</dd> <dt>

<span id="Put"></span><span id="put"></span><span id="PUT"></span>Colocar
</dt> <dd>

Há suporte para operações put no [*URI do recurso.*](windows-remote-management-glossary.md) O **atributo SupportFragment** será usado se a operação put for compatível com o conceito . O **atributo SupportFiltering** não é válido e deve ser definido como **False.** Essa funcionalidade não será válida para um *URI de* recurso se também há suporte para operações de shell.

</dd> <dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>Criar
</dt> <dd>

Há suporte para operações de criação no [*URI do recurso.*](windows-remote-management-glossary.md) O **atributo SupportFragment** será usado se a operação de criação for compatível com o conceito. O **atributo SupportFiltering** não é válido e deve ser definido como **False.** Essa funcionalidade não será válida para um *URI de* recurso se também há suporte para operações de shell.

</dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>Excluir
</dt> <dd>

Há suporte para operações de exclusão no [*URI do recurso.*](windows-remote-management-glossary.md) O **atributo SupportFragment** será usado se a operação de exclusão for compatível com o conceito. O **atributo SupportFiltering** não é válido e deve ser definido como **False.** Essa funcionalidade não será válida para um *URI de* recurso se também há suporte para operações de shell.

</dd> <dt>

<span id="Invoke"></span><span id="invoke"></span><span id="INVOKE"></span>Invocar
</dt> <dd>

Há suporte para operações de invocação no [*URI do recurso.*](windows-remote-management-glossary.md) O **atributo SupportFragment** não tem suporte para operações de invocação e deve ser definido como false. O **atributo SupportFiltering** não é válido e deve ser definido como **False.** Essa funcionalidade não será válida para um *URI de* recurso se também há suporte para operações de shell.

</dd> <dt>

<span id="Enumerate"></span><span id="enumerate"></span><span id="ENUMERATE"></span>Enumerar
</dt> <dd>

Há suporte para operações de enumeração no [*URI do recurso.*](windows-remote-management-glossary.md) O **atributo SupportFragment** não tem suporte para operações de enumeração e deve ser definido como **False.** O **atributo SupportFiltering** é válido e, se o plug-in dá suporte à filtragem, esse atributo deve ser definido como **True.** Essa funcionalidade não será válida para um *URI de* recurso se também há suporte para operações de shell.

</dd> <dt>

<span id="Subscribe"></span><span id="subscribe"></span><span id="SUBSCRIBE"></span>Assinar
</dt> <dd>

Há suporte para operações de assinatura no [*URI do recurso.*](windows-remote-management-glossary.md) O **atributo SupportFragment** não tem suporte para operações de assinatura e deve ser definido como **False.** O **atributo SupportFiltering** não é válido e deve ser definido como **False.** Essa funcionalidade não será válida para um *URI de* recurso se também há suporte para operações de shell.

</dd> <dt>

<span id="Shell"></span><span id="shell"></span><span id="SHELL"></span>Shell
</dt> <dd>

Há suporte para operações de shell no [*URI do recurso.*](windows-remote-management-glossary.md) O **atributo SupportFragment** não tem suporte para operações de shell e deve ser definido como **False.** O **atributo SupportFiltering** não é válido e deve ser definido como **False.** Essa funcionalidade não será válida para um *URI de* recurso se qualquer outra funcionalidade de operação também tiver suporte. Se uma funcionalidade de operação de shell estiver configurada para um *URI* de recurso, as operações get, put, create, delete, invoke e enumerar serão processadas internamente dentro do serviço WinRm para gerenciar shells. Como resultado, o plug-in não pode lidar com as operações em si.

</dd> </dl> </dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_Security"></span><span id="pluginconfiguration_resources_resource_security"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_SECURITY"></span>**PlugInConfiguration** / **Recursos** / **Recurso** / **Segurança**
</dt> <dd>

Esse elemento define o descritor de segurança (por meio do atributo **Sddl)** que deve ser aplicado para determinar o acesso a um [*URI*](windows-remote-management-glossary.md) de recurso específico (por meio do **atributo URI).** Se **ExactMatch** não estiver presente, o elemento **Security** assume False como **padrão,** o que significa que o **Sddl** se aplica a todos os *URIs* de recurso que compartilham **URI** como um prefixo. Se **ExactMatch** for definido como true, o **Sddl** se aplicará somente ao **URI** exato especificado. Se houver várias **entradas de** segurança que podem ser aplicadas a um recurso *específico URIs*, a combinação de prefixo mais longo será usada para determinar o **Sddl apropriado.** Como resultado da combinação de prefixo mais longo, se existir uma entrada **de URI** de combinação exata, ela sempre será escolhida como o elemento security apropriado.

</dd> </dl>

A seguir está o esquema de configuração de plug-in especificado como um XSD.

``` syntax
<?xml version="1.0" encoding="utf-8"?>
<xs:schema attributeFormDefault="unqualified" 
           elementFormDefault="qualified" 
           targetNamespace="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
           xmlns="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
           xmlns:xs="https://www.w3.org/2001/XMLSchema">
 <xs:element name="PlugInConfiguration">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="InitializationParameters" minOccurs="0" maxOccurs="1">
     <xs:complexType>
      <xs:sequence>
       <xs:element name="Param">
        <xs:complexType>
         <xs:sequence></xs:sequence>
         <xs:attribute name="Name" type="xs:string"/>
         <xs:attribute name="Value" type="xs:string"/>
        </xs:complexType>
       </xs:element>
      </xs:sequence>
     </xs:complexType>
    </xs:element>
    <xs:element name="Resources">
     <xs:complexType>
      <xs:sequence>
       <xs:element minOccurs="1" maxOccurs="unbounded" name="Resource">
        <xs:complexType>
         <xs:sequence>
          <xs:element name="Capability" minOccurs="1" maxOccurs="unbounded">
           <xs:complexType>
            <xs:simpleContent>
             <xs:extension base="ResourceCapabilityType">
              <xs:attribute name="SupportsFragment" type="xs:boolean" use="optional" default="false"/>
              <xs:attribute name="SupportsFiltering" type="xs:boolean" use="optional" default="false"/>
              <xs:attribute name="Type" type="ResourceCapabilityType"/>
             </xs:extension>
            </xs:simpleContent>
           </xs:complexType>
          </xs:element>
          <xs:element name="Security" minOccurs="0" maxOccurs="unbounded">
           <xs:complexType>
            <xs:sequence></xs:sequence>
            <xs:attribute name="Uri" type="xs:string"/>
            <xs:attribute name="Sddl" type="xs:string"/>
            <xs:attribute name="ExactMatch" type="xs:boolean" use="optional" default="false"/>
           </xs:complexType>
          </xs:element>
         </xs:sequence>
         <xs:attribute name="ResourceUri" type="xs:string"/>
         <xs:attribute name="ExactMatch" type="xs:boolean" use="optional" default="false"/>
         <xs:attribute name="SupportOptions" type="xs:boolean" use="optional" default="false"/>
        </xs:complexType>
       </xs:element>
      </xs:sequence>
     </xs:complexType>
    </xs:element>
   </xs:sequence>
   <xs:attribute name="Filename" type="xs:token"/>
   <xs:attribute name="SDKVersion" type="xs:unsignedInt"/>
   <xs:attribute name="Name" type="xs:string"/>
   <xs:attribute name="XmlRenderingType" type="XmlRenderingTypeType" use="optional" default="text"/>
   <!--Architecture will default to 32 on x86 systems; 64 on 64-bit systems.-->
   <xs:attribute name="Architecture" type="ArchitectureType" use="optional" default="32"/>
  </xs:complexType>
 </xs:element>
 <xs:simpleType name="ResourceCapabilityType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="Get"/>
   <xs:enumeration value="Put"/>
   <xs:enumeration value="Create"/>
   <xs:enumeration value="Delete"/>
   <xs:enumeration value="Invoke"/>
   <xs:enumeration value="Enumerate"/>
   <xs:enumeration value="Subscribe"/>
   <xs:enumeration value="Shell"/>
  </xs:restriction>
 </xs:simpleType>
 <xs:simpleType name="XmlRenderingTypeType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="text"/>
   <xs:enumeration value="XmlReader"/>
  </xs:restriction>
 </xs:simpleType>
 <xs:simpleType name="ArchitectureType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="32"/>
   <xs:enumeration value="64"/>
  </xs:restriction>
 </xs:simpleType>
</xs:schema>
```

 

 




