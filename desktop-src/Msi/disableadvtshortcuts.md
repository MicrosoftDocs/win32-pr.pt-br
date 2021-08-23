---
description: Definir a propriedade DISABLEADVTSHORTCUTS desabilita a geração de atalhos que suportam instalação sob demanda e anúncio. Definir essa propriedade especifica que esses atalhos devem ser substituídos por atalhos regulares.
ms.assetid: 1b55ecbe-932f-4f08-98b1-8c5e7a57d2e8
title: Propriedade DISABLEADVTSHORTCUTS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86fd8465620abab56ebfe18f68254bf6d29b6e752a7550157231a0b1abe95ecd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745556"
---
# <a name="disableadvtshortcuts-property"></a>Propriedade DISABLEADVTSHORTCUTS

Definir a **propriedade DISABLEADVTSHORTCUTS** desabilita a geração de atalhos que suportam instalação [sob demanda](installation-on-demand.md) e [anúncio](advertisement.md). Definir essa propriedade especifica que esses atalhos devem ser substituídos por atalhos regulares.

## <a name="default-value"></a>Valor padrão

Por padrão, a geração de atalhos de instalação sob demanda está habilitada.

## <a name="remarks"></a>Comentários

Os atalhos que suportam o anúncio têm o nome de um recurso, em vez de um caminho de arquivo formatado da chave de arquivo do formulário , inserido na coluna Destino da tabela \[ \# \] [Atalho](shortcut-table.md). Se essa propriedade estiver definida e o recurso estiver instalado, o instalador gerará um atalho regular para o recurso.

Essa propriedade geralmente é usada por administradores para usuários que fazem roaming entre ambientes que têm e não são suportados por publicidade. Essa propriedade pode ser definida por uma transformação, no fluxo administrativo ou na [tabela Propriedade](property-table.md). Se for definido usando a linha de comando ou por uma chamada para [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya), ele deverá ser redefinido novamente durante cada instalação subsequente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




