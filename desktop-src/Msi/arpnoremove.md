---
description: A configuração da propriedade ARPNOREMOVE desabilita a funcionalidade adicionar ou remover programas no painel de controle que remove o produto.
ms.assetid: f86c1af8-c984-4075-9c6b-0a71000b01a1
title: Propriedade ARPNOREMOVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf8960234456a7010fb81cb195d63d4c5c79bb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770386"
---
# <a name="arpnoremove-property"></a>Propriedade ARPNOREMOVE

A configuração da propriedade **ARPNOREMOVE** desabilita a funcionalidade **Adicionar ou remover programas** no **painel de controle** que remove o produto. Para o Windows 2000, isso desabilita o botão **remover** do produto em **Adicionar ou remover programas** no **painel de controle**. Para sistemas operacionais anteriores, isso tem o efeito de remover o produto da lista de produtos instalados em **Adicionar ou remover programas** no painel de **controle**.

Se a propriedade **ARPNOREMOVE** for definida, a [ação RegisterProduct](registerproduct-action.md) gravará o valor "NoRemove" na chave do registro:

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Desinstalar** \\ o **{*chave do produto*}**

A definição da propriedade **ARPNOREMOVE** impede que o valor desinstallstring seja gravado nessa chave. O valor de Desinstalastring é uma linha de comando para remover o produto, em vez de reconfigurar o produto.

## <a name="remarks"></a>Comentários

Por exemplo, essa propriedade pode ser definida durante uma transformação de personalização para impedir que os usuários removam uma personalização do administrador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 ou posterior no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




