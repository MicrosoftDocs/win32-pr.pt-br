---
description: A propriedade MSIDEPLOYMENTCOMPLIANT pode ser definida para indicar ao instalador que o pacote foi criado e testado para estar em conformidade com o UAC (controle de conta de usuário) no Windows Vista.
ms.assetid: 7ee0dc56-bb9d-4a6e-aa3e-ae4c83f583d7
title: Propriedade MSIDEPLOYMENTCOMPLIANT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a965b7dce941a3d651e2f9f32e3d8f4993ded33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752845"
---
# <a name="msideploymentcompliant-property"></a>Propriedade MSIDEPLOYMENTCOMPLIANT

A propriedade **MSIDEPLOYMENTCOMPLIANT** pode ser definida para indicar ao instalador que o pacote foi criado e testado para estar em conformidade com o UAC ( [*controle de conta de usuário*](u-gly.md) ) no Windows Vista. Se essa propriedade não for definida, o instalador determinará se o pacote está em conformidade com o UAC no Windows Vista.

Para obter mais informações sobre o UAC e o Windows Installer, consulte [usando o Windows Installer com o UAC](using-windows-installer-with-uac.md) e [diretrizes para pacotes](guidelines-for-packages.md).

**Windows Installer 3,1, Windows Installer 3,0 e Windows Installer 2,0:** Esta propriedade é ignorada. Essa propriedade só é usada pelo Windows Installer 4,0 no Windows Vista.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o mínimo Service Pack exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Sem suporte no Windows Installer 3,1 e versões anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




