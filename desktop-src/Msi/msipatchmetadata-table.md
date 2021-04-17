---
description: A tabela MsiPatchMetadata contém informações sobre um patch Windows Installer necessário para remover o patch e que é usado por adicionar ou remover programas.
ms.assetid: b1c30e16-6c91-451a-8b75-7ddbcefcc092
title: Tabela MsiPatchMetadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2642661a8f9dc067086926f8e993fc32c95a4a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747753"
---
# <a name="msipatchmetadata-table"></a>Tabela MsiPatchMetadata

A tabela MsiPatchMetadata contém informações sobre um patch Windows Installer necessário para remover o patch e que é usado por **Adicionar ou remover programas**.

Os patches instalados sem esta tabela presentes no banco de dados de patch (arquivo. msp) não podem ser removidos e estão faltando algumas informações em **Adicionar ou remover programas**. A tabela deve estar no banco de dados do arquivo de patch e não em uma transformação no patch.

A tabela MsiPatchMetadata tem as colunas a seguir.



| Coluna   | Tipo                         | Chave | Nullable |
|----------|------------------------------|-----|----------|
| Empresa  | [Identificador](identifier.md) | S   | S        |
| Propriedade | [Identificador](identifier.md) | S   | N        |
| Valor    | [Text](text.md)             | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Corporativa
</dt> <dd>

O nome da empresa. Um campo vazio (um valor nulo) indica que a linha contém uma das propriedades de metadados padrão do Windows Installer. Para obter mais informações, consulte a seção comentários deste tópico.

Ao adicionar uma linha à tabela e inserir um nome de empresa neste campo, você pode adicionar qualquer empresa para estender o conjunto de propriedades.

</dd> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriedade
</dt> <dd>

O nome de uma propriedade de metadados.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

O valor da propriedade de metadados. Isso nunca pode ser nulo ou uma cadeia de caracteres vazia.

</dd> </dl>

## <a name="remarks"></a>Comentários

Disponível no Windows Installer 3,0 e posterior.

As linhas na tabela MsiPatchMetadata que contêm um valor nulo no campo CompanyName referem-se a uma das propriedades de metadados de Windows Installer padrão a seguir.



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
<td>Indica se o patch é um <a href="uninstallable-patches.md">patch desinstalável</a>ou não. Se o campo de valor contiver 0 (zero), o patch não poderá ser removido. Se o campo de valor contiver um (1), o patch será um patch desinstalável. essa propriedade é registrada e seu valor pode ser obtido usando a função <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> . <br/></td>
</tr>
<tr class="even">
<td>ManufacturerName</td>
<td>Nome do fabricante do aplicativo.</td>
</tr>
<tr class="odd">
<td>MinorUpdateTargetRTM</td>
<td>Indica que o patch destina-se à versão RTM do produto ou ao patch de atualização principal mais recente. Crie essa propriedade opcional em patches de atualização secundárias que contenham informações de sequenciamento para indicar que o patch remove todos os patches até a versão RTM do produto ou até o patch de atualização principal mais recente. Essa propriedade está disponível no Windows Installer 3,1 e posterior. <br/></td>
</tr>
<tr class="even">
<td>TargetProductName</td>
<td>Nome do aplicativo ou conjunto de aplicativos de destino.</td>
</tr>
<tr class="odd">
<td>MoreInfoURL</td>
<td>Uma URL que fornece informações específicas para esse patch. Essa propriedade é registrada e seu valor pode ser obtido usando a função <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> . A partir do Windows XP com Service Pack 2 (SP2), esse valor pode ser o link de suporte para o patch exibido em <strong>Adicionar ou remover programas</strong>.<br/></td>
</tr>
<tr class="even">
<td>CreationTimeUTC</td>
<td>Hora de criação do arquivo. msp no formato mm-dd-aa HH: MM (mês-dia-ano hora: minuto).</td>
</tr>
<tr class="odd">
<td>DisplayName</td>
<td>Um título para o patch que é OK para a exibição pública. Essa propriedade é registrada e seu valor pode ser obtido usando a função <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> . A partir do Windows XP com SP2, esse valor é o nome do patch exibido em <strong>Adicionar ou remover programas</strong>.<br/></td>
</tr>
<tr class="even">
<td>Descrição</td>
<td>Breve descrição do patch.</td>
</tr>
<tr class="odd">
<td>classificação</td>
<td>Um valor de cadeia de caracteres que contém a categoria arbitrária de atualizações, conforme definido pelo autor do patch. Por exemplo, os autores de patch podem especificar que cada patch seja classificado como um hotfix, ROLLUP de segurança, atualização crítica, atualização, Service Pack ou pacote cumulativo de atualizações. Esta propriedade é necessária.</td>
</tr>
<tr class="even">
<td>OptimizeCA</td>
<td>Indica se o Windows Installer deve ignorar ações personalizadas ao aplicar o patch. Isso pode reduzir o tempo necessário para aplicar o patch. A propriedade OptimizeCA pode ter um dos seguintes valores:<br/>
<ul>
<li>0-não ignore nenhuma ação personalizada.</li>
<li>1-ignorar ações personalizadas de atribuição de propriedade e de diretório. O <a href="custom-action-type-35.md">tipo de ação personalizada 35</a> e o <a href="custom-action-type-51.md">tipo de ação personalizada 51</a> podem ser ações personalizadas de atribuição de diretório e propriedade.</li>
<li>2-ignorar ações personalizadas imediatas que não se enquadram nas atribuições de propriedade ou de diretório. As ações personalizadas imediatas não incluem a opção msidbCustomActionTypeInScript na coluna Type da <a href="customaction-table.md">tabela CustomAction</a>.</li>
<li>4-ignorar ações personalizadas que são executadas no script.</li>
</ul>
O valor de OptimizeCA deve ser o mesmo para todos os patches que estão sendo instalados ou nenhuma ação personalizada é ignorada. Por exemplo, se dois patches estiverem sendo instalados e OptimizeCA for definido para os valores 1 e 2, respectivamente, nenhuma ação personalizada será ignorada. <br/> Os valores de OptimizeCA podem ser combinados ao processar vários novos patches. Se todos os patches tiverem um (um) incluído nos valores, todas as ações personalizadas de atribuição de propriedades e de diretórios serão ignoradas. Se um patch tiver o valor 3 (três) para a propriedade e um patch tiver o valor 1 (um) para a propriedade, as ações personalizadas de atribuição de diretório e propriedade serão ignoradas. No entanto, as outras ações personalizadas imediatas são executadas, pois nem todos os patches solicitados são ignorados. <br/></td>
</tr>
<tr class="odd">
<td>OptimizedInstallMode</td>
<td>Se essa propriedade for definida como 1 (uma) em todos os patches a serem aplicados em uma transação, um aplicativo do patch será otimizado, se possível. Para obter mais informações, consulte <a href="patch-optimization.md">otimização de patch</a>. Disponível a partir do Windows Installer 3,1.</td>
</tr>
</tbody>
</table>



 

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




