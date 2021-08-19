---
description: O instalador define a propriedade AFTERREBOOT como 1 após uma reinicialização invocada pela ação ForceReboot. O instalador adiciona AFTERREBOOT=1 à linha de comando executado imediatamente após a reinicialização.
ms.assetid: d8a71d9a-64bf-4a38-9c3b-073c216de7fa
title: Propriedade AFTERREBOOT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf8fb80a3d8ff167f93aab6c95fc3eadb8b5312daf9d2a2856f01cb7d01ee383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145909"
---
# <a name="afterreboot-property"></a>Propriedade AFTERREBOOT

O instalador define a **propriedade AFTERREBOOT** como 1 após uma reinicialização invocada pela [ação ForceReboot](forcereboot-action.md). O instalador adiciona AFTERREBOOT=1 à linha de comando executado imediatamente após a reinicialização.

## <a name="remarks"></a>Comentários

A [ação ForceReboot](forcereboot-action.md) sempre deve ser usada com uma instrução condicional, de forma que o instalador acione uma reinicialização somente quando necessário. Uma reinicialização poderá ser necessária se um arquivo específico tiver sido substituído ou um componente específico tiver sido instalado. O caso é diferente para cada produto e uma ação personalizada pode ser necessária para determinar se uma reinicialização é necessária. A condição na ação ForceReboot normalmente usa a **propriedade AFTERREBOOT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Reinicializações do sistema](system-reboots.md)
</dt> </dl>

 

 




