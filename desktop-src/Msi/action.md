---
description: A propriedade ACTION pode ser definida com os valores a seguir.
ms.assetid: f2c436b6-ebd9-4ac4-8609-f54129023ca7
title: Propriedade de ação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901061f953ffaed030ff6d3a94f440eada25fc59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749806"
---
# <a name="action-property"></a>Propriedade de ação

A propriedade **Action** pode ser definida com os valores a seguir.

## <a name="value"></a>Valor



| Valor                                                                                                                                            | Significado                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="INSTALL"></span><span id="install"></span><dl> <dt>**PRÉ-instalação**</dt> </dl>       | [Ação de instalação](install-action.md)<br/>     |
| <span id="ADVERTISE"></span><span id="advertise"></span><dl> <dt>**ANUNCI**</dt> </dl> | [Ação de anúncio](advertise-action.md)<br/> |
| <span id="ADMIN"></span><span id="admin"></span><dl> <dt>**ADM**</dt> </dl>             | [Ação de administrador](admin-action.md)<br/>         |



 

A propriedade **Action** determina qual ação executar se um nome de ação nulo for fornecido para [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) ou para o [**método DoAction**](session-doaction.md). Se nenhum valor for definido para a propriedade **Action** , o instalador chamará a [ação de instalação](install-action.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




