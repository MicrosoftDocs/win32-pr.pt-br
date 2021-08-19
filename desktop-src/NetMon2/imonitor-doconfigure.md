---
description: O método doconfigure deve ser implementado pelo monitor. O MCSVC chama esse método para obter informações de configuração para a captura.
ms.assetid: bc2a3246-28dc-4452-a98e-a8a2447bb127
title: 'IMonitor: método oConfigure de:D (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoConfigure
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 9776ca62cbb61b6708f00d5e1d6d85eeab245b32798683b5afde546d835633c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779186"
---
# <a name="imonitordoconfigure-method"></a>IMonitor: método oConfigure de:D

O método **doconfigure** deve ser implementado pelo monitor. O MCSVC chama esse método para obter informações de configuração para a captura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE DoConfigure(
  [in]  char *pName,
  [in]  char *pConfiguration,
  [out] char **ppScriptInstance
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* \[ no\]
</dt> <dd>

Nome de uma instância do monitor.

</dd> <dt>

*pConfiguration* \[ no\]
</dt> <dd>

Cadeia de caracteres de configuração fornecida pelo MCSVC. O monitor deve analisar esta cadeia de caracteres para dados de configuração.

</dd> <dt>

*ppScriptInstance* \[ fora\]
</dt> <dd>

Endereço da cadeia de caracteres HTML usada para configurar o monitor. Se um script padrão for usado para configuração, esse valor deverá ser definido como **nulo**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será S \_ OK (que é o mesmo que NOERROR) e o MCSVC executará o monitor.

Se o método não for bem-sucedido, o valor de retorno será um código de erro. Um valor de retorno da \_ configuração do monitor NMERR \_ \_ é aceitável, mas quando esse erro é retornado, o monitor não pode iniciar até que uma chamada de **doconfigure** futura tenha êxito. Qualquer outro erro impede que a instância do monitor seja habilitada.

## <a name="remarks"></a>Comentários

O MCSVC chama esse método depois que ele se conectou à rede e antes do método [IRTC:: Configure](irtc-configure.md) ser chamado.

O monitor pode armazenar informações fornecidas por essa chamada, atualizar o script HTML ou a cadeia de caracteres de configuração e definir o [filtro de captura](capture-filters.md) no blob NPP.

O MCSVC pode chamar esse método várias vezes, mas não pode ser chamado enquanto o monitor estiver capturando dados. Observe que sempre que um [NPP](network-packet-providers.md) inicia uma captura, a conexão com a rede deve ser configurada. Essa restrição inclui situações em que o NPP é iniciado e interrompe a mesma captura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




