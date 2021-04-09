---
description: Preparando um arquivo de configuração de recurso
ms.assetid: 292b57ea-1c7e-49b6-876c-4ad307a2ec43
title: Preparando um arquivo de configuração de recurso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac162ad7f6d20148e0ef60cb9dc15da41cc27186
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090259"
---
# <a name="preparing-a-resource-configuration-file"></a>Preparando um arquivo de configuração de recurso

Os utilitários de compilador MUIRCT e RC descritos em [utilitários de recursos](resource-utilities.md) fornecem uma opção de linha de comando que permite especificar um arquivo de configuração de recurso para os recursos de idioma base. O uso desse arquivo XML público e legível por humanos permite mais controle sobre a divisão de recursos do que pode ser obtido usando as opções de linha de comando regulares dos utilitários. No entanto, mesmo que você não forneça um arquivo de configuração de recurso como uma entrada, os arquivos de recursos do LN e do idioma específico conterão dados de configuração de recursos.

Todos os arquivos de configuração de recurso para aplicativos Win32 começam e terminam de forma idêntica:


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>

<resources>
        
        <!-- a single win32Resources element goes here -->

</resources>
</localization>
```



Este tópico se concentra nos aspectos do esquema XML que são úteis na criação de código não gerenciado no Windows Vista e posterior. Em particular, ele se preocupa apenas com o comportamento do elemento win32Resources.

## <a name="win32resources-element"></a>Elemento win32Resources

O elemento win32Resources tem os atributos descritos na tabela a seguir.



| Nome do atributo           | Obrigatório | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FileType                 | Não        | Tipo de arquivo. Deve sempre ser "Application".                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| soma de verificação                 | Não        | O valor da soma de verificação deve aparecer nos dados de configuração do recurso do arquivo LN e dos arquivos de recursos específicos do idioma. Por exemplo, esse atributo permite copiar a soma de verificação de um único arquivo de recurso específico de idioma, por convenção, um para inglês (Estados Unidos) e posicionar a soma de verificação em um arquivo de recurso específico de idioma diferente. A soma de verificação pode ser especificada como uma cadeia de caracteres de número hexadecimal que não tenha mais de 32 caracteres. O valor numérico deve ser confinado em um número de 128 bits. |
| Linguagem                 | Não        | Idioma especificado usando um formato de nome compatível com RFC 4646 (Windows Vista e posterior), por exemplo, en-US para inglês (Estados Unidos).                                                                                                                                                                                                                                                                                                                                                                             |
| ultimateFallbackLanguage | Não        | Idioma para inserir nos dados de configuração de recurso do arquivo LN, representando o idioma de fallback final a ser usado em uma pesquisa de um arquivo de recurso específico do idioma correspondente. Se o carregador de recursos não carregar um arquivo de recursos solicitado dos idiomas de interface do usuário preferenciais do thread, ele usará um idioma de fallback final como sua última tentativa. O idioma é especificado usando um formato de nome compatível com RFC 4646 (Windows Vista e posterior), por exemplo, en-US para inglês (Estados Unidos).       |
| ultimateFallbackLocation | Não        | Local de fallback. Especifique "interno" se os recursos de fallback finais forem compilados no arquivo LN. Especifique "external" (padrão) se o arquivo LN for referenciar um arquivo de recurso específico de idioma para seus recursos de fallback definitivos.                                                                                                                                                                                                                                                                                |



 

No arquivo de configuração de recurso, o elemento win32Resources tem os subelementos descritos na tabela a seguir.



| Nome do elemento       | Descrição                                                                                                                              |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| localizedResources | Recursos que encapsulam informações sobre os tipos de recursos e recursos individuais contidos em um arquivo de recurso específico de idioma. |
| neutralResources   | Recursos que encapsulam informações sobre os tipos de recursos contidos em um arquivo LN.                                                 |



 

## <a name="localizedresources-element"></a>Elemento localizedResources

Elemento de recursos localizados. Por padrão, esse elemento não tem atributos e apenas um tipo de subelemento. É apenas um contêiner para elementos resourceType.



| Nome do atributo | Descrição                                                                    |
|----------------|--------------------------------------------------------------------------------|
| resourceType   | Tipo de um recurso individual contido em um arquivo de recurso específico do idioma. |



 

## <a name="neutralresources-element"></a>Elemento neutralResources

Elemento de recursos neutros. Esse elemento é apenas um contêiner para elementos resourceType.



| Nome do atributo | Descrição                                        |
|----------------|----------------------------------------------------|
| resourceType   | Tipo de um único recurso contido em um arquivo LN. |



 

## <a name="resourcetype-element"></a>Elemento resourceType

O elemento resourceType encapsula informações sobre um único tipo de recurso ou recurso individual. Ele tem os atributos listados abaixo.

> [!Caution]  
> Alguns defeitos de configuração de recursos são capturados somente pelo compilador RC ou MUIRCT, dependendo do arquivo de recurso de entrada ou do conteúdo do arquivo binário. Os erros de resourceType no arquivo de configuração de recurso que não existem no arquivo de entrada não são capturados, resultando em um comportamento inesperado. Os usuários podem usar um arquivo de configuração de recurso com defeito e não sabem até que introduzam binários que usam as partes quebradas do arquivo de configuração de recurso, o que cria a aparência das quebras dos binários atuais.

 



| Nome do atributo | Obrigatório | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| typeNameid     | Sim       | Nome ou identificador do tipo para o recurso. Especifique um nome de cadeia de caracteres ou um número. Se estiver usando um número, preceda a cadeia de caracteres com um " \# " para indicar que ele representa um número. Cada elemento resourceType deve ter apenas um atributo *typenameid* .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| itemName       | Não        | A cadeia de caracteres do nome do item para o recurso deve ser colocada no arquivo de recurso específico do idioma. Você pode especificar vários nomes, separados por espaços em branco, por exemplo, "HTML MOFDATA".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| itemId         | Não        | Identificador de item de recurso individual, a ser colocado no arquivo de recurso específico do idioma. O item pode ser especificado como um intervalo (por exemplo, "1-12") ou por identificadores individuais separados por espaços em branco (por exemplo, "1 3 4").                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| stringId       | Não        | Identificador de cadeia de caracteres para item de recurso individual, a ser colocado no arquivo de recurso específico do idioma. A cadeia de caracteres pode ser especificada como um intervalo (por exemplo, "1-12") ou por identificadores individuais separados por espaços em branco (por exemplo, "1 3 4"). Esse atributo permite a especificação de entradas de tabela de cadeias de caracteres localizáveis e não localizáveis. Ele deve ser usado em conjunto com o valor de *typenameid* de "6", denotando um tipo de recurso de entrada de tabela de cadeia de caracteres.<br/> As cadeias são armazenadas em blocos de 16 em uma tabela de cadeia de caracteres. Por exemplo, as cadeias de caracteres de 0 a 15 são armazenadas em um único bloco de item de recurso e podem ser referenciadas no arquivo de configuração de recurso como *ItemId* 1 ou como *stringid* "0-15". Por exemplo, se houver cinco cadeias de caracteres localizáveis e três cadeias não localizáveis, você deverá atribuir os identificadores de cadeia 0-4 para as cadeias de caracteres localizáveis e os identificadores de cadeia 16-18 para as cadeias não localizáveis. Se você não organizar cadeias de caracteres dessa forma, os blocos de cadeias de caracteres afetados serão colocados no arquivo LN e no arquivo de recurso específico do idioma.<br/> |



 

Se você especificar os atributos *ItemName*, *ItemId* e/ou *stringid* para um tipo de recurso específico no elemento localizedResource, somente esses itens ou cadeias de caracteres especificados para o tipo de recurso designado serão colocados no arquivo de recurso específico do idioma. Se um elemento resourceType for especificado sem nenhum nome de item explícito, identificador de item ou identificador de cadeia de caracteres, todos os itens do tipo de recurso especificado serão colocados no arquivo de recurso específico do idioma. Os itens ou tipos não listados em nenhum elemento localizedResource são colocados no arquivo LN.

A seguir estão os tipos de recursos padrão e seus identificadores numéricos:

-   CURSOR (1)
-   BITMAP (2)
-   ÍCONE (3)
-   MENU (4)
-   CAIXA DE DIÁLOGO (5)
-   CADEIA DE CARACTERES (6)
-   FONTDIR (7)
-   FONTE (8)
-   ACELERADORES (9)
-   RCDATA (10)
-   MENSAGEM (11)
-   \_Cursor do grupo (12)
-   \_Ícone de grupo (14)
-   VERSÃO (16)
-   HTML (23)

## <a name="example"></a>Exemplo


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>
  <resources>
    <win32Resources fileType="Application">
      <neutralResources>
        <resourceType
           typeNameId="#16"
        />
      </neutralResources>
      <localizedResources> 
         <resourceType
                typeNameId="#2"
                itemId="5 6 7 8 9 10 11 12"
                itemName="HTML PRI"
         />
         <resourceType
                typeNameId="#4"
         />
         <resourceType
                typeNameId="#5"
         />
         <resourceType
                typeNameId="#6"
         />
         <resourceType
                typeNameId="#9"
         />
         <resourceType
                typeNameId="#11"
         />
         <resourceType
                typeNameId="#16"
         />
         <resourceType
                typeNameId="HTML"
         />
         <resourceType
                typeNameId="#23"
         />
         <resourceType
                typeNameId="#240"
         />
         <resourceType
                typeNameId="#1024"
         />
         <resourceType
                typeNameId="MY_TYPE"
         />
      </localizedResources> 
    </win32Resources>
  </resources>
</localization>
```



## <a name="remarks"></a>Comentários

Se você incluir qualquer ícone (3), caixa de diálogo (5), Cadeia de caracteres (6) ou tipo de recurso de versão (16) no elemento neutralResources, terá que duplicar essa entrada no elemento localizedResources. Você pode ver isso ilustrado no exemplo acima, em que o tipo de recurso 16 aparece nas seções de recursos neutros e localizados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Preparando recursos](preparing-resources.md)
</dt> </dl>

 

 




