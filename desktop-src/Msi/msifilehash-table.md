---
description: A tabela MsiFileHash é usada para armazenar um hash de 128 bits de um arquivo de origem fornecido pelo pacote Windows Installer. O hash é dividido em quatro valores de 32 bits e armazenado em colunas separadas da tabela.
ms.assetid: 972a2784-418d-4cb3-b13c-df89b079e94c
title: Tabela MsiFileHash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc43c7fd812781057ec0be271ffc370a6b5eb2e3054926e1f969383c0fb390c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944943"
---
# <a name="msifilehash-table"></a>Tabela MsiFileHash

A **tabela MsiFileHash** é usada para armazenar um hash de 128 bits de um arquivo de origem fornecido pelo pacote Windows Installer. O hash é dividido em quatro valores de 32 bits e armazenado em colunas separadas da tabela.

Windows O instalador pode usar o hash de arquivo como um meio de detectar e eliminar a cópia desnecessária de arquivos. Um hash de arquivo armazenado na tabela **MsiFileHash** pode ser comparado com um hash de um arquivo existente no computador do usuário obtido chamando [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha). A **tabela MsiFileHash** só pode ser usada com arquivos sem versão.

A **tabela MsiFileHash** tem as seguintes colunas.



| Coluna    | Tipo                               | Chave | Nullable |
|-----------|------------------------------------|-----|----------|
| Arquivo\_    | [Identificador](identifier.md)       | Y   | N        |
| Opções   | [Inteiro](integer.md)             | N   | N        |
| HashPart1 | [DoubleInteger](doubleinteger.md) | N   | N        |
| HashPart2 | [DoubleInteger](doubleinteger.md) | N   | N        |
| HashPart3 | [DoubleInteger](doubleinteger.md) | N   | N        |
| Hashpart4 | [DoubleInteger](doubleinteger.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Arquivo\_
</dt> <dd>

Chave estrangeira para [Tabela de arquivos](file-table.md). Cadeia de caracteres de 72 caracteres.

</dd> <dt>

<span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Opções
</dt> <dd>

Essa coluna deve ser 0 e é reservada para uso futuro.

</dd> <dt>

<span id="HashPart1"></span><span id="hashpart1"></span><span id="HASHPART1"></span>HashPart1
</dt> <dd>

Primeiros 32 bits de hash. O hash de arquivo inserido nesse campo deve ser obtido chamando [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) ou o [**método FileHash**](installer-filehash.md). Não use outros métodos.

</dd> <dt>

<span id="HashPart2"></span><span id="hashpart2"></span><span id="HASHPART2"></span>HashPart2
</dt> <dd>

Segundo 32 bits de hash. O hash de arquivo inserido nesse campo deve ser obtido chamando [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) ou o [**método FileHash**](installer-filehash.md). Não use outros métodos de hash.

</dd> <dt>

<span id="HashPart3"></span><span id="hashpart3"></span><span id="HASHPART3"></span>HashPart3
</dt> <dd>

Terceiro 32 bits de hash. O hash de arquivo inserido nesse campo deve ser obtido chamando [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) ou o [**método FileHash**](installer-filehash.md). Não use outros métodos.

</dd> <dt>

<span id="HashPart4"></span><span id="hashpart4"></span><span id="HASHPART4"></span>HashPart4
</dt> <dd>

Quarto 32 bits de hash. O hash de arquivo inserido nesse campo deve ser obtido chamando [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) ou o [**método FileHash**](installer-filehash.md). Não use outros métodos.

</dd> </dl>

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE60](ice60.md)  
[ICE66](ice66.md)  
</dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> <dt>

[Versão do arquivo padrão](default-file-versioning.md)
</dt> </dl>

 

 



