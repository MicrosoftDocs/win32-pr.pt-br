---
description: A propriedade ShellAdvtSupport é definida pelo instalador se a interface IShellLink do sistema der suporte à resolução do descritor de instalador.
ms.assetid: 8c3503c5-2a9c-43ad-8cc5-ea10df39b24d
title: Propriedade ShellAdvtSupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfacc34bfffdde9ce34841030f38c443a243c9923cb70749a27615cccc1c676e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628436"
---
# <a name="shelladvtsupport-property"></a>Propriedade ShellAdvtSupport

A propriedade **ShellAdvtSupport** é definida pelo instalador se a interface [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) do sistema der suporte à resolução do descritor de instalador.

## <a name="remarks"></a>Comentários

Se essa propriedade for definida, a interface [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) do sistema dará suporte à resolução do descritor de instalador. isso tem suporte no Windows 2000 e em sistemas que executam o Internet Explorer 4, 1. Se essa propriedade não for definida, o instalador terá o comportamento padrão de criação de recursos não anunciados durante a instalação, seja localmente ou executado a partir da origem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Suporte de plataforma do anúncio](platform-support-of-advertisement.md)
</dt> </dl>

 

 
