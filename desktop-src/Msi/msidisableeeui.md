---
description: Para desabilitar a interface do usuário inserida para a instalação definida na tabela MsiEmbeddedUI, defina a propriedade MSIDISABLEEEUI como 1 na linha de comando.
ms.assetid: c5ada690-c5dd-455f-babe-8c09750525c4
title: Propriedade MSIDISABLEEEUI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d89ce43f649d406e4ae086db236375c02c43e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757511"
---
# <a name="msidisableeeui-property"></a>Propriedade MSIDISABLEEEUI

Para desabilitar a interface do usuário inserida para a instalação definida na [tabela MsiEmbeddedUI](msiembeddedui-table.md), defina a propriedade MSIDISABLEEEUI como 1 na linha de comando.

**[Windows Installer 4,0 e anteriores](not-supported-in-windows-installer-4-0.md):** Sem suporte. Versões anteriores a Windows Installer 4,5 ignoram a propriedade MSIDISABLEEEUI.

## <a name="remarks"></a>Comentários

Em uma instalação de vários pacotes, um pacote filho normalmente deve usar a interface do usuário do pacote pai e não inicializar sua própria interface de usuários inserida. Se a propriedade MSIDISABLEEEUI não estiver definida dentro do pacote pai, o pacote filho usará a interface do usuário inserida do pacote pai por padrão e ignorará a propriedade MSIDISABLEEEUI dentro do pacote filho.

A propriedade MSIDISABLEEEUI desabilita a interface do usuário incorporada para um único pacote. Você pode usar a política [MsiDisableEmbeddedUI](msidisableembeddedui.md) para desabilitar interfaces de usuário inseridas para todos os pacotes no computador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,5 no Windows Server 2008, no Windows Vista, no Windows Server 2003 e no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




