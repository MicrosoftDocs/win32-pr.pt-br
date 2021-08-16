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

A **propriedade ROOTDRIVE** especifica a unidade padrão para o diretório de destino da instalação. Se a coluna [](directory-table.md) Diretório da tabela Diretório indicar o diretório de destino raiz por um nome de propriedade indefinido, o instalador usará o valor da propriedade **ROOTDRIVE** para resolver o caminho para o diretório de destino.

Se **ROOTDRIVE** não estiver definido em uma linha de comando ou criado na tabela [Propriedade](property-table.md), o instalador definirá essa propriedade. Durante uma [instalação administrativa,](administrative-installation.md) o instalador define **ROOTDRIVE** como a primeira unidade de rede conectada que ele encontra que pode ser gravado. Se não for uma instalação administrativa ou se o instalador não puder encontrar nenhuma unidade de rede, o instalador define **ROOTDRIVE** como a unidade local que pode ser escrita para ter mais espaço livre.

O valor dessa propriedade deve terminar com ' \\ '.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




