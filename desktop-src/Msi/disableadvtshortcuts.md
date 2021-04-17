---
description: A definição da propriedade DISABLEADVTSHORTCUTS desabilita a geração de atalhos que dão suporte à instalação sob demanda e ao anúncio. Definir essa propriedade especifica que esses atalhos devem ser substituídos por atalhos regulares.
ms.assetid: 1b55ecbe-932f-4f08-98b1-8c5e7a57d2e8
title: Propriedade DISABLEADVTSHORTCUTS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c3f7d2cf800745691dde6011e6ab62232b94117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747982"
---
# <a name="disableadvtshortcuts-property"></a>Propriedade DISABLEADVTSHORTCUTS

A definição da propriedade **DISABLEADVTSHORTCUTS** desabilita a geração de atalhos que dão suporte à [instalação sob demanda e ao](installation-on-demand.md) [anúncio](advertisement.md). Definir essa propriedade especifica que esses atalhos devem ser substituídos por atalhos regulares.

## <a name="default-value"></a>Valor padrão

Por padrão, a geração de atalhos de instalação sob demanda está habilitada.

## <a name="remarks"></a>Comentários

Os atalhos que dão suporte ao anúncio têm o nome de um recurso, em vez de um caminho de arquivo formatado do formato \[ \# FileKey \] , inseridos na coluna Target da [tabela de atalho](shortcut-table.md). Se essa propriedade for definida e o recurso for instalado, o instalador gerará um atalho regular para o recurso.

Essa propriedade é normalmente usada por administradores para usuários que fazem roaming entre ambientes que não dão suporte a anúncios. Essa propriedade pode ser definida por uma transformação, no fluxo administrativo ou na [tabela de propriedades](property-table.md). Se ele for definido usando a linha de comando ou por uma chamada para [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya), ele deverá ser redefinido novamente durante cada instalação subsequente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




