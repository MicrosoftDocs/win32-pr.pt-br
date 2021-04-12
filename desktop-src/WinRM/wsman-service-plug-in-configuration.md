---
title: Configuração de plug-in do serviço WinRM
description: Um plug-in Gerenciamento Remoto do Windows (WinRM) deve ser registrado no catálogo do WinRM para permitir que a infraestrutura determine dinamicamente o conjunto de plug-ins disponíveis e os URIs de recursos aos quais eles dão suporte.
ms.assetid: d71cd244-3f10-40e3-a756-36cdf41b9cad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60bf618d71e55c6afd28de918198725895088559
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104294593"
---
# <a name="winrm-service-plug-in-configuration"></a>Configuração de plug-in do serviço WinRM

Um plug-in Gerenciamento Remoto do Windows (WinRM) deve ser registrado no catálogo do WinRM para permitir que a infraestrutura determine dinamicamente o conjunto de plug-ins disponíveis e os [*URIs de recursos*](windows-remote-management-glossary.md) aos quais eles dão suporte. Todos os [*URIs de recurso*](windows-remote-management-glossary.md) para plug-ins WinRM devem estar em conformidade com o formato definido no RFC 3986 ( [https://www.ietf.org/rfc/rfc3986.txt](https://www.ietf.org/rfc/rfc3986.txt) ). A configuração é feita por meio do serviço WinRM principal.

O comando a seguir registra uma configuração de plug-in com o serviço WinRM:

```console
winrm create http://schemas.microsoft.com/wbem/wsman/1/config/plugin?name=MyPlugIn -file:myplugin.xml
```

> [!NOTE]
> O serviço WinRM precisa ser reiniciado para expor os plug-ins registrados recentemente.

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



A lista a seguir descreve os elementos XML em mais detalhes e é seguida pelo esquema de configuração especificado como um XSD.

<dl> <dt>

<span id="PlugInConfiguration_OperationsConfiguration"></span><span id="pluginconfiguration_operationsconfiguration"></span><span id="PLUGINCONFIGURATION_OPERATIONSCONFIGURATION"></span>**PlugInConfiguration** / **OperationsConfiguration**
</dt> <dd>

Especifica o nome do arquivo do plug-in de operações. Todas as variáveis de ambiente colocadas nessa entrada serão expandidas no contexto dos usuários quando uma solicitação chegar. Cada usuário pode ter uma versão diferente da mesma variável de ambiente, de modo que cada usuário poderia acabar com um plug-in diferente. Essa entrada não pode ficar em branco e deve apontar para um plug-in válido.

</dd> <dt>

<span id="PlugInConfiguration_Name"></span><span id="pluginconfiguration_name"></span><span id="PLUGINCONFIGURATION_NAME"></span>**PlugInConfiguration** / **Nome** do
</dt> <dd>

Especifica o nome de exibição a ser usado para o plug-in. Se um erro for retornado do plug-in, esse nome será colocado no XML de erro que é retornado para o aplicativo cliente. O nome não é específico da localidade.

</dd> <dt>

<span id="PlugInConfiguration_Architecture"></span><span id="pluginconfiguration_architecture"></span><span id="PLUGINCONFIGURATION_ARCHITECTURE"></span>**PlugInConfiguration** / **Arquitetura** do
</dt> <dd>

Especifica se o plug-in de operações é de 32 bits ou 64 bits. Se esse elemento não for especificado, o valor padrão será "32" em sistemas x86 e "64" nos sistemas de 64 bits. Para sistemas x86, o único valor válido é "32". Se o valor for "32" em um sistema de 64 bits, o redirecionamento do WOW64 precisará ser levado em conta ao inserir as informações de **nome de arquivo** . O sistema de arquivos subjacente usará o redirecionamento de WOW64 para converter system32 em SysWOW64. Por exemplo, se **filename** for "% windir% \\ System32 \\myplugin.dll" e a **arquitetura** for "32", o arquivo de plug-in real estará localizado em "% windir% \\ SysWOW64 \\myplugin.dll".

</dd> <dt>

<span id="PlugInConfiguration_XmlRenderingType"></span><span id="pluginconfiguration_xmlrenderingtype"></span><span id="PLUGINCONFIGURATION_XMLRENDERINGTYPE"></span>**PlugInConfiguration** / **Xmlrenderizatype**
</dt> <dd>

Configura o formato em que o XML é passado para plug-ins por meio do objeto de [**\_ dados WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_data) . Os seguintes tipos estão disponíveis:

<dl> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Texto
</dt> <dd>

Os dados XML de entrada estão contidos em uma \_ estrutura de texto de tipo de dados WSMan \_ \_ , que representa o XML como um buffer de memória **PCWSTR** .

</dd> <dt>

<span id="XMLReader"></span><span id="xmlreader"></span><span id="XMLREADER"></span>XMLReader
</dt> <dd>

Os dados XML de entrada estão contidos em \_ uma \_ estrutura de leitor XML do WS tipo de dados \_ do WSMan \_ \_ , que representa o XML como um objeto **XmlReader** , que é definido no arquivo de cabeçalho WebServices. h.

</dd> </dl> </dd> <dt>

<span id="PlugInConfiguration_InitializationXml"></span><span id="pluginconfiguration_initializationxml"></span><span id="PLUGINCONFIGURATION_INITIALIZATIONXML"></span>**PlugInConfiguration** / **InitializationXml**
</dt> <dd>

Esse nó é opcional e permite que um plug-in configure o XML extra que será passado para o método [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup). A maioria dos plug-ins não precisará dessas informações adicionais, mas se um plug-in precisar ser usado em mais de um cenário que requer semântica de tempo de execução diferente, esse XML dará ao plug-in a flexibilidade para fazer isso.

</dd> <dt>

<span id="PlugInConfiguration_Resources"></span><span id="pluginconfiguration_resources"></span><span id="PLUGINCONFIGURATION_RESOURCES"></span>**PlugInConfiguration** / **Recursos** do
</dt> <dd>

Especifica uma lista de [*URIs de recursos*](windows-remote-management-glossary.md)aos quais esse plug-in dá suporte. Pelo menos uma entrada **ResourceURI** deve ser especificada; caso contrário, o XML será rejeitado.

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource"></span><span id="pluginconfiguration_resources_resource"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE"></span>**PlugInConfiguration** / **Recursos** / do **Recurso** do
</dt> <dd>

Representa uma configuração de [*URI de recurso*](windows-remote-management-glossary.md)único.

> [!Note]  
> O atributo de **suporteoptions** pode ser definido como false. Se o **suporteoptions** for definido como false, esse atributo não será listado quando o recurso for enumerado.

 

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_ResourceUri"></span><span id="pluginconfiguration_resources_resource_resourceuri"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_RESOURCEURI"></span>**PlugInConfiguration** / **Recursos** / do **Recurso** / do **ResourceURI**
</dt> <dd>

Especifica um único [*URI de recurso*](windows-remote-management-glossary.md) em completo ou como uma cadeia de caracteres de correspondência parcial com base no atributo **ExactMatch** . Se **ExactMatch** não estiver presente, o padrão será **false**, o que significa que o processador SOAP do WinRM fará uma correspondência parcial com o início do *URI do recurso* e, se houver uma correspondência, passá-lo para o plug-in. O atributo de **suporteoptions** poderá ser especificado se esse *URI de recurso* tiver permissão para ter qualquer opção passada. Por padrão, não há suporte para nenhuma opção e, se houver alguma presente na solicitação do cliente, será retornado um erro. Se houver suporte para as opções do plug-in, é importante que o plug-in retorne o erro correto se uma opção estiver presente de que o plug-in não entende quando o sinalizador **MustUnderstand** está definido como **true**.

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_Capability"></span><span id="pluginconfiguration_resources_resource_capability"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_CAPABILITY"></span>**PlugInConfiguration** / **Recursos** / do **Recurso** / do **Funcionalidade** do
</dt> <dd>

Especifica um recurso que está disponível neste [*URI de recurso*](windows-remote-management-glossary.md). Haverá uma entrada para cada tipo de operação que ele suporta. As seguintes opções estão disponíveis:

<dl> <dt>

<span id="Get"></span><span id="get"></span><span id="GET"></span>Obter
</dt> <dd>

Há suporte para operações Get no [*URI do recurso*](windows-remote-management-glossary.md). O atributo **SupportFragment** será usado se a operação get der suporte ao conceito. O atributo **SupportFiltering** não é válido e deve ser definido como false. Esse recurso não será válido para um *URI de recurso* se também houver suporte para operações de Shell.

</dd> <dt>

<span id="Put"></span><span id="put"></span><span id="PUT"></span>Posicione
</dt> <dd>

As operações Put têm suporte no [*URI de recurso*](windows-remote-management-glossary.md). O atributo **SupportFragment** será usado se a operação Put der suporte ao conceito. O atributo **SupportFiltering** não é válido e deve ser definido como **false**. Esse recurso não será válido para um *URI de recurso* se também houver suporte para operações de Shell.

</dd> <dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>Criada
</dt> <dd>

Há suporte para operações de criação no [*URI de recurso*](windows-remote-management-glossary.md). O atributo **SupportFragment** será usado se a operação de criação der suporte ao conceito. O atributo **SupportFiltering** não é válido e deve ser definido como **false**. Esse recurso não será válido para um *URI de recurso* se também houver suporte para operações de Shell.

</dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>Apagar
</dt> <dd>

As operações de exclusão têm suporte no [*URI de recurso*](windows-remote-management-glossary.md). O atributo **SupportFragment** será usado se a operação de exclusão der suporte ao conceito. O atributo **SupportFiltering** não é válido e deve ser definido como **false**. Esse recurso não será válido para um *URI de recurso* se também houver suporte para operações de Shell.

</dd> <dt>

<span id="Invoke"></span><span id="invoke"></span><span id="INVOKE"></span>Chame
</dt> <dd>

As operações Invoke têm suporte no [*URI de recurso*](windows-remote-management-glossary.md). O atributo **SupportFragment** não tem suporte para operações Invoke e deve ser definido como false. O atributo **SupportFiltering** não é válido e deve ser definido como **false**. Esse recurso não será válido para um *URI de recurso* se também houver suporte para operações de Shell.

</dd> <dt>

<span id="Enumerate"></span><span id="enumerate"></span><span id="ENUMERATE"></span>Enumera
</dt> <dd>

As operações de enumeração têm suporte no [*URI de recurso*](windows-remote-management-glossary.md). O atributo **SupportFragment** não tem suporte para operações de enumeração e deve ser definido como **false**. O atributo **SupportFiltering** é válido e, se o plug-in der suporte à filtragem, esse atributo deverá ser definido como **true**. Esse recurso não será válido para um *URI de recurso* se também houver suporte para operações de Shell.

</dd> <dt>

<span id="Subscribe"></span><span id="subscribe"></span><span id="SUBSCRIBE"></span>Faça
</dt> <dd>

As operações de assinatura têm suporte no [*URI de recurso*](windows-remote-management-glossary.md). O atributo **SupportFragment** não tem suporte para operações de assinatura e deve ser definido como **false**. O atributo **SupportFiltering** não é válido e deve ser definido como **false**. Esse recurso não será válido para um *URI de recurso* se também houver suporte para operações de Shell.

</dd> <dt>

<span id="Shell"></span><span id="shell"></span><span id="SHELL"></span>Shell
</dt> <dd>

Há suporte para operações de Shell no [*URI de recurso*](windows-remote-management-glossary.md). O atributo **SupportFragment** não tem suporte para operações de shell e deve ser definido como **false**. O atributo **SupportFiltering** não é válido e deve ser definido como **false**. Esse recurso não será válido para um *URI de recurso* se qualquer outra funcionalidade de operação também tiver suporte. Se uma funcionalidade de operação do Shell estiver configurada para um *URI de recurso*, as operações obter, colocar, criar, excluir, invocar e enumerar serão processadas internamente no serviço WinRM para gerenciar shells. Como resultado, o plug-in não pode lidar com as operações em si.

</dd> </dl> </dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_Security"></span><span id="pluginconfiguration_resources_resource_security"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_SECURITY"></span>**PlugInConfiguration** / **Recursos** / do **Recurso** / do **Segurança** do
</dt> <dd>

Esse elemento define o descritor de segurança (por meio do atributo **SDDL** ) que deve ser aplicado para determinar o acesso a um [*URI de recurso*](windows-remote-management-glossary.md) específico (por meio do atributo **URI** ). Se **ExactMatch** não estiver presente, o elemento de **segurança** assume como padrão **false**, o que significa que o **SDDL** se aplica a todos os *URIs de recurso* que compartilham o **URI** como um prefixo. Se **ExactMatch** for definido como true, o **SDDL** se aplicará somente ao **URI** exato especificado. Se houver várias entradas de **segurança** que possam se aplicar a *URIs de recursos* específicos, a correspondência de prefixo mais longo será usada para determinar a **SDDL** apropriada. Como resultado da correspondência de prefixo mais longo, se existir uma entrada de **URI** de correspondência exata, ela será sempre escolhida como o elemento de segurança apropriado.

</dd> </dl>

Este é o esquema de configuração de plug-in especificado como um XSD.

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

 

 




