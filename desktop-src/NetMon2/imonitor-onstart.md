---
description: O método OnStart é um método opcional que pode ser implementado pelo monitor. O MCSVC chama esse método para solicitar que o monitor inicie a captura.
ms.assetid: 992ee27e-aaba-4e65-989b-e3f0fbd542ea
title: 'Método IMonitor:: OnStart (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStart
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: ca9e5e17de1d6baf2c79cc0077c5e2036a2a6246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089958"
---
# <a name="imonitoronstart-method"></a>Método IMonitor:: OnStart

O método **OnStart** é um método opcional que pode ser implementado pelo monitor. O MCSVC chama esse método para solicitar que o monitor inicie a captura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnStart(
  [in] IUnknown *pUnkNPP
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pUnkNPP* \[ no\]
</dt> <dd>

Um ponteiro [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) para a interface [IRTC](irtc.md) . O monitor pode usar essa interface para obter estatísticas que podem ser usadas para determinar se a captura deve ser iniciada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, o valor de retorno será S \_ OK (que é o mesmo que NOERROR). Quando S \_ OK é retornado, o MCSVC chama o método [IRTC:: Start](irtc-start.md) .

Se o método não for bem-sucedido, o valor de retorno será um código de erro. O MCSVC não iniciará a captura se qualquer código de erro for retornado.

## <a name="remarks"></a>Comentários

O MCSVC chama esse método antes de o método [IRTC:: Start](irtc-start.md) do NPP ser chamado para iniciar a captura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IMonitor](imonitor.md)
</dt> <dt>

[Provedores de pacotes de rede](network-packet-providers.md)
</dt> </dl>

 

