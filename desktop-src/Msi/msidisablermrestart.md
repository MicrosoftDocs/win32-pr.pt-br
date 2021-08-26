---
description: A propriedade MSIDISABLERMRESTART determina como os aplicativos ou serviços que estão usando atualmente arquivos afetados por uma atualização devem ser desligados e reiniciados para habilitar a instalação da atualização.
ms.assetid: 45c804bf-6d15-416a-b106-d8bb3f4c547d
title: Propriedade MSIDISABLERMRESTART
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d46bdaee34b154ccaacddc36dcb08113fce9e3f749090eb80176080a60235e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042786"
---
# <a name="msidisablermrestart-property"></a>Propriedade MSIDISABLERMRESTART

A propriedade **MSIDISABLERMRESTART** determina como os aplicativos ou serviços que estão usando atualmente arquivos afetados por uma atualização devem ser desligados e reiniciados para habilitar a instalação da atualização.

## <a name="value"></a>Valor



| Valor                                                                        | Significado                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Todos os serviços do sistema que foram desligados para instalar a atualização são reiniciados. Todos os aplicativos que se registraram com o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) são reiniciados.<br/> |
| <dl> <dt>1</dt> </dl> | Os processos que foram desligados usando o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) durante a instalação da atualização não serão reiniciados depois que a atualização for aplicada.<br/>                           |



 

## <a name="remarks"></a>Comentários

A propriedade **MSIDISABLERMRESTART** será ignorada se o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) não estiver disponível ou desabilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o mínimo service pack exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[sem suporte no Windows Installer 3,1 e versões anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
