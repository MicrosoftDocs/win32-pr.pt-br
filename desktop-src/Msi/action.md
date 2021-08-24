---
description: A propriedade ACTION pode ser definida com os valores a seguir.
ms.assetid: f2c436b6-ebd9-4ac4-8609-f54129023ca7
title: Propriedade ACTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b4f17c7bd08b2e366fa23a55ad2b8044ce845ac4df04d0164ba34ad6dff32b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145989"
---
# <a name="action-property"></a>Propriedade ACTION

A **propriedade ACTION** pode ser definida com os valores a seguir.

## <a name="value"></a>Valor



| Valor                                                                                                                                            | Significado                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="INSTALL"></span><span id="install"></span><dl> <dt>**Instalar**</dt> </dl>       | [Ação INSTALL](install-action.md)<br/>     |
| <span id="ADVERTISE"></span><span id="advertise"></span><dl> <dt>**Anunciar**</dt> </dl> | [Ação ADVERTISE](advertise-action.md)<br/> |
| <span id="ADMIN"></span><span id="admin"></span><dl> <dt>**Admin**</dt> </dl>             | [Ação admin](admin-action.md)<br/>         |



 

A **propriedade ACTION** determina qual ação executar se um nome de ação Null for fornecido para [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) ou o Método [**DoAction**](session-doaction.md). Se nenhum valor for definido para a **propriedade ACTION,** o instalador chamará a [ação INSTALL](install-action.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




