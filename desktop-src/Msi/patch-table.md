---
description: A tabela patch especifica o arquivo que deve receber um patch específico e o local físico dos arquivos de patch nas imagens de mídia.
ms.assetid: 1b624702-de25-4b1a-9dac-21f359ee97f7
title: Tabela de patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e5f41f206557589bf0b90d9ffb125a80d05d39ce809dc01a8e687a21045475
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558456"
---
# <a name="patch-table"></a>Tabela de patches

A tabela patch especifica o arquivo que deve receber um patch específico e o local físico dos arquivos de patch nas imagens de mídia.

A tabela patch tem as seguintes colunas.



| Coluna      | Tipo                               | Chave | Nullable |
|-------------|------------------------------------|-----|----------|
| Arquivo\_      | [Identificador](identifier.md)       | Y   | N        |
| Sequência    | [Inteiro](integer.md)             | Y   | N        |
| PatchSize   | [DoubleInteger](doubleinteger.md) | N   | N        |
| Atributos  | [Inteiro](integer.md)             | N   | N        |
| Cabeçalho      | [Binary](binary.md)               | N   | Y        |
| StreamRef\_ | [Identificador](identifier.md)       | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Grupo\_
</dt> <dd>

O patch é aplicado ao arquivo especificado pelo identificador nesta coluna. Essa é uma chave primária para a tabela e é uma chave estrangeira para a [tabela de arquivos](file-table.md).

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Ordem
</dt> <dd>

Essa é a posição do arquivo de patch na ordem de sequência dos arquivos nas imagens de mídia. A ordem de sequência deve corresponder à ordem dos arquivos no arquivo de gabinete do pacote de patch. Esta é uma chave primária para esta tabela. o limite máximo é de 32767 arquivos, para criar um pacote de Windows Installer com mais arquivos, consulte [criando um pacote grande](authoring-a-large-package.md).

</dd> <dt>

<span id="PatchSize"></span><span id="patchsize"></span><span id="PATCHSIZE"></span>PatchSize
</dt> <dd>

Essa coluna fornece o tamanho do patch em bytes gravados como um inteiro longo.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

Inteiro que contém os sinalizadores de bit que representam os atributos de patch. Insira um valor de 1 nesta coluna para indicar que a falha ao aplicar esse patch não é um erro fatal.



| Constante                         | Hexadecimal | Decimal | Descrição                                                          |
|----------------------------------|-------------|---------|----------------------------------------------------------------------|
| (nenhum)                           | 0x000       | 0       | A falha ao aplicar esse patch é um erro fatal.                        |
| **msidbPatchAttributesNonVital** | 0x001       | 1       | Indica que a falha ao aplicar esse patch não é um erro fatal. |



 

</dd> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>Verga
</dt> <dd>

Esta coluna é o cabeçalho de patch de fluxo binário usado para validação de patch. Essa coluna deverá ser nula se a \_ coluna StreamRef não for nula. nesse caso, o fluxo do cabeçalho de patch é armazenado na [tabela MsiPatchHeaders](msipatchheaders-table.md) para superar a limitação de nome de fluxo descrita em [limitações de OLE em Fluxos](ole-limitations-on-streams.md).

</dd> <dt>

<span id="StreamRef_"></span><span id="streamref_"></span><span id="STREAMREF_"></span>StreamRef\_
</dt> <dd>

Chave externa na tabela MsiPatchHeaders especificando a linha que contém o fluxo do cabeçalho de patch.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa tabela é processada pela [ação PatchFiles](patchfiles-action.md). Normalmente, ele é adicionado ao pacote de instalação por uma transformação de um pacote de patch. Normalmente, ele não é criado diretamente em um pacote de instalação.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE45](ice45.md)  
</dl>

 

 



