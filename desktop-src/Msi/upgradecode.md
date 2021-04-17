---
description: A propriedade UpgradeCode é um GUID que representa um conjunto de produtos relacionado. O UpgradeCode é usado na tabela de atualização para pesquisar versões relacionadas do produto que já estão instaladas. Essa propriedade é usada pela ação RegisterProduct.
ms.assetid: 6cdee5d8-8aa0-4fad-9338-152ee33b8077
title: Propriedade UpgradeCode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1e5493ad651e609f6ef9d7ae14e07c0c15b5b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751178"
---
# <a name="upgradecode-property"></a>Propriedade UpgradeCode

A propriedade **UpgradeCode** é um GUID que representa um conjunto de produtos relacionado. O **UpgradeCode** é usado na [tabela de atualização](upgrade-table.md) para pesquisar versões relacionadas do produto que já estão instaladas.

Essa propriedade é usada pela [ação RegisterProduct](registerproduct-action.md).

## <a name="remarks"></a>Comentários

É altamente recomendável que os autores de pacotes de instalação especifiquem um **UpgradeCode** para seu aplicativo.

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

[Preparando um aplicativo para atualizações principais futuras](preparing-an-application-for-future-major-upgrades.md)
</dt> </dl>

 

 




