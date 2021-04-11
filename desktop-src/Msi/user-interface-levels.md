---
description: O Windows Installer fornece aos desenvolvedores de pacotes a capacidade de criar uma interface de usuário interna que tem vários níveis de funcionalidade.
ms.assetid: 9f5796a7-e244-4fc8-af85-52a147bb2c0b
title: Níveis de interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a835d1b11a4db4393041e83c1b1dc885018610f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172004"
---
# <a name="user-interface-levels"></a>Níveis de interface do usuário

O Windows Installer fornece aos desenvolvedores de pacotes a capacidade de criar uma interface de usuário interna que tem vários níveis de funcionalidade. Como a interface do usuário interna deve ser criada pelo autor do pacote, o comportamento da interface do usuário completa, da interface do usuário reduzida, da interface do usuário básica e de nenhum nível depende do pacote de instalação. A tabela a seguir descreve a funcionalidade comumente astranscrita aos níveis de interface do usuário.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nível da interface do usuário</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>IU completa</td>
<td>Exibe caixas de diálogo modais e sem janela restrita que foram criadas na interface do usuário interna. Exibe caixas de <a href="error-dialog.md">diálogo de erro</a> criadas.
<blockquote>
[!Note]<br />
As caixas de diálogo modais exigem a entrada do usuário para que a instalação possa continuar e é especificada pela configuração do <a href="modal-dialog-style-bit.md">bit do estilo da caixa de diálogo modal</a> na coluna atributos da tabela de <a href="dialog-table.md">diálogo</a> . Uma caixa de diálogo sem janela restrita não exige a entrada do usuário para que a instalação continue.
</blockquote>
<br/> Uma interface de usuário completa normalmente exibe o <a href="user-interface-wizard-behavior.md">comportamento do assistente de interface do usuário</a>.<br/></td>
</tr>
<tr class="even">
<td>Interface do usuário reduzida</td>
<td>Exibe qualquer caixa de diálogo sem janela restrita que tenha sido criada na interface do usuário. Não exibe nenhuma caixa de diálogo modal criada. Exibe caixas de <a href="error-dialog.md">diálogo de erro</a> criadas. Exibe mensagens de <a href="authoring-disk-prompt-messages.md">prompt de disco</a> . Exibe caixas de <a href="filesinuse-dialog.md">diálogo FilesInUse</a> .</td>
</tr>
<tr class="odd">
<td>Interface do usuário básica</td>
<td>Exibe as caixas de diálogo do modelo interno que mostram as mensagens de progresso. Exibe caixas de diálogo de erro internas. Não exibe nenhuma caixa de diálogo criada. Solicita que os usuários insiram um disco exibindo uma caixa de diálogo contendo o valor da propriedade <a href="diskprompt.md"><strong>DiskPrompt</strong></a> .</td>
</tr>
<tr class="even">
<td>Nenhum</td>
<td>Nenhum significa uma instalação silenciosa que não exibe nenhuma interface do usuário.</td>
</tr>
</tbody>
</table>



 

O nível da interface do usuário interna pode ser definido usando [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui). O instalador define a propriedade [**UILevel**](uilevel.md) para o nível atual da interface do usuário.

Se a propriedade [**LIMITUI**](limitui.md) for definida, o nível da interface do usuário usada ao instalar o pacote será restrito ao básico.

Para obter um exemplo de criação de interface do usuário, consulte [um exemplo de instalação](an-installation-example.md).

 

 




