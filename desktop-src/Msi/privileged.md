---
description: A propriedade Privileged indica se a instalação é executada no contexto de privilégios elevados.
ms.assetid: 483ab73a-3ff7-4111-a6b5-eac990d85bd7
title: Propriedade privilegiada
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d28a7079e7ab12b9832447172f1b3b2c8650a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748141"
---
# <a name="privileged-property"></a>Propriedade privilegiada

A propriedade **Privileged** indica se a instalação é executada no contexto de privilégios elevados. O instalador definirá essa propriedade se o usuário tiver privilégios de administrador, se o aplicativo tiver sido atribuído por um administrador de sistema ou se as políticas de usuário e máquina AlwaysInstallElevated estiverem definidas como true.

## <a name="default-value"></a>Valor padrão

O instalador não definirá essa propriedade se o usuário não tiver permissão para instalar com privilégios elevados.

## <a name="remarks"></a>Comentários

Os desenvolvedores de pacotes do instalador podem usar a propriedade **Privileged** para tornar a instalação condicional na diretiva do sistema, o usuário sendo um administrador ou uma atribuição por um administrador.

Ao executar no Windows Vista, o **Privileged** e o [**AdminUser**](adminuser.md) são os mesmos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




