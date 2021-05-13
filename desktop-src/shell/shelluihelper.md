---
description: Implementado pelo shell para ajudar o script e os desenvolvedores de Visual Basic da Microsoft a usar alguns dos recursos disponíveis no Shell. O objeto ShellUIHelper não tem nenhuma propriedade ou evento. Os métodos são fornecidos para adicionar itens ao shell.
title: Objeto ShellUIHelper (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9fffebc8-29b9-4064-b60c-c8c63690a79e
ms.openlocfilehash: b77d618c4c772859a9009f3cca761c59df83257a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842427"
---
# <a name="shelluihelper-object"></a>Objeto ShellUIHelper

Implementado pelo shell para ajudar o script e os desenvolvedores de Visual Basic da Microsoft a usar alguns dos recursos disponíveis no Shell. O objeto **ShellUIHelper** não tem nenhuma propriedade ou evento. Os métodos são fornecidos para adicionar itens ao shell.

## <a name="members"></a>Membros

O objeto **ShellUIHelper** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

O objeto **ShellUIHelper** tem esses métodos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Método</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="shelluihelper-addchannel.md"><strong>Addchannel</strong></a></td>
<td style="text-align: left;">Adiciona um novo canal à lista de canais no menu <strong>favoritos</strong> do Internet Explorer e à barra de <strong>canais</strong> na área de trabalho.<br/>
<blockquote>
[!Note]<br />
Não há mais suporte para esse método no Windows Vista. Nesse sistema operacional, ele retorna E_NOTIMPL.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></td>
<td style="text-align: left;">Adiciona um item à área de trabalho ativa.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shelluihelper-addfavorite.md"><strong>Addfavorito</strong></a></td>
<td style="text-align: left;">Exibe a interface do usuário padrão para criar um item favorito. A interface do usuário é inicializada para os parâmetros especificados.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></td>
<td style="text-align: left;">Indica se uma URL especificada é assinada.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, somente aplicativos da área de trabalho do Windows XP \[\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Exdisp.h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4.71 ou posterior)</dt> </dl> |



 

 




