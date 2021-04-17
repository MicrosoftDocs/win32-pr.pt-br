---
description: Se a propriedade LIMITUI for definida, o nível da interface do usuário usada ao instalar o pacote será restrito ao básico.
ms.assetid: 1a75e66b-958a-4fa8-b13c-ced976c9508e
title: Propriedade LIMITUI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e564e82a2daba4b6d5a91cb05acd74e1efc26c84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782334"
---
# <a name="limitui-property"></a>Propriedade LIMITUI

Se a propriedade **LIMITUI** for definida, o nível da interface do usuário usada ao instalar o pacote será restrito ao básico. Essa propriedade é necessária em pacotes que não têm interface do usuário criada, mas que ainda contêm tabelas de interface do usuário, como a [tabela de diálogo](dialog-table.md). Para obter uma descrição dos níveis de interface do usuário, consulte [ **MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

## <a name="remarks"></a>Comentários

Os pacotes de instalação que contêm a propriedade **LIMITUI** também devem conter a propriedade [**ARPNOMODIFY**](arpnomodify.md) . Isso é necessário para que um usuário obtenha o comportamento correto a partir de **Adicionar ou remover programas** no utilitário do **painel de controle** ao tentar configurar um produto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
</dt> <dt>

[**ARPNOMODIFY**](arpnomodify.md)
</dt> </dl>

 

 




