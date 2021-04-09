---
description: A tabela Atualizadofile \_ OptionalData contém informações sobre arquivos específicos em uma imagem atualizada. Essa tabela é opcional no banco de dados de criação de patches (arquivo. PCP) e é usada pela função UiCreatePatchPackageEx.
ms.assetid: 8b96a83a-2bfa-47b7-bde0-896bdcc97d29
title: Tabela de UpgradedFiles_OptionalData (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2a648623e2a0cde11af34a3b948b4f2ac6fba59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171690"
---
# <a name="upgradedfiles_optionaldata-table-patchwizdll"></a>\_Tabela UpgradedFiles OptionalData (Patchwiz.dll)

A tabela Atualizadofile \_ OptionalData contém informações sobre arquivos específicos em uma imagem atualizada. Essa tabela é opcional no banco de dados de criação de patches (arquivo. PCP) e é usada pela função [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .

A tabela Atualizadofile \_ OptionalData tem as colunas a seguir.



| Coluna                  | Tipo    | Chave | Nullable |
|-------------------------|---------|-----|----------|
| Atualizado                | text    | S   | N        |
| FTK                     | text    | S   | N        |
| SymbolPaths             | text    |     | S        |
| AllowIgnoreOnPatchError | Número inteiro |     | S        |
| IncludeWholeFile        | Número inteiro |     | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Foram
</dt> <dd>

Chave estrangeira para a coluna atualizada da [tabela UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Chave de tabela de arquivo. Chave estrangeira na [tabela de arquivos](file-table.md) do arquivo. msi da imagem atualizada. Se duas ou mais imagens atualizadas em uma família tiverem o mesmo valor de FTK, o valor deverá se referir ao mesmo arquivo. Os arquivos compartilhados por várias imagens de atualização devem ter o mesmo FTK para minimizar o tamanho do arquivo de gabinete.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

O valor nesse campo é adicionado à lista delimitada por ponto-e-vírgula das pastas na coluna SymbolPaths da [tabela UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md) quando o patch é gerado e pode ser usado para adicionar arquivos de símbolo para um arquivo específico.

</dd> <dt>

<span id="AllowIgnoreOnPatchError"></span><span id="allowignoreonpatcherror"></span><span id="ALLOWIGNOREONPATCHERROR"></span>AllowIgnoreOnPatchError
</dt> <dd>

Defina como 1 para indicar que o patch não é vital. Defina como 0 para indicar que o patch é vital. Se Windows Installer encontrar um problema ao aplicar esse patch ao arquivo especificado na coluna FTK, o valor nesse campo determinará se a caixa de mensagem de erro inclui um botão **ignorar** para permitir que o usuário continue o processo de aplicação de patch.

</dd> <dt>

<span id="IncludeWholeFile"></span><span id="includewholefile"></span><span id="INCLUDEWHOLEFILE"></span>IncludeWholeFile
</dt> <dd>

Defina como um valor diferente de zero se o arquivo inteiro especificado na coluna FTK deve ser instalado em vez de criar um patch binário.

</dd> </dl>

 

 



