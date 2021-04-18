---
description: A interface IAMTimelineTransable adiciona transições a um objeto nos serviços de edição do DirectShow (DES).
ms.assetid: 1be9adaa-4145-447c-b307-dabb4419c86c
title: Interface IAMTimelineTransable (QEdit. h)
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
ms.openlocfilehash: d083b768e8dcf54236945755f4b26ecf13409b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792547"
---
# <a name="iamtimelinetransable-interface"></a>Interface IAMTimelineTransable

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IAMTimelineTransable` interface adiciona transições a um objeto nos [serviços de edição do DirectShow](directshow-editing-services.md) (des). Essa interface é exposta por qualquer objeto que possa ter transições aplicadas a ela, incluindo faixas, composições e grupos. Um objeto que implementa essa interface pode ter qualquer número de transições, mas as transições não devem se sobrepor no tempo.

> [!Note]  
> O áudio não oferece suporte a transições. Os objetos nos grupos de áudio podem expor a `IAMTimelineTransable` interface, mas o aplicativo não deve adicionar transições a eles.

 

## <a name="members"></a>Membros

A interface **IAMTimelineTransable** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineTransable** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IAMTimelineTransable** tem esses métodos.



| Método                                                          | Descrição                                                                                                                        |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**GetNextTrans**](iamtimelinetransable-getnexttrans.md)       | Recupera a primeira transição que aparece na hora especificada ou posteriormente.<br/>                                             |
| [**GetNextTrans2**](iamtimelinetransable-getnexttrans2.md)     | Recupera a primeira transição que aparece na hora especificada ou posteriormente, com o tempo fornecido como um valor de **REFTIME** .<br/> |
| [**GetTransAtTime**](iamtimelinetransable-gettransattime.md)   | Recupera a transição mais próxima ao tempo especificado.<br/>                                                                 |
| [**GetTransAtTime2**](iamtimelinetransable-gettransattime2.md) | Recupera a transição mais próxima ao tempo especificado, dado como um valor **REFTIME** .<br/>                                   |
| [**TransAdd**](iamtimelinetransable-transadd.md)               | Adiciona uma transição para o objeto.<br/>                                                                                        |
| [**TransGetCount**](iamtimelinetransable-transgetcount.md)     | Recupera o número de transições neste objeto.<br/>                                                                     |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
