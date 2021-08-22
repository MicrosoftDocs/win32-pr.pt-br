---
description: A classe CAutoLock contém uma seção crítica para o escopo de um bloco de código.
ms.assetid: 8013b3a7-297b-4cf8-8107-4cee1fc12b56
title: Classe CAutoLock (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b046111e3a7e22fcf9e380fae09bb2d2007a583e49c0507b8e214142505fe02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661698"
---
# <a name="cautolock-class"></a>Classe CAutoLock

A `CAutoLock` classe contém uma seção crítica para o escopo de um bloco de código.

Essa classe funciona em conjunto com a [**classe CCritSec,**](ccritsec.md) que é um wrapper para objetos de seção críticos. O `CAutoLock` construtor bloqueia a seção crítica e o destruidor a desbloqueia. Usando um objeto como uma variável local, você pode bloquear uma seção crítica com a garantia de que todos os caminhos de código `CAutoLock` desbloquearão a seção crítica.

O exemplo de código a seguir mostra como usar essa classe:


```
CCritSec csMyLock;  // Critical section is not locked yet.
{
    CAutoLock cObjectLock(&csMyLock);  // Lock the critical section.

    // Protected section of code.     

} // Lock goes out of scope here.

```



Os métodos nesta classe não foram projetados para serem substituídos.



| Variáveis de membro protegidas                 | Descrição                                                      |
|--------------------------------------------|------------------------------------------------------------------|
| [**m \_ pLock**](cautolock-m-plock.md)      | Seção crítica para esse bloqueio.                                  |
| Métodos públicos                             | Descrição                                                      |
| [**CAutoLock**](cautolock-cautolock.md)   | Método do construtor. Bloqueia o objeto de seção crítico especificado. |
| [**~CAutoLock**](cautolock--cautolock.md) | Método destruidor. Desbloqueia o objeto de seção crítico.          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




