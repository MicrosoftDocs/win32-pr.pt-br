---
description: Definir a propriedade ARPNOREMOVE desabilita a funcionalidade Adicionar ou Remover Programas Painel de Controle que remove o produto.
ms.assetid: f86c1af8-c984-4075-9c6b-0a71000b01a1
title: Propriedade ARPNOREMOVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d69e066aeb96861be220a40334d44bf55fe0569e855029d2a19399b56a1c205
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105426"
---
# <a name="arpnoremove-property"></a>Propriedade ARPNOREMOVE

Definir a **propriedade ARPNOREMOVE** desabilita a funcionalidade **Adicionar** ou Remover Programas Painel de Controle **que** remove o produto. Por Windows 2000, desabilita o  botão Remover para o produto do botão Adicionar ou Remover **Programas** no **Painel de Controle**. Para sistemas operacionais anteriores, isso tem o efeito de remover o produto da lista de produtos instalados em Adicionar ou Remover **Programas** no **Painel de Controle**.

Se **a propriedade ARPNOREMOVE** estiver definida, a ação [RegisterProduct](registerproduct-action.md) grava o valor "NoRemove" na chave do Registro:

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Desinstalar** \\ **{*product key*}**

Definir **a propriedade ARPNOREMOVE** impede que o valor UninstallString seja gravado sob essa chave. O valor UnistallString é uma linha de comando para remover o produto, em vez de reconfigurar o produto.

## <a name="remarks"></a>Comentários

Por exemplo, essa propriedade pode ser definida durante uma transformação de personalização para impedir que os usuários removam uma personalização de administrador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 ou posterior no Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




