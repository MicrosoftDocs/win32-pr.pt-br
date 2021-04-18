---
description: A propriedade MSIARPSETTINGSIDENTIFIER contém uma lista delimitada por ponto e vírgula dos locais do registro onde o aplicativo armazena as configurações e preferências de um usuário.
ms.assetid: 524ba004-d3a2-4619-8c98-362761a3ae7a
title: Propriedade MSIARPSETTINGSIDENTIFIER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a32c979237e6443bec5451f36e36ef49ae4a1f59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753440"
---
# <a name="msiarpsettingsidentifier-property"></a>Propriedade MSIARPSETTINGSIDENTIFIER

A propriedade **MSIARPSETTINGSIDENTIFIER** contém uma lista delimitada por ponto e vírgula dos locais do registro onde o aplicativo armazena as configurações e preferências de um usuário. Durante uma atualização do sistema operacional, a instalação pode usar essas informações para melhorar a experiência de usuários que estão migrando aplicativos.

O valor da propriedade **MSIARPSETTINGSIDENTIFIER** é um texto literal que contém a lista de locais de registro onde o aplicativo armazena suas configurações. O valor pode especificar vários locais de registro possíveis. Separe vários locais de registro usando ponto e vírgula. As configurações de aplicativo normalmente são armazenadas nos hives do registro **HKCU** ou **HKLM** no formato *: \\ \\ versão do aplicativo da empresa*. O exemplo a seguir é um valor possível para a propriedade **MSIARPSETTINGSIDENTIFIER** .

*MyCompany \\ AppSuite \\ 1,0; MyCompany \\ App1 \\ 1,0; MyCompany \\ App2 \\ 1,0*

Essa propriedade é opcional e pode ser definida na tabela de [Propriedades](property-table.md) . Se essa propriedade aparecer na tabela de propriedades, o valor não deverá ser definido como **nulo**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer 4,5 no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Sem suporte no Windows Installer 3,1 e versões anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




