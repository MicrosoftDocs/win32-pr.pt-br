---
description: Preparando um arquivo de configuração de recurso
ms.assetid: 292b57ea-1c7e-49b6-876c-4ad307a2ec43
title: Preparando um arquivo de configuração de recurso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b862f48f15997300f079a39de0eb385c535758d9392dc452e1d338d86c8d59e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147099"
---
# <a name="preparing-a-resource-configuration-file"></a>Preparando um arquivo de configuração de recurso

Os utilitários do COMPILador DE RC [](resource-utilities.md) e DOLCT descritos em Utilitários de Recurso fornecem uma opção de linha de comando que permite especificar um arquivo de configuração de recurso para os recursos de linguagem base. O uso desse arquivo XML público e acessível por humanos permite mais controle sobre a divisão de recursos do que pode ser obtido usando as opções de linha de comando regulares dos utilitários. No entanto, mesmo se você não fornecer um arquivo de configuração de recurso como entrada, os arquivos de recurso LN e específicos de idioma conterão dados de configuração de recursos.

Todos os arquivos de configuração de recursos para aplicativos Win32 começam e terminam de forma idêntica:


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>

<resources>
        
        <!-- a single win32Resources element goes here -->

</resources>
</localization>
```



Este tópico se concentra nos aspectos do esquema XML que são úteis na criação de código não Windows Vista e posterior. Em particular, ele se preocupa apenas com o comportamento do elemento win32Resources.

## <a name="win32resources-element"></a>Elemento win32Resources

O elemento win32Resources tem os atributos descritos na tabela a seguir.



| Nome do atributo           | Obrigatório | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FileType                 | Não        | Tipo de arquivo. Sempre deve ser "Aplicativo".                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| soma de verificação                 | Não        | Valor da verificação a ser exibido nos dados de configuração de recurso do arquivo LN e dos arquivos de recurso específicos de idioma. Por exemplo, esse atributo permite que você copie a verificação de um único arquivo de recurso específico do idioma, por convenção, aquele para inglês (Estados Unidos) e coloque a verificação em um arquivo de recurso específico de idioma diferente. A verificação pode ser especificada como uma cadeia de caracteres de número hexadecimal que não tem mais de 32 caracteres. O valor numérico deve ser contenível em um número de 128 bits. |
| Linguagem                 | Não        | Idioma especificado usando um formato de nome compatível com RFC 4646 (Windows Vista e posterior), por exemplo, en-US para inglês (Estados Unidos).                                                                                                                                                                                                                                                                                                                                                                             |
| ultimateFallbackLanguage | Não        | Idioma a ser inserido nos dados de configuração de recurso para o arquivo LN, representando o idioma de fallback final a ser usado em uma pesquisa por um arquivo de recurso específico do idioma correspondente. Se o carregador de recursos não conseguir carregar um arquivo de recurso solicitado dos idiomas de interface do usuário preferenciais do thread, ele usará um idioma de fallback final como sua última tentativa. O idioma é especificado usando um formato de nome compatível com RFC 4646 (Windows Vista e posterior), por exemplo, en-US para inglês (Estados Unidos).       |
| ultimateFallbackLocation | Não        | Local de fallback. Especifique "interno" se os recursos de fallback final são compilados no arquivo LN. Especifique "external" (padrão) se o arquivo LN for referenciar um arquivo de recurso específico de idioma para seus recursos de fallback final.                                                                                                                                                                                                                                                                                |



 

No arquivo de configuração de recurso, o elemento win32Resources tem os subconjunto descritos na tabela a seguir.



| Nome do elemento       | Descrição                                                                                                                              |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| localizedResources | Recursos que encapsulam informações sobre os tipos de recursos e recursos individuais contidos em um arquivo de recurso específico do idioma. |
| neutralResources   | Recursos que encapsulam informações sobre os tipos de recursos contidos em um arquivo LN.                                                 |



 

## <a name="localizedresources-element"></a>Elemento localizedResources

Elemento recursos localizados. Por padrão, esse elemento não tem atributos e apenas um tipo de subconjunto. É apenas um contêiner para elementos resourceType.



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
> Alguns defeitos de configuração de recurso são capturados apenas pelo Compilador RC ou PELOTACT, dependendo do arquivo de recurso de entrada ou do conteúdo do arquivo binário. Os erros resourceType no arquivo de configuração de recurso que não existem no arquivo de entrada não são capturados, resultando em comportamento inesperado. Os usuários podem estar usando um arquivo de configuração de recurso com defeito e não saber até introduzir binários que usam as partes quebradas do arquivo de configuração de recurso, o que cria a aparência de que as quebras são dos binários atuais.

 



| Nome do atributo | Obrigatório | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| typeNameId     | Sim       | Nome do tipo ou identificador do recurso. Especifique um nome de cadeia de caracteres ou um número. Se estiver usando um número, prepare a cadeia de caracteres com um " " para \# indicar que ele representa um número. Cada elemento resourceType deve ter apenas um *atributo typeNameId.*                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| itemName       | Não        | Cadeia de caracteres de nome de item para o recurso, a ser colocada no arquivo de recurso específico do idioma. Você pode especificar vários nomes, separados por espaços em branco, por exemplo, "HTML MOFDATA".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| itemId         | Não        | Identificador do item de recurso individual, a ser colocado no arquivo de recurso específico do idioma. O item pode ser especificado como um intervalo (por exemplo, "1-12") ou por identificadores individuais separados por espaços em branco (por exemplo, "1 3 4").                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| stringId       | Não        | Identificador de cadeia de caracteres para item de recurso individual, a ser colocado no arquivo de recurso específico do idioma. A cadeia de caracteres pode ser especificada como um intervalo (por exemplo, "1-12") ou por identificadores individuais separados por espaços em branco (por exemplo, "1 3 4"). Esse atributo permite a especificação de entradas de tabela de cadeia de caracteres localizáveis e não localizáveis. Ele deve ser usado em conjunto com o *valor typeNameId* de "6", denotando um tipo de recurso de entrada de tabela de cadeia de caracteres.<br/> As cadeias de caracteres são armazenadas em blocos de 16 em uma tabela de cadeia de caracteres. Por exemplo, as cadeias de caracteres de 0 a 15 são armazenadas em um único bloco de item de recurso e podem ser referenciadas no arquivo de configuração de recurso como *itemId* 1 ou como *stringId* "0-15". Por exemplo, se houver cinco cadeias de caracteres localizáveis e três cadeias de caracteres não localizáveis, você deverá atribuir identificadores de cadeia de caracteres de 0 a 4 para as cadeias de caracteres localizáveis e identificadores de cadeia de caracteres 16 a 18 para as cadeias de caracteres não localizáveis. Se você não organizar cadeias de caracteres dessa forma, os blocos de cadeias de caracteres afetados serão colocados no arquivo LN e no arquivo de recurso específico do idioma.<br/> |



 

Se você especificar os atributos *itemName*, *itemId* e/ou *stringId* para um tipo de recurso específico no elemento localizedResource, somente esses itens ou cadeias de caracteres especificados para o tipo de recurso designado serão colocados no arquivo de recurso específico do idioma. Se um elemento resourceType for especificado sem qualquer nome de item explícito, identificador de item ou identificador de cadeia de caracteres, todos os itens do tipo de recurso especificado serão colocados no arquivo de recurso específico do idioma. Itens ou tipos não listados em nenhum elemento localizedResource são colocados no arquivo LN.

Veja a seguir os tipos de recursos padrão e seus identificadores numéricos:

-   CURSOR(1)
-   BITMAP(2)
-   ICON(3)
-   MENU(4)
-   DIALOG(5)
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

 

 




