---
description: a propriedade MSIDEPLOYMENTCOMPLIANT pode ser definida para indicar ao instalador que o pacote foi criado e testado para estar em conformidade com o UAC (controle de conta de usuário) no Windows Vista.
ms.assetid: 7ee0dc56-bb9d-4a6e-aa3e-ae4c83f583d7
title: Propriedade MSIDEPLOYMENTCOMPLIANT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cd1cea551c68858b4286e168862488e6d3361bfc501001b491ec9e655537185
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077946"
---
# <a name="msideploymentcompliant-property"></a>Propriedade MSIDEPLOYMENTCOMPLIANT

a propriedade **MSIDEPLOYMENTCOMPLIANT** pode ser definida para indicar ao instalador que o pacote foi criado e testado para estar em conformidade com o UAC ( [*controle de conta de usuário*](u-gly.md) ) no Windows Vista. se essa propriedade não for definida, o instalador determinará se o pacote está em conformidade com o UAC no Windows Vista.

para obter mais informações sobre o uac e o Windows Installer, consulte [usando o Windows Installer com o uac](using-windows-installer-with-uac.md) e [diretrizes para pacotes](guidelines-for-packages.md).

**Windows Installer 3,1, Windows Installer 3,0 e Windows Installer 2,0:** Esta propriedade é ignorada. essa propriedade só é usada pelo Windows Installer 4,0 no Windows Vista.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o mínimo service pack exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[sem suporte no Windows Installer 3,1 e versões anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




