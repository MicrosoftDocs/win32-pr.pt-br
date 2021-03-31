---
title: Interface ITfContextRenderingMarkup
description: A interface ITfContextRenderingMarkup é implementada pelo Gerenciador do TSF e usada por aplicativos. Essa interface pode ser recuperada usando IQueryInterface do objeto ITfContext. Essa interface ajuda o aplicativo a enumerar informações de renderização.
ms.assetid: 733d2db2-f9e9-4b78-af13-adc03825bf2b
keywords:
- Estrutura de serviços de texto da interface ITfContextRenderingMarkup
- Estrutura de serviços de texto da interface ITfContextRenderingMarkup, descrita
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b71e977665a4b3a6e817ef782ee558064e0986a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823854"
---
# <a name="itfcontextrenderingmarkup-interface"></a>Interface ITfContextRenderingMarkup

A interface **ITfContextRenderingMarkup** é implementada pelo Gerenciador do TSF e usada por aplicativos. Essa interface pode ser recuperada usando IQueryInterface do objeto [ITfContext](/windows/desktop/api/Msctf/nn-msctf-itfcontext) . Essa interface ajuda o aplicativo a enumerar informações de renderização.



| Métodos ITfContextRenderingMarkup                                                | Description                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [GetRenderingMarkup](itfcontextrenderingmarkup-getrenderingmarkup.md)           | Recupera um enumerador das marcações de renderização para o intervalo especificado. |
| [FindNextRenderingMarkup](itfcontextrenderingmarkup-findnextrenderingmarkup.md) | Esta função não está implementada. Ele sempre retorna E \_ NOTIMPL.       |



 

## <a name="members"></a>Membros

A interface **ITfContextRenderingMarkup** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa interface não está atualmente nos arquivos de cabeçalho públicos. Para usar essa API, você deve compilar o [protótipo](prototypes.md)em MIDL.

 

 

 