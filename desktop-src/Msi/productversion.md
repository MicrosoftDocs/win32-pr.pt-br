---
description: O valor da propriedade ProductVersion é a versão do produto no formato de cadeia de caracteres.
ms.assetid: 551fca7e-a827-482d-bc56-ff2fe5a17025
title: Propriedade ProductVersion
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e09d2fb436dffba5ae2fa98144d39e5824d09796472297db116a2a4543d55168
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074636"
---
# <a name="productversion-property"></a>Propriedade ProductVersion

O valor da propriedade **ProductVersion** é a versão do produto no formato de cadeia de caracteres. Essa propriedade é REQUIRED.

O formato da cadeia de caracteres é o seguinte:

<dl> major.minor.build  
</dl>

O primeiro campo é a versão principal e tem um valor máximo de 255. O segundo campo é a versão secundária e tem um valor máximo de 255. O terceiro campo é chamado de versão de build ou versão de atualização e tem um valor máximo de 65.535.

## <a name="remarks"></a>Comentários

Pelo menos um dos três campos de **ProductVersion** deve ser altere para uma atualização usando a [tabela Upgrade](upgrade-table.md). Qualquer atualização que altere apenas o código do pacote, mas **deixa ProductVersion e** [**ProductCode**](productcode.md) inalterados, é chamada de [pequena atualização.](small-updates.md) Os três campos de versões são fornecidos principalmente para conveniência. Por exemplo, se você quiser alterar **ProductVersion**, mas não quiser alterar as versões principais ou secundárias, poderá alterar a versão de build.

Observe que Windows Instalador usa apenas os três primeiros campos da versão do produto. Se você incluir um quarto campo em sua versão do produto, o instalador ignorará o quarto campo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[A patch e as atualizações](patching-and-upgrades.md)
</dt> <dt>

[pequena atualização](small-updates.md)
</dt> </dl>

 

 




