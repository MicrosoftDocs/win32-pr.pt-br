---
description: A interface IAMErrorLog fornece um método de retorno de chamada para registro em log de erros DirectShow DeS (Serviços de Edição). O DES não implementa essa interface.
ms.assetid: d5366072-2de7-437c-b198-cbc4d8623c45
title: Interface IAMErrorLog (Qedit.h)
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
ms.openlocfilehash: f2edd1d315cc7ae35bbc200209667d49d53392ce86a10b40a067182cd0621124
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756456"
---
# <a name="iamerrorlog-interface"></a>Interface IAMErrorLog

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IAMErrorLog` interface fornece um método de retorno de chamada para o log de erros DirectShow [DES (Serviços](directshow-editing-services.md) de Edição).

O DES não implementa essa interface. Para executar o log de erros, implemente essa interface em seu aplicativo e chame [**IAMSetErrorLog::p ut \_ ErrorLog**](iamseterrorlog-put-errorlog.md) na linha do tempo. Se ocorrer um erro quando você renderizar o projeto, o DES chamará o método [**IAMErrorLog::LogError**](iamerrorlog-logerror.md) implementado pelo seu aplicativo.

O DES registra erros somente quando você renderiza um projeto usando a interface [**IRenderEngine.**](irenderengine.md) Por exemplo, se você salvar um projeto como um DirectShow de filtro (formato .grf) e reproduzir o arquivo de grafo, não haverá registro em log de erros. Para obter mais informações sobre como usar essa interface, consulte [Erros de log](logging-errors.md).

## <a name="members"></a>Membros

A interface **IAMErrorLog** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMErrorLog** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IAMErrorLog** tem esses métodos.



| Método                                   | Descrição               |
|:-----------------------------------------|:--------------------------|
| [**Logerror**](iamerrorlog-logerror.md) | Registra um erro.<br/> |



 

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



 

 
