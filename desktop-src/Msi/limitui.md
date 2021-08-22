---
description: Se a propriedade LIMITUI for definida, o nível da interface do usuário usada ao instalar o pacote será restrito ao básico.
ms.assetid: 1a75e66b-958a-4fa8-b13c-ced976c9508e
title: Propriedade LIMITUI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969b6e1c1de5a55581fa8d24f6d538c829e18fb48afb9bdc2fd04bae69c15162
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013134"
---
# <a name="limitui-property"></a>Propriedade LIMITUI

Se a propriedade **LIMITUI** for definida, o nível da interface do usuário usada ao instalar o pacote será restrito ao básico. Essa propriedade é necessária em pacotes que não têm interface do usuário criada, mas que ainda contêm tabelas de interface do usuário, como a [tabela de diálogo](dialog-table.md). Para obter uma descrição dos níveis de interface do usuário, consulte [ **MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

## <a name="remarks"></a>Comentários

Os pacotes de instalação que contêm a propriedade **LIMITUI** também devem conter a propriedade [**ARPNOMODIFY**](arpnomodify.md) . Isso é necessário para que um usuário obtenha o comportamento correto a partir de **Adicionar ou remover programas** no utilitário do **painel de controle** ao tentar configurar um produto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
</dt> <dt>

[**ARPNOMODIFY**](arpnomodify.md)
</dt> </dl>

 

 




