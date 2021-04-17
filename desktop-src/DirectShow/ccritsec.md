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
ms.openlocfilehash: 8db0243ecfecd47655f547d40390e602c04d5b88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757327"
---
# <a name="ccritsec-class"></a>Classe CCritSec

A classe **CCritSec** fornece um bloqueio de thread.

Essa classe é um wrapper fino para um objeto **de \_ seção crítica** do Windows. Você pode bloquear e desbloquear o thread chamando os métodos [**CCritSec:: Lock**](ccritsec-lock.md) e [**CCritSec:: Unlock**](ccritsec-unlock.md) . No entanto, é mais seguro usar essa classe em conjunto com a classe [**CAutoLock**](cautolock.md) . Quando a classe **CAutoLock** sai do escopo, ela automaticamente desbloqueia o objeto **CCritSec** . Além disso, ele é compilado para um código embutido eficiente.



| Variáveis de membro público                            | Descrição                                              |
|----------------------------------------------------|----------------------------------------------------------|
| [**\_currentOwner m**](ccritsec-m-currentowner.md) | Identificador de thread do thread proprietário.                  |
| [**\_lockCount m**](ccritsec-m-lockcount.md)       | Número de bloqueios pendentes neste objeto.              |
| [**\_fTrace m**](ccritsec-m-ftrace.md)             | Valor booliano que especifica se o bloqueio deve ser rastreado. |
| Métodos públicos                                     | Descrição                                              |
| [**CCritSec**](ccritsec-ccritsec.md)              | Método de construtor.                                      |
| [**~ CCritSec**](ccritsec--ccritsec.md)            | Método destruidor.                                       |
| [**Bloquear**](ccritsec-lock.md)                      | Bloqueia o objeto de seção crítica.                       |
| [**Unlock**](ccritsec-unlock.md)                  | Desbloqueia o objeto da seção crítica.                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de seção crítica](/windows/desktop/Sync/critical-section-objects)
</dt> <dt>

[Referência de classe base do DirectShow](base-class-reference.md)
</dt> </dl>

 

