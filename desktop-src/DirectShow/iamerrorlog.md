---
description: A interface IAMErrorLog fornece um método de retorno de chamada para log de erros nos serviços de edição do DirectShow (DES). O DES não implementa essa interface.
ms.assetid: d5366072-2de7-437c-b198-cbc4d8623c45
title: Interface IAMErrorLog (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 48a1515ebf3e7c829a3e23772f1f84ee76c36ae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757297"
---
# <a name="iamerrorlog-interface"></a>Interface IAMErrorLog

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IAMErrorLog` interface fornece um método de retorno de chamada para log de erros nos [serviços de edição do DirectShow](directshow-editing-services.md) (des).

O DES não implementa essa interface. Para executar o log de erros, implemente essa interface em seu aplicativo e chame [**IAMSetErrorLog \_ ::p UT**](iamseterrorlog-put-errorlog.md) log de erros na linha do tempo. Se ocorrer um erro quando você renderizar o projeto, o DES chamará o método [**IAMErrorLog:: LogError**](iamerrorlog-logerror.md) implementado pelo seu aplicativo.

O DES registra erros somente quando você renderiza um projeto usando a interface [**IRenderEngine**](irenderengine.md) . Por exemplo, se você salvar um projeto como um grafo de filtro do DirectShow (formato. GRF) e reproduzir o arquivo de grafo, não haverá log de erros. Para obter mais informações sobre como usar essa interface, consulte [log de erros](logging-errors.md).

## <a name="members"></a>Membros

A interface **IAMErrorLog** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMErrorLog** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IAMErrorLog** tem esses métodos.



| Método                                   | Descrição               |
|:-----------------------------------------|:--------------------------|
| [**LogError**](iamerrorlog-logerror.md) | Registra um erro.<br/> |



 

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



 

 
