---
description: A classe CCritSec fornece um bloqueio de thread.
ms.assetid: ecc60afe-15d0-4780-8133-1dfc558c6325
title: Classe CCritSec (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eb57004935a85392057120c0ec369d19217148780079ab4be83088dd3de3ea8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872186"
---
# <a name="ccritsec-class"></a>Classe CCritSec

A classe **CCritSec** fornece um bloqueio de thread.

essa classe é um wrapper fino para um Windows objeto de **\_ seção crítica** . Você pode bloquear e desbloquear o thread chamando os métodos [**CCritSec:: Lock**](ccritsec-lock.md) e [**CCritSec:: Unlock**](ccritsec-unlock.md) . No entanto, é mais seguro usar essa classe em conjunto com a classe [**CAutoLock**](cautolock.md) . Quando a classe **CAutoLock** sai do escopo, ela automaticamente desbloqueia o objeto **CCritSec** . Além disso, ele é compilado para um código embutido eficiente.



| Variáveis de membro público                            | Descrição                                              |
|----------------------------------------------------|----------------------------------------------------------|
| [**\_currentOwner m**](ccritsec-m-currentowner.md) | Identificador de thread do thread proprietário.                  |
| [**\_lockCount m**](ccritsec-m-lockcount.md)       | Número de bloqueios pendentes neste objeto.              |
| [**\_fTrace m**](ccritsec-m-ftrace.md)             | Valor booliano que especifica se o bloqueio deve ser rastreado. |
| Métodos públicos                                     | Descrição                                              |
| [**CCritSec**](ccritsec-ccritsec.md)              | Método de construtor.                                      |
| [**~ CCritSec**](ccritsec--ccritsec.md)            | Método destruidor.                                       |
| [**Bloqueio**](ccritsec-lock.md)                      | Bloqueia o objeto de seção crítica.                       |
| [**Automático**](ccritsec-unlock.md)                  | Desbloqueia o objeto da seção crítica.                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de seção crítica](/windows/desktop/Sync/critical-section-objects)
</dt> <dt>

[DirectShow Referência de classe base](base-class-reference.md)
</dt> </dl>

 

