---
description: Recupera o número de versão do sistema de eventos.
ms.assetid: 6355f1b3-e1e7-435f-9795-d92464e004ae
title: 'Método IEventSystem2:: GetVersion'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.GetVersion
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2c75538d9fd71cb8ee81e454249fd5116ccd090c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457162"
---
# <a name="ieventsystem2getversion-method"></a>Método IEventSystem2:: GetVersion

Recupera o número de versão do sistema de eventos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetVersion(
  [out] int *pnVersion
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pnVersion* \[ fora\]
</dt> <dd>

O número de versão do sistema de eventos.

</dd> </dl>

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

 

 




