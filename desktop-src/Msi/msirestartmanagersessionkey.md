---
description: O instalador define o valor da propriedade MsiRestartManagerSessionKey para a chave de sessão para a sessão do Gerenciador de reinicialização.
ms.assetid: efbf11f2-38ab-4509-aa01-23fa8cfdaa60
title: Propriedade MsiRestartManagerSessionKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489095e0af617c7ae403811f0eab800c5502e3bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750799"
---
# <a name="msirestartmanagersessionkey-property"></a>Propriedade MsiRestartManagerSessionKey

O instalador define o valor da propriedade **MsiRestartManagerSessionKey** para a chave de sessão para a sessão do [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) . As ações personalizadas podem usar a chave de sessão para ingressar na sessão do [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) .

## <a name="remarks"></a>Comentários

O instalador define o valor da propriedade **MsiRestartManagerSessionKey** na inicialização e, em seguida, limpa o valor durante a ação [InstallValidate](installvalidate-action.md) . Ações personalizadas que precisam do valor da propriedade **MsiRestartManagerSessionKey** devem vir antes da ação InstallValidate na sequência de ação.

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

 

 
