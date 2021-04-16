---
description: A tabela PatchMetadata contém informações sobre um patch Windows Installer que é necessário para remover um patch e que é usado por adicionar ou remover programas.
ms.assetid: 09a06de4-0713-4e92-ab29-f34f6c94b677
title: Tabela PatchMetadata (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2521684714b91d8d172f8eb56bab984ffea87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747745"
---
# <a name="patchmetadata-table-patchwizdll"></a>Tabela PatchMetadata (PATCHWIZ.DLL)

A tabela PatchMetadata contém informações sobre um patch Windows Installer que é necessário para remover um patch e que é usado por adicionar ou remover programas. Todas as propriedades na tabela PatchMetadata são adicionadas à [tabela MsiPatchMetadata](msipatchmetadata-table.md) do arquivo. msp para um patch.

A tabela PatchMetadata é necessária em arquivos de propriedades de criação de patch (arquivos. PCP) que têm um MinimumRequiredMsiVersion igual a 300 na [tabela de propriedades](properties-table-patchwiz-dll-.md). A tabela será opcional se MinimumRequiredMsiVersion não for igual a 300.

A tabela PatchMetadata tem as colunas a seguir.



| Coluna   | Tipo | Chave | Nullable |
|----------|------|-----|----------|
| Empresa  | text | S   | S        |
| Propriedade | text | S   | N        |
| Valor    | text |     | S        |



 

### <a name="columns"></a>Colunas

<dl> <dt>

<span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Corporativa
</dt> <dd>

O nome da empresa. Um campo vazio (um valor nulo) indica que essa linha contém uma das propriedades de metadados padrão. Uma empresa pode estender o conjunto de propriedades adicionando uma linha à tabela e inserindo um nome de empresa neste campo.

</dd> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriedade
</dt> <dd>

O nome de uma propriedade de metadados. As propriedades AllowRemoval, ManufacturerName, TargetProductName, MoreInfoURL, DisplayName, Description e Classification são necessárias na tabela PatchMetadata. Esse campo deve conter uma das propriedades de metadados padrão a seguir se o campo da empresa estiver vazio (um valor nulo).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Propriedade</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AllowRemoval</td>
<td>Um valor inteiro que indica se o patch é um <a href="uninstallable-patches.md">patch desinstalável</a>. Se o campo de valor contiver um 0 (zero), o patch não poderá ser removido. Se o campo de valor contiver 1 (um), o patch será um patch desinstalável. Essa propriedade é necessária. Essa propriedade é registrada e seu valor pode ser obtido usando a função <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .<br/></td>
</tr>
<tr class="even">
<td>ManufacturerName</td>
<td>Um valor de cadeia de caracteres que contém o nome do fabricante do aplicativo. Esta propriedade é necessária.</td>
</tr>
<tr class="odd">
<td>MinorUpdateTargetRTM</td>
<td>Indica que o patch destina-se à versão RTM do produto ou ao patch de atualização principal mais recente. Crie essa propriedade opcional em patches de atualização secundárias que contenham informações de sequenciamento para indicar que o patch remove todos os patches até a versão RTM do produto ou até o patch de atualização principal mais recente. Essa propriedade está disponível a partir do Windows Installer 3,1.
<blockquote>
[!Note]<br />
Para exigir que o Windows Installer 3,1 seja instalado para aplicar o patch, defina a propriedade MinimumRequiredMsiVersion como 310 na <a href="properties-table-patchwiz-dll-.md">tabela Properties</a> do arquivo. PCP.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>TargetProductName</td>
<td>Um valor de cadeia de caracteres que contém o nome do aplicativo ou conjunto de aplicativos de destino. Esta propriedade é necessária.</td>
</tr>
<tr class="odd">
<td>MoreInfoURL</td>
<td>Um valor de cadeia de caracteres que contém uma URL que aponta para informações para esse patch. Essa propriedade necessária é registrada e seu valor pode ser obtido usando a função <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> . A partir do Windows XP com Service Pack 2 (SP2), esse valor pode ser o link de suporte para o patch exibido em Adicionar ou remover programas.<br/></td>
</tr>
<tr class="even">
<td>CreationTimeUTC</td>
<td>Um valor de cadeia de caracteres que contém a hora de criação do arquivo. msp no formato mm-dd-aa HH: MM (mês-dia-ano hora: minuto). Essa propriedade é opcional.</td>
</tr>
<tr class="odd">
<td>DisplayName</td>
<td>Um valor de cadeia de caracteres que contém o título para o patch que é adequado para exibição pública. Esta propriedade é necessária. Essa propriedade é registrada e seu valor pode ser obtido usando a função <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> . A partir do Windows XP com SP2, esse valor é o nome do patch exibido em Adicionar ou remover programas, começando com o Windows XP com SP2.<br/></td>
</tr>
<tr class="even">
<td>Descrição</td>
<td>Um valor de cadeia de caracteres que contém uma breve descrição do patch. Esta propriedade é necessária.</td>
</tr>
<tr class="odd">
<td>classificação</td>
<td>Um valor de cadeia de caracteres que contém a categoria arbitrária de atualizações, conforme definido pelo autor do patch. Por exemplo, os autores de patch podem especificar que cada patch seja classificado como um hotfix, ROLLUP de segurança, atualização crítica, atualização, Service Pack ou pacote cumulativo de atualizações. Esta propriedade é necessária.</td>
</tr>
<tr class="even">
<td>OptimizedInstallMode</td>
<td>Se essa propriedade for definida como 1 (uma) em todos os patches a serem aplicados em uma transação, a aplicação do patch será otimizada, se possível. Para obter informações, consulte <a href="patch-optimization.md">otimização de patch</a>. Disponível a partir do Windows Installer 3,1.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Valor da propriedade de metadados. Isso nunca pode ser nulo ou uma cadeia de caracteres vazia. Esse valor pode ser localizado.

</dd> </dl>

### <a name="remarks"></a>Comentários

Disponível a partir do Windows Installer 3,0.

Todas as propriedades criadas na tabela PatchMetadata são adicionadas à tabela MsiPatchMetadata do arquivo MSP. As propriedades AllowRemoval, MoreInfoURL e DisplayName são registradas e podem ser acessadas por meio do [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).

 

 




