---
description: A interface IAMSetErrorLog define ou recupera um log de erros nos serviços de edição do DirectShow (DES).
ms.assetid: ce658533-eacf-4b5d-9910-dca918de09e7
title: Interface IAMSetErrorLog (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c0a24d29625bf08bc2f4c728a61f5188e8bec211
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751228"
---
# <a name="iamseterrorlog-interface"></a>Interface IAMSetErrorLog

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IAMSetErrorLog` interface define ou recupera um log de erros nos [serviços de edição do DirectShow](directshow-editing-services.md) (des). O objeto Timeline implementa essa interface. Os aplicativos podem usar essa interface para registrar erros de renderização em tempo de execução. Implemente a interface [**IAMErrorLog**](iamerrorlog.md) em seu aplicativo e, em seguida, chame o método [**IAMSetErrorLog::p UT log de \_ erros**](iamseterrorlog-put-errorlog.md) na linha do tempo.

Para obter mais informações sobre como usar essa interface, consulte [log de erros](logging-errors.md).

## <a name="members"></a>Membros

A interface **IAMSetErrorLog** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMSetErrorLog** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IAMSetErrorLog** tem esses métodos.



| Método                                               | Descrição                                                 |
|:-----------------------------------------------------|:------------------------------------------------------------|
| [**obter log de \_ erros**](iamseterrorlog-get-errorlog.md) | Recupera o log de erros atual deste objeto.<br/> |
| [**colocar log de \_ erros**](iamseterrorlog-put-errorlog.md) | Especifica um log de erros para o objeto.<br/>           |



 

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



 

 
