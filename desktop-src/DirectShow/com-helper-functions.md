---
description: Essas funções fornecem suporte para implementar a interface IUnknown no DirectShow.
ms.assetid: 991e4c69-7d30-4ecf-9ccf-4920452c21d6
title: Funções auxiliares COM (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COM
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa8558cd0d04258adf89cbacdd99952cf00c6d0aa5f24ee38cca2dceb4e5478f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084336"
---
# <a name="com-helper-functions"></a>Funções auxiliares COM

Essas funções fornecem suporte para implementar a interface **IUnknown** no DirectShow.



| Função                                               | Descrição                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------|
| [**DECLARAR \_ IUnknown**](declare-iunknown.md)          | Declara os três métodos da interface base para uma nova interface. |
| [**GetInterface**](getinterface.md)                   | Recupera um ponteiro de interface para o cliente solicitado.               |
| [**INonDelegatingUnknown**](inondelegatingunknown.md) | Versão não delegada da interface **IUnknown** .                  |
| [**LoadOLEAut32**](loadoleaut32.md)                   | Carrega a DLL de automação (OleAut32.dll).                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>combase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de utilitário](utility-functions.md)
</dt> </dl>

 

 




