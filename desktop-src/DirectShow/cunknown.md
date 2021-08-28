---
description: A classe CUnknown implementa a interface IUnknown. a maioria dos objetos COM Component Object Model (COM) no DirectShow deriva de CUnknown.
ms.assetid: 9711d36b-6987-4fb0-a8df-eba94348dc7b
title: Classe CUnknown (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 06b6089f7f1c108a9b99ad4f1b16f4638b84d8d687a3590353c32841ccfff499
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075987"
---
# <a name="cunknown-class"></a>Classe CUnknown

![hierarquia de classe CUnknown](images/cbase01.png)

A classe **CUnknown** implementa a interface **IUnknown** . a maioria dos objetos COM Component Object Model (COM) no DirectShow deriva de **CUnknown**.

Se você implementar um objeto COM, talvez queira derivá-lo de **CUnknown**. A derivação de **CUnknown** fornece uma implementação thread-safe e economiza o problema de implementação de **IUnknown**.

Para obter uma discussão detalhada sobre como usar essa classe base, consulte [como implementar IUnknown](how-to-implement-iunknown.md). O seguinte é um breve resumo:

-   Inclua a macro [**Declare \_ IUnknown**](declare-iunknown.md) na seção pública de sua definição de classe. Essa macro declara os três métodos da interface **IUnknown** .
-   Substitua o método [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) para dar suporte a interfaces diferentes de **IUnknown**. Dentro desse método, chame a função [**GetInterface**](getinterface.md) para recuperar ponteiros de interface.
-   Em seu construtor de classe, invoque o método do construtor **CUnknown** .



| Variáveis de membro protegido                                                  | Descrição                                                        |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**\_cRef m**](cunknown-m-cref.md)                                          | Contagem de referência.                                                   |
| Métodos públicos                                                              | Descrição                                                        |
| [**CUnknown**](cunknown-cunknown.md)                                       | Método de construtor.                                                |
| [**~ CUnknown**](cunknown--cunknown.md)                                    | Método destruidor. VirtuaisLUNs.                                        |
| [**GetOwner**](cunknown-getowner.md)                                       | Obtém um ponteiro para o **IUnknown** de controle.                    |
| Métodos INonDelegatingUnknown                                               | Descrição                                                        |
| [**NonDelegatingAddRef**](cunknown-nondelegatingaddref.md)                 | Incrementa a contagem de referência.                                    |
| [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) | Recupera um ponteiro de interface e incrementa a contagem de referência. |
| [**NonDelegatingRelease**](cunknown-nondelegatingrelease.md)               | Decrementa a contagem de referência.                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>combase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[DirectShow Classes base](directshow-base-classes.md)
</dt> </dl>

 

 




