---
description: Definir a propriedade DISABLEMEDIA impede que o instalador Registre qualquer fonte de mídia, como um CD-ROM, como uma fonte válida para o produto. No entanto, se a navegação estiver habilitada, um usuário ainda poderá navegar para uma fonte de mídia.
ms.assetid: 83c4e7f6-fced-447f-bfa2-847dce660139
title: Propriedade DISABLEMEDIA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc1cad17269541fdb60573ae11065d485af9bda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750828"
---
# <a name="disablemedia-property"></a>Propriedade DISABLEMEDIA

Definir a propriedade [**DISABLEMEDIA**](disablemedia.md) impede que o instalador Registre qualquer fonte de mídia, como um CD-ROM, como uma fonte válida para o produto. No entanto, se a navegação estiver habilitada, um usuário ainda poderá navegar para uma fonte de mídia.

## <a name="remarks"></a>Comentários

Observe que a propriedade [**DISABLEMEDIA**](disablemedia.md) tem um efeito diferente de definir a política DISABLEMEDIA. A definição de **DISABLEMEDIA** impede o registro de qualquer fonte de mídia, e isso também impede a primeira instalação de um aplicativo de fontes de mídia.

Para obter detalhes sobre como proteger as fontes de mídia do [*aplicativo gerenciado*](m-gly.md) em busca e instalação por usuários não administrativos, consulte [resiliência de origem](source-resiliency.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




