---
description: Esses elementos compõem o esquema XML usado na publicação da Web e no manifesto de transferência dos assistentes de ordenação de impressão online.
title: Transferir esquema de manifesto
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 488b6fc9-ff85-4860-9cd5-61d5de7e15e8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 30324e32e1bd841423318a37eb1472d673ffc53c6e745f54f9398cec73138239
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858852"
---
# <a name="transfer-manifest-schema"></a>Transferir esquema de manifesto

Esses elementos compõem o esquema XML usado na publicação da Web e no manifesto de transferência dos assistentes de ordenação de impressão online.

Os elementos a seguir são definidos para o manifesto de transferência.

-   [cancelledpage](#syntax)
    -   [Sintaxe](#syntax)
    -   [Atributos](#attributes)
    -   [Informações do elemento](#element-information)
-   [failurepage](#syntax)
    -   [Sintaxe](#syntax)
    -   [Atributos](#attributes)
    -   [Informações do elemento](#element-information)
-   [preferência](#syntax)
    -   [Sintaxe](#syntax)
    -   [Atributos](#attributes)
    -   [Informações do elemento](#element-information)
-   [file](#syntax)
    -   [Sintaxe](#syntax)
    -   [Atributos](#attributes)
    -   [Informações do elemento](#element-information)
-   [File](#syntax)
    -   [Sintaxe](#syntax)
    -   [Atributos](#attributes)
    -   [Informações do elemento](#element-information)
-   [pasta](#syntax)
    -   [Sintaxe](#syntax)
    -   [Atributos](#attributes)
    -   [Informações do elemento](#element-information)
-   [pastalist](#syntax)
    -   [Sintaxe](#syntax)
    -   [Atributos](#attributes)
    -   [Informações do elemento](#element-information)
-   [formdata](#syntax)
    -   [Sintaxe](#syntax)
    -   [Atributos](#attributes)
    -   [Informações do elemento](#element-information)
-   [htmlui](#syntax)
    -   [Sintaxe](#syntax)
    -   [Atributos](#attributes)
    -   [Informações do elemento](#element-information)
-   [ImageProperty](#syntax)
    -   [Sintaxe](#syntax)
    -   [Atributos](#attributes)
    -   [Informações do elemento](#element-information)
-   [metadados](#syntax)
    -   [Sintaxe](#syntax)
    -   [Atributos](#attributes)
    -   [Informações do elemento](#element-information)
-   [netplace](#syntax)
    -   [Sintaxe](#syntax)
    -   [Atributos](#attributes)
    -   [Informações do elemento](#element-information)
-   [Postar](#syntax)
    -   [Sintaxe](#syntax)
    -   [Atributos](#attributes)
    -   [Informações do elemento](#element-information)
-   [alonga](#syntax)
    -   [Sintaxe](#syntax)
    -   [Atributos](#attributes)
    -   [Informações do elemento](#element-information)
-   [successpage](#syntax)
    -   [Sintaxe](#syntax)
    -   [Atributos](#attributes)
    -   [Informações do elemento](#element-information)
-   [destino](#syntax)
    -   [Sintaxe](#syntax)
    -   [Atributos](#attributes)
    -   [Informações do elemento](#element-information)
-   [transfermanifest](#syntax)
    -   [Sintaxe](#syntax)
    -   [Atributos](#attributes)
    -   [Informações do elemento](#element-information)
-   [uploadinfo](#syntax)
    -   [Sintaxe](#syntax)
    -   [Atributos](#attributes)
    -   [Informações do elemento](#element-information)

## <a name="cancelledpage"></a>cancelledpage

Especifica a página HTML do lado do servidor a ser exibida antes que o assistente seja fechado quando o usuário clicar no botão **Cancelar** .

### <a name="syntax"></a>Syntax


```
<cancelledpage
    href = "string"
>
<!-- child elements -->
</cancelledpage>                  
                    
```



### <a name="attributes"></a>Atributos



| Atributo | Descrição                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------|
| href      | Obrigatórios. A URL da página HTML do lado do servidor a ser exibida quando o usuário clica no botão **Cancelar** . |



 

### <a name="element-information"></a>Informações do elemento



| Elemento pai        | Elementos filho |
|-----------------------|----------------|
| [uploadinfo](#syntax) | Nenhum           |



 

## <a name="failurepage"></a>failurepage

Especifica a página HTML do lado do servidor a ser exibida se o carregamento não for bem-sucedido.

### <a name="syntax"></a>Syntax


```
<failurepage
    href = "string"
>
<!-- child elements -->
</failurepage>                    
                    
```



### <a name="attributes"></a>Atributos



| Atributo | Descrição                                                                                |
|-----------|--------------------------------------------------------------------------------------------|
| href      | Obrigatórios. A URL da página HTML do lado do servidor a ser exibida se o carregamento não for bem-sucedido. |



 

### <a name="element-information"></a>Informações do elemento



| Elemento pai        | Elementos filho         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Nenhum. O texto é permitido. |



 

## <a name="favorite"></a>favorito

Instrui o assistente a criar uma entrada de site favorita no menu **favoritos** para a URL fornecida. Se esse elemento não for especificado, o elemento [htmlui](#syntax) será usado em seu lugar.

### <a name="syntax"></a>Syntax


```
<favorite
    comment = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</favorite>                   
                    
```



### <a name="attributes"></a>Atributos



| Atributo | Descrição                                                            |
|-----------|------------------------------------------------------------------------|
| comentário   | Obrigatórios. O comentário associado à entrada de **favoritos** .         |
| href      | Obrigatórios. A URL da entrada de **favoritos** .                          |
| name      | Obrigatórios. O nome da URL que aparece no menu **favoritos** . |



 

### <a name="element-information"></a>Informações do elemento



| Elemento pai        | Elementos filho         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Nenhum. O texto é permitido. |



 

## <a name="file"></a>file

Descreve um único arquivo a ser copiado. Vários elementos de [arquivo](#syntax) podem estar contidos em um único nó [FileList](#syntax) .

### <a name="syntax"></a>Syntax


```
<file
    contenttype = "string"
    destination = "string"
    extension = "string"
    id = "string"
    size = "string"
    source = "string"
>
<!-- child elements -->
</file>                   
                    
```



### <a name="attributes"></a>Atributos



| Atributo   | Descrição                                                                                                                                                                  |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ContentType | Opcional. O tipo MIME do arquivo.                                                                                                                                         |
| destino | Obrigatórios. Um caminho sugerido para o arquivo depois que ele é carregado. Esse caminho é relativo à URL de destino do site de carregamento. O site de upload pode modificar esse valor conforme necessário. |
| extensão   | Opcional. A extensão de nome de arquivo do arquivo.                                                                                                                               |
| id          | Obrigatórios. O índice numérico do arquivo.                                                                                                                                   |
| tamanho        | Opcional. O tamanho do arquivo, em bytes.                                                                                                                                    |
| source      | Obrigatórios. O caminho completo do sistema de arquivos para o arquivo.                                                                                                                            |



 

### <a name="element-information"></a>Informações do elemento



| Elemento pai      | Elementos filho                                          |
|---------------------|---------------------------------------------------------|
| [File](#syntax) | [metadados](#syntax), [post](#syntax), [redimensionamento](#syntax) |



 

## <a name="filelist"></a>File

Um contêiner para elementos que descrevem os arquivos a serem copiados. Vários elementos de [FileList](#syntax) podem estar contidos em um único nó [transfermanifest](#syntax) .

### <a name="syntax"></a>Syntax


```
<filelist
    usesfolders = "1"
>
<!-- child elements -->
</filelist>                   
                    
```



### <a name="attributes"></a>Atributos



| Atributo   | Descrição      |
|-------------|------------------|
| usesfolders | Não implementado. |



 

### <a name="element-information"></a>Informações do elemento



| Elemento pai              | Elementos filho  |
|-----------------------------|-----------------|
| [transfermanifest](#syntax) | [file](#syntax) |



 

## <a name="folder"></a>folder

Descreve uma pasta na qual os arquivos são armazenados. Vários elementos de [pasta](#syntax) podem estar contidos em um único nó [folderList](#syntax) .

### <a name="syntax"></a>Syntax


```
<folder
    destination = "string"
>
<!-- child elements -->
</folder>                 
                    
```



### <a name="attributes"></a>Atributos



| Atributo   | Descrição                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| destino | Obrigatórios. Um caminho sugerido para a pasta assim que ela é carregada. Esse caminho é relativo à URL de destino do site de carregamento. O site de upload pode modificar esse valor conforme necessário. |



 

### <a name="element-information"></a>Informações do elemento



| Elemento pai        | Elementos filho |
|-----------------------|----------------|
| [pastalist](#syntax) | Nenhum           |



 

## <a name="folderlist"></a>pastalist

Um contêiner para elementos que descrevem os arquivos a serem copiados. Vários elementos [folderList](#syntax) podem estar contidos em um único nó [transfermanifest](#syntax) .

### <a name="syntax"></a>Syntax


```
<folderlist>
<!-- child elements -->
</folderlist>                 
                    
```



### <a name="attributes"></a>Atributos

Nenhum.

### <a name="element-information"></a>Informações do elemento



| Elemento pai              | Elementos filho    |
|-----------------------------|-------------------|
| [transfermanifest](#syntax) | [Pasta](#syntax) |



 

## <a name="formdata"></a>formdata

Descreve dados de formulário codificados em HTML opcionais que podem ser transferidos com os arquivos. Esse elemento será adicionado pelo serviço se ele optar por carregar os arquivos como uma postagem de várias partes. Os dados do formulário, juntamente com as informações do [elemento post,](#syntax) são usados para criar o header de postagem.

Vários [elementos formdata](#syntax) podem estar contidos em um único [nó uploadinfo.](#syntax)

### <a name="syntax"></a>Syntax


```
<formdata
    name = "string"
>
<!-- child elements -->
</formdata>                   
                    
```



### <a name="attributes"></a>Atributos



| Atributo | Descrição                                                                      |
|-----------|----------------------------------------------------------------------------------|
| name      | Obrigatórios. Define o nome de dados do formulário associado a esta seção do upload. |



 

### <a name="element-information"></a>Informações do elemento



| Elemento pai        | Elementos filho |
|-----------------------|----------------|
| [uploadinfo](#syntax) | Nenhum           |



 

## <a name="htmlui"></a>htmlui

A URL da página HTML do lado do servidor a ser exibida quando o assistente é fechado. Esse elemento criará uma entrada de página [](#syntax) da Web favorita no menu **Favoritos** se o elemento favorito estiver ausente e o nome amigável do site de upload for especificado.

### <a name="syntax"></a>Syntax


```
<htmlui
    href = "string"
>
<!-- child elements -->
</htmlui>                 
                    
```



### <a name="attributes"></a>Atributos



| Atributo | Descrição                                                                          |
|-----------|--------------------------------------------------------------------------------------|
| href      | Obrigatórios. A URL da página HTML do lado do servidor a ser exibida quando o assistente é fechado. |



 

### <a name="element-information"></a>Informações do elemento



| Elemento pai        | Elementos filho         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Nenhum. O texto é permitido. |



 

## <a name="imageproperty"></a>imageproperty

Especifica uma propriedade de imagem relacionada ao arquivo. Vários [elementos imageproperty](#syntax) podem estar contidos em um único nó [de metadados.](#syntax)

### <a name="syntax"></a>Syntax


```
<imageproperty
    id = "string"
>
<!-- child elements -->
</imageproperty>                  
                    
```



### <a name="attributes"></a>Atributos



| Atributo | Descrição                                  |
|-----------|----------------------------------------------|
| id        | Obrigatórios. A ID da propriedade específica. |



 

### <a name="element-information"></a>Informações do elemento



| Elemento pai      | Elementos filho         |
|---------------------|------------------------|
| [metadados](#syntax) | Nenhum. O texto é permitido. |



 

## <a name="metadata"></a>metadata

Um contêiner para elementos e texto que definem metadados para o arquivo específico. Vários [elementos de metadados](#syntax) podem estar contidos em um único [nó de](#syntax) arquivo.

### <a name="syntax"></a>Syntax


```
<metadata>
<!-- child elements -->
</metadata>                   
                    
```



### <a name="attributes"></a>Atributos

Nenhum.

### <a name="element-information"></a>Informações do elemento



| Elemento pai  | Elementos filho           |
|-----------------|--------------------------|
| [file](#syntax) | [imageproperty](#syntax) |



 

## <a name="netplace"></a>netplace

Define o destino para um local de rede criado em Meus Locais **de Rede** quando o upload é concluído. A criação de um local de rede pode ser impedida por meio [**do método IPublishingWizard::Initialize.**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize)

### <a name="syntax"></a>Syntax


```
<netplace
    comment = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</netplace>                   
                    
```



### <a name="attributes"></a>Atributos



| Atributo | Descrição                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| comentário   | Obrigatórios. O comentário exibido para o ícone de local de rede quando o cursor está sobre ele.         |
| href      | Obrigatórios. A URL da entrada de local de rede.                                                   |
| name      | Obrigatórios. O nome do ícone de local de rede que aparece na **pasta Meus Locais de** Rede. |



 

### <a name="element-information"></a>Informações do elemento



| Elemento pai        | Elementos filho         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Nenhum. O texto é permitido. |



 

## <a name="post"></a>post

URL na qual o arquivo deve ser postado. Esse elemento é adicionado pelo serviço quando a transferência é feita como uma postagem de várias partes e, com [formdata,](#syntax)é usado para criar o post-header. Se o serviço optar por executar a transferência de arquivo usando World Wide Web WebDAV (Distributed Authoring and Versioning), ele não deverá adicionar esse elemento. Vários [elementos de](#syntax) postagem podem estar contidos em um único nó [de](#syntax) arquivo.

### <a name="syntax"></a>Syntax


```
<post
    filename = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</post>                   
                    
```



### <a name="attributes"></a>Atributos



| Atributo | Descrição                                                                    |
|-----------|--------------------------------------------------------------------------------|
| filename  | Opcional. O nome do arquivo postado.                                   |
| href      | Obrigatórios. A URL da pasta de destino.                                   |
| name      | Obrigatórios. Define o nome de dados do formulário associado a esta seção da postagem. |



 

### <a name="element-information"></a>Informações do elemento



| Elemento pai  | Elementos filho      |
|-----------------|---------------------|
| [file](#syntax) | [formdata](#syntax) |



 

## <a name="resize"></a>redimensionar

Define o dimensionamento e a recompactação de um arquivo de imagem no formato JPEG. Se o arquivo de origem já estiver no formato JPEG e for menor ou igual à largura e altura especificadas, ele não será dimensionado. Se o arquivo de origem não for um arquivo JPEG, ele será convertido. O dimensionamento, a recompactação e a conversão do arquivo podem ser impedidos por meio do [**método IPublishingWizard::Initialize.**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) Vários [elementos de resize](#syntax) podem estar contidos em um único [nó de](#syntax) arquivo.

### <a name="syntax"></a>Syntax


```
<resize
    cx = "string"
    cy = "string"
    quality = "string"
>
<!-- child elements -->
</resize>                 
                    
```



### <a name="attributes"></a>Atributos



| Atributo | Descrição                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cx        | Obrigatórios. A largura da imagem, em pixels, após o upload. Se esse valor for 0, **cx** será calculado com base no valor **cy** para preservar dimensões relativas.  |
| cy        | Obrigatórios. A altura da imagem, em pixels, após o upload. Se esse valor for 0, **cy** será calculado com base no **valor cx** para preservar dimensões relativas. |
| qualidade   | Obrigatórios. O valor de qualidade JPEG, entre 0 e 100, sendo 100 a qualidade mais alta.                                                                            |



 

### <a name="element-information"></a>Informações do elemento



| Elemento pai  | Elementos filho |
|-----------------|----------------|
| [file](#syntax) | Nenhum.          |



 

## <a name="successpage"></a>página de sucesso

Especifica a página HTML do lado do servidor a ser exibida se o upload for bem-sucedido.

### <a name="syntax"></a>Syntax


```
<successpage
    href = "string"
>
<!-- child elements -->
</successpage>                    
                    
```



### <a name="attributes"></a>Atributos



| Atributo | Descrição                                                                            |
|-----------|----------------------------------------------------------------------------------------|
| href      | Obrigatórios. A URL da página HTML do lado do servidor a ser exibida se o upload for bem-sucedido. |



 

### <a name="element-information"></a>Informações do elemento



| Elemento pai        | Elementos filho         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Nenhum. O texto é permitido. |



 

## <a name="target"></a>destino

Uma pasta de destino especificada no formato UNC ou como um servidor WebDAV. O serviço adiciona esse destino para especificar uma pasta de destino se a transferência usar um protocolo WebDAV ou do sistema de arquivos. Se o serviço optar por executar a transferência de arquivo como uma postagem de várias partes, ele não deverá adicionar esse elemento.

### <a name="syntax"></a>Syntax


```
<target
    href = "string"
>
<!-- child elements -->
</target>                 
                    
```



### <a name="attributes"></a>Atributos



| Atributo | Descrição                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| href      | Obrigatórios. A URL da pasta de destino. Use o **https://** para WebDAV ou o formulário **\\ \\ de \\ compartilhamento de** servidor para UNC. |



 

### <a name="element-information"></a>Informações do elemento



| Elemento pai        | Elementos filho         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Nenhum. O texto é permitido. |



 

## <a name="transfermanifest"></a>transfermanifest

O nó pai do arquivo de manifesto de transferência.

### <a name="syntax"></a>Syntax


```
<transfermanifest>
<!-- child elements -->
</transfermanifest>                   
                    
```



### <a name="attributes"></a>Atributos

Nenhum.

### <a name="element-information"></a>Informações do elemento



| Elemento pai | Elementos filho                                                    |
|----------------|-------------------------------------------------------------------|
| Nenhum           | [filelist](#syntax), [folderlist](#syntax), [uploadinfo](#syntax) |



 

## <a name="uploadinfo"></a>uploadinfo

Um contêiner para elementos que fornece informações do site de upload usado na transação. Vários [elementos uploadinfo](#syntax) podem estar contidos em um único [nó transfermanifest.](#syntax)

### <a name="syntax"></a>Syntax


```
<uploadinfo
    friendlyname = "string"
>
<!-- child elements -->
</uploadinfo>                 
                    
```



### <a name="attributes"></a>Atributos



| Atributo    | Descrição                                                                 |
|--------------|-----------------------------------------------------------------------------|
| Friendlyname | Obrigatórios. Um nome amigável para o site que é exibido no assistente. |



 

### <a name="element-information"></a>Informações do elemento



| Elemento pai              | Elementos filho                                                                                                                                           |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [transfermanifest](#syntax) | [cancelledpage](#syntax), [failurepage](#syntax), [favorite](#syntax), [htmlui](#syntax), [netplace](#syntax), [successpage](#syntax), [target](#syntax) |



 

 

 



