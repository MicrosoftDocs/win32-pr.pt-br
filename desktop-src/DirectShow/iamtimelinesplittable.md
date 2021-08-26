---
description: a interface IAMTimelineSplittable divide um objeto de linha do tempo em serviços de edição DirectShow (DES). Fontes, efeitos, transições e faixas implementam essa interface.
ms.assetid: bb066d34-0ffd-495f-83ce-59ad054a7782
title: Interface IAMTimelineSplittable (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd9f3ca6b1bdea5f80c117b869163d9a2375d5b434765b5962c6216795dd9e64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078966"
---
# <a name="iamtimelinesplittable-interface"></a>Interface IAMTimelineSplittable

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

a `IAMTimelineSplittable` interface divide um objeto de linha do tempo em [serviços de edição DirectShow](directshow-editing-services.md) (DES). Fontes, efeitos, transições e faixas implementam essa interface.

## <a name="members"></a>Membros

A interface **IAMTimelineSplittable** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineSplittable** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IAMTimelineSplittable** tem esses métodos.



| Método                                             | Descrição                                                                                          |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**SplitAt**](iamtimelinesplittable-splitat.md)   | Divide o objeto na hora especificada.<br/>                                                  |
| [**SplitAt2**](iamtimelinesplittable-splitat2.md) | Divide o objeto na hora especificada, especificado como um valor de [**REFTIME**](reftime.md) .<br/> |



 

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



 

 
