---
description: O instalador define o valor da propriedade MsiRestartManagerSessionKey como a chave de sessão da sessão do Gerenciador de Reinicialização.
ms.assetid: efbf11f2-38ab-4509-aa01-23fa8cfdaa60
title: Propriedade MsiRestartManagerSessionKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f48fe8d2ce4b287afc5c222acdc1f71eec393ff9a1ab1773a822e30405e6a317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944534"
---
# <a name="msirestartmanagersessionkey-property"></a>Propriedade MsiRestartManagerSessionKey

O instalador define o valor da **propriedade MsiRestartManagerSessionKey** como a chave de sessão da sessão [do Gerenciador de Reinicialização.](../rstmgr/restart-manager-portal.md) Ações personalizadas podem usar a chave de sessão para ingressar na [sessão do Gerenciador de Reinicialização.](../rstmgr/restart-manager-portal.md)

## <a name="remarks"></a>Comentários

O instalador define o valor da propriedade **MsiRestartManagerSessionKey** na inicialização e limpa o valor durante a ação [InstallValidate.](installvalidate-action.md) Ações personalizadas que precisam do valor da **propriedade MsiRestartManagerSessionKey** devem ser feitas antes da ação InstallValidate na sequência de ação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Consulte o [Windows instalador Run-Time requisitos](windows-installer-portal.md) para obter informações sobre o service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Sem suporte no Windows 3.1 e versões anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
