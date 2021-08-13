---
description: A propriedade ROOTDRIVE especifica a unidade padrão para o diretório de destino da instalação.
ms.assetid: 9f36dc2a-2fb5-4787-a630-c7cc93ef51ec
title: Propriedade ROOTDRIVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ca4a3230dde5086b1383f3016da30d99976cf6560d0be994ecb0aaccc0ba6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625733"
---
# <a name="rootdrive-property"></a>Propriedade ROOTDRIVE

A propriedade **ROOTDRIVE** especifica a unidade padrão para o diretório de destino da instalação. Se a coluna Directory da [tabela de diretórios](directory-table.md) indicar o diretório de destino raiz por um nome de propriedade que está indefinido, o instalador usará o valor da propriedade **ROOTDRIVE** para resolver o caminho para o diretório de destino.

Se **ROOTDRIVE** não estiver definido em uma linha de comando ou for criado na [tabela de propriedades](property-table.md), o instalador definirá essa propriedade. Durante uma [instalação administrativa](administrative-installation.md) , o instalador define **ROOTDRIVE** para a primeira unidade de rede conectada que pode ser gravada. Se não for uma instalação administrativa ou se o instalador não encontrar unidades de rede, o instalador definirá **ROOTDRIVE** para a unidade local que pode ser gravada para ter mais espaço livre.

O valor desta propriedade deve terminar com ' \\ '.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




