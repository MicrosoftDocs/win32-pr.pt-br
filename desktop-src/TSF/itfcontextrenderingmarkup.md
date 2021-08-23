---
title: Interface ITfContextRenderingMarkup
description: A interface ITfContextRenderingMarkup é implementada pelo gerenciador do TSF e usada por aplicativos. Essa interface pode ser recuperada usando IQueryInterface do objeto ITfContext. Essa interface ajuda o aplicativo a enumerar informações de renderização.
ms.assetid: 733d2db2-f9e9-4b78-af13-adc03825bf2b
keywords:
- Interface ITfContextRenderingMarkup Estrutura de Serviços de Texto
- Interface ITfContextRenderingMarkup Estrutura de Serviços de Texto , descrita
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80abb7e68e017ec4cd048a7b7df1799578a4d41568b2fcc062ec3845fcf49c2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118877024"
---
# <a name="itfcontextrenderingmarkup-interface"></a>Interface ITfContextRenderingMarkup

A interface **ITfContextRenderingMarkup** é implementada pelo gerenciador do TSF e usada por aplicativos. Essa interface pode ser recuperada usando IQueryInterface do [objeto ITfContext.](/windows/desktop/api/Msctf/nn-msctf-itfcontext) Essa interface ajuda o aplicativo a enumerar informações de renderização.



| Métodos ITfContextRenderingMarkup                                                | Descrição                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [GetRenderingMarkup](itfcontextrenderingmarkup-getrenderingmarkup.md)           | Recupera um enumerador das marcações de renderização para o intervalo determinado. |
| [FindNextRenderingMarkup](itfcontextrenderingmarkup-findnextrenderingmarkup.md) | Essa função não é implementada. Ele sempre retorna E \_ NOTIMPL.       |



 

## <a name="members"></a>Membros

A interface **ITfContextRenderingMarkup** herda da interface [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) mas não tem membros adicionais.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa interface não está atualmente nos arquivos de header públicos. Para usar essa API, você deve compilar MIDL o [protótipo](prototypes.md).

 

 

 