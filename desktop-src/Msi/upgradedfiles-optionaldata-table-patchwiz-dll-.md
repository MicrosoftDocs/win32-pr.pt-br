---
description: A tabela UpgradedFile \_ OptionalData contém informações sobre arquivos específicos em uma imagem atualizada. Essa tabela é opcional no banco de dados de criação de patch (arquivo .pcp) e é usada pela função UiCreatePatchPackageEx.
ms.assetid: 8b96a83a-2bfa-47b7-bde0-896bdcc97d29
title: UpgradedFiles_OptionalData (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08eb766f8db9d295546670c80627284991da1ff8dccb5a0c2900be74bd785dab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012834"
---
# <a name="upgradedfiles_optionaldata-table-patchwizdll"></a>Tabela UpgradedFiles \_ OptionalData (Patchwiz.dll)

A tabela UpgradedFile \_ OptionalData contém informações sobre arquivos específicos em uma imagem atualizada. Essa tabela é opcional no banco de dados de criação de patch (arquivo .pcp) e é usada pela [função UiCreatePatchPackageEx.](uicreatepatchpackageex--patchwiz-dll-.md)

A tabela UpgradedFile \_ OptionalData tem as seguintes colunas.



| Coluna                  | Tipo    | Chave | Nullable |
|-------------------------|---------|-----|----------|
| Atualizado                | texto    | Y   | N        |
| Ftk                     | texto    | Y   | N        |
| SymbolPaths             | texto    |     | Y        |
| AllowIgnoreOnPatchError | Número inteiro |     | Y        |
| IncludeWholeFile        | Número inteiro |     | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Atualizado
</dt> <dd>

Chave estrangeira para a coluna Atualizado da [Tabela UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>Ftk
</dt> <dd>

Chave da tabela de arquivos. Chave estrangeira [na tabela Arquivo](file-table.md) do .msi arquivo da imagem atualizada. Se duas ou mais imagens atualizadas em uma família têm o mesmo valor FTK, o valor deve se referir ao mesmo arquivo. Os arquivos compartilhados por várias imagens de atualização devem ter o mesmo FTK para minimizar o tamanho do arquivo de gabinete.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

O valor nesse campo é adicionado à lista delimitada por ponto e vírgula de pastas na coluna SymbolPaths da [Tabela UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md) quando o patch é gerado e pode ser usado para adicionar arquivos de símbolo para um arquivo específico.

</dd> <dt>

<span id="AllowIgnoreOnPatchError"></span><span id="allowignoreonpatcherror"></span><span id="ALLOWIGNOREONPATCHERROR"></span>AllowIgnoreOnPatchError
</dt> <dd>

De definido como 1 para indicar que o patch não é vital. De definido como 0 para indicar que o patch é vital. Se Windows Instalador encontrar um problema ao aplicar esse patch ao arquivo especificado na coluna FTK, o valor nesse campo  determinará se a caixa de mensagem de erro inclui um botão Ignorar para permitir que o usuário continue o processo de aplicação de patch.

</dd> <dt>

<span id="IncludeWholeFile"></span><span id="includewholefile"></span><span id="INCLUDEWHOLEFILE"></span>IncludeWholeFile
</dt> <dd>

Definido como um valor diferente de zero se todo o arquivo especificado na coluna FTK deve ser instalado em vez de criar um patch binário.

</dd> </dl>

 

 



