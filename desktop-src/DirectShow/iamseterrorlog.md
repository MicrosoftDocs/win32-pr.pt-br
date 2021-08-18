---
description: a interface IAMSetErrorLog define ou recupera um log de erros no DES (DirectShow Editing Services).
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
ms.openlocfilehash: 8a16e56de7f350b30c1b92c0c94ff3e3e06afc31b363c0b3a6e98017ce483aec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756396"
---
# <a name="iamseterrorlog-interface"></a>Interface IAMSetErrorLog

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

a `IAMSetErrorLog` interface define ou recupera um log de erros em [serviços de edição DirectShow](directshow-editing-services.md) (DES). O objeto Timeline implementa essa interface. Os aplicativos podem usar essa interface para registrar erros de renderização em tempo de execução. Implemente a interface [**IAMErrorLog**](iamerrorlog.md) em seu aplicativo e, em seguida, chame o método [**IAMSetErrorLog::p UT log de \_ erros**](iamseterrorlog-put-errorlog.md) na linha do tempo.

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
> para obter o Qedit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
