---
description: A Tabela PatchMetadata contém informações sobre um patch do Windows Installer que é necessário para remover um patch e que é usado por Adicionar/Remover Programas.
ms.assetid: 09a06de4-0713-4e92-ab29-f34f6c94b677
title: Tabela PatchMetadata (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af760fbe286cf37cdb3aefe389ee8d09d7a759d3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475442"
---
# <a name="patchmetadata-table-patchwizdll"></a>Tabela PatchMetadata (PATCHWIZ.DLL)

A Tabela PatchMetadata contém informações sobre um patch do Windows Installer que é necessário para remover um patch e que é usado por Adicionar/Remover Programas. Todas as propriedades na Tabela PatchMetadata são adicionadas à [Tabela MsiPatchMetadata](msipatchmetadata-table.md) do arquivo .msp para um patch.

A Tabela PatchMetadata é necessária nos arquivos de propriedades de criação de patch (arquivos .pcp) que têm um MinimumRequiredMsiVersion igual a 300 na [Tabela de Propriedades](properties-table-patchwiz-dll-.md). A tabela será opcional se MinimumRequiredMsiVersion não for igual a 300.

A Tabela PatchMetadata tem as seguintes colunas.



| Coluna   | Tipo | Chave | Nullable |
|----------|------|-----|----------|
| Empresa  | text | S   | S        |
| Propriedade | text | S   | N        |
| Valor    | text |     | S        |



 

### <a name="columns"></a>Colunas

<dl> <dt>

<span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Empresa
</dt> <dd>

O nome da empresa. Um campo vazio (um valor Nulo) indica que essa linha contém uma das propriedades de metadados padrão. Uma empresa pode estender o conjunto de propriedades adicionando uma linha à tabela e inserindo um nome da empresa nesse campo.

</dd> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriedade
</dt> <dd>

O nome de uma propriedade de metadados. As propriedades AllowRemoval, ManufacturerName, TargetProductName, MoreInfoURL, DisplayName, Description e Classification são necessárias na Tabela PatchMetadata . Esse campo deverá conter uma das seguintes propriedades de metadados padrão se o campo Empresa estiver vazio (um valor Nulo).




| Propriedade | Descrição | 
|----------|-------------|
| AllowRemoval | Um valor inteiro que indica se o patch é ou não um Patch <a href="uninstallable-patches.md">Desinstalável.</a> Se o campo Valor contiver um 0 (zero), o patch não poderá ser removido. Se o campo Valor contiver 1 (um), o patch será um Patch Desinstalável. Essa propriedade é necessária. Essa propriedade é registrada e seu valor pode ser obtido usando a <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>função MsiGetPatchInfoEx.</strong></a><br /> | 
| ManufacturerName | Um valor de cadeia de caracteres que contém o nome do fabricante do aplicativo. Esta propriedade é necessária. | 
| MinorUpdateTargetRTM | Indica que o patch tem como destino a versão RTM do produto ou o patch de atualização principal mais recente. Autorize essa propriedade opcional em patches de atualização secundários que contêm informações de sequenciamento para indicar que o patch remove todos os patches até a versão RTM do produto ou até o patch de atualização principal mais recente. Essa propriedade está disponível a partir do Windows Installer 3.1.<blockquote>[!Note]<br />Para exigir que Windows Instalador 3.1 seja instalado para aplicar o patch, de definir a propriedade MinimumRequiredMsiVersion como 310 na Tabela de Propriedades do arquivo .pcp. <a href="properties-table-patchwiz-dll-.md"></a></blockquote><br /><br /> | 
| TargetProductName | Um valor de cadeia de caracteres que contém o nome do aplicativo ou do pacote de aplicativos de destino. Esta propriedade é necessária. | 
| MoreInfoURL | Um valor de cadeia de caracteres que contém uma URL que aponta para informações para esse patch. Essa propriedade necessária é registrada e seu valor pode ser obtido usando a <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>função MsiGetPatchInfoEx.</strong></a> Começando com Windows XP com Service Pack 2 (SP2), esse valor pode ser o link de suporte para o patch exibido em Adicionar/Remover Programas.<br /> | 
| Creationtimeutc | Um valor de cadeia de caracteres que contém a hora de criação do arquivo .msp no formato mm-dd-aa HH:MM (month-day-year hour:minute). Esta propriedade é opcional. | 
| DisplayName | Um valor de cadeia de caracteres que contém o título do patch adequado para exibição pública. Esta propriedade é necessária. Essa propriedade é registrada e seu valor pode ser obtido usando a <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>função MsiGetPatchInfoEx.</strong></a> Começando com Windows XP com SP2, esse valor é o nome do patch exibido em Adicionar/Remover Programas começando com Windows XP com SP2.<br /> | 
| Descrição | Um valor de cadeia de caracteres que contém uma breve descrição do patch. Esta propriedade é necessária. | 
| classificação | Um valor de cadeia de caracteres que contém a categoria arbitrária de atualizações, conforme definido pelo autor do patch. Por exemplo, os autores de patch podem especificar que cada patch seja classificado como um Hotfix, Rollup de Segurança, Atualização Crítica, Atualização, Service Pack ou Pacote De Atualização. Esta propriedade é necessária. | 
| OptimizedInstallMode | Se essa propriedade for definida como 1 (um) em todos os patches a serem aplicados em uma transação, o aplicativo do patch será otimizado, se possível. Para obter informações, consulte <a href="patch-optimization.md">Otimização de patch</a>. Disponível a partir do Windows Instalador 3.1. | 




 

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Valor da propriedade de metadados. Isso nunca pode ser Nulo ou uma cadeia de caracteres vazia. Esse valor pode ser localizado.

</dd> </dl>

### <a name="remarks"></a>Comentários

Disponível a partir do Windows Instalador 3.0.

Todas as propriedades autoradas na Tabela PatchMetadata são adicionadas à tabela MsiPatchMetadata do arquivo msp. As propriedades AllowRemoval, MoreInfoURL e DisplayName são registradas e podem ser acessadas por [**meio do MsiGetPatchInfoEx.**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)

 

 




