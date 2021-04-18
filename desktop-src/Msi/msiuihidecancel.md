---
description: Essa propriedade Windows Installer indica quando o nível da interface do usuário interna foi definido para ocultar o botão Cancelar.
ms.assetid: 0e842bee-32c2-41ae-97f3-bc8b34960a44
title: Propriedade MsiUIHideCancel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a25a940921dd4b0d91155765ee6768ec0d6d2bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768726"
---
# <a name="msiuihidecancel-property"></a>Propriedade MsiUIHideCancel

O instalador define a propriedade **MsiUIHideCancel** como 1 quando o nível da interface do usuário interna tiver sido definido para incluir INSTALLUILEVEL \_ HIDECANCEL com a função [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) ou a propriedade [UILevel](installer-uilevel.md)do objeto do [**instalador**](installer-object.md) ou usando opções de [linha de comando](command-line-options.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer 3,0 ou posterior no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




