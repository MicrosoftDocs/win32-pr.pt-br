---
description: Definir a propriedade ARPNOMODIFY desabilita a funcionalidade Adicionar ou Remover Programas Painel de Controle que modifica o produto.
ms.assetid: dc804910-cf15-4f9e-863f-78dcac248717
title: Propriedade ARPNOMODIFY
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c9a097f183c13e1c5b6f8f8b6a521c8a03149df130befaa1221b14b732418a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581806"
---
# <a name="arpnomodify-property"></a>Propriedade ARPNOMODIFY

Definir a **propriedade ARPNOMODIFY** desabilita a funcionalidade Adicionar ou Remover Programas Painel de Controle que modifica o produto. Por Windows 2000, desabilita o  botão Modificar para o produto em Adicionar ou Remover **Programas** **no Painel de Controle**. Em sistemas operacionais anteriores, clicar no **botão Adicionar** ou Remover Programas desinstala o produto em vez de entrar no assistente de modo de manutenção.

Se a **propriedade ARPNOMODIFY** estiver definida, a ação [RegisterProduct](registerproduct-action.md) grava o valor "NoModify" na chave do Registro:

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Desinstalar** \\ **{*product key*}**

Se **a propriedade ARPNOMODIFY** estiver definida e a propriedade [**ARPNOREMOVE**](arpnoremove.md) não estiver definida, a ação RegisterProduct também grava o valor UninstallString nessa chave. O valor UnistallString é uma linha de comando para remover o produto, em vez de reconfigurar o produto.

## <a name="remarks"></a>Comentários

No Windows 2000, isso desabilita  o botão Alterar para o produto em Adicionar ou Remover **Programas** do **Painel de Controle**.

Essa propriedade pode ser definida por uma transformação de **personalização** para impedir que os usuários mudem a personalização de um administrador por meio de Adicionar ou Remover Programas . Essa propriedade afeta apenas **Adicionar ou Remover Programas**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Um exemplo de transformação de personalização](a-customization-transform-example.md)
</dt> </dl>

 

 




