---
description: A propriedade ROOTDRIVE especifica a unidade padrão para o diretório de destino da instalação.
ms.assetid: 9f36dc2a-2fb5-4787-a630-c7cc93ef51ec
title: Propriedade ROOTDRIVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e16f64b50105727d307867b5ed2910aed042cd28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760832"
---
# <a name="rootdrive-property"></a>Propriedade ROOTDRIVE

A propriedade **ROOTDRIVE** especifica a unidade padrão para o diretório de destino da instalação. Se a coluna Directory da [tabela de diretórios](directory-table.md) indicar o diretório de destino raiz por um nome de propriedade que está indefinido, o instalador usará o valor da propriedade **ROOTDRIVE** para resolver o caminho para o diretório de destino.

Se **ROOTDRIVE** não estiver definido em uma linha de comando ou for criado na [tabela de propriedades](property-table.md), o instalador definirá essa propriedade. Durante uma [instalação administrativa](administrative-installation.md) , o instalador define **ROOTDRIVE** para a primeira unidade de rede conectada que pode ser gravada. Se não for uma instalação administrativa ou se o instalador não encontrar unidades de rede, o instalador definirá **ROOTDRIVE** para a unidade local que pode ser gravada para ter mais espaço livre.

O valor desta propriedade deve terminar com ' \\ '.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




