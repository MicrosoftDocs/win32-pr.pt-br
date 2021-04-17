---
description: O valor da propriedade ProductVersion é a versão do produto no formato de cadeia de caracteres.
ms.assetid: 551fca7e-a827-482d-bc56-ff2fe5a17025
title: Propriedade ProductVersion
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01f82fcbd28c4a4132e4c3f76adfd68e33c43b36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748970"
---
# <a name="productversion-property"></a>Propriedade ProductVersion

O valor da propriedade **ProductVersion** é a versão do produto no formato de cadeia de caracteres. Essa propriedade é necessária.

O formato da cadeia de caracteres é o seguinte:

<dl> major.minor.build  
</dl>

O primeiro campo é a versão principal e tem um valor máximo de 255. O segundo campo é a versão secundária e tem um valor máximo de 255. O terceiro campo é chamado de versão de compilação ou versão de atualização e tem um valor máximo de 65.535.

## <a name="remarks"></a>Comentários

Pelo menos um dos três campos de **ProductVersion** deve ser alterado para uma atualização usando a [tabela de atualização](upgrade-table.md). Qualquer atualização que altere apenas o código do pacote, mas deixa o **ProductVersion** e o [**ProductCode**](productcode.md) inalterados é chamado de uma [pequena atualização](small-updates.md). Os campos de três versões são fornecidos principalmente por conveniência. Por exemplo, se você quiser alterar o **ProductVersion**, mas não quiser alterar as versões principal ou secundária, poderá alterar a versão da compilação.

Observe que Windows Installer usa apenas os três primeiros campos da versão do produto. Se você incluir um quarto campo em sua versão do produto, o instalador ignorará o quarto campo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Aplicação de patch e atualizações](patching-and-upgrades.md)
</dt> <dt>

[pequena atualização](small-updates.md)
</dt> </dl>

 

 




