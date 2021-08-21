---
description: O método OnStart é um método opcional que pode ser implementado pelo monitor. O MCSVC chama esse método para solicitar que o monitor inicie a captura.
ms.assetid: 992ee27e-aaba-4e65-989b-e3f0fbd542ea
title: Método IMonitor::OnStart (Netmon.h)
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
ms.openlocfilehash: 9f012a84772631783eaf1bdd33419478e34cc868b1a8fdbb718f5fa0749b2308
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063936"
---
# <a name="imonitoronstart-method"></a>Método IMonitor::OnStart

O **método OnStart** é um método opcional que pode ser implementado pelo monitor. O MCSVC chama esse método para solicitar que o monitor inicie a captura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnStart(
  [in] IUnknown *pUnkNPP
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pUnkNPP* \[ Em\]
</dt> <dd>

Um [ponteiro IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) para a interface [IRTC.](irtc.md) O monitor pode usar essa interface para obter estatísticas que podem ser usadas para determinar se a captura deve ser iniciada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será S \_ OK (que é o mesmo que NOERROR). Quando S \_ OK é retornado, o MCSVC chama o [método IRTC::Start.](irtc-start.md)

Se o método não for bem-sucedido, o valor de retorno será um código de erro. O MCSVC não iniciará a captura se algum código de erro for retornado.

## <a name="remarks"></a>Comentários

O MCSVC chama esse método antes que o método [IRTC::Start](irtc-start.md) do NPP seja chamado para iniciar a captura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Imonitor](imonitor.md)
</dt> <dt>

[Provedores de Pacotes de Rede](network-packet-providers.md)
</dt> </dl>

 

