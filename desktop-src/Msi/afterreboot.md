---
description: O instalador define a propriedade AFTERREBOOT como 1 após uma reinicialização invocada pela ação ForceReboot. O instalador adiciona AFTERREBOOT = 1 à linha de comando executar imediatamente após a reinicialização.
ms.assetid: d8a71d9a-64bf-4a38-9c3b-073c216de7fa
title: Propriedade AFTERREBOOT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa891c84e2e8f7bdea5bb90311e9706a37e46e31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752467"
---
# <a name="afterreboot-property"></a>Propriedade AFTERREBOOT

O instalador define a propriedade **AFTERREBOOT** como 1 após uma reinicialização invocada pela [ação ForceReboot](forcereboot-action.md). O instalador adiciona AFTERREBOOT = 1 à linha de comando executar imediatamente após a reinicialização.

## <a name="remarks"></a>Comentários

A [ação ForceReboot](forcereboot-action.md) sempre deve ser usada com uma instrução condicional, de modo que o instalador disparará uma reinicialização somente quando necessário. Uma reinicialização poderá ser necessária se um determinado arquivo tiver sido substituído ou um componente específico tiver sido instalado. O caso é diferente para cada produto e uma ação personalizada pode ser necessária para determinar se uma reinicialização é necessária. A condição na ação ForceReboot normalmente usa a propriedade **AFTERREBOOT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Reinicializações do sistema](system-reboots.md)
</dt> </dl>

 

 




