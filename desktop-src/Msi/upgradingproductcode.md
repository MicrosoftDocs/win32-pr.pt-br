---
description: a propriedade UPGRADINGPRODUCTCODE é definida por Windows Installer quando uma atualização remove um aplicativo.
ms.assetid: 903e4c22-e7ae-47bd-989b-d8c922de8d1a
title: Propriedade UPGRADINGPRODUCTCODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f5b0096878d06c4eb3880ab8d965265b04114bcf4e3d732d8243bb4fb02cc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809506"
---
# <a name="upgradingproductcode-property"></a>Propriedade UPGRADINGPRODUCTCODE

a propriedade **UPGRADINGPRODUCTCODE** é definida por Windows Installer quando uma atualização remove um aplicativo. O instalador define essa propriedade quando executa a [ação RemoveExistingProducts](removeexistingproducts-action.md). Essa propriedade não é definida removendo um aplicativo usando Adicionar ou remover programas no painel de controle. Um aplicativo determina se ele está sendo removido por uma atualização ou adicionar ou remover programas, verificando **UPGRADINGPRODUCTCODE**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




