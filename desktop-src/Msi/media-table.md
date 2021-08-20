---
description: A tabela de mídia descreve o conjunto de discos que compõem a mídia de origem para a instalação do.
ms.assetid: f9789f1d-35bf-40d6-9724-d5a160a0d06d
title: Tabela de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29939553e64fb6558aa6480fb69b7beab208a4ccb3e2c9ce55c4d8fcbfc18cc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117805091"
---
# <a name="media-table"></a>Tabela de mídia

A tabela de mídia descreve o conjunto de discos que compõem a mídia de origem para a instalação do.

A tabela de mídia contém as colunas mostradas na tabela a seguir.



| Coluna       | Tipo                     | Chave | Nullable |
|--------------|--------------------------|-----|----------|
| DiskId       | [Inteiro](integer.md)   | Y   | N        |
| LastSequence | [Inteiro](integer.md)   | N   | N        |
| DiskPrompt   | [Text](text.md)         | N   | Y        |
| Gabinete      | [Gabinete](cabinet.md)   | N   | Y        |
| VolumeLabel  | [Text](text.md)         | N   | Y        |
| Fonte       | [Propriedade](property.md) | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="DiskId"></span><span id="diskid"></span><span id="DISKID"></span>DiskId
</dt> <dd>

Determina a ordem de classificação da tabela. Esse número deve ser igual ou maior que 1.

</dd> <dt>

<span id="LastSequence"></span><span id="lastsequence"></span><span id="LASTSEQUENCE"></span>LastSequence
</dt> <dd>

Número de sequência do arquivo para o último arquivo desta mídia. Os números na coluna LastSequence especificam quais dos arquivos na tabela de [arquivos](file-table.md) são encontrados em um determinado disco de origem. Cada disco de origem contém todos os arquivos com números de sequência (conforme mostrado na coluna sequência da tabela de arquivos) menor ou igual ao valor na coluna LastSequence e maior que o valor de LastSequence do disco anterior (ou maior que 0, para a primeira entrada na tabela de mídia). Esse número deve ser não negativo; o limite máximo é de 32767 arquivos. para obter mais informações sobre como criar um pacote de Windows Installer com mais arquivos, consulte [criando um pacote grande](authoring-a-large-package.md).

</dd> <dt>

<span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt
</dt> <dd>

O nome do disco, que geralmente é o texto visível impresso no disco. Esse texto localizável é usado para solicitar ao usuário quando esse disco precisa ser inserido.

</dd> <dt>

<span id="Cabinet"></span><span id="cabinet"></span><span id="CABINET"></span>Gabinete
</dt> <dd>

O nome do gabinete se alguns ou todos os arquivos armazenados na mídia forem compactados em um arquivo de gabinete. Se nenhum gabinete for usado, essa coluna deverá ficar em branco. O nome do gabinete deve usar a sintaxe do tipo de dados de [gabinete](cabinet.md) . Windows O instalador sempre requer uma origem válida para reparar arquivos incluídos em arquivos de gabinete inseridos. quando Windows Installer instala um pacote que contém um arquivo de gabinete inserido, uma cópia do arquivo de gabinete pode ser salva pelo sistema. Esta cópia não pode ser usada para reparar o arquivo de gabinete. Para conservar o espaço em disco, use arquivos de gabinete externo em vez de arquivos de gabinete inseridos.

</dd> <dt>

<span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel
</dt> <dd>

O rótulo atribuído ao volume. Esse é o rótulo de volume retornado pela função [**GetVolumeInformation**](/windows/win32/api/fileapi/nf-fileapi-getvolumeinformationa) . Se a propriedade [**SourceDir**](sourcedir.md) se referir a um volume removível (disquete ou CD-ROM), esse rótulo de volume será usado para verificar se o disco apropriado está na unidade antes de tentar instalar os arquivos. A entrada nesta coluna deve corresponder ao rótulo de volume da mídia física.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Original
</dt> <dd>

Esse campo só é usado pela aplicação de patch e, de outra forma, é deixado em branco. Uma transformação de patch pode inserir uma propriedade aqui que é o local do arquivo de gabinete que contém os arquivos de patch ou quaisquer arquivos novos adicionados pelo patch. Uma fonte diferente precisa ser especificada para esses arquivos porque a origem do pacote de patch pode ser armazenada separadamente da origem do produto. Se o campo de gabinete estiver vazio, o instalador ignorará o valor nesta coluna. Se esse campo estiver vazio, o instalador usará o valor da propriedade [**SourceDir**](sourcedir.md) como a origem do gabinete.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se o nome do gabinete for precedido por um sinal numérico ( \# ), os arquivos que fazem referência a esse registro de tabela de mídia serão empacotados em um arquivo de gabinete armazenado no banco de dados como um fluxo separado.

Para obter mais informações sobre como adicionar gabinetes às tabelas de arquivos e tabelas de mídia, consulte [usando gabinetes e fontes compactadas](using-cabinets-and-compressed-sources.md).

Windows O instalador requer que o arquivo de .msi esteja no primeiro disco de mídia removível (CD, DVD ou disquete) usado para a instalação do produto.

**Determinando o Sourcemode**

A propriedade de [**Resumo contagem de palavras**](word-count-summary.md) determina o modo de origem para a instalação atual. Se essa propriedade for definida como 2 ou 3, uma instalação de gabinete será presumida. Nesse modo, supõe-se que os arquivos de gabinete existam no diretório indicado pela propriedade [**SourceDir**](sourcedir.md) . Se o valor do tipo de origem for 0 ou 1, todos os arquivos de origem serão considerados na árvore cuja raiz é indicada pela propriedade **SourceDir** .

Observe que isso só se aplica a arquivos na tabela de arquivos que não têm os bits compactados ou não compactados definidos na coluna atributos. Esses bits substituem o valor da propriedade de [**Resumo de contagem de palavras**](word-count-summary.md) ao determinar se um arquivo específico é compactado ou descompactado.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE04](ice04.md)  
[ICE06](ice06.md)  
[ICE35](ice35.md)  
[ICE58](ice58.md)  
[ICE71](ice71.md)  
[ICE81](ice81.md)  
</dl>

 

 
