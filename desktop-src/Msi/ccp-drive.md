---
description: A \_ propriedade da unidade CCP é definida como o caminho raiz do volume removível que deve ser pesquisado por RMCCPSearch.
ms.assetid: 567b7d11-6d80-4ec5-810d-f32b9ebf5809
title: Propriedade CCP_DRIVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a7e96b5c69ecb3b52ae57da5476f4b9408039659f5cf26474cc443072b870de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075136"
---
# <a name="ccp_drive-property"></a>\_Propriedade da unidade CCP

A propriedade da **\_ unidade CCP** é definida como o caminho raiz do volume removível que deve ser pesquisado por [RMCCPSearch](rmccpsearch-action.md). A ação RMCCPSearch usa assinaturas de arquivo para validar se os produtos qualificados estão instalados em um sistema antes de executar uma instalação de atualização.

Essa propriedade normalmente é definida por meio da interface do usuário ou de uma ação personalizada. Essa propriedade deve ser definida antes que a ação [RMCCPSearch](rmccpsearch-action.md) seja executada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




