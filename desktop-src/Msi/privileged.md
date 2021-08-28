---
description: A propriedade Privileged indica se a instalação é executada no contexto de privilégios elevados.
ms.assetid: 483ab73a-3ff7-4111-a6b5-eac990d85bd7
title: Propriedade privilegiada
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfe61f17e5ef3453021c98bac8eb383171a678adfb204886ecdaa840e0df832
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129126"
---
# <a name="privileged-property"></a>Propriedade privilegiada

A propriedade **Privileged** indica se a instalação é executada no contexto de privilégios elevados. O instalador definirá essa propriedade se o usuário tiver privilégios de administrador, se o aplicativo tiver sido atribuído por um administrador de sistema ou se as políticas de usuário e máquina AlwaysInstallElevated estiverem definidas como true.

## <a name="default-value"></a>Valor padrão

O instalador não definirá essa propriedade se o usuário não tiver permissão para instalar com privilégios elevados.

## <a name="remarks"></a>Comentários

Os desenvolvedores de pacotes do instalador podem usar a propriedade **Privileged** para tornar a instalação condicional na diretiva do sistema, o usuário sendo um administrador ou uma atribuição por um administrador.

ao executar o Windows Vista, os **privilégios** e [**AdminUser**](adminuser.md) são os mesmos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




