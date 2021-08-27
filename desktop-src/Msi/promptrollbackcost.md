---
description: A propriedade PROMPTROLLBACKCOST especifica a ação que o instalador executará se os recursos de reversão da instalação estiverem habilitados e não houver espaço em disco suficiente para concluir a instalação. Os valores possíveis de PROMPTROLLBACKCOST são os seguintes. ValueActionPDisplay uma caixa de diálogo perguntando se deseja continuar sem uma reversão. DDisable reversão e continue sem perguntar ao usuário. FFail com a solicitação de erro de espaço em disco insuficiente.
ms.assetid: 6ffd0b3f-79b8-4ce3-a262-4d27ffc5a175
title: Propriedade PROMPTROLLBACKCOST
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71cca3134593039354735e2e306a924620db8100eb0fd0e0a51f392c58f61897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129036"
---
# <a name="promptrollbackcost-property"></a>Propriedade PROMPTROLLBACKCOST

A propriedade **PROMPTROLLBACKCOST** especifica a ação que o instalador executará se os recursos de [reversão da instalação](rollback-installation.md) estiverem habilitados e não houver espaço em disco suficiente para concluir a instalação.

Os valores possíveis de **PROMPTROLLBACKCOST** são os seguintes.



| Valor | Ação                                                              |
|-------|---------------------------------------------------------------------|
| P     | Exibir uma caixa de diálogo perguntando se deseja continuar sem uma reversão. |
| D     | Desabilite a reversão e continue sem perguntar ao usuário.                  |
| F     | Falha com a solicitação de erro de espaço em disco insuficiente.                       |



 

## <a name="remarks"></a>Comentários

Quando a interface do usuário é executada no nível básico ou sem interface do usuário, o instalador manipula toda a lógica de espaço em disco automaticamente.

Quando a interface do usuário é executada no nível completo, o usuário pode receber opções adicionais, como solicitar antes de continuar com uma reversão, desabilitar a reversão ou prosseguir sem reversão quando o disco estiver cheio. Cabe ao desenvolvedor do pacote criar a sequência da caixa de diálogo para fornecer as opções apropriadas ao usuário. Os elementos disponíveis para fazer isso são o [EnableRollback ControlEvent,](enablerollback-controlevent.md), a propriedade [**OutOfDiskSpace**](outofdiskspace.md) , a propriedade [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) e a propriedade **PROMPTROLLBACKCOST** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




