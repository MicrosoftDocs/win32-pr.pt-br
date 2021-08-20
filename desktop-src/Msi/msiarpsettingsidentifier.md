---
description: A propriedade MSIARPSETTINGSIDENTIFIER contém uma lista delimitada por ponto e vírgula dos locais do registro onde o aplicativo armazena as configurações e preferências de um usuário.
ms.assetid: 524ba004-d3a2-4619-8c98-362761a3ae7a
title: Propriedade MSIARPSETTINGSIDENTIFIER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7944d1f372437342ba193ea1c9b3d15f6ae21067096da0a41df2ccdd5d527c3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804490"
---
# <a name="msiarpsettingsidentifier-property"></a>Propriedade MSIARPSETTINGSIDENTIFIER

A propriedade **MSIARPSETTINGSIDENTIFIER** contém uma lista delimitada por ponto e vírgula dos locais do registro onde o aplicativo armazena as configurações e preferências de um usuário. Durante uma atualização do sistema operacional, a instalação pode usar essas informações para melhorar a experiência de usuários que estão migrando aplicativos.

O valor da propriedade **MSIARPSETTINGSIDENTIFIER** é um texto literal que contém a lista de locais de registro onde o aplicativo armazena suas configurações. O valor pode especificar vários locais de registro possíveis. Separe vários locais de registro usando ponto e vírgula. As configurações de aplicativo normalmente são armazenadas nos hives do registro **HKCU** ou **HKLM** no formato *: \\ \\ versão do aplicativo da empresa*. O exemplo a seguir é um valor possível para a propriedade **MSIARPSETTINGSIDENTIFIER** .

*MyCompany \\ AppSuite \\ 1,0; MyCompany \\ App1 \\ 1,0; MyCompany \\ App2 \\ 1,0*

Essa propriedade é opcional e pode ser definida na tabela de [Propriedades](property-table.md) . Se essa propriedade aparecer na tabela de propriedades, o valor não deverá ser definido como **nulo**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador 4,5 no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[sem suporte no Windows Installer 3,1 e versões anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




