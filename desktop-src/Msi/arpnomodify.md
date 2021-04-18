---
description: A definição da propriedade ARPNOMODIFY desabilita a funcionalidade adicionar ou remover programas no painel de controle que modifica o produto.
ms.assetid: dc804910-cf15-4f9e-863f-78dcac248717
title: Propriedade ARPNOMODIFY
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ee118c8b0e9d3c1cebef5aeefbf9e97c4793623
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749595"
---
# <a name="arpnomodify-property"></a>Propriedade ARPNOMODIFY

A definição da propriedade **ARPNOMODIFY** desabilita a funcionalidade adicionar ou remover programas no painel de controle que modifica o produto. Para o Windows 2000, isso desabilita o botão **Modificar** do produto em **Adicionar ou remover programas** no painel de **controle**. Em sistemas operacionais anteriores, clicar no botão **Adicionar ou remover programas** desinstala o produto em vez de entrar no assistente de modo de manutenção.

Se a propriedade **ARPNOMODIFY** for definida, a [ação RegisterProduct](registerproduct-action.md) gravará o valor "NoModify" na chave do registro:

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Desinstalar** \\ o **{*chave do produto*}**

Se a propriedade **ARPNOMODIFY** for definida e a propriedade [**ARPNOREMOVE**](arpnoremove.md) não estiver definida, a ação RegisterProduct também gravará o valor de UninstallString nessa chave. O valor de Desinstalastring é uma linha de comando para remover o produto, em vez de reconfigurar o produto.

## <a name="remarks"></a>Comentários

No Windows 2000, isso desabilita o botão **alterar** do produto em **Adicionar ou remover programas** do **painel de controle**.

Essa propriedade pode ser definida por uma transformação de personalização para impedir que os usuários alterem a personalização de um administrador por meio de **Adicionar ou remover programas**. Essa propriedade só afeta **Adicionar ou remover programas**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Um exemplo de transformação de personalização](a-customization-transform-example.md)
</dt> </dl>

 

 




