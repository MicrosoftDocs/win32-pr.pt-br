---
description: Para desabilitar a interface do usuário inserida para a instalação definida na tabela MsiEmbeddedUI, defina a propriedade MSIDISABLEEEUI como 1 na linha de comando.
ms.assetid: c5ada690-c5dd-455f-babe-8c09750525c4
title: Propriedade MSIDISABLEEEUI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb1e599ed0786c7d2c55644eb5759db3917757d3b41f6107161d72a3cc559484
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039946"
---
# <a name="msidisableeeui-property"></a>Propriedade MSIDISABLEEEUI

Para desabilitar a interface do usuário inserida para a instalação definida na [tabela MsiEmbeddedUI](msiembeddedui-table.md), defina a propriedade MSIDISABLEEEUI como 1 na linha de comando.

**[Windows Installer 4,0 e anteriores](not-supported-in-windows-installer-4-0.md):** Sem suporte. versões anteriores a Windows Installer 4,5 ignoram a propriedade MSIDISABLEEEUI.

## <a name="remarks"></a>Comentários

Em uma instalação de vários pacotes, um pacote filho normalmente deve usar a interface do usuário do pacote pai e não inicializar sua própria interface de usuários inserida. Se a propriedade MSIDISABLEEEUI não estiver definida dentro do pacote pai, o pacote filho usará a interface do usuário inserida do pacote pai por padrão e ignorará a propriedade MSIDISABLEEEUI dentro do pacote filho.

A propriedade MSIDISABLEEEUI desabilita a interface do usuário incorporada para um único pacote. Você pode usar a política [MsiDisableEmbeddedUI](msidisableembeddedui.md) para desabilitar interfaces de usuário inseridas para todos os pacotes no computador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows instalador 4,5 no Windows server 2008, Windows Vista, Windows server 2003 e Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




