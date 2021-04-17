---
description: A propriedade instalada será definida somente se o produto estiver instalado por computador ou para o usuário atual.
ms.assetid: 139a6324-58fb-485e-8b3e-c5cf2881d5d1
title: Propriedade instalada
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae5126107fff51f3790fb3ab9a9209490b9627a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747976"
---
# <a name="installed-property"></a>Propriedade instalada

A propriedade **instalada** será definida somente se o produto estiver instalado por computador ou para o usuário atual. Essa propriedade não será definida se o produto for instalado para um usuário diferente.

A propriedade **installed** pode ser usada em expressões condicionais para determinar se um produto está instalado por computador ou para o usuário atual. Por exemplo, a propriedade pode ser usada na coluna condicional de uma tabela de sequência ou para diferenciar entre uma primeira instalação e uma instalação de manutenção.

Para determinar se o produto está instalado para um usuário diferente, verifique a propriedade [**productstate**](productstate.md) .

O valor da propriedade [**ProductVersion**](productversion.md) é a versão do produto no formato de cadeia de caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




