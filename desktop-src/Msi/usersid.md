---
description: O instalador define o valor da Propriedade UserID como a representação da cadeia de caracteres do identificador de segurança (SID) do usuário que está executando a instalação. Para obter mais informações, consulte estruturas de autorização.
ms.assetid: 94524636-c7f2-4de2-b35e-644c0c171193
title: Propriedade UserID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b26185c886117b39355241151ffef6d8615bd5f8d10a7f50bd5937a301f7b398
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809156"
---
# <a name="usersid-property"></a>Propriedade UserID

O instalador define o valor da propriedade **userid** como a representação da cadeia de caracteres do identificador de segurança (SID) do usuário que está executando a instalação. Para obter mais informações, consulte [estruturas de autorização](../secauthz/authorization-structures.md).

## <a name="default-value"></a>Valor padrão

Nenhum.

## <a name="remarks"></a>Comentários

o Windows Installer definir essa propriedade em Windows 2000, Windows XP e Windows Vista. Essa propriedade não está definida em todos os outros sistemas operacionais.

Observe que essa propriedade tem o atributo especial que pode ser recuperado de uma ação personalizada adiada. Uma ação personalizada em execução com privilégios elevados ainda pode retornar o SID do usuário na propriedade **userid** . Para obter informações, consulte [obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 
