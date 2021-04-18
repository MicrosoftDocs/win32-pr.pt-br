---
description: A propriedade MSIRESTARTMANAGERCONTROL especifica se o pacote de Windows Installer usa a funcionalidade de caixa de diálogo do Gerenciador de reinicialização ou FilesInUse.
ms.assetid: fefff18b-892a-440e-9f57-d23aeb99af74
title: Propriedade MSIRESTARTMANAGERCONTROL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d965f1b814ce2969a6253ba227672c54769791
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778719"
---
# <a name="msirestartmanagercontrol-property"></a>Propriedade MSIRESTARTMANAGERCONTROL

A propriedade **MSIRESTARTMANAGERCONTROL** especifica se o pacote de Windows Installer usa a funcionalidade de [caixa de diálogo](filesinuse-dialog.md) do Gerenciador de [reinicialização](../rstmgr/restart-manager-portal.md) ou FilesInUse.

## <a name="value"></a>Valor



| Valor                                                                                        | Significado                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                 | Esse será o valor padrão se a propriedade não estiver definida. Windows Installer sempre tenta usar o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) no Windows Vista.<br/>                                                                                                                                                                                                       |
| <dl> <dt>Desativar</dt> </dl>         | Desabilita a interação do pacote com o Gerenciador de [reinicialização](../rstmgr/restart-manager-portal.md). Windows Installer usa a [caixa de diálogo FilesInUse](filesinuse-dialog.md). <br/>                                                                                                                                                                                                      |
| <dl> <dt>"DisableShutdown"</dt> </dl> | Windows Installer usa a [caixa de diálogo FilesInUse](filesinuse-dialog.md). Essa configuração desabilita as tentativas do Gerenciador de [reinicialização](../rstmgr/restart-manager-portal.md) para atenuar as reinicializações ao instalar um pacote de Windows Installer que não foi criado para usar o Gerenciador de reinicialização. O instalador ainda usa o Gerenciador de reinicialização para detectar arquivos em uso pelos aplicativos. <br/> |



 

## <a name="remarks"></a>Comentários

A propriedade **MSIRESTARTMANAGERCONTROL** será ignorada se o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) não estiver disponível ou desabilitado.

O valor dessa propriedade pode ser modificado usando transformações ou atualizações de personalização. Alterar o valor dessa propriedade de ações personalizadas não tem nenhum efeito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o mínimo Service Pack exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md)
</dt> <dt>

[Sem suporte no Windows Installer 3,1 e versões anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
