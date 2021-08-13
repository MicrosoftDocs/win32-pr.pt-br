---
description: A propriedade Instalado será definida somente se o produto estiver instalado por computador ou para o usuário atual.
ms.assetid: 139a6324-58fb-485e-8b3e-c5cf2881d5d1
title: Propriedade instalada
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5925f68595f6b0975e64281be0ba7326fa831d08f0298f9b84375df97e5196c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633519"
---
# <a name="installed-property"></a>Propriedade instalada

A **propriedade Instalado** será definida somente se o produto estiver instalado por computador ou para o usuário atual. Essa propriedade não será definida se o produto estiver instalado para um usuário diferente.

A **propriedade Installed** pode ser usada em expressões condicionais para determinar se um produto está instalado por computador ou para o usuário atual. Por exemplo, a propriedade pode ser usada na coluna condicional de uma tabela de sequência ou para diferenciar entre uma primeira instalação e uma instalação de manutenção.

Para determinar se o produto está instalado para um usuário diferente, verifique a [**propriedade ProductState.**](productstate.md)

O valor da propriedade [**ProductVersion**](productversion.md) é a versão do produto no formato de cadeia de caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




