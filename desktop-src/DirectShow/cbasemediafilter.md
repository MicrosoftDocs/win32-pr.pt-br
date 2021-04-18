---
description: A classe CBaseMediaFilter implementa a interface IMediaFilter.
ms.assetid: 45c8973b-d0b3-4aeb-96e7-be47f8d7f4a7
title: Classe CBaseMediaFilter (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e594fd941fffecc836af26bd3d70cced82ddcaa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756644"
---
# <a name="cbasemediafilter-class"></a>Classe CBaseMediaFilter

![cbasemediafilter](images/filter05.png)

A `CBaseMediaFilter` classe implementa a interface [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) . Use essa classe para distribuidores de plug-in ou outros objetos que precisam dar suporte a **IMediaFilter** sem dar suporte à interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) . Não use essa classe para filtros. Em vez disso, use a classe [**CBaseFilter**](cbasefilter.md) ou uma classe base derivada de **CBaseFilter**.



| Variáveis de membro protegido                                       | Descrição                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------|
| [**\_estado m**](cbasemediafilter-m-state.md)                     | Estado atual do objeto.                                 |
| [**\_pClock m**](cbasemediafilter-m-pclock.md)                   | Ponteiro para o relógio de referência do objeto.                     |
| [**\_tStart m**](cbasemediafilter-m-tstart.md)                   | Tempo de referência que corresponde ao tempo de fluxo 0.            |
| [**CLSID do m \_**](cbasemediafilter-m-clsid.md)                     | Identificador de classe (CLSID) do objeto.                      |
| [**\_pLock m**](cbasemediafilter-m-plock.md)                     | Ponteiro para uma seção crítica.                               |
| Métodos públicos                                                   | Descrição                                                  |
| [**CBaseMediaFilter**](cbasemediafilter-cbasemediafilter.md)    | Método de construtor.                                          |
| [**~ CBaseMediaFilter**](cbasemediafilter--cbasemediafilter.md) | Método destruidor. VirtuaisLUNs.                                  |
| [**Fluxo de transmissão**](cbasemediafilter-streamtime.md)                | Recupera a hora atual do fluxo. VirtuaisLUNs.                  |
| [**IsActive**](cbasemediafilter-isactive.md)                    | Determina se o objeto está ativo (em execução ou em pausa). |
| Métodos IPersist                                                 | Descrição                                                  |
| [**GetClassID**](cbasemediafilter-getclassid.md)                | Recupera o identificador de classe.                              |
| Métodos IMediaFilter                                             | Descrição                                                  |
| [**GetState**](cbasemediafilter-getstate.md)                    | Recupera o estado do objeto (em execução, parado ou pausado).  |
| [**Setsynce**](cbasemediafilter-setsyncsource.md)          | Define um relógio de referência para o objeto.                       |
| [**Getsync**](cbasemediafilter-getsyncsource.md)          | Recupera o relógio de referência que o objeto está usando.      |
| [**Stop**](cbasemediafilter-stop.md)                            | Interrompe o objeto.                                            |
| [**Pausar**](cbasemediafilter-pause.md)                          | Pausa o objeto.                                           |
| [**Executar**](cbasemediafilter-run.md)                              | Executa o objeto.                                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




