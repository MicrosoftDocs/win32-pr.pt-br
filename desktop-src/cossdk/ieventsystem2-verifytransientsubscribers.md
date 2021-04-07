---
description: Verifica a existência de todos os assinantes transitórios no repositório de dados. Ao chamar esse método, você pode garantir que todos os assinantes transitórios listados no repositório de dados estejam ativos.
ms.assetid: fffdde33-e960-42ef-a089-8ea8a6f33d52
title: 'Método IEventSystem2:: VerifyTransientSubscribers'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.VerifyTransientSubscribers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4415f405b95f341b645ca1dccbf254df2ffc7167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920301"
---
# <a name="ieventsystem2verifytransientsubscribers-method"></a>Método IEventSystem2:: VerifyTransientSubscribers

Verifica a existência de todos os assinantes transitórios no repositório de dados. Ao chamar esse método, você pode garantir que todos os assinantes transitórios listados no repositório de dados estejam ativos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT VerifyTransientSubscribers();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método pode retornar os valores de retorno padrão E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inesperado, e \_ falha e S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEventSystem2**](ieventsystem2.md)
</dt> </dl>

 

 




