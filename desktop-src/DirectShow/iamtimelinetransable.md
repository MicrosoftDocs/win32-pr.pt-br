---
description: A interface IAMTimelineTransable adiciona transições a um objeto no DES (DirectShow de Edição).
ms.assetid: 1be9adaa-4145-447c-b307-dabb4419c86c
title: Interface IAMTimelineTransable (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6228b836f85251dda7f43d6c3b421d486b727c6bdc6c319b9cf7ca1e37d34a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052026"
---
# <a name="iamtimelinetransable-interface"></a>Interface IAMTimelineTransable

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IAMTimelineTransable` interface adiciona transições a um objeto [DirectShow DES (Serviços](directshow-editing-services.md) de Edição). Essa interface é exposta por qualquer objeto que possa ter transições aplicadas a ela, incluindo faixas, composições e grupos. Um objeto que implementa essa interface pode ter qualquer número de transições, mas as transições não devem se sobrepor no tempo.

> [!Note]  
> O áudio não dá suporte a transições. Objetos dentro de grupos de áudio podem `IAMTimelineTransable` expor a interface, mas o aplicativo não deve adicionar transições a eles.

 

## <a name="members"></a>Membros

A interface **IAMTimelineTransable** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineTransable** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IAMTimelineTransable** tem esses métodos.



| Método                                                          | Descrição                                                                                                                        |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**GetNextTrans**](iamtimelinetransable-getnexttrans.md)       | Recupera a primeira transição que aparece no horário especificado ou posterior.<br/>                                             |
| [**GetNextTrans2**](iamtimelinetransable-getnexttrans2.md)     | Recupera a primeira transição que aparece na hora especificada ou posterior, com o tempo determinado como um **valor REFTIME.**<br/> |
| [**GetTransAtTime**](iamtimelinetransable-gettransattime.md)   | Recupera a transição mais próxima ao tempo especificado.<br/>                                                                 |
| [**GetTransAtTime2**](iamtimelinetransable-gettransattime2.md) | Recupera a transição mais próxima ao tempo especificado, dado como um **valor REFTIME.**<br/>                                   |
| [**TransAdd**](iamtimelinetransable-transadd.md)               | Adiciona uma transição ao objeto .<br/>                                                                                        |
| [**TransGetCount**](iamtimelinetransable-transgetcount.md)     | Recupera o número de transições neste objeto.<br/>                                                                     |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
