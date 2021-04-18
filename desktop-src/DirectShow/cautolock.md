---
description: A classe CAutoLock mantém uma seção crítica para o escopo de um bloco de código.
ms.assetid: 8013b3a7-297b-4cf8-8107-4cee1fc12b56
title: Classe CAutoLock (Wxutil. h)
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
ms.openlocfilehash: 866ca7164fdaef5a93679da000779c51fb4ddb24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750714"
---
# <a name="cautolock-class"></a>Classe CAutoLock

A `CAutoLock` classe mantém uma seção crítica para o escopo de um bloco de código.

Essa classe funciona em conjunto com a classe [**CCritSec**](ccritsec.md) , que é um wrapper para objetos de seção críticos. O `CAutoLock` Construtor bloqueia a seção crítica e o destruidor a desbloqueia. Usando um `CAutoLock` objeto como uma variável local, você pode bloquear uma seção crítica com a garantia de que todos os caminhos de código desbloquearão a seção crítica.

O exemplo de código a seguir mostra como usar essa classe:


```
CCritSec csMyLock;  // Critical section is not locked yet.
{
    CAutoLock cObjectLock(&csMyLock);  // Lock the critical section.

    // Protected section of code.     

} // Lock goes out of scope here.

```



Os métodos nesta classe não foram projetados para serem substituídos.



| Variáveis de membro protegido                 | Descrição                                                      |
|--------------------------------------------|------------------------------------------------------------------|
| [**\_pLock m**](cautolock-m-plock.md)      | Seção crítica para este bloqueio.                                  |
| Métodos públicos                             | Descrição                                                      |
| [**CAutoLock**](cautolock-cautolock.md)   | Método de construtor. Bloqueia o objeto de seção crítica especificado. |
| [**~ CAutoLock**](cautolock--cautolock.md) | Método destruidor. Desbloqueia o objeto da seção crítica.          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




