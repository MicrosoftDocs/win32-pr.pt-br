---
description: A propriedade UPGRADINGPRODUCTCODE é definida por Windows Installer quando uma atualização remove um aplicativo.
ms.assetid: 903e4c22-e7ae-47bd-989b-d8c922de8d1a
title: Propriedade UPGRADINGPRODUCTCODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a256ade7f03275752ad4d176e64cd9d0fa12ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751832"
---
# <a name="upgradingproductcode-property"></a>Propriedade UPGRADINGPRODUCTCODE

A propriedade **UPGRADINGPRODUCTCODE** é definida por Windows Installer quando uma atualização remove um aplicativo. O instalador define essa propriedade quando executa a [ação RemoveExistingProducts](removeexistingproducts-action.md). Essa propriedade não é definida removendo um aplicativo usando Adicionar ou remover programas no painel de controle. Um aplicativo determina se ele está sendo removido por uma atualização ou adicionar ou remover programas, verificando **UPGRADINGPRODUCTCODE**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




