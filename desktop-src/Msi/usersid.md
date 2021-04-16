---
description: O instalador define o valor da Propriedade UserID como a representação da cadeia de caracteres do identificador de segurança (SID) do usuário que está executando a instalação. Para obter mais informações, consulte estruturas de autorização.
ms.assetid: 94524636-c7f2-4de2-b35e-644c0c171193
title: Propriedade UserID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fab01b3f87c654a306bfe3633adf0973ed58aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747314"
---
# <a name="usersid-property"></a>Propriedade UserID

O instalador define o valor da propriedade **userid** como a representação da cadeia de caracteres do identificador de segurança (SID) do usuário que está executando a instalação. Para obter mais informações, consulte [estruturas de autorização](../secauthz/authorization-structures.md).

## <a name="default-value"></a>Valor padrão

Nenhum.

## <a name="remarks"></a>Comentários

O Windows Installer definir essa propriedade no Windows 2000, Windows XP e Windows Vista. Essa propriedade não está definida em todos os outros sistemas operacionais.

Observe que essa propriedade tem o atributo especial que pode ser recuperado de uma ação personalizada adiada. Uma ação personalizada em execução com privilégios elevados ainda pode retornar o SID do usuário na propriedade **userid** . Para obter informações, consulte [obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 
